---
description: 'Al implementar su propio reconocedor de gestos de Microsoft, debe definir el nombre y el valor del intervalo Unicode para cualquier gesto que el reconocedor reconozca. Si decide implementar los gestos que ya se admiten o definen como parte del reconocedor de gestos de Microsoft, use los nombres definidos y los valores de intervalo Unicode para estos gestos. Toda la colección de nombres y valores de intervalo Unicode para los gestos implementados y no implementados en el reconocedor de gestos de Microsoft se proporciona en el archivo de encabezado Recdefs.h (instalado de forma predeterminada en C: Archivos de programa, Incluido el SDK de la plataforma de PC para tabletas de \\ \\ \\ Microsoft). Los nombres de gestos y los valores de intervalo Unicode también se muestran en las tablas siguientes. Nota El gesto GESTURE NULL se usa para indicar que un reconocedor \_ no reconoce la entrada como gesto.'
ms.assetid: 931fc69a-1f7a-492c-8158-0691cd2fe57a
title: Valores de intervalo Unicode de gestos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b66b9b4ee511e9eeadd79e0dff2675391ceee6d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361005"
---
# <a name="unicode-range-values-of-gestures"></a>Valores de intervalo Unicode de gestos

Al implementar su propio reconocedor de gestos de Microsoft, debe definir el nombre y el valor del intervalo Unicode para cualquier gesto que el reconocedor reconozca.

Si decide implementar los gestos que ya se admiten o definen como parte del reconocedor de gestos de Microsoft, use los nombres definidos y los valores de intervalo Unicode para estos gestos. Toda la colección de nombres y valores de intervalo Unicode para los gestos implementados y no implementados en el reconocedor de gestos de Microsoft se proporciona en el archivo de encabezado Recdefs.h (instalado de forma predeterminada en C: Archivos de programa, Incluido el SDK de la plataforma de PC para tabletas de \\ \\ \\ Microsoft). Los nombres de gestos y los valores de intervalo Unicode también se muestran en las tablas siguientes.

> [!Note]  
> El gesto GESTURE \_ NULL se usa para indicar que un reconocedor no reconoce la entrada como gesto.

 

## <a name="implemented-gestures"></a>Gestos implementados



