---
title: Referencia del modo de formato BC7
description: Esta documentación contiene una lista de los 8 modos de bloque y las asignaciones de bits para los bloques de formato de compresión de textura BC7.
ms.assetid: B1CEB729-6694-49BF-ACB9-FD1EFAB0B0D1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 719a223e6ac057b949d5e1222582058f637ec526
ms.sourcegitcommit: 62e758931c610782807c7c9fad284921a6c56232
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/22/2020
ms.locfileid: "104420120"
---
# <a name="bc7-format-mode-reference"></a>Referencia del modo de formato BC7

Esta documentación contiene una lista de los 8 modos de bloque y las asignaciones de bits para los bloques de formato de compresión de textura BC7.

Los colores de cada subconjunto dentro de un bloque se representan mediante dos colores de extremo explícitos y un conjunto de colores interpolados entre ellos. Dependiendo de la precisión del índice del bloque, cada subconjunto puede tener 4, 8 o 16 colores posibles.

-   [Modo 0](#mode-0)
-   [Modo 1](#mode-1)
-   [Modo 2](#mode-2)
-   [Modo 3](#mode-3)
-   [Modo 4](#mode-4)
-   [Modo 5](#mode-5)
-   [Modo 6](#mode-6)
-   [Modo 7](#mode-7)
-   [Comentarios:](#remarks)
-   [Temas relacionados](#related-topics)

## <a name="mode-0"></a>Modo 0

El modo de BC7 0 tiene las siguientes características:

-   Solo componentes de color (no alfa)
-   3 subconjuntos por bloque
-   Puntos de conexión de RGBP 4.4.4.1 con un bit P único por punto de conexión
-   índices de 3 bits
-   16 particiones

![diseño de bits de modo 0](images/bc7-mode0.png)

## <a name="mode-1"></a>Modo 1

El modo de BC7 1 tiene las siguientes características:

-   Solo componentes de color (no alfa)
-   2 subconjuntos por bloque
-   RGBP extremos de 6.6.6.1 con un bit P compartido por subconjunto)
-   índices de 3 bits
-   64 particiones

![diseño de bits de modo 1](images/bc7-mode1.png)

## <a name="mode-2"></a>Modo 2

El modo 2 de BC7 tiene las siguientes características:

-   Solo componentes de color (no alfa)
-   3 subconjuntos por bloque
-   Extremos 5.5.5 RGB
-   índices de 2 bits
-   64 particiones

![diseño de bits de modo 2](images/bc7-mode2.png)

## <a name="mode-3"></a>Modo 3

El modo de BC7 3 tiene las siguientes características:

-   Solo componentes de color (no alfa)
-   2 subconjuntos por bloque
-   Puntos de conexión de RGBP 7.7.7.1 con un bit P único por subconjunto)
-   índices de 2 bits
-   64 particiones

![diseño de modo de 3 bits](images/bc7-mode3.png)

## <a name="mode-4"></a>Modo 4

El modo de BC7 4 tiene las siguientes características:

-   Componentes de color con componentes alfa independientes
-   1 subconjunto por bloque
-   Extremos de color RGB 5.5.5
-   puntos de conexión alfa de 6 bits
-   16 índices de 2 bits
-   16 índices de 3 bits
-   rotación de componentes de 2 bits
-   Selector de índice de 1 bit (si se usan los índices de 2 o 3 bits)

![diseño de modo 4 bits](images/bc7-mode4.png)

## <a name="mode-5"></a>Modo 5

El modo de BC7 5 tiene las siguientes características:

-   Componentes de color con componentes alfa independientes
-   1 subconjunto por bloque
-   Extremos de color RGB 7.7.7
-   puntos de conexión alfa de 8 bits
-   16 índices de color de 2 bits
-   16 índices alfa de 2 bits
-   rotación de componentes de 2 bits

![diseño de bits de modo 5](images/bc7-mode5.png)

## <a name="mode-6"></a>Modo 6

El modo de BC7 6 tiene las siguientes características:

-   Componentes de color y alfa combinados
-   Un subconjunto por bloque
-   Puntos de conexión de color (y alfa) de RGBAP 7.7.7.7.1 (único P bits por extremo)
-   16 índices x 4 bits

![diseño de modo de 6 bits](images/bc7-mode6.png)

## <a name="mode-7"></a>Modo 7

El modo de BC7 7 tiene las siguientes características:

-   Componentes de color y alfa combinados
-   2 subconjuntos por bloque
-   Puntos de conexión de color (y alfa) de RGBAP 5.5.5.5.1 (único P bits por extremo)
-   índices de 2 bits
-   64 particiones

![diseño de bits de modo 7](images/bc7-mode7.png)

## <a name="remarks"></a>Observaciones

El modo 8 (el byte menos significativo está establecido en 0x00). No lo use en el codificador. Si pasa este modo al hardware, se devuelve un bloque inicializado con ceros.

En BC7, puede codificar el componente alfa de una de las siguientes maneras:

-   Tipos de bloque sin codificación de componentes alfa explícita. En estos bloques, los extremos de color tienen una codificación solo RGB, con el componente alfa descodificado en 1,0 para todos los textura.
-   Tipos de bloque con componentes de color y alfa combinados. En estos bloques, los valores de color del punto de conexión se especifican en el formato RGBA y los valores del componente alfa se interpolan junto con los valores de color.
-   Tipos de bloque con componentes de color y alfa separados. En estos bloques, los valores de color y alfa se especifican por separado, cada uno con su propio conjunto de índices. Como resultado, tienen un vector efectivo y un canal escalar codificados por separado, donde el vector especifica normalmente los canales de color \[ R, G, B \] y el valor escalar especifica el canal alfa \[ a \] . Para admitir este enfoque, se proporciona un campo de 2 bits independiente en la codificación, que permite la especificación de la codificación de canal independiente como un valor escalar. Como resultado, el bloque puede tener una de las siguientes cuatro representaciones diferentes de esta codificación alfa (como se indica en el campo de 2 bits):
    -   RGB \| A: canal alfa independiente
    -   AGB \| R: canal de color "rojo" independiente
    -   RAB \| G: canal de color verde independiente
    -   RGA \| B: canal de color azul independiente

    El descodificador vuelve a ordenar el orden del canal a RGBA después de la descodificación, por lo que el formato de bloque interno no es visible para el desarrollador. Los negros con componentes de color y alfa independientes también tienen dos conjuntos de datos de índice: uno para el conjunto de canales de vectores y otro para el canal escalar. (En el caso del modo 4, estos índices son de distintos anchos \[ 2 o 3 bits \] . El modo 4 también contiene un selector de 1 bit que especifica si el vector o el canal escalar utiliza los índices de 3 bits).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Formato BC7](bc7-format.md)
</dt> </dl>

 

 




