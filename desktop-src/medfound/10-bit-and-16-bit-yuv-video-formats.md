---
description: En este tema se describen los formatos YUV de 10 y 16 bits que se recomiendan para capturar, procesar y mostrar vídeo en el sistema operativo microsoft Windows.
ms.assetid: fcaaaa6f-f886-4f6e-9c3c-e513ccc90d37
title: Formatos de vídeo YUV de 10 y 16 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bbc357653848cd51ce6f56ebd8a1da3e5f60403
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467217"
---
# <a name="10-bit-and-16-bit-yuv-video-formats"></a>Formatos de vídeo YUV de 10 y 16 bits

En este tema se describen los formatos YUV de 10 y 16 bits que se recomiendan para capturar, procesar y mostrar vídeo en el sistema operativo microsoft Windows.

Este tema contiene las siguientes secciones:

-   [Información general](#overview)
-   [Códigos FOURCC para YUV de 10 y 16 bits](#fourcc-codes-for-10-bit-and-16-bit-yuv)
-   [Definiciones de surface](#surface-definitions)
    -   [Formatos 4:2:0](#420-formats)
    -   [Formatos 4:2:2](#422-formats)
    -   [Formatos 4:4:4](#444-formats)
-   [Formatos YUV preferidos](#preferred-yuv-formats)
-   [Temas relacionados](#related-topics)

## <a name="overview"></a>Información general

Estos formatos usan una representación de punto fijo para los canales luma y verón (C'b y C'r). Los valores de ejemplo se escalan con valores de 8 bits, con un factor de escalado de 2^(n - 8), donde n es 10 o 16, según las secciones 7.7-7.8 y 7.11-7.12 de SMPTE 274M. Las conversiones de precisión se pueden realizar mediante desplazamientos de bits simples. Por ejemplo, si el punto blanco de un formato de 8 bits es 235, el formato de 10 bits correspondiente tiene un punto blanco en 940 (235 × 4).

Las representaciones de 16 bits que se describen aquí usan valores **word** little-endian para cada canal. Los formatos de 10 bits también usan 16 bits para cada canal, con los 6 bits más bajos establecidos en cero, como se muestra en el diagrama siguiente.

![diagrama que muestra una representación de 10 bits](images/ee3aae23-4f0a-47d0-a46c-f3d7d94205e6.gif)

Dado que las representaciones de 10 y 16 bits del mismo formato YUV tienen el mismo diseño de memoria, es posible convertir una representación de 10 bits en una representación de 16 bits sin pérdida de precisión. También es posible convertir una representación de 16 bits en una representación de 10 bits. (Los formatos Y416 e Y410 son una excepción a esta regla general, sin embargo, porque no comparten el mismo diseño de memoria).

Cuando el hardware gráfico lee una superficie que contiene una representación de 10 bits, debe omitir los 6 bits de orden inferior de cada canal. Sin embargo, si una superficie contiene datos válidos de 16 bits, debe identificarse como una superficie de 16 bits.

En los formatos que contienen alfa, un píxel completamente transparente tiene un valor alfa de cero y un píxel completamente opaco tiene un valor alfa de (2^n) – 1, donde n es el número de bits alfa. Alfa se supone que es un valor lineal que se aplica a cada componente después de que el componente se haya convertido a su forma lineal normalizada.

En el caso de las imágenes en la memoria de vídeo, el controlador de gráficos selecciona la alineación de la memoria de la superficie. La superficie debe estar **alineada con DWORD.** Es decir, se garantiza que las líneas individuales de una superficie comienzan en un límite de 32 bits, aunque la alineación puede ser superior a 32 bits. El origen (0,0) siempre es la esquina superior izquierda de la superficie.

Para los fines de esta documentación, el término *U* es equivalente a *Cb* y el término *V* es equivalente a *Cr*.

## <a name="fourcc-codes-for-10-bit-and-16-bit-yuv"></a>Códigos FOURCC para YUV de 10 y 16 bits

Los códigos FOURCC para los formatos descritos aquí usan la convención siguiente:

-   Si el formato es plana, el primer carácter del código FOURCC es "P". Si el formato está empaquetado, el primer carácter es "Y".
-   El segundo carácter del código FOURCC viene determinado por el muestreo de muestreo, como se muestra en la tabla siguiente.

    

    | Muestreo de muestreo de muestreo | Letra de código FOURCC |
    |-----------------|--------------------|
    | 4:4:4           | '4'                |
    | 4:2:2           | '2'                |
    | 4:2:1           | '1'                |
    | 4:2:0           | "0"                |

    

     

-   Los dos caracteres finales de FOURCC indican el número de bits por canal, ya sea "16" para 16 bits o "10" para 10 bits.

Con este esquema, se han definido los siguientes códigos FOURCC. No se han definido formatos 4:2:1 para YUV de 10 o 16 bits en este momento.



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



 

Los GUID de subtipo también se han definido a partir de estos FOURCC; vea [GUID de subtipo de vídeo.](video-subtype-guids.md)

## <a name="surface-definitions"></a>Definiciones de surface

En esta sección se describe el diseño de memoria de cada formato. En las descripciones siguientes, el término **WORD** hace referencia a un valor little-endian de 16 bits y el término **DWORD** hace referencia a un valor little-endian de 32 bits.

### <a name="420-formats"></a>Formatos 4:2:0

Se definen dos formatos 4:2:0, con los códigos FOURCC P016 y P010. Comparten el mismo diseño de memoria, pero P016 usa 16 bits por canal y P010 usa 10 bits por canal.

### <a name="p016-and-p010"></a>P016 y P010

En estos dos formatos, todos los ejemplos de Y aparecen primero en memoria como una matriz de **WORD** con un número par de líneas. El paso de superficie puede ser mayor que el ancho del plano Y. Esta matriz va seguida inmediatamente de una matriz de **WORD** que contiene ejemplos intercalados de usted y V, como se muestra en el diagrama siguiente.

![diagrama que muestra el diseño de píxeles p016 y p010](images/1e1c4d66-6172-4d3a-bd25-4b5caa67edcd.gif)

Si la matriz de U-V combinada se trata como una matriz de **DWORD,** la palabra menos significativa (LSW) contiene el valor U y la palabra más significativa (MSW) contiene el valor V. El paso del plano de U-V combinado es igual al paso del plano Y. El plano U-V tiene la mitad de líneas que el plano Y.

Estos dos formatos son los formatos de píxel plano preferidos de 4:2:0 para las representaciones YUV de mayor precisión. Se espera que sean un requisito a medio plazo para los aceleradores de aceleración de vídeo de DirectX (DXVA) que admiten vídeo de 10 o 16 bits 4:2:0.

### <a name="422-formats"></a>Formatos 4:2:2

Se definen cuatro formatos 4:2:2, dos planas y dos empaquetados. Tienen los siguientes códigos FOURCC:

-   P216
-   P210
-   Y216
-   Y210

### <a name="p216-and-p210"></a>P216 y P210

En estos dos formatos planas, todos los ejemplos de Y aparecen primero en memoria como una matriz de **WORD** con un número par de líneas. El paso de superficie puede ser mayor que el ancho del plano Y. Esta matriz va seguida inmediatamente de una matriz de **WORD** que contiene ejemplos intercalados de usted y V, como se muestra en el diagrama siguiente.

![diagrama que muestra el diseño de píxeles p216 y p210](images/ff672fef-218f-4722-b806-d06c77fe8cfa.gif)

Si la matriz de U-V combinada se trata como una matriz de **DWORD,** el LSW contiene el valor U y el MSW contiene el valor V. El paso del plano de U-V combinado es igual al paso del plano Y. El plano U-V tiene el mismo número de líneas que el plano Y.

Estos dos formatos son los formatos de píxel plano preferidos de 4:2:2 para las representaciones YUV de mayor precisión. Se espera que sean un requisito de término intermedio para los aceleradores de aceleración de vídeo de DirectX (DXVA) que admiten vídeo de 10 o 16 bits de 4:2:2.

### <a name="y216-and-y210"></a>Y216 e Y210

En estos dos formatos empaquetados, cada par de píxeles se almacena como una matriz de cuatro **WORD** s, como se muestra en la ilustración siguiente.

![diagrama que muestra el diseño de píxeles y216 e y210.](images/6f68aeeb-18ca-48ee-82c4-5b79d5510e9f.gif)

La primera **PALABRA** de la matriz contiene la primera muestra Y del  par, la segunda **WORD** contiene el ejemplo U, la tercera WORD contiene la segunda muestra Y y la cuarta **word** contiene la muestra V.

Y210 es idéntico a Y216, salvo que cada muestra contiene solo 10 bits de datos significativos. Los 6 bits menos significativos se establecen en cero, como se ha descrito anteriormente.

### <a name="444-formats"></a>Formatos 4:4:4

Se definen dos formatos 4:4:4, con los códigos FOURCC Y410 e Y416. Ambos son formatos empaquetados.

### <a name="y410"></a>Y410

Este formato es una representación empaquetada de 10 bits que incluye 2 bits de alfa. Cada píxel se codifica como un único **DWORD** con el diseño de memoria que se muestra en el diagrama siguiente.

![diagrama que muestra el diseño de píxeles y410.](images/f8a71437-e3f1-4331-be30-f766c028d648.gif)

Los bits 0-9 contienen la muestra U, los bits 10-19 contienen la muestra Y, los bits 20-29 contienen la muestra V y los bits 30-31 contienen el valor alfa. Para indicar que un píxel es totalmente opaco, una aplicación debe establecer los dos bits alfa iguales a 0x03.

### <a name="y416"></a>Y416

Este formato es una representación empaquetada de 16 bits que incluye 16 bits de alfa. Cada píxel se codifica como un par de **DWORD,** como se muestra en la ilustración siguiente.

![diagrama que muestra el diseño de píxeles y416.](images/c928523a-25d3-4712-9aec-5b492b51435f.gif)

Los bits 0-15 contienen la muestra U, los bits 16-31 contienen la muestra Y, los bits 32-47 contienen la muestra V y los bits 48-63 contienen el valor alfa.

Para indicar que un píxel es totalmente opaco, una aplicación debe establecer los dos bits alfa iguales a 0xFFFF. Este formato está pensado principalmente como un formato intermedio durante el procesamiento de imágenes para evitar la acumulación de errores.

## <a name="preferred-yuv-formats"></a>Formatos YUV preferidos

En la tabla siguiente se enumeran los formatos YUV preferidos, incluidos los formatos de 8 bits.



| Formato | Muestreo de muestreo de muestreo | Empaquetado o plano | Bits por canal |
|--------|-----------------|------------------|------------------|
| AYUV   | 4:4:4           | Embalado           | 8                |
| Y410   | 4:4:4           | Embalado           | 10               |
| Y416   | 4:4:4           | Embalado           | 16               |
| AI44   | 4:4:4           | Embalado           | Se ha desenlazado       |
| YUY2   | 4:2:2           | Embalado           | 8                |
| Y210   | 4:2:2           | Embalado           | 10               |
| Y216   | 4:2:2           | Embalado           | 16               |
| P210   | 4:2:2           | Planar           | 10               |
| P216   | 4:2:2           | Planar           | 16               |
| NV12   | 4:2:0           | Planar           | 8                |
| P010   | 4:2:0           | Planar           | 10               |
| P016   | 4:2:0           | Planar           | 16               |
| NV11   | 4:1:1           | Planar           | 8                |



 

Se recomienda que si un objeto admite una profundidad de bits determinada y un esquema de muestreo, debe admitir los formatos YUV correspondientes enumerados en esta tabla. (Los objetos pueden admitir formatos adicionales que no se enumeran aquí).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Formatos YUV de 8 bits recomendados para la representación en vídeo](recommended-8-bit-yuv-formats-for-video-rendering.md)
</dt> <dt>

[GUID de subtipo de vídeo](video-subtype-guids.md)
</dt> <dt>

[Tipos de medios de vídeo](video-media-types.md)
</dt> </dl>

 

 



