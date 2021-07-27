---
title: Referencia del modo de formato BC7
description: Esta documentación contiene una lista de los 8 modos de bloque y las asignaciones de bits para los bloques de formato de compresión de textura BC7.
ms.assetid: B1CEB729-6694-49BF-ACB9-FD1EFAB0B0D1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9756582d7d5ac52d4c16b2f4734decebbd66ae8
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436110"
---
# <a name="bc7-format-mode-reference"></a>Referencia del modo de formato BC7

Esta documentación contiene una lista de los 8 modos de bloque y las asignaciones de bits para los bloques de formato de compresión de textura BC7.

Los colores de cada subconjunto dentro de un bloque se representan mediante dos colores de punto de conexión explícitos y un conjunto de colores interpolados entre ellos. En función de la precisión del índice del bloque, cada subconjunto puede tener 4, 8 o 16 colores posibles.

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

El modo 0 de BC7 tiene las siguientes características:

-   Solo componentes de color (sin alfa)
-   3 subconjuntos por bloque
-   Puntos de conexión RGBP 4.4.4.1 con un bit P único por punto de conexión
-   Índices de 3 bits
-   16 particiones

![diseño de modo de 0 bits](images/bc7-mode0.png)

## <a name="mode-1"></a>Modo 1

El modo 1 de BC7 tiene las siguientes características:

-   Solo componentes de color (sin alfa)
-   2 subconjuntos por bloque
-   Puntos de conexión RGBP 6.6.6.1 con un bit P compartido por subconjunto)
-   Índices de 3 bits
-   64 particiones

![diseño de modo de 1 bit](images/bc7-mode1.png)

## <a name="mode-2"></a>Modo 2

El modo 2 de BC7 tiene las siguientes características:

-   Solo componentes de color (sin alfa)
-   3 subconjuntos por bloque
-   Puntos de conexión RGB 5.5.5
-   Índices de 2 bits
-   64 particiones

![diseño de modo de 2 bits](images/bc7-mode2.png)

## <a name="mode-3"></a>Modo 3

El modo 3 de BC7 tiene las siguientes características:

-   Solo componentes de color (sin alfa)
-   2 subconjuntos por bloque
-   Puntos de conexión RGBP 7.7.7.1 con un bit P único por subconjunto)
-   Índices de 2 bits
-   64 particiones

![diseño de modo de 3 bits](images/bc7-mode3.png)

## <a name="mode-4"></a>Modo 4

El modo 4 de BC7 tiene las siguientes características:

-   Componentes de color con componente alfa independiente
-   1 subconjunto por bloque
-   Puntos de conexión de color RGB 5.5.5
-   Puntos de conexión alfa de 6 bits
-   Índices de 16 x 2 bits
-   Índices de 16 x 3 bits
-   Rotación de componentes de 2 bits
-   Selector de índice de 1 bit (independientemente de si se usan índices de 2 o 3 bits)

![diseño de modo de 4 bits](images/bc7-mode4.png)

## <a name="mode-5"></a>Modo 5

El modo 5 de BC7 tiene las siguientes características:

-   Componentes de color con componente alfa independiente
-   1 subconjunto por bloque
-   Puntos de conexión de color RGB 7.7.7
-   Puntos de conexión alfa de 8 bits
-   Índices de color de 16 x 2 bits
-   Índices alfa de 16 x 2 bits
-   Rotación de componentes de 2 bits

![diseño de modo de 5 bits](images/bc7-mode5.png)

## <a name="mode-6"></a>Modo 6

El modo 6 de BC7 tiene las siguientes características:

-   Componentes de color y alfa combinados
-   Un subconjunto por bloque
-   Puntos de conexión RGBAP 7.7.7.7.1 de color (y alfa) (bit P único por punto de conexión)
-   Índices de 16 x 4 bits

![diseño de modo de 6 bits](images/bc7-mode6.png)

## <a name="mode-7"></a>Modo 7

El modo 7 de BC7 tiene las siguientes características:

-   Componentes de color y alfa combinados
-   2 subconjuntos por bloque
-   Puntos de conexión RGBAP 5.5.5.5.1 de color (y alfa) (bit P único por punto de conexión)
-   Índices de 2 bits
-   64 particiones

![diseño de modo de 7 bits](images/bc7-mode7.png)

## <a name="remarks"></a>Observaciones

El modo 8 (el byte menos significativo se establece en 0x00) está reservado. No la use en el codificador. Si pasa este modo al hardware, se devuelve un bloque inicializado a todos los ceros.

En BC7, puede codificar el componente alfa de una de las maneras siguientes:

-   Bloquear tipos sin codificación explícita de componentes alfa. En estos bloques, los puntos de conexión de color tienen una codificación solo RGB, con el componente alfa descodificado en 1.0 para todos los elementos de textura.
-   Tipos de bloques con componentes de color y alfa combinados. En estos bloques, los valores de color del punto de conexión se especifican en formato RGBA y los valores del componente alfa se interpolan junto con los valores de color.
-   Tipos de bloques con componentes de color y alfa separados. En estos bloques, los valores de color y alfa se especifican por separado, cada uno con su propio conjunto de índices. Como resultado, tienen un vector efectivo y un canal escalar codificados por separado, donde el vector normalmente especifica los canales de color R, G, B y el escalar especifica el canal \[ \] alfa A \[ \] . Para admitir este enfoque, se proporciona un campo de 2 bits independiente en la codificación, que permite la especificación de la codificación de canal independiente como un valor escalar. Como resultado, el bloque puede tener una de las cuatro representaciones diferentes siguientes de esta codificación alfa (como se indica en el campo de 2 bits):
    -   RGB \| A: canal alfa independiente
    -   AGB \| R: canal de color "rojo" independiente
    -   ASÍ COMO \| G: canal de color "verde" independiente
    -   GAL \| B: canal de color "azul" independiente

    El descodificador reordena el orden del canal a RGBA después de la descodificación, por lo que el formato de bloque interno es invisible para el desarrollador. Los bloques con componentes alfa y de color independientes también tienen dos conjuntos de datos de índice: uno para el conjunto vectorizado de canales y otro para el canal escalar. (En el caso del modo 4, estos índices tienen distintos anchos \[ de 2 o 3 \] bits. El modo 4 también contiene un selector de 1 bit que especifica si el vector o el canal escalar usa los índices de 3 bits).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Formato BC7](bc7-format.md)
</dt> </dl>

 

 




