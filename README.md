<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <title>Controle de Diárias</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet"/>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js"></script>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap" rel="stylesheet">
  <style>
    :root {
      --primary-color: #4e73df;
      --secondary-color: #1cc88a;
      --accent-color: #f6c23e;
    }

    body {
      font-family: 'Poppins', sans-serif;
      background-color: #f8f9fc;
      opacity: 0;
      transition: opacity 0.5s ease;
    }

    .bg-gradient-primary {
      background: linear-gradient(135deg, var(--primary-color) 0%, #224abe 100%);
    }

    .card {
      border: none;
      border-radius: 0.35rem;
      box-shadow: 0 0.15rem 1.75rem 0 rgba(58, 59, 69, 0.15);
    }

    .btn-success {
      background-color: var(--secondary-color);
      border-color: var(--secondary-color);
    }

    .btn-primary {
      background-color: var(--primary-color);
      border-color: var(--primary-color);
    }

    .dia {
      padding: 8px; /* Reduzido de 12px */
      border: 1px solid #e3e6f0;
      border-radius: 4px;
      text-align: center;
      cursor: pointer;
      user-select: none;
      transition: all 0.3s ease;
      font-weight: 600;
      background-color: white;
      font-size: 0.9rem; /* Tamanho da fonte reduzido */
    }

    .dia:hover {
      transform: translateY(-2px); /* Efeito mais sutil */
      box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
    }

    .trabalhado { 
      background-color: var(--secondary-color); 
      color: #fff; 
      border-color: var(--secondary-color);
    }
    .folga { 
      background-color: var(--accent-color); 
      color: #000; 
      border-color: var(--accent-color);
    }
    .falta { 
      background-color: #e74a3b; 
      color: #fff; 
      border-color: #e74a3b;
    }
    .empty { 
      visibility: hidden; 
    }

    .grid { 
      display: grid; 
      grid-template-columns: repeat(7, 1fr); 
      gap: 5px; /* Reduzido de 8px */
    }

    .calendar-header {
      display: grid;
      grid-template-columns: repeat(7, 1fr);
      gap: 5px; /* Reduzido de 8px */
      margin-bottom: 8px; /* Reduzido de 10px */
      font-weight: bold;
      text-align: center;
      color: var(--primary-color);
      font-size: 0.9rem; /* Tamanho da fonte reduzido */
    }

    #lista-despesas .list-group-item {
      padding: 0.5rem 1rem; /* Reduzido */
      border-left: 3px solid transparent;
      border-right: none;
      transition: all 0.3s;
      font-size: 0.9rem; /* Tamanho da fonte reduzido */
    }

    /* Restante do CSS mantido igual */
    /* ... */
  </style>
</head>
<body>
<!-- Cabeçalho e estrutura HTML mantidos iguais -->
<!-- ... -->

<script>
  // ... (código anterior mantido)

  function removerDespesa(id) {
    // REMOVIDO O CONFIRM
    despesas = despesas.filter(d => d.id !== id);
    localStorage.setItem('despesas', JSON.stringify(despesas));
    atualizarDespesas();
    atualizarResumo();
  }

  // ... (restante do código mantido)
</script>
</body>
</html>