| Nombre del gesto                          | Valor de intervalo Unicode |
|---------------------------------------|---------------------|
| GESTURE \_ NULL<br/>              | 0xf000<br/>   |
| SCRATCHOUT \_ DE GESTO<br/>        | 0xf001<br/>   |
| TRIÁNGULO \_ GESTUAL<br/>          | 0xf002<br/>   |
| CUADRADO DE \_ GESTO<br/>            | 0xf003<br/>   |
| ESTRELLA \_ DE GESTO<br/>              | 0xf004<br/>   |
| COMPROBACIÓN DE \_ GESTOS<br/>             | 0xf005<br/>   |
| \_CURLICUE DE GESTO<br/>          | 0xf010<br/>   |
| GESTO \_ DOUBLE \_ CURLICUE<br/>  | 0xf011<br/>   |
| CÍRCULO DE \_ GESTOS<br/>            | 0xf020<br/>   |
| CÍRCULO \_ DOBLE DE \_ GESTO<br/>    | 0xf021<br/>   |
| GESTO \_ SEMICIRCLE \_ LEFT<br/>  | 0xf028<br/>   |
| GESTO \_ SEMICIRCLE \_ RIGHT<br/> | 0xf029<br/>   |
| BOTÓN \_ DE CONTENIDO ADICIONAL DE \_ GESTO<br/>       | 0xf030<br/>   |
| BOTÓN \_ DE CONTENIDO ADICIONAL GESTUAL HACIA \_ ABAJO<br/>     | 0xf031<br/>   |
| BOTÓN \_ DE CONTENIDO ADICIONAL DE GESTO A LA \_ IZQUIERDA<br/>     | 0xf032<br/>   |
| BOTÓN \_ DE CONTENIDO ADICIONAL DE GESTO A LA \_ DERECHA<br/>    | 0xf033<br/>   |
| FLECHA \_ DE GESTO HACIA \_ ARRIBA<br/>         | 0xf038<br/>   |
| FLECHA \_ DE GESTO HACIA \_ ABAJO<br/>       | 0xf039<br/>   |
| FLECHA \_ DE GESTO A LA \_ IZQUIERDA<br/>       | 0xf03a<br/>   |
| FLECHA \_ DE GESTO A LA \_ DERECHA<br/>      | 0xf03b<br/>   |
| GESTO \_ HACIA ARRIBA<br/>                | 0xf058<br/>   |
| GESTO \_ HACIA ABAJO<br/>              | 0xf059<br/>   |
| GESTO \_ A LA IZQUIERDA<br/>              | 0xf05a<br/>   |
| GESTO \_ A LA DERECHA<br/>             | 0xf05b<br/>   |
| GESTO \_ HACIA \_ ABAJO<br/>          | 0xf060<br/>   |
| GESTO \_ HACIA ABAJO HACIA \_ ARRIBA<br/>          | 0xf061<br/>   |
| GESTO \_ A LA \_ DERECHA<br/>       | 0xf062<br/>   |
| GESTO \_ A LA DERECHA \_ IZQUIERDA<br/>       | 0xf063<br/>   |
| GESTO \_ HACIA ARRIBA A LA IZQUIERDA \_ \_ LARGO<br/>    | 0xf064<br/>   |
| GESTO \_ HACIA ARRIBA A LA \_ \_ DERECHA<br/>   | 0xf065<br/>   |
| GESTO \_ HACIA ABAJO A LA IZQUIERDA \_ \_ LARGO<br/>  | 0xf066<br/>   |
| GESTO \_ HACIA ABAJO A LA \_ \_ DERECHA<br/> | 0xf067<br/>   |
| GESTO \_ HACIA ARRIBA A LA \_ IZQUIERDA<br/>          | 0xf068<br/>   |
| GESTO \_ HACIA ARRIBA A LA \_ DERECHA<br/>         | 0xf069<br/>   |
| GESTO \_ HACIA ABAJO A LA \_ IZQUIERDA<br/>        | 0xf06a<br/>   |
| GESTO \_ HACIA ABAJO A LA \_ DERECHA<br/>       | 0xf06b<br/>   |
| GESTO \_ DE IZQUIERDA HACIA \_ ARRIBA<br/>          | 0xf06c<br/>   |
| GESTO \_ A LA \_ IZQUIERDA<br/>        | 0xf06d<br/>   |
| GESTO \_ HACIA \_ ARRIBA<br/>         | 0xf06e<br/>   |
| GESTO \_ HACIA \_ ABAJO<br/>       | 0xf06f<br/>   |
| \_EXCLAMACIÓN DE GESTO<br/>       | 0xf0a4<br/>   |
| PULSACIÓN \_ DE GESTO<br/>               | 0xf0f0<br/>   |
| GESTO \_ DE DOBLE \_ PULSACIÓN<br/>       | 0xf0f1<br/>   |



 

## <a name="unimplemented-gestures"></a>Gestos sin implementar



