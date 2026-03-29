<!DOCTYPE html>

<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Evaluación Giras de Estudio — 21 Alumnos</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700;900&family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
  :root {
    --ink: #1a1a2e;
    --gold: #c9a84c;
    --gold-light: #f0d98a;
    --teal: #0d7377;
    --teal-light: #e0f4f4;
    --rose: #c0392b;
    --amber: #e67e22;
    --purple: #7f3fbf;
    --grey: #f5f5f0;
    --mid: #888;
    --border: #e0ddd4;
    --adjusted: #1a5c38;
    --adjusted-bg: #d1fae5;
    --unchanged: #5b21b6;
    --unchanged-bg: #ede9fe;
  }
  * { box-sizing: border-box; margin: 0; padding: 0; }
  body { font-family: 'Inter', sans-serif; background: #faf9f6; color: var(--ink); font-size: 15px; line-height: 1.65; }

header { background: var(–ink); color: white; padding: 48px 40px 36px; position: relative; overflow: hidden; }
header::after { content: ‘’; position: absolute; bottom: 0; left: 0; right: 0; height: 4px; background: linear-gradient(90deg, var(–gold), var(–teal), #c0392b, var(–amber)); }
.badge { display: inline-block; background: rgba(255,255,255,.12); border: 1px solid rgba(255,255,255,.2); border-radius: 20px; padding: 4px 14px; font-size: 12px; font-weight: 500; letter-spacing: .5px; margin-bottom: 16px; text-transform: uppercase; }
header h1 { font-family: ‘Playfair Display’, serif; font-size: clamp(26px, 4.5vw, 44px); font-weight: 900; letter-spacing: -1px; line-height: 1.15; }
header h1 span { color: var(–gold-light); }
header p { margin-top: 10px; opacity: .72; font-size: 14px; font-weight: 300; max-width: 600px; }

.container { max-width: 1200px; margin: 0 auto; padding: 0 24px; }
section { padding: 44px 24px; max-width: 1200px; margin: 0 auto; }
h2 { font-family: ‘Playfair Display’, serif; font-size: 24px; font-weight: 700; margin-bottom: 6px; color: var(–ink); }
.sub { font-family: ‘Inter’, sans-serif; font-size: 13px; font-weight: 400; color: var(–mid); display: block; margin-top: 2px; margin-bottom: 24px; }

/* INFO BAR */
.info-bar { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 16px; margin-bottom: 36px; }
.info-pill { background: white; border: 1px solid var(–border); border-radius: 12px; padding: 16px 20px; }
.info-pill .label { font-size: 11px; text-transform: uppercase; letter-spacing: .8px; color: var(–mid); font-weight: 600; margin-bottom: 4px; }
.info-pill .value { font-family: ‘Playfair Display’, serif; font-size: 22px; font-weight: 700; color: var(–ink); }
.info-pill .note { font-size: 12px; color: var(–mid); margin-top: 2px; }
.info-pill.highlight { background: var(–ink); border-color: var(–ink); }
.info-pill.highlight .label { color: rgba(255,255,255,.5); }
.info-pill.highlight .value { color: var(–gold-light); }
.info-pill.highlight .note { color: rgba(255,255,255,.5); }

/* LEGEND */
.legend { display: flex; gap: 16px; flex-wrap: wrap; margin-bottom: 20px; }
.legend-item { display: flex; align-items: center; gap: 7px; font-size: 12.5px; font-weight: 500; }
.legend-dot { width: 12px; height: 12px; border-radius: 3px; flex-shrink: 0; }

/* TABLE */
.table-wrap { overflow-x: auto; border-radius: 14px; border: 1px solid var(–border); background: white; }
table { width: 100%; border-collapse: collapse; min-width: 900px; }
thead { background: var(–ink); color: white; }
thead th { padding: 13px 11px; text-align: left; font-size: 11px; font-weight: 600; text-transform: uppercase; letter-spacing: .7px; white-space: nowrap; }
tbody tr { border-bottom: 1px solid var(–border); }
tbody tr:last-child { border-bottom: none; }
tbody tr.adjusted { background: #f0fdf4; }
tbody tr.adjusted:hover { background: #dcfce7; }
tbody tr:not(.adjusted):hover { background: var(–grey); }
td { padding: 11px 11px; font-size: 13px; vertical-align: top; }
td:first-child { font-size: 12px; }

.pkg-name { font-weight: 600; font-size: 13px; }
.pkg-op { font-size: 11px; color: var(–mid); margin-top: 2px; }

.cuota { font-family: ‘Playfair Display’, serif; font-size: 17px; font-weight: 700; }
.cuota.up { color: #c0392b; }
.cuota.same { color: var(–teal); }
.valor-dia { font-size: 11px; color: var(–mid); margin-top: 2px; }
.liberados { display: inline-block; background: #fef9c3; color: #854d0e; border-radius: 5px; padding: 1px 7px; font-size: 11px; font-weight: 600; margin-top: 3px; }

.delta { font-size: 11px; font-weight: 600; margin-top: 3px; }
.delta.up { color: #c0392b; }
.delta.none { color: var(–mid); }

.tag { display: inline-block; border-radius: 5px; padding: 2px 7px; font-size: 11px; font-weight: 600; white-space: nowrap; }
.tag-green { background: #d1fae5; color: #065f46; }
.tag-blue { background: #dbeafe; color: #1e40af; }
.tag-orange { background: #ffedd5; color: #9a3412; }
.tag-adjusted { background: var(–adjusted-bg); color: var(–adjusted); border: 1px solid #a7f3d0; }
.tag-unchanged { background: var(–unchanged-bg); color: var(–unchanged); }

.badge-adj { display: inline-block; font-size: 10px; font-weight: 700; text-transform: uppercase; letter-spacing: .5px; padding: 2px 7px; border-radius: 4px; }
.badge-adj.adj { background: #d1fae5; color: #065f46; }
.badge-adj.fix { background: #ede9fe; color: #5b21b6; }

/* VERDICT */
.verdicts { display: grid; grid-template-columns: repeat(auto-fit, minmax(290px, 1fr)); gap: 20px; margin-top: 32px; }
.verdict { border-radius: 14px; padding: 24px; position: relative; overflow: hidden; }
.verdict::before { content: ‘’; position: absolute; top: 0; left: 0; width: 100%; height: 4px; }
.verdict-gold { background: #fffbeb; border: 1px solid #f0d98a; }
.verdict-gold::before { background: var(–gold); }
.verdict-teal { background: var(–teal-light); border: 1px solid #a7d8d8; }
.verdict-teal::before { background: var(–teal); }
.verdict-purple { background: #f3ebfc; border: 1px solid #c4a0f0; }
.verdict-purple::before { background: var(–purple); }
.verdict-emoji { font-size: 30px; margin-bottom: 8px; display: block; }
.verdict-title { font-family: ‘Playfair Display’, serif; font-size: 18px; font-weight: 700; margin-bottom: 6px; }
.verdict-winner { display: inline-block; border-radius: 20px; padding: 3px 12px; font-size: 12px; font-weight: 700; margin-bottom: 10px; }
.verdict-gold .verdict-winner { background: var(–gold); color: white; }
.verdict-teal .verdict-winner { background: var(–teal); color: white; }
.verdict-purple .verdict-winner { background: var(–purple); color: white; }
.verdict p { font-size: 13.5px; line-height: 1.6; }
.verdict .data { font-weight: 600; }

.disclaimer { background: var(–grey); border-radius: 12px; padding: 18px 22px; font-size: 12px; color: var(–mid); margin-top: 28px; line-height: 1.7; }
.disclaimer strong { color: var(–ink); }

.alert-box { background: #fff7ed; border: 1px solid #fed7aa; border-radius: 10px; padding: 14px 18px; font-size: 13px; color: #7c2d12; margin-bottom: 28px; line-height: 1.6; }
.alert-box strong { color: #7c2d12; }
</style>

</head>
<body>

<header>
  <div class="container">
    <div class="badge">🎓 Evaluación Ajustada · 21 Alumnos Confirmados</div>
    <h1>Precios ajustados para<br><span>tu curso de 21 alumnos</span></h1>
    <p>Se recalcularon los paquetes con estructura de precios por tramos de pasajeros. Funtour mantiene precio único. Raitrai y Atui aplican su tramo correspondiente a 21 pagados.</p>
  </div>
</header>

<section>
  <div class="info-bar">
    <div class="info-pill highlight">
      <div class="label">Alumnos confirmados</div>
      <div class="value">21 pagados</div>
      <div class="note">Tramo activo según cada operador</div>
    </div>
    <div class="info-pill">
      <div class="label">Funtour</div>
      <div class="value">Sin cambio</div>
      <div class="note">Precio único sin mínimo de pax</div>
    </div>
    <div class="info-pill">
      <div class="label">Raitrai — tramo activo</div>
      <div class="value">20–22 pax</div>
      <div class="note">2 pasajeros liberados</div>
    </div>
    <div class="info-pill">
      <div class="label">Atui — tramo activo</div>
      <div class="value">25–21 pax</div>
      <div class="note">2 pasajeros liberados</div>
    </div>
  </div>

  <div class="alert-box">
    ⚠️ <strong>Importante sobre los liberados con 21 alumnos:</strong> Raitrai y Atui otorgan <strong>2 pasajeros liberados</strong> en el tramo de 21 pagados. Eso significa que el colegio puede enviar 2 adultos acompañantes (profesores/apoderado responsable) sin costo adicional. Con Funtour, el liberado sigue siendo 1 cada 10 pagados (= 2 liberados con 21 pagados también, según la regla estándar).
  </div>

  <h2>Tabla Comparativa — 21 Alumnos</h2>
  <span class="sub">Ordenada de menor a mayor cuota mensual calculada para este grupo. Tipo de cambio USD: $950.</span>

  <div class="legend">
    <div class="legend-item"><div class="legend-dot" style="background:#d1fae5;border:1px solid #a7f3d0"></div> Precio ajustado para 21 pax</div>
    <div class="legend-item"><div class="legend-dot" style="background:#ede9fe;border:1px solid #c4a0f0"></div> Precio fijo (no varía con cantidad)</div>
  </div>

  <div class="table-wrap">
    <table>
      <thead>
        <tr>
          <th>#</th>
          <th>Paquete / Operador</th>
          <th>Destino</th>
          <th>Días/Noches</th>
          <th>Precio Total pp.</th>
          <th>Cuota ÷20</th>
          <th>Valor/Día</th>
          <th>Liberados</th>
          <th>Noches Disco</th>
          <th>Estado precio</th>
        </tr>
      </thead>
      <tbody>

```
    <!-- 1 Pucón Terrestre FIJO -->
    <tr>
      <td>1</td>
      <td><div class="pkg-name">Pucón Terrestre</div><div class="pkg-op">Funtour · PUC_Directo_65</div></td>
      <td>Pucón, Chile</td>
      <td>6d / 5n</td>
      <td>$730.000</td>
      <td><div class="cuota same">$36.500</div><div class="valor-dia">$122k/día</div></td>
      <td>$122.000</td>
      <td><div class="liberados">2 liberados</div></td>
      <td><span class="tag tag-orange">1 disco</span></td>
      <td><span class="badge-adj fix">Precio fijo</span></td>
    </tr>

    <!-- 2 Pucón Aéreo FIJO -->
    <tr>
      <td>2</td>
      <td><div class="pkg-name">Pucón Aéreo</div><div class="pkg-op">Funtour · PUC_Directo_54</div></td>
      <td>Pucón, Chile</td>
      <td>5d / 4n</td>
      <td>$815.000</td>
      <td><div class="cuota same">$40.750</div><div class="valor-dia">$163k/día</div></td>
      <td>$163.000</td>
      <td><div class="liberados">2 liberados</div></td>
      <td><span class="tag tag-orange">1 disco</span></td>
      <td><span class="badge-adj fix">Precio fijo</span></td>
    </tr>

    <!-- 3 Bariloche Terrestre Funtour FIJO -->
    <tr>
      <td>3</td>
      <td><div class="pkg-name">Bariloche Terrestre Charter</div><div class="pkg-op">Funtour · 9D/8N Bus Compartido</div></td>
      <td>Bariloche + Pucón regreso</td>
      <td>9d / 8n</td>
      <td>$999.000</td>
      <td><div class="cuota same">$49.950</div><div class="valor-dia">$111k/día</div></td>
      <td>$111.000</td>
      <td><div class="liberados">2 liberados</div></td>
      <td><span class="tag tag-green">4 discos</span></td>
      <td><span class="badge-adj fix">Precio fijo</span></td>
    </tr>

    <!-- 4 ATUI Bariloche+Sur Terrestre AJUSTADO -->
    <tr class="adjusted">
      <td>4</td>
      <td><div class="pkg-name">Bariloche + Sur Terrestre</div><div class="pkg-op">Atui · T70026 — tramo 25–21</div></td>
      <td>Puerto Varas + Bariloche</td>
      <td>7d / 6n</td>
      <td>$1.089.000</td>
      <td><div class="cuota up">$54.450</div><div class="valor-dia">$156k/día</div></td>
      <td>$156.000</td>
      <td><div class="liberados">2 liberados</div></td>
      <td><span class="tag tag-green">3 discos</span></td>
      <td><span class="badge-adj adj">↑ Ajustado</span></td>
    </tr>

    <!-- 5 ATUI Bariloche+Sur Aéreo AJUSTADO -->
    <tr class="adjusted">
      <td>5</td>
      <td><div class="pkg-name">Bariloche + Sur Aéreo</div><div class="pkg-op">Atui · T70126 — tramo 25–21</div></td>
      <td>Puerto Varas + Bariloche</td>
      <td>6d / 5n</td>
      <td>$1.099.000</td>
      <td><div class="cuota up">$54.950</div><div class="valor-dia">$183k/día</div></td>
      <td>$183.000</td>
      <td><div class="liberados">2 liberados</div></td>
      <td><span class="tag tag-green">3 discos</span></td>
      <td><span class="badge-adj adj">↑ Ajustado</span></td>
    </tr>

    <!-- 6 Bariloche 7D Funtour Directo FIJO -->
    <tr>
      <td>6</td>
      <td><div class="pkg-name">Bariloche Vuelo Directo</div><div class="pkg-op">Funtour · 7D/6N Chárter</div></td>
      <td>Bariloche, Argentina</td>
      <td>7d / 6n</td>
      <td>$1.279.000</td>
      <td><div class="cuota same">$63.950</div><div class="valor-dia">$183k/día</div></td>
      <td>$183.000</td>
      <td><div class="liberados">2 liberados</div></td>
      <td><span class="tag tag-green">4 discos</span></td>
      <td><span class="badge-adj fix">Precio fijo</span></td>
    </tr>

    <!-- 7 Raitrai Bariloche Solo AJUSTADO -->
    <tr class="adjusted">
      <td>7</td>
      <td><div class="pkg-name">Bariloche Solo — Aéreo</div><div class="pkg-op">Raitrai · IA_B27 — tramo 20–22</div></td>
      <td>Bariloche, Argentina</td>
      <td>6d / 5n</td>
      <td>$1.444.950 <small>(USD$1.521)</small></td>
      <td><div class="cuota up">$72.248</div><div class="valor-dia">$241k/día</div></td>
      <td>$241.000</td>
      <td><div class="liberados">2 liberados</div></td>
      <td><span class="tag tag-green">3 discos</span></td>
      <td><span class="badge-adj adj">↑ Ajustado</span></td>
    </tr>

    <!-- 8 Funtour Camboriu FIJO -->
    <tr>
      <td>8</td>
      <td><div class="pkg-name">Camboriú Vuelo Directo</div><div class="pkg-op">Funtour · 8D/7N Chárter</div></td>
      <td>Balneario Camboriú, Brasil</td>
      <td>8d / 7n</td>
      <td>$1.650.000</td>
      <td><div class="cuota same">$82.500</div><div class="valor-dia">$206k/día</div></td>
      <td>$206.000</td>
      <td><div class="liberados">2 liberados</div></td>
      <td><span class="tag tag-green">4 discos</span></td>
      <td><span class="badge-adj fix">Precio fijo</span></td>
    </tr>

    <!-- 9 ATUI Camboriu Est AJUSTADO -->
    <tr class="adjusted">
      <td>9</td>
      <td><div class="pkg-name">Camboriú Estudiantil</div><div class="pkg-op">Atui · T77326 — tramo 25–21</div></td>
      <td>Balneario Camboriú, Brasil</td>
      <td>7d / 6n</td>
      <td>$1.642.550 <small>(USD$1.729)</small></td>
      <td><div class="cuota up">$82.128</div><div class="valor-dia">$235k/día</div></td>
      <td>$235.000</td>
      <td><div class="liberados">2 liberados</div></td>
      <td><span class="tag tag-green">3 discos</span></td>
      <td><span class="badge-adj adj">↑ Ajustado</span></td>
    </tr>

    <!-- 10 ATUI Camboriu Full AJUSTADO -->
    <tr class="adjusted">
      <td>10</td>
      <td><div class="pkg-name">Camboriú Full</div><div class="pkg-op">Atui · T77426 — tramo 25–21</div></td>
      <td>Balneario Camboriú, Brasil</td>
      <td>8d / 7n</td>
      <td>$1.804.050 <small>(USD$1.899)</small></td>
      <td><div class="cuota up">$90.202</div><div class="valor-dia">$225k/día</div></td>
      <td>$225.000</td>
      <td><div class="liberados">2 liberados</div></td>
      <td><span class="tag tag-green">3 discos</span></td>
      <td><span class="badge-adj adj">↑ Ajustado</span></td>
    </tr>

    <!-- 11 Raitrai Camboriu ECO Hotel 3* AJUSTADO -->
    <tr class="adjusted">
      <td>11</td>
      <td><div class="pkg-name">Camboriú Eco — Hotel 3★</div><div class="pkg-op">Raitrai · IA_ECO — tramo 20–22</div></td>
      <td>Balneario Camboriú, Brasil</td>
      <td>8d / 7n</td>
      <td>$1.877.200 <small>(USD$1.976)</small></td>
      <td><div class="cuota up">$93.860</div><div class="valor-dia">$234k/día</div></td>
      <td>$234.000</td>
      <td><div class="liberados">2 liberados</div></td>
      <td><span class="tag tag-orange">3 discos</span></td>
      <td><span class="badge-adj adj">↑ Ajustado</span></td>
    </tr>

    <!-- 12 Raitrai Camboriu ECO Hotel 4* AJUSTADO -->
    <tr class="adjusted">
      <td>12</td>
      <td><div class="pkg-name">Camboriú Eco — Hotel 4★ Brut/Ibis</div><div class="pkg-op">Raitrai · IA_ECO — tramo 20–22</div></td>
      <td>Balneario Camboriú, Brasil</td>
      <td>8d / 7n</td>
      <td>$1.913.300 <small>(USD$2.014)</small></td>
      <td><div class="cuota up">$95.665</div><div class="valor-dia">$239k/día</div></td>
      <td>$239.000</td>
      <td><div class="liberados">2 liberados</div></td>
      <td><span class="tag tag-orange">3 discos</span></td>
      <td><span class="badge-adj adj">↑ Ajustado</span></td>
    </tr>

    <!-- 13 Raitrai Camboriu FULL Hotel 3* AJUSTADO -->
    <tr class="adjusted">
      <td>13</td>
      <td><div class="pkg-name">Camboriú Full — Hotel 3★</div><div class="pkg-op">Raitrai · IA_FULL — tramo 20–22</div></td>
      <td>Balneario Camboriú, Brasil</td>
      <td>8d / 7n</td>
      <td>$1.971.250 <small>(USD$2.075)</small></td>
      <td><div class="cuota up">$98.562</div><div class="valor-dia">$246k/día</div></td>
      <td>$246.000</td>
      <td><div class="liberados">2 liberados</div></td>
      <td><span class="tag tag-orange">3 discos</span></td>
      <td><span class="badge-adj adj">↑ Ajustado</span></td>
    </tr>

    <!-- 14 Raitrai Camboriu FULL Hotel 4* AJUSTADO -->
    <tr class="adjusted">
      <td>14</td>
      <td><div class="pkg-name">Camboriú Full — Hotel 4★</div><div class="pkg-op">Raitrai · IA_FULL — tramo 20–22</div></td>
      <td>Balneario Camboriú, Brasil</td>
      <td>8d / 7n</td>
      <td>$2.121.350 <small>(USD$2.233)</small></td>
      <td><div class="cuota up">$106.068</div><div class="valor-dia">$265k/día</div></td>
      <td>$265.000</td>
      <td><div class="liberados">2 liberados</div></td>
      <td><span class="tag tag-orange">3 discos</span></td>
      <td><span class="badge-adj adj">↑ Ajustado</span></td>
    </tr>

  </tbody>
</table>
```

  </div>

  <!-- VERDICTS -->

  <h2 style="margin-top:48px">Veredicto — Con 21 alumnos</h2>
  <span class="sub">¿Cambia algo con respecto al análisis general?</span>

  <div class="verdicts">

```
<div class="verdict verdict-gold">
  <span class="verdict-emoji">🥇</span>
  <div class="verdict-title">Mejor relación precio/experiencia</div>
  <div class="verdict-winner">Bariloche Terrestre Charter — Funtour</div>
  <p>Sigue siendo el campeón con <span class="data">$49.950/mes y $111.000/día</span>. Al tener precio único, 21 alumnos pagan exactamente lo mismo que 39. Es el único paquete del comparativo donde el tamaño del grupo no penaliza el precio. Además, incluye 2 destinos (Bariloche + Pucón) y 4 noches de disco con 5 comidas diarias.</p>
</div>

<div class="verdict verdict-teal">
  <span class="verdict-emoji">🛡️</span>
  <div class="verdict-title">Más seguro para padres tranquilos</div>
  <div class="verdict-winner">Camboriú Full Hotel 4★ — Raitrai</div>
  <p>Con 21 alumnos, Raitrai aplica su tramo 20–22, subiendo la cuota a <span class="data">$106.068/mes</span>. El seguro de <span class="data">USD$150.000 pp. + ambulancia en discos + rondas médicas + seguro cancelación Any Reason</span> sigue siendo la red de seguridad más robusta del mercado, aunque ahora es también el paquete más caro. Para una familia que prioriza cobertura sobre precio, los $23.568 extra al mes respecto al Funtour Brasil se justifican.</p>
</div>

<div class="verdict verdict-purple">
  <span class="verdict-emoji">🎉</span>
  <div class="verdict-title">Más entretenido para el estudiante</div>
  <div class="verdict-winner">Camboriú Vuelo Directo — Funtour</div>
  <p>Con 21 alumnos, el Funtour Brasil mantiene su precio en <span class="data">$82.500/mes</span>, siendo ahora más barato que los equivalentes Atui ($82.128 ≈ igual) y Raitrai ($93.860+). La diferencia clave: <span class="data">4 noches de disco</span> (vs. 3 de Atui y Raitrai) y la actividad exclusiva Private Beach Funtour en Itapema, que ningún otro grupo puede acceder. Para el estudiante que quiere el máximo de noches de fiesta, Funtour gana.</p>
</div>
```

  </div>

  <div class="disclaimer">
    <strong>Precios calculados para 21 pasajeros pagados:</strong> Raitrai aplica tramo 20–22 pax (USD cotizados en los documentos × $950 CLP). Atui aplica tramo 25–21 pax (precios en CLP para terrestre; USD × $950 para Brasil). Funtour no tiene ajuste por cantidad. Los <strong>2 liberados</strong> de Raitrai y Atui corresponden a adultos acompañantes sin costo (profesores/apoderados designados por el colegio). Precios Funtour vigentes hasta el 30/04/2026 para viajes en diciembre 2026. Precios Raitrai y Atui son preventa 2027. Tipo de cambio USD $950 es referencial; el valor al momento del pago puede diferir.
  </div>
</section>

</body>
</html>