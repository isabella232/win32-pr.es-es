---
description: En este tema se describen los formatos YUV de 10 y 16 bits que se recomiendan para la captura, el procesamiento y la visualización de vídeo en el sistema operativo Microsoft Windows.
ms.assetid: fcaaaa6f-f886-4f6e-9c3c-e513ccc90d37
title: Formatos de vídeo YUV de 10 y 16 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bbc357653848cd51ce6f56ebd8a1da3e5f60403
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154467"
---
# <a name="10-bit-and-16-bit-yuv-video-formats"></a>Formatos de vídeo YUV de 10 y 16 bits

En este tema se describen los formatos YUV de 10 y 16 bits que se recomiendan para la captura, el procesamiento y la visualización de vídeo en el sistema operativo Microsoft Windows.

Este tema contiene las siguientes secciones:

-   [Información general](#overview)
-   [Códigos FOURCC para YUV de 10 bits y de 16 bits](#fourcc-codes-for-10-bit-and-16-bit-yuv)
-   [Definiciones de Surface](#surface-definitions)
    -   [formatos de 4:2:0](#420-formats)
    -   [formatos de 4:2:2](#422-formats)
    -   [formatos de 4:4:4](#444-formats)
-   [Formatos YUV preferidos](#preferred-yuv-formats)
-   [Temas relacionados](#related-topics)

## <a name="overview"></a>Información general

Estos formatos usan una representación de punto fijo tanto para el canal de luminancia como para los canales croma (C'b y C'r). Los valores de ejemplo son valores de 8 bits escalados, con un factor de escala de 2 ^ (n − 8), donde n es 10 o 16, según las secciones 7.7-7.8 y 7.11-7.12 de SMPTE 274M. Las conversiones de precisión se pueden realizar mediante desplazamientos de bits simples. Por ejemplo, si el punto blanco de un formato de 8 bits es 235, el formato de 10 bits correspondiente tiene un punto blanco en 940 (235 × 4).

Las representaciones de 16 bits que se describen aquí usan valores de **palabra** Little-Endian para cada canal. Los formatos de 10 bits también usan 16 bits para cada canal, con los 6 bits inferiores establecidos en cero, tal como se muestra en el diagrama siguiente.

![diagrama que muestra la representación de 10 bits](images/ee3aae23-4f0a-47d0-a46c-f3d7d94205e6.gif)

Dado que las representaciones de 10 bits y de 16 bits del mismo formato YUV tienen el mismo diseño de memoria, es posible convertir una representación de 10 bits en una representación de 16 sin pérdida de precisión. También es posible convertir una representación de 16 bits en una representación de 10 bits. (Los formatos Y416 y Y410 son una excepción a esta regla general, sin embargo, porque no comparten el mismo diseño de memoria).

Cuando el hardware gráfico Lee una superficie que contiene una representación de 10 bits, debe omitir los 6 bits de orden inferior de cada canal. Sin embargo, si una superficie contiene datos válidos de 16 bits, debe identificarse como una superficie de 16 bits.

En los formatos que contienen alfa, un píxel completamente transparente tiene un valor alfa de cero y un píxel completamente opaco tiene un valor alfa de (2 ^ n) – 1, donde n es el número de bits alfa. Se supone que alfa es un valor lineal que se aplica a cada componente después de que el componente se haya convertido en su forma lineal normalizada.

En el caso de las imágenes de la memoria de vídeo, el controlador de gráficos selecciona la alineación de memoria de la superficie. La superficie debe estar alineada con **DWORD** . Es decir, se garantiza que las líneas individuales dentro de una superficie empiezan en un límite de 32 bits, aunque la alineación puede ser superior a 32 bits. El origen (0,0) siempre es la esquina superior izquierda de la superficie.

Para los fines de esta documentación, el término *U* es equivalente a *CB* y el término *V* es equivalente a *CR*.

## <a name="fourcc-codes-for-10-bit-and-16-bit-yuv"></a>Códigos FOURCC para YUV de 10 bits y de 16 bits

Los códigos FOURCC para los formatos descritos aquí usan la Convención siguiente:

-   Si el formato es plano, el primer carácter del código FOURCC es ' P '. Si el formato es empaquetado, el primer carácter es ' Y '.
-   El segundo carácter del código FOURCC viene determinado por el muestreo de croma, tal y como se muestra en la tabla siguiente.

    

    | Muestreo de croma | Letra de código FOURCC |
    |-----------------|--------------------|
    | 4:4:4           | 4                |
    | 4:2:2           | dos                |
    | 4:2:1           | '1'                |
    | 4:2:0           | "0"                |

    

     

-   Los dos caracteres finales de FOURCC indican el número de bits por canal, ' 16 ' para 16 bits o ' 10 ' para 10 bits.

Con este esquema, se han definido los siguientes códigos FOURCC. En este momento no se han definido formatos 4:2:1 para el formato YUV de 10 bits o 16 bits.



| FOURCC | Descripción            |
|--------|------------------------|
| P016   | Planar, 4:2:0, 16 bits. |
| P010   | Planar, 4:2:0, 10 bits. |
| P216   | Planar, 4:2:2, 16 bits. |
| P210   | Planar, 4:2:2, 10 bits. |
| Y216   | Empaquetado, 4:2:2, 16 bits. |
| Y210   | Empaquetado, 4:2:2, 10 bits. |
| Y416   | Empaquetado, 4:4:4, 16 bits  |
| Y410   | Empaquetado, 4:4:4, 10 bits. |



 

Los GUID de subtipo también se han definido a partir de estos FOURCCs; vea [GUID de subtipo de vídeo](video-subtype-guids.md).

## <a name="surface-definitions"></a>Definiciones de Surface

En esta sección se describe el diseño de memoria de cada formato. En las descripciones siguientes, el término **palabra** hace referencia a un valor de 16 bits Little-endian y el término **DWORD** hace referencia a un valor little-endian de 32 bits.

### <a name="420-formats"></a>formatos de 4:2:0

Se definen dos formatos 4:2:0, con los códigos FOURCC P016 y P010. Comparten el mismo diseño de memoria, pero P016 usa 16 bits por canal y P010 usa 10 bits por canal.

### <a name="p016-and-p010"></a>P016 y P010

En estos dos formatos, todos los ejemplos Y aparecen en primer lugar en la memoria como una matriz de **palabras** con un número par de líneas. El intervalo de superficie puede ser mayor que el ancho del plano Y. Esta matriz va seguida inmediatamente por una matriz de **palabras** que contiene ejemplos intercalados y de V, tal como se muestra en el diagrama siguiente.

![diagrama que muestra el diseño de píxeles de P016 y P010](images/1e1c4d66-6172-4d3a-bd25-4b5caa67edcd.gif)

Si la matriz de U-V combinada se dirige como una matriz de **DWORD** s, la palabra menos significativa (LSW) contiene el valor U y la palabra más significativa (MSW) contiene el valor V. El intervalo del plano U-V combinado es igual que el intervalo del plano Y. El plano U-V tiene la mitad de tantas líneas como el plano Y.

Estos dos formatos son los formatos de píxel plano de 4:2:0 preferidos para las representaciones YUV de precisión superior. Se espera que sean un requisito intermedio para los aceleradores de aceleración de vídeo de DirectX (DXVA) que admiten vídeo 4:2:0 de 10 o 16 bits.

### <a name="422-formats"></a>formatos de 4:2:2

Se definen cuatro formatos de 4:2:2, dos planos y dos empaquetados. Tienen los siguientes códigos FOURCC:

-   P216
-   P210
-   Y216
-   Y210

### <a name="p216-and-p210"></a>P216 y P210

En estos dos formatos planos, todos los ejemplos Y aparecen en primer lugar en la memoria como una matriz de **palabras** con un número par de líneas. El intervalo de superficie puede ser mayor que el ancho del plano Y. Esta matriz va seguida inmediatamente por una matriz de **palabras** que contiene ejemplos intercalados y de V, tal como se muestra en el diagrama siguiente.

![diagrama que muestra el diseño de píxeles de P216 y P210](images/ff672fef-218f-4722-b806-d06c77fe8cfa.gif)

Si la matriz de U-V combinada se dirige como una matriz de **DWORD** s, LSW contiene el valor U y el MSW contiene el valor V. El intervalo del plano U-V combinado es igual que el intervalo del plano Y. El plano U-V tiene el mismo número de líneas que el plano Y.

Estos dos formatos son los formatos de píxel plano de 4:2:2 preferidos para las representaciones YUV de precisión superior. Se espera que sean un requisito intermedio para los aceleradores de aceleración de vídeo de DirectX (DXVA) que admiten vídeo 4:2:2 de 10 o 16 bits.

### <a name="y216-and-y210"></a>Y216 y Y210

En estos dos formatos empaquetados, cada par de píxeles se almacena como una matriz de cuatro **palabras**, tal y como se muestra en la siguiente ilustración.

![diagrama que muestra el diseño de píxeles de Y216 y y210.](images/6f68aeeb-18ca-48ee-82c4-5b79d5510e9f.gif)

La primera **palabra** de la matriz contiene el primer ejemplo y del par, la segunda **palabra** contiene el ejemplo U, la tercera **palabra** contiene el segundo ejemplo y y la cuarta **palabra** contiene el ejemplo V.

Y210 es idéntico a Y216, salvo que cada ejemplo contiene solo 10 bits de datos significativos. Los 6 bits menos significativos se establecen en cero, como se describió anteriormente.

### <a name="444-formats"></a>formatos de 4:4:4

Se definen dos formatos 4:4:4, con los códigos FOURCC Y410 y Y416. Ambos son formatos empaquetados.

### <a name="y410"></a>Y410

Este formato es una representación de 10 bits empaquetada que incluye 2 bits de alfa. Cada píxel se codifica como un **DWORD** único con el diseño de memoria que se muestra en el diagrama siguiente.

![diagrama que muestra el diseño de píxeles de y410.](images/f8a71437-e3f1-4331-be30-f766c028d648.gif)

Los bits 0-9 contienen el ejemplo U, bits 10-19 contienen el ejemplo Y, bits 20-29 contienen el ejemplo V y los bits 30-31 contienen el valor alfa. Para indicar que un píxel es totalmente opaco, una aplicación debe establecer los dos bits alfa iguales a 0x03.

### <a name="y416"></a>Y416

Este formato es una representación de 16 bits empaquetada que incluye 16 bits de alfa. Cada píxel se codifica como un par de **DWORD** s, tal y como se muestra en la siguiente ilustración.

![diagrama que muestra el diseño de píxeles de y416.](images/c928523a-25d3-4712-9aec-5b492b51435f.gif)

Los bits 0-15 contienen el ejemplo U, bits 16-31 contienen el ejemplo Y, bits 32-47 contienen el ejemplo V y los bits 48-63 contienen el valor alfa.

Para indicar que un píxel es totalmente opaco, una aplicación debe establecer los dos bits alfa iguales a 0xFFFF. Este formato está diseñado principalmente como un formato intermedio durante el procesamiento de imágenes para evitar la acumulación de errores.

## <a name="preferred-yuv-formats"></a>Formatos YUV preferidos

En la tabla siguiente se enumeran los formatos YUV preferidos, incluidos los formatos de 8 bits.



| Formato | Muestreo de croma | Empaquetado o plano | Bits por canal |
|--------|-----------------|------------------|------------------|
| AYUV   | 4:4:4           | Equipado           | 8                |
| Y410   | 4:4:4           | Equipado           | 10               |
| Y416   | 4:4:4           | Equipado           | 16               |
| AI44   | 4:4:4           | Equipado           | Paleta       |
| YUY2   | 4:2:2           | Equipado           | 8                |
| Y210   | 4:2:2           | Equipado           | 10               |
| Y216   | 4:2:2           | Equipado           | 16               |
| P210   | 4:2:2           | Trayectoria           | 10               |
| P216   | 4:2:2           | Trayectoria           | 16               |
| NV12   | 4:2:0           | Trayectoria           | 8                |
| P010   | 4:2:0           | Trayectoria           | 10               |
| P016   | 4:2:0           | Trayectoria           | 16               |
| NV11   | 4:1:1           | Trayectoria           | 8                |



 

Se recomienda que si un objeto admite una profundidad de bits determinada y un esquema de muestreo de croma, debe admitir los formatos YUV correspondientes que se enumeran en esta tabla. (Los objetos podrían admitir formatos adicionales que no se enumeran aquí).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Formatos YUV de 8 bits recomendados para la representación de vídeo](recommended-8-bit-yuv-formats-for-video-rendering.md)
</dt> <dt>

[GUID de subtipo de vídeo](video-subtype-guids.md)
</dt> <dt>

[Tipos de medios de vídeo](video-media-types.md)
</dt> </dl>

 

 



