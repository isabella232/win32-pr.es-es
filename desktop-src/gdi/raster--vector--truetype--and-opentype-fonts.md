---
description: Fuentes Raster, Vector, TrueType y OpenType
ms.assetid: 4fe98f04-3fb0-4a03-86c3-d0ea6f07f8f0
title: Fuentes Raster, Vector, TrueType y OpenType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e9b4be20ac7d02075fcd5c6cdbefe9eb516ea21
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566412"
---
# <a name="raster-vector-truetype-and-opentype-fonts"></a>Fuentes Raster, Vector, TrueType y OpenType

Las aplicaciones pueden usar cuatro tipos diferentes de tecnologías de fuente para mostrar e imprimir texto:

-   Mapa de bits
-   Vector
-   TrueType
-   Microsoft OpenType

Las diferencias entre estas fuentes reflejan la manera en que el *glifo* de cada carácter o símbolo se almacena en el archivo de recursos de fuente correspondiente:

-   En las fuentes de trama, un glifo es un mapa de bits que el sistema usa para dibujar un solo carácter o símbolo en la fuente.
-   En las fuentes vectoriales, un glifo es una colección de puntos de conexión de línea que definen los segmentos de línea que el sistema usa para dibujar un carácter o símbolo en la fuente.
-   En las fuentes TrueType y OpenType, un glifo es una colección de comandos de línea y curva, así como una colección de sugerencias.

El sistema usa los comandos de línea y curva para definir el contorno del mapa de bits de un carácter o símbolo en la fuente TrueType o Microsoft OpenType. El sistema usa las sugerencias para ajustar la longitud de las líneas y formas de las curvas utilizadas para dibujar el carácter o el símbolo. Estas sugerencias y los ajustes respectivos se basan en la cantidad de escalado que se usa para reducir o aumentar el tamaño del mapa de bits. Una fuente OpenType es equivalente a una fuente TrueType, salvo que una fuente OpenType permite PostScript definiciones de glifo además de definiciones de glifo TrueType.

Dado que los mapas de bits de cada glifo de una fuente de trama están diseñados para una resolución específica del dispositivo, las fuentes de trama generalmente se consideran dependientes del dispositivo. Por otro lado, las fuentes vectoriales no dependen del dispositivo, ya que cada glifo se almacena como una colección de líneas escalables. Sin embargo, las fuentes vectoriales suelen dibujarse más lentamente que las fuentes raster o TrueType y OpenType. Las fuentes TrueType y OpenType proporcionan velocidad de dibujo relativamente rápida y verdadera independencia del dispositivo. Mediante el uso de las sugerencias asociadas a un glifo, un desarrollador puede escalar o reducir verticalmente los caracteres de una fuente TrueType o OpenType y mantener su forma original.

Como se mencionó anteriormente, los glifos de una fuente se almacenan en un archivo font-resource. Un archivo de recursos de fuente es realmente un archivo DLL que contiene solo datos, no hay código. Para las fuentes de trama y vector, estos datos se dividen en dos partes: un encabezado que describe las métricas de la fuente y los datos del glifo. La extensión de nombre de archivo .fon identifica un archivo de recursos de fuente para una fuente de trama o vector. Para las fuentes TrueType y OpenType, hay dos archivos para cada fuente: el primer archivo contiene un encabezado relativamente corto y el segundo contiene los datos de fuente reales. El primer archivo se identifica mediante una extensión .fot y el segundo se identifica mediante una extensión .ttf.

 

 



