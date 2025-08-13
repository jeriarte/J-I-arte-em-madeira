TRANSFOMANDO MADEIRA EM ARTE
<!doctype html>
<html lang="pt-BR">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>J&I ARTES EM MADEIRAS</title>
  <meta name="description" content="Carpintaria e artesanato - móveis sob medida, restauração e peças decorativas. Veja o portfólio e peça um orçamento pelo WhatsApp." />
  <style>
    :root {
      --bg: #f7f5f2;
      --card: #fff;
      --accent: #9b6b3a;
      --muted: #6b6b6b;
      --maxw: 1100px;
      --radius: 14px;
    }
    * { box-sizing: border-box; }
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      background: var(--bg);
      color: #222;
    }
    .container {
      max-width: var(--maxw);
      margin: 0 auto;
      padding: 28px;
    }
    header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 16px;
      flex-wrap: wrap;
    }
    .brand {
      display: flex;
      align-items: center;
      gap: 14px;
    }
    .logo {
      width: 62px;
      height: 62px;
      background: linear-gradient(135deg, #c48a5b, #8b5a36);
      border-radius: 12px;
      display: flex;
      align-items: center;
      justify-content: center;
      color: white;
      font-weight: 700;
      font-size: 24px;
      user-select: none;
    }
    nav a {
      margin-left: 14px;
      color: var(--muted);
      text-decoration: none;
      font-weight: 600;
    }
    nav a:hover {
      color: var(--accent);
    }
    .hero {
      display: flex;
      gap: 28px;
      align-items: center;
      margin-top: 28px;
      flex-wrap: wrap;
    }
    .hero-left {
      flex: 1;
      min-width: 280px;
    }
    .hero h1 {
      font-size: clamp(26px, 4vw, 44px);
      margin: 0 0 12px;
      color: var(--accent);
    }
    .hero p {
      margin: 0 0 18px;
      color: var(--muted);
      font-weight: 600;
    }
    .btn {
      background: var(--accent);
      color: white;
      padding: 12px 18px;
      border-radius: 10px;
      text-decoration: none;
      display: inline-block;
      font-weight: 600;
      cursor: pointer;
      border: none;
      transition: background-color 0.3s ease;
    }
    .btn:hover {
      background: #7a5230;
    }
    .card {
      background: var(--card);
      border-radius: var(--radius);
      padding: 18px;
      box-shadow: 0 6px 20px rgba(30, 30, 30, 0.06);
      margin-bottom: 28px;
    }
    section {
      margin-top: 34px;
    }
    .grid-2 {
      display: grid;
      grid-template-columns: 1fr 380px;
      gap: 22px;
      flex-wrap: wrap;
    }
    @media (max-width: 900px) {
      .hero {
        flex-direction: column;
        align-items: flex-start;
      }
      .grid-2 {
        grid-template-columns: 1fr;
      }
      nav {
        display: none;
      }
    }
    /* Gallery styles */
    .filters {
      display: flex;
      gap: 10px;
      margin: 20px 0;
    }
    .filters button {
      border: 1px solid #e6e6e6;
      padding: 8px 12px;
      border-radius: 10px;
      background: white;
      cursor: pointer;
      font-weight: 600;
    }
    .filters button.active {
      background: var(--accent);
      color: white;
      border-color: transparent;
    }
    .gallery {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
      gap: 14px;
    }
    .item {
      position: relative;
      overflow: hidden;
      border-radius: 12px;
      cursor: pointer;
      box-shadow: 0 2px 8px rgb(0 0 0 / 0.1);
    }
    .item img {
      width: 100%;
      height: 220px;
      object-fit: cover;
      display: block;
      transition: transform 0.35s;
      border-radius: 12px;
    }
    .item:hover img {
      transform: scale(1.06);
    }
    .item .meta {
      position: absolute;
      left: 10px;
      bottom: 10px;
      background: rgba(0, 0, 0, 0.45);
      color: white;
      padding: 6px 10px;
      border-radius: 8px;
      font-size: 13px;
      user-select: none;
    }
    /* Contact multi WhatsApp */
    .whatsapp-list {
      display: flex;
      gap: 14px;
      margin-top: 16px;
      flex-wrap: wrap;
    }
    .whatsapp-contact {
      background: var(--accent);
      color: white;
      padding: 10px 14px;
      border-radius: 10px;
      text-align: center;
      cursor: pointer;
      flex: 1;
      min-width: 150px;
      user-select: none;
      transition: background-color 0.3s ease;
      font-weight: 600;
      text-decoration: none;
      display: inline-block;
    }
    .whatsapp-contact:hover {
      background: #7a5230;
    }
    /* Lightbox */
    .lightbox {
      position: fixed;
      inset: 0;
      display: none;
      align-items: center;
      justify-content: center;
      background: rgba(0, 0, 0, 0.6);
      z-index: 999;
    }
    .lightbox img {
      max-width: 92%;
      max-height: 80%;
      border-radius: 10px;
    }
    .lightbox .close {
      position: absolute;
      top: 20px;
      right: 20px;
      background: white;
      border-radius: 50%;
      width: 36px;
      height: 36px;
      display: flex;
      align-items: center;
      justify-content: center;
      cursor: pointer;
      font-weight: 700;
      font-size: 22px;
      user-select: none;
    }
    /* Form styles */
    label {
      font-size: 14px;
      margin-bottom: 6px;
      display: block;
      font-weight: 600;
    }
    input,
    textarea {
      width: 100%;
      padding: 10px;
      border-radius: 8px;
      border: 1px solid #ddd;
      font-family: inherit;
      font-size: 14px;
      resize: vertical;
    }
    textarea {
      min-height: 100px;
    }
    /* Footer */
    footer {
      margin-top: 36px;
      padding: 26px 0;
      text-align: center;
      color: var(--muted);
      font-size: 14px;
      user-select: none;
    }
  </style>
</head>
<body>
  <div class="container">
    <header>
      <div class="brand">
        <div class="logo">J&I</div>
        <div>
          <div style="font-weight:700; font-size: 18px;">J&I ARTES EM MADEIRAS</div>
          <div style="font-size: 13px; color: var(--muted);">Peças sob medida · Restauração · Projetos autorais</div>
        </div>
      </div>
      <nav>
        <a href="#home">Início</a>
        <a href="#portfolio">Portfólio</a>
        <a href="#services">Serviços</a>
        <a href="#contact">Contato</a>
      </nav>
    </header>

    <main id="home">
      <div class="hero">
        <div class="hero-left">
          <h1>O QUE MUITOS NÃO DÃO VALOR CONSEGUIMOS TRANSFORMAR EM ARTE RÚSTICA EM MADEIRAS FAÇA JÁ SEU ORÇAMENTO</h1>
          <p>Móveis sob medida, restauração e peças decorativas com acabamento artesanal e madeira de qualidade.</p>
          <button class="btn" id="btn-whatsapp">Pedir orçamento pelo WhatsApp</button>
        </div>
        <div style="width:360px; max-width: 100%;">
          <div class="card">
            <div style="font-weight:700; margin-bottom:8px">Orçamento rápido</div>
            <form id="quick-form">
              <label>Nome</label>
              <input required name="name" placeholder="Seu nome" />
              <label>O que precisa?</label>
              <input name="project" placeholder="Ex: mesa de jantar 6 lugares" />
              <label>Telefone</label>
              <input name="phone" placeholder="(xx) xxxxx-xxxx" />
              <div style="margin-top:12px; text-align:right">
                <button type="submit" class="btn">Enviar</button>
              </div>
            </form>
          </div>
        </div>
      </div>

      <section id="about">
        <div class="card">
          <h2>Sobre nós</h2>
          <p>
            Na J&I ARTES EM MADEIRAS, unimos tradição e inovação para transformar madeira em peças únicas e cheias de personalidade.
            Com anos de experiência em carpintaria e artesanato, nossa equipe especializada oferece móveis sob medida, restauração cuidadosa e objetos decorativos que valorizam o ambiente e refletem o estilo de cada cliente.
          </p>
          <p>
            Valorizamos a qualidade dos materiais, o acabamento impecável e o atendimento personalizado, garantindo que cada projeto seja tratado com dedicação e respeito.
            Seja para sua casa, escritório ou espaço comercial, estamos prontos para dar vida às suas ideias em madeira.
          </p>
        </div>
      </section>

      <section id="portfolio">
        <div style="display:flex; align-items:center; justify-content:space-between; flex-wrap: wrap;">
          <h2>Portfólio</h2>
          <div style="background:#fff5e8; color: var(--accent); padding: 6px 10px; border-radius: 999px; font-weight: 600;">Feito à mão</div>
        </div>

        <div class="filters" id="filters">
          <button data-filter="all" class="active">Todos</button>
          <button data-filter="moveis">Móveis</button>
          <button data-filter="decor">Itens de decoração</button>
          <button data-filter="restauracao">Restauração</button>
          <button data-filter="cercas">Cercas</button>
          <button data-filter="currais">Currais</button>
        </div>

        <div class="gallery" id="gallery">
          <!-- Aqui você adiciona as imagens no formato abaixo quando quiser:
          <div class="item" data-cat="moveis">
            <img src="images/nome-da-imagem.jpg" alt="Descrição da imagem" loading="lazy" />
            <div class="meta">Descrição da peça</div>
          </div>
          -->
        </div>
      </section>

      <section id="services">
        <div class="grid-2">
          <div>
            <h2>Serviços</h2>
            <div>
              <div class="card" style="margin-bottom:10px;">
                <b>Projetos sob medida</b>
                <p style="color: var(--muted); margin:4px 0 0 0;">Planejamento, projeto e fabricação de móveis sob medida.</p>
              </div>
              <div class="card" style="margin-bottom:10px;">
                <b>Restauração</b>
                <p style="color: var(--muted); margin:4px 0 0 0;">Recupero móveis antigos preservando o estilo original.</p>
              </div>
              <div class="card">
                <b>Peças decorativas</b>
                <p style="color: var(--muted); margin:4px 0 0 0;">Prateleiras, nichos, luminárias e itens autorais.</p>
              </div>
            </div>
          </div>
          <aside>
            <div class="card" style="text-align:center;">
              <h3>Por que escolher nosso trabalho?</h3>
              <ul style="color: var(--muted); text-align:left; padding-left:20px;">
                <li>Acabamento premium</li>
                <li>Materiais selecionados</li>
                <li>Projetos personalizados conforme seu espaço</li>
              </ul>
              <div style="margin-top:12px;">
                <a class="btn" href="#contact">Fale conosco</a>
              </div>
            </div>
          </aside>
        </div>
      </section>

      <section id="contact">
        <div class="card">
          <h2>Contato</h2>
          <p>Quer um orçamento ou tem uma ideia? Me mande uma mensagem no WhatsApp ou preencha o formulário abaixo.</p>

          <div class="whatsapp-list">
            <a href="#" class="whatsapp-contact" data-number="5534998933615" data-name="Ivan">Ivan</a>
            <a href="#" class="whatsapp-contact" data-number="5534996995777" data-name="Renata">Renata</a>
            <a href="#" class="whatsapp-contact" data-number="5534996713379" data-name="Jean">Jean</a>
          </div>

          <form id="contact-form" style="margin-top:20px;">
            <label>Seu nome</label>
            <input name="name" required />
            <label>Telefone ou WhatsApp</label>
            <input name="phone" />
            <label>Mensagem</label>
            <textarea name="message" placeholder="Descreva seu projeto"></textarea>
            <div style="margin-top: 10px; text-align: right;">
              <button type="submit" class="btn">Enviar por e-mail</button>
            </div>
          </form>

          <div style="margin-top: 12px; font-size: 13px; color: var(--muted); user-select:none;">
            E-mail: jeriarteemmadeira@gmail.com
          </div>
        </div>
      </section>
    </main>

    <footer>
      © 2025 — J&I ARTES EM MADEIRAS. Todos os direitos reservados.
    </footer>
  </div>

  <!-- Lightbox para ampliar imagens -->
  <div class="lightbox" id="lightbox">
    <div class="close" id="lb-close">✕</div>
    <img id="lb-img" src="" alt="" />
  </div>

  <script>
    // Contatos WhatsApp
    const whatsappContacts = [
      { name: 'Ivan', number: '5534998933615' },
      { name: 'Renata', number: '5534996995777' },
      { name: 'Jean', number: '5534996713379' },
    ];
    const whatsappMessage = encodeURIComponent(
      'Olá! Vi seu trabalho e gostaria de um orçamento.'
    );

    // Botão principal WhatsApp abre seletor
    const btnWhatsapp = document.getElementById('btn-whatsapp');
    btnWhatsapp.addEventListener('click', () => {
      const choice = prompt(
        'Escolha um contato para falar no WhatsApp:\\n' +
          whatsappContacts.map((c, i) => `${i + 1} - ${c.name}`).join('\\n')
      );
      const index = parseInt(choice, 10) - 1;
      if (whatsappContacts[index]) {
        window.open(
          `https://wa.me/${whatsappContacts[index].number}?text=${whatsappMessage}`,
          '_blank'
        );
      }
    });

    // Lista contatos WhatsApp no contato
    document.querySelectorAll('.whatsapp-contact').forEach((el) => {
      el.addEventListener('click', (e) => {
        e.preventDefault();
        const num = e.currentTarget.dataset.number;
        window.open(
          `https://wa.me/${num}?text=${whatsappMessage}`,
          '_blank'
        );
      });
    });

    // Formulário rápido (abre WhatsApp)
    document.getElementById('quick-form').addEventListener('submit', (e) => {
      e.preventDefault();
      const data = new FormData(e.target);
      const name = data.get('name') || '';
      const project = data.get('project') || '';
      const phone = data.get('phone') || '';
      const text = encodeURIComponent(
        `Olá, meu nome é ${name}. Gostaria de orçamento para: ${project}. Meu contato: ${phone}`
      );
      // Abre no WhatsApp do primeiro contato (Ivan)
      window.open(
        `https://wa.me/${whatsappContacts[0].number}?text=${text}`,
        '_blank'
      );
    });

    // Formulário de contato (usa mailto)
    document.getElementById('contact-form').addEventListener('submit', (e) => {
      e.preventDefault();
      const data = new FormData(e.target);
      const name = data.get('name') || '(sem nome)';
      const phone = data.get('phone') || '';
      const message = data.get('message') || '';
      const subject = encodeURIComponent(`Orçamento de ${name}`);
      const body = encodeURIComponent
