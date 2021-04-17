---
description: 'Al implementar su propio reconocedor de gestos de Microsoft, debe definir el nombre y el valor de intervalo Unicode para cualquier movimiento que el reconocedor tenga que reconocer. Si decide implementar los gestos que ya se admiten o se definen como parte del reconocedor de gestos de Microsoft, use los nombres definidos y los valores de intervalo Unicode para estos gestos. Toda la colección de nombres y valores de intervalo Unicode para los gestos implementados y no implementados en el reconocedor de gestos de Microsoft se proporciona en el archivo de encabezado Recdefs. h (instalado de forma predeterminada en C: \\ archivos de programa \\ Microsoft Tablet PC Platform SDK \\ include). Los nombres de gestos y los valores de intervalo Unicode también se muestran en las tablas siguientes. Tenga en cuenta que el gesto de nulo de GESTOs \_ se usa para indicar que un reconocedor no reconoce la entrada como un gesto.'
ms.assetid: 931fc69a-1f7a-492c-8158-0691cd2fe57a
title: Valores de intervalo Unicode de gestos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b66b9b4ee511e9eeadd79e0dff2675391ceee6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706567"
---
# <a name="unicode-range-values-of-gestures"></a>Valores de intervalo Unicode de gestos

Al implementar su propio reconocedor de gestos de Microsoft, debe definir el nombre y el valor de intervalo Unicode para cualquier movimiento que el reconocedor tenga que reconocer.

Si decide implementar los gestos que ya se admiten o se definen como parte del reconocedor de gestos de Microsoft, use los nombres definidos y los valores de intervalo Unicode para estos gestos. Toda la colección de nombres y valores de intervalo Unicode para los gestos implementados y no implementados en el reconocedor de gestos de Microsoft se proporciona en el archivo de encabezado Recdefs. h (instalado de forma predeterminada en C: \\ archivos de programa \\ Microsoft Tablet PC Platform SDK \\ include). Los nombres de gestos y los valores de intervalo Unicode también se muestran en las tablas siguientes.

> [!Note]  
> El gesto de nulo de GESTOs \_ se usa para indicar que un reconocedor no reconoce la entrada como un gesto.

 

## <a name="implemented-gestures"></a>Gestos implementados



| Nombre del gesto                          | Valor de intervalo Unicode |
|---------------------------------------|---------------------|
| MOVIMIENTO \_ nulo<br/>              | 0xf000<br/>   |
| GESTOs \_ SCRATCHOUT<br/>        | 0xf001<br/>   |
| triángulo de gesto \_<br/>          | 0xf002<br/>   |
| MOVIMIENTO \_ cuadrado<br/>            | 0xf003<br/>   |
| estrella de GESTOs \_<br/>              | 0xf004<br/>   |
| comprobación de GESTOs \_<br/>             | 0xf005<br/>   |
| GESTOs \_ arabesco<br/>          | 0xf010<br/>   |
| MOVIMIENTO \_ doble \_ arabesco<br/>  | 0xf011<br/>   |
| Círculo de GESTOs \_<br/>            | 0xf020<br/>   |
| \_círculo doble de gestos \_<br/>    | 0xf021<br/>   |
| GESTO \_ semicircular \_ izquierda<br/>  | 0xf028<br/>   |
| GESTO \_ semicircular \_ derecha<br/> | 0xf029<br/>   |
| \_botón de contenido adicional \_ hacia arriba<br/>       | 0xf030<br/>   |
| \_botón de contenido adicional de gestos \_<br/>     | 0xf031<br/>   |
| cheurón de GESTOs a la \_ \_ izquierda<br/>     | 0xf032<br/>   |
| \_botón de contenido adicional de gestos \_<br/>    | 0xf033<br/>   |
| \_flecha \_ de gesto hacia arriba<br/>         | 0xf038<br/>   |
| flecha de gesto \_ \_ hacia abajo<br/>       | 0xf039<br/>   |
| flecha de gesto \_ \_ izquierda<br/>       | 0xf03a<br/>   |
| flecha de gesto \_ \_ derecha<br/>      | 0xf03b<br/>   |
| GESTOs \_ hacia arriba<br/>                | 0xf058<br/>   |
| GESTOs \_ hacia abajo<br/>              | 0xf059<br/>   |
| GESTO a la \_ izquierda<br/>              | 0xf05a<br/>   |
| GESTO hacia la \_ derecha<br/>             | 0xf05b<br/>   |
| GESTOs hacia \_ \_ abajo<br/>          | 0xf060<br/>   |
| GESTOs \_ hacia \_ arriba<br/>          | 0xf061<br/>   |
| GESTO a la \_ izquierda \_<br/>       | 0xf062<br/>   |
| GESTO a la \_ derecha \_<br/>       | 0xf063<br/>   |
| GESTO \_ hacia arriba a la \_ izquierda \_<br/>    | 0xf064<br/>   |
| MOVIMIENTO \_ hacia arriba a la \_ derecha \_<br/>   | 0xf065<br/>   |
| GESTO \_ hacia abajo a la \_ izquierda \_<br/>  | 0xf066<br/>   |
| GESTO \_ hacia abajo a la \_ derecha \_<br/> | 0xf067<br/>   |
| GESTO \_ hacia arriba a la \_ izquierda<br/>          | 0xf068<br/>   |
| GESTO \_ hacia arriba \_<br/>         | 0xf069<br/>   |
| GESTO \_ hacia abajo a la \_ izquierda<br/>        | 0xf06a<br/>   |
| GESTO \_ hacia abajo a la \_ derecha<br/>       | 0xf06b<br/>   |
| MOVIMIENTO a la \_ izquierda \_<br/>          | 0xf06c<br/>   |
| MOVIMIENTO a la \_ izquierda \_<br/>        | 0xf06d<br/>   |
| MOVIMIENTO a la \_ derecha \_<br/>         | 0xf06e<br/>   |
| GESTO a la \_ derecha \_<br/>       | 0xf06f<br/>   |
| exclamación de GESTOs \_<br/>       | 0xf0a4<br/>   |
| \_puntear en gestos<br/>               | 0xf0f0<br/>   |
| \_doble punteo de gestos \_<br/>       | 0xf0f1<br/>   |



 

