---
description: Fuentes de trama, vectoriales, TrueType y OpenType
ms.assetid: 4fe98f04-3fb0-4a03-86c3-d0ea6f07f8f0
title: Fuentes de trama, vectoriales, TrueType y OpenType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e9b4be20ac7d02075fcd5c6cdbefe9eb516ea21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997324"
---
# <a name="raster-vector-truetype-and-opentype-fonts"></a>Fuentes de trama, vectoriales, TrueType y OpenType

Las aplicaciones pueden usar cuatro tipos diferentes de tecnologías de fuente para mostrar e imprimir texto:

-   Cuadrícula
-   Vector
-   TrueType
-   Microsoft OpenType

Las diferencias entre estas fuentes reflejan la manera en que el *glifo* de cada carácter o símbolo se almacena en el archivo de recursos de fuente respectivo:

-   En las fuentes de trama, un glifo es un mapa de bits que el sistema utiliza para dibujar un solo carácter o símbolo en la fuente.
-   En las fuentes de Vector, un glifo es una colección de extremos de línea que definen los segmentos de línea que el sistema utiliza para dibujar un carácter o un símbolo en la fuente.
-   En las fuentes TrueType y OpenType, un glifo es una colección de comandos de línea y curva, así como una colección de sugerencias.

El sistema utiliza los comandos line y Curve para definir el contorno del mapa de bits para un carácter o un símbolo en la fuente OpenType o OpenType de Microsoft. El sistema utiliza las sugerencias para ajustar la longitud de las líneas y formas de las curvas utilizadas para dibujar el carácter o el símbolo. Estas sugerencias y los ajustes respectivos se basan en la cantidad de escalado que se usa para reducir o aumentar el tamaño del mapa de bits. Una fuente OpenType es equivalente a una fuente TrueType, salvo que una fuente OpenType permite definiciones de glifo PostScript además de definiciones de glifos TrueType.

Dado que los mapas de bits de cada glifo en una fuente de trama están diseñados para una resolución específica del dispositivo, las fuentes de trama se suelen considerar dependientes del dispositivo. Por otro lado, las fuentes vectoriales no dependen del dispositivo, ya que cada glifo se almacena como una colección de líneas escalables. Sin embargo, las fuentes vectoriales normalmente se dibujan más lentamente que las fuentes raster o TrueType y OpenType. Las fuentes TrueType y OpenType proporcionan una velocidad de dibujo relativamente rápida y verdadera independencia del dispositivo. Mediante el uso de las sugerencias asociadas con un glifo, un programador puede escalar o reducir verticalmente los caracteres de una fuente TrueType o OpenType y mantener su forma original.

Como se mencionó anteriormente, los glifos de una fuente se almacenan en un archivo de recursos de fuente. Un archivo de recursos de fuente es realmente un archivo DLL que solo contiene datos, no hay ningún código. En el caso de las fuentes de trama y vectoriales, estos datos se dividen en dos partes: un encabezado que describe las métricas de la fuente y los datos del glifo. La extensión de nombre de archivo. fon identifica un archivo de recursos de fuente para una fuente de mapa de bits o de vector. En el caso de las fuentes TrueType y OpenType, hay dos archivos para cada fuente: el primer archivo contiene un encabezado relativamente corto y el segundo contiene los datos de la fuente real. El primer archivo se identifica mediante una extensión. fot y el segundo se identifica mediante una extensión. ttf.

 

 