| Nombre del gesto                             | Valor de intervalo Unicode |
|------------------------------------------|---------------------|
| INFINITO DE \_ GESTOS<br/>             | 0xf006<br/>   |
| GESTO \_ CRUZADO<br/>                | 0xf007<br/>   |
| PÁRRAFO DE \_ GESTO<br/>            | 0xf008<br/>   |
| SECCIÓN \_ GESTO<br/>              | 0xf009<br/>   |
| VIÑETA \_ DE GESTO<br/>               | 0xf00a<br/>   |
| GESTO \_ DE VIÑETA \_ CRUZADA<br/>        | 0xf00b<br/>   |
| GESTO \_ ONDULADO<br/>             | 0xf00c<br/>   |
| INTERCAMBIO DE \_ GESTOS<br/>                 | 0xf00d<br/>   |
| APERTURA \_ DE GESTOS<br/>               | 0xf00e<br/>   |
| CIERRE \_ DE GESTOS<br/>              | 0xf00f<br/>   |
| RECTÁNGULO DE \_ GESTOS<br/>            | 0xf012<br/>   |
| GESTO \_ DE PULSAR \_ CÍRCULO<br/>          | 0xf022<br/>   |
| CÍRCULO \_ DE \_ GESTOS<br/>       | 0xf023<br/>   |
| GESTO \_ CÍRCULO \_ CRUZADO<br/>        | 0xf025<br/>   |
| VERT \_ DE LÍNEA DE CÍRCULO \_ \_ GESTUAL<br/>   | 0xf026<br/>   |
| LÍNEA \_ DE \_ CÍRCULO \_ GESTUAL HORZ<br/>   | 0xf027<br/>   |
| GESTO \_ FLECHA DOBLE HACIA \_ \_ ARRIBA<br/>    | 0xf03c<br/>   |
| GESTO \_ FLECHA DOBLE HACIA \_ \_ ABAJO<br/>  | 0xf03d<br/>   |
| GESTO \_ FLECHA \_ DOBLE IZQUIERDA \_<br/>  | 0xf03e<br/>   |
| GESTO \_ FLECHA \_ DOBLE DERECHA \_<br/> | 0xf03f<br/>   |
| GESTO \_ FLECHA ARRIBA A LA \_ \_ IZQUIERDA<br/>      | 0xf040<br/>   |
| GESTO \_ FLECHA ARRIBA A LA \_ \_ DERECHA<br/>     | 0xf041<br/>   |
| GESTO \_ FLECHA ABAJO A LA \_ \_ IZQUIERDA<br/>    | 0xf042<br/>   |
| GESTO \_ FLECHA ABAJO A LA \_ \_ DERECHA<br/>   | 0xf043<br/>   |
| GESTO \_ FLECHA IZQUIERDA HACIA \_ \_ ARRIBA<br/>      | 0xf044<br/>   |
| GESTO \_ FLECHA IZQUIERDA HACIA \_ \_ ABAJO<br/>    | 0xf045<br/>   |
| GESTO \_ FLECHA DERECHA HACIA \_ \_ ARRIBA<br/>     | 0xf046<br/>   |
| GESTO \_ FLECHA DERECHA HACIA \_ \_ ABAJO<br/>   | 0xf047<br/>   |
| GESTO \_ DIAGONAL \_ LEFTUP<br/>     | 0xf05c<br/>   |
| GESTO \_ DIAGONAL A LA \_ DERECHA<br/>    | 0xf05d<br/>   |
| GESTO \_ DIAGONAL A LA \_ IZQUIERDA<br/>   | 0xf05e<br/>   |
| DIAGONAL \_ DE GESTO A LA \_ DERECHA<br/>  | 0xf05f<br/>   |
| LETRA \_ DE GESTO \_ A<br/>            | 0xf080<br/>   |
| GESTO \_ LETRA \_ B<br/>            | 0xf081<br/>   |
| LETRA \_ DE GESTO \_ C<br/>            | 0xf082<br/>   |
| LETRA \_ \_ GESTUAL D<br/>            | 0xf083<br/>   |
| LETRA \_ DE GESTO \_ E<br/>            | 0xf084<br/>   |
| LETRA \_ \_ GESTUAL F<br/>            | 0xf085<br/>   |
| LETRA \_ G DE \_ GESTO<br/>            | 0xf086<br/>   |
| LETRA \_ DE GESTO \_ H<br/>            | 0xf087<br/>   |
| LETRA \_ DE GESTO \_ I<br/>            | 0xf088<br/>   |
| LETRA \_ \_ GESTUAL J<br/>            | 0xf089<br/>   |
| LETRA \_ DE GESTO \_ K<br/>            | 0xf08a<br/>   |
| LETRA \_ \_ GESTUAL L<br/>            | 0xf08b<br/>   |
| LETRA \_ DE GESTO \_ M<br/>            | 0xf08c<br/>   |
| LETRA \_ \_ GESTUAL N<br/>            | 0xf08d<br/>   |
| LETRA \_ O DE \_ GESTO<br/>            | 0xf08e<br/>   |
| LETRA \_ DE GESTO \_ P<br/>            | 0xf08f<br/>   |
| LETRA \_ \_ GESTUAL Q<br/>            | 0xf090<br/>   |
| LETRA \_ \_ GESTUAL R<br/>            | 0xf091<br/>   |
| LETRAS \_ DE \_ GESTOS S<br/>            | 0xf092<br/>   |
| LETRA \_ DE GESTO \_ T<br/>            | 0xf093<br/>   |
| LETRA \_ DE GESTO \_ U<br/>            | 0xf094<br/>   |
| LETRA \_ \_ GESTUAL V<br/>            | 0xf095<br/>   |
| LETRA \_ DE GESTO \_ W<br/>            | 0xf096<br/>   |
| LETRA \_ \_ GESTUAL X<br/>            | 0xf097<br/>   |
| LETRA \_ DE GESTO \_ Y<br/>            | 0xf098<br/>   |
| LETRA \_ Z DE \_ GESTO<br/>            | 0xf099<br/>   |
| DÍGITO \_ DE \_ GESTO 0<br/>             | 0xf09a<br/>   |
| DÍGITO \_ DE \_ GESTO 1<br/>             | 0xf09b<br/>   |
| DÍGITO \_ DE \_ GESTO 2<br/>             | 0xf09c<br/>   |
| GESTO \_ DÍGITO \_ 3<br/>             | 0xf09d<br/>   |
| DÍGITO \_ DE \_ GESTO 4<br/>             | 0xf09e<br/>   |
| DÍGITO \_ DE \_ GESTO 5<br/>             | 0xf09f<br/>   |
| GESTO \_ DÍGITO \_ 6<br/>             | 0xf0a0<br/>   |
| GESTO \_ DÍGITO \_ 7<br/>             | 0xf0a1<br/>   |
| GESTO \_ DÍGITO \_ 8<br/>             | 0xf0a2<br/>   |
| GESTO \_ DÍGITO \_ 9<br/>             | 0xf0a3<br/>   |
| PREGUNTA DE \_ GESTO<br/>             | 0xf0a5<br/>   |
| GESTO \_ SHARP<br/>                | 0xf0a6<br/>   |
| DÓLAR \_ GESTUAL<br/>               | 0xf0a7<br/>   |
| ASTERISCO DE \_ GESTO<br/>             | 0xf0a8<br/>   |
| GESTO \_ MÁS<br/>                 | 0xf0a9<br/>   |
| GESTO \_ DOBLE \_ ARRIBA<br/>           | 0xf0b8<br/>   |
| GESTO \_ DOBLE \_ HACIA ABAJO<br/>         | 0xf0b9<br/>   |
| GESTO \_ DOBLE A LA \_ IZQUIERDA<br/>         | 0xf0ba<br/>   |
| GESTO \_ DOBLE A LA \_ DERECHA<br/>        | 0xf0bb<br/>   |
| GESTO \_ TRIPLE \_ ARRIBA<br/>           | 0xf0bc<br/>   |
| GESTO \_ TRIPLE \_ HACIA ABAJO<br/>         | 0xf0bd<br/>   |
| GESTO \_ TRIPLE A LA \_ IZQUIERDA<br/>         | 0xf0be<br/>   |
| GESTO \_ TRIPLE \_ DERECHA<br/>        | 0xf0bf<br/>   |
| CORCHETE \_ DE \_ GESTOS SOBRE<br/>        | 0xf0e4<br/>   |
| CORCHETE \_ DE \_ GESTOS EN<br/>       | 0xf0e5<br/>   |
| CORCHETE \_ DE GESTO A LA \_ IZQUIERDA<br/>        | 0xf0e6<br/>   |
| CORCHETE \_ DE \_ GESTOS A LA DERECHA<br/>       | 0xf0e7<br/>   |
| LLAVE \_ DE GESTO \_ SOBRE<br/>          | 0xf0e8<br/>   |
| LLAVE \_ DE GESTO \_ EN<br/>         | 0xf0e9<br/>   |
| LLAVE \_ DE GESTO A LA \_ IZQUIERDA<br/>          | 0xf0ea<br/>   |
| LLAVE \_ DE GESTO A LA \_ DERECHA<br/>         | 0xf0eb<br/>   |
| GESTO \_ TRIPLE \_ TAP<br/>          | 0xf0f2<br/>   |
| PULSACIÓN \_ DE \_ CUÁDUAL GESTO<br/>            | 0xf0f3<br/>   |



 

 

 