## <a name="unimplemented-gestures"></a>Gestos no implementados



| Nombre del gesto                             | Valor de intervalo Unicode |
|------------------------------------------|---------------------|
| infinito de GESTOs \_<br/>             | 0xf006<br/>   |
| MOVIMIENTO \_ cruzado<br/>                | 0xf007<br/>   |
| párrafo de gesto \_<br/>            | 0xf008<br/>   |
| sección de GESTOs \_<br/>              | 0xf009<br/>   |
| viñeta de gesto \_<br/>               | 0xf00a<br/>   |
| viñeta de gesto \_ \_ cruzado<br/>        | 0xf00b<br/>   |
| MOVIMIENTO en \_ zigzag<br/>             | 0xf00c<br/>   |
| intercambio de GESTOs \_<br/>                 | 0xf00d<br/>   |
| GESTOs \_ OPENUP<br/>               | 0xf00e<br/>   |
| GESTOs \_ primer plano<br/>              | 0xf00f<br/>   |
| rectángulo de GESTOs \_<br/>            | 0xf012<br/>   |
| GESTO \_ de \_ tocar círculo<br/>          | 0xf022<br/>   |
| Círculo de movimiento de \_ círculo \_<br/>       | 0xf023<br/>   |
| \_Cruz de círculo de gestos \_<br/>        | 0xf025<br/>   |
| MOVIMIENTO de \_ línea de círculo de gestos \_ \_<br/>   | 0xf026<br/>   |
| línea de círculo de GESTOs \_ \_ \_ horizontal<br/>   | 0xf027<br/>   |
| \_flecha doble \_ \_ de gesto hacia arriba<br/>    | 0xf03c<br/>   |
| \_flecha doble de gesto \_ \_ hacia abajo<br/>  | 0xf03d<br/>   |
| \_flecha doble de gesto \_ \_ izquierda<br/>  | 0xf03e<br/>   |
| flecha doble de gesto a la \_ \_ \_ derecha<br/> | 0xf03f<br/>   |
| \_flecha arriba de movimiento a la \_ \_ izquierda<br/>      | 0xf040<br/>   |
| GESTO \_ hacia arriba a la \_ \_ derecha<br/>     | 0xf041<br/>   |
| GESTO \_ hacia abajo \_ flecha \_ izquierda<br/>    | 0xf042<br/>   |
| GESTO \_ hacia abajo a la \_ \_ derecha<br/>   | 0xf043<br/>   |
| \_flecha izquierda \_ \_ de gesto hacia arriba<br/>      | 0xf044<br/>   |
| \_flecha izquierda de gesto \_ \_ hacia abajo<br/>    | 0xf045<br/>   |
| \_ \_ flecha hacia la derecha \_ hacia arriba<br/>     | 0xf046<br/>   |
| \_flecha derecha \_ \_ hacia abajo del gesto<br/>   | 0xf047<br/>   |
| LEFTUP de movimiento \_ diagonal \_<br/>     | 0xf05c<br/>   |
| RIGHTUP de movimiento \_ diagonal \_<br/>    | 0xf05d<br/>   |
| LEFTDOWN de movimiento \_ diagonal \_<br/>   | 0xf05e<br/>   |
| RIGHTDOWN de movimiento \_ diagonal \_<br/>  | 0xf05f<br/>   |
| \_letra \_ de gesto A<br/>            | 0xf080<br/>   |
| Letra de gesto \_ \_ B<br/>            | 0xf081<br/>   |
| Letra de gesto \_ \_ C<br/>            | 0xf082<br/>   |
| Letra de gesto \_ \_ D<br/>            | 0xf083<br/>   |
| Letra de gesto \_ \_ E<br/>            | 0xf084<br/>   |
| Letra de gesto \_ \_ F<br/>            | 0xf085<br/>   |
| Letra de gesto \_ \_ G<br/>            | 0xf086<br/>   |
| Letra de gesto \_ \_ H<br/>            | 0xf087<br/>   |
| Letra de gesto \_ \_ I<br/>            | 0xf088<br/>   |
| Letra de gesto \_ \_ J<br/>            | 0xf089<br/>   |
| Letra de gesto \_ \_ K<br/>            | 0xf08a<br/>   |
| Letra de gesto \_ \_ L<br/>            | 0xf08b<br/>   |
| Letra de gesto \_ \_ M<br/>            | 0xf08c<br/>   |
| Letra de gesto \_ \_ N<br/>            | 0xf08d<br/>   |
| Letra de gesto \_ \_ O<br/>            | 0xf08e<br/>   |
| Letra de gesto \_ \_ P<br/>            | 0xf08f<br/>   |
| Letra de gesto \_ \_ Q<br/>            | 0xf090<br/>   |
| Letra de gesto \_ \_ R<br/>            | 0xf091<br/>   |
| Carta de gesto \_ \_ S<br/>            | 0xf092<br/>   |
| Letra de gesto \_ \_ T<br/>            | 0xf093<br/>   |
| Letra de gesto \_ \_ U<br/>            | 0xf094<br/>   |
| Letra de gesto \_ \_ V<br/>            | 0xf095<br/>   |
| Letra de gesto \_ \_ W<br/>            | 0xf096<br/>   |
| Letra de gesto \_ \_ X<br/>            | 0xf097<br/>   |
| Letra de gesto \_ \_ Y<br/>            | 0xf098<br/>   |
| Letra de gesto \_ \_ Z<br/>            | 0xf099<br/>   |
| Dígito de gesto \_ \_ 0<br/>             | 0xf09a<br/>   |
| Dígito de gesto \_ \_ 1<br/>             | 0xf09b<br/>   |
| Dígito de gesto \_ \_ 2<br/>             | 0xf09c<br/>   |
| Dígito de gesto \_ \_ 3<br/>             | 0xf09d<br/>   |
| Dígito de gesto \_ \_ 4<br/>             | 0xf09e<br/>   |
| Dígito de gesto \_ \_ 5<br/>             | 0xf09f<br/>   |
| Dígito de gesto \_ \_ 6<br/>             | 0xf0a0<br/>   |
| Dígito de gesto \_ \_ 7<br/>             | 0xf0a1<br/>   |
| Dígito de gesto \_ \_ 8<br/>             | 0xf0a2<br/>   |
| Dígito de gesto \_ \_ 9<br/>             | 0xf0a3<br/>   |
| pregunta de gesto \_<br/>             | 0xf0a5<br/>   |
| GESTOs \_ sostenidos<br/>                | 0xf0a6<br/>   |
| Dólar de GESTOs \_<br/>               | 0xf0a7<br/>   |
| asterisco de gesto \_<br/>             | 0xf0a8<br/>   |
| GESTOs \_ más<br/>                 | 0xf0a9<br/>   |
| MOVIMIENTO \_ doble \_ hacia arriba<br/>           | 0xf0b8<br/>   |
| GESTO \_ doble \_ hacia abajo<br/>         | 0xf0b9<br/>   |
| MOVIMIENTO \_ doble a la \_ izquierda<br/>         | 0xf0ba<br/>   |
| MOVIMIENTO \_ doble a la \_ derecha<br/>        | 0xf0bb<br/>   |
| GESTO \_ triple \_ arriba<br/>           | 0xf0bc<br/>   |
| GESTO \_ triple \_ abajo<br/>         | 0xf0bd<br/>   |
| GESTO \_ triple a la \_ izquierda<br/>         | 0xf0be<br/>   |
| GESTO \_ triple \_ derecha<br/>        | 0xf0bf<br/>   |
| corchete de GESTOs \_ \_<br/>        | 0xf0e4<br/>   |
| \_corchete \_ de gesto en<br/>       | 0xf0e5<br/>   |
| corchete de gesto a la \_ \_ izquierda<br/>        | 0xf0e6<br/>   |
| corchete de gesto a la \_ \_ derecha<br/>       | 0xf0e7<br/>   |
| llave de GESTOs \_ \_<br/>          | 0xf0e8<br/>   |
| \_llave de gestos \_ en<br/>         | 0xf0e9<br/>   |
| llave de GESTOs \_ \_ izquierda<br/>          | 0xf0ea<br/>   |
| llave de gesto \_ \_ derecha<br/>         | 0xf0eb<br/>   |
| GESTO \_ triple \_ tocar<br/>          | 0xf0f2<br/>   |
| GESTO \_ - \_ TAP cuádruple<br/>            | 0xf0f3<br/>   |



 

 

 




