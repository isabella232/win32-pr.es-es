---
title: Exclusión mutua
description: Exclusión mutua
ms.assetid: 3a3f6763-a241-4bbd-a6e8-62041b05622d
keywords:
- Windows SDK de formato multimedia, exclusión mutua
- Formato de sistemas avanzados (ASF), exclusión mutua
- ASF (formato de sistemas avanzados), exclusión mutua
- Windows SDK de formato multimedia, exclusión mutua de MBR
- Formato de sistemas avanzados (ASF), exclusión mutua de MBR
- ASF (formato de sistemas avanzados), exclusión mutua de MBR
- Windows SDK de formato multimedia, velocidad de bits múltiple (MBR)
- Formato de sistemas avanzados (ASF), velocidad de bits múltiple (MBR)
- ASF (formato de sistemas avanzados), velocidad de bits múltiple (MBR)
- exclusión mutua, acerca de
- velocidad de bits múltiple (MBR), exclusión mutua
- MBR (velocidad de bits múltiple), exclusión mutua
- exclusión mutua, velocidad de bits
- exclusión mutua, idioma
- exclusión mutua, presentación
- exclusión mutua, desconocido
- exclusión mutua, características
- exclusión mutua, características avanzadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be220873965b10a0da8d22529fa735175bb8366ebe3088c7b1b385af6012b88a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084672"
---
# <a name="mutual-exclusion"></a>Exclusión mutua

Cada archivo ASF contiene una o varias secuencias, cada una con datos multimedia digitales. En circunstancias normales, cada secuencia está asociada a una única salida. En la reproducción, el objeto lector proporciona ejemplos para cada salida. Por lo tanto, de forma predeterminada, el lector entrega todas las secuencias de un archivo ASF durante la reproducción.

Hay situaciones en las que no desea que se entreguen todas las secuencias al cliente. Por ejemplo, si crea un archivo de vídeo con cinco secuencias de audio, una para cada uno de los cinco idiomas, desea que solo se entregue uno de ellos a la vez. La exclusión mutua es una característica del SDK de formato multimedia de Windows que permite especificar una serie de secuencias mutuamente excluyentes que equivalen a la misma salida.

La exclusión mutua se define en el perfil utilizado para crear un archivo. La exclusión mutua se configura en un perfil mediante objetos de exclusión mutua. Agregue secuencias de una en una al objeto de exclusión mutua, establezca el tipo e incluya el objeto en el perfil.

El SDK Windows Media Format reconoce cuatro tipos de exclusión mutua:

-   Velocidad de bits
-   Lenguaje
-   Presentación
-   Unknown

## <a name="mutual-exclusion-by-bit-rate"></a>Exclusión mutua por velocidad de bits

La exclusión mutua de velocidad de bits es un tipo especial de exclusión mutua y se conoce más comúnmente como exclusión mutua de velocidad de bits múltiple (MBR). Una exclusión mutua de MBR contiene una serie de secuencias que se originan en la misma entrada, pero se codifican a velocidades de bits diferentes. Al reproducir un archivo con MBR, el lector determina la mejor secuencia para usar en función del ancho de banda disponible.

El SDK Windows Media Format admite MBR para secuencias de audio y vídeo. El SDK también admite un tipo especial de vídeo MBR denominado MBR de tamaño de vídeo múltiple. Esto es como un vídeo MBR normal, salvo que las secuencias individuales pueden tener diferentes tamaños de fotograma. Por ejemplo, puede tener algunas secuencias con el tamaño de vídeo predeterminado de 320 x 240 y otras con velocidades de bits más altas y un tamaño de vídeo de 640 x 480.

## <a name="mutual-exclusion-by-language"></a>Exclusión mutua por idioma

La exclusión mutua basada en lenguaje está diseñada para su uso con contenido (normalmente audio) grabado en varios idiomas. Una exclusión mutua basada en lenguaje incluye varias secuencias que se originan a partir de entradas únicas. Cada entrada tiene el mismo contenido, pero en un idioma diferente.

Para que la exclusión mutua por idioma funcione, la aplicación de lectura debe incluir lógica para seleccionar el idioma adecuado. Si escribe una aplicación para reproducir archivos ASF y desea admitir archivos con exclusión mutua basada en lenguaje, debe seleccionar la secuencia adecuada antes de comenzar la reproducción.

## <a name="mutual-exclusion-by-presentation"></a>Exclusión mutua por presentación

La exclusión mutua basada en la presentación se proporciona para admitir secuencias de vídeo que contienen el mismo contenido codificado con diferentes relaciones de aspecto. Normalmente, esto se usa al proporcionar vídeo en una versión de letterbox (relación de aspecto 16:9), así como con formato para pantallas de televisión (relación de aspecto 4:3).

El usuario suele determinar la selección de una presentación para la reproducción. Si escribe una aplicación para reproducir archivos ASF y desea admitir archivos con exclusión mutua basada en presentación, debe presentar al usuario la opción de seleccionar un tipo de presentación para su visualización.

## <a name="unknown-mutual-exclusion"></a>Exclusión mutua desconocida

Puede crear la exclusión mutua en función de los criterios que quiera. Todos los tipos de exclusión mutua personalizados deben crearse con el tipo desconocido.

## <a name="advanced-mutual-exclusion-features"></a>Características avanzadas de exclusión mutua

También puede usar la exclusión mutua para asignar secuencias a grupos que se excluyen mutuamente entre sí. Por ejemplo, puede que desee tener secuencias de audio en varios idiomas y asignar una secuencia de vídeo diferente a cada uno. Use la exclusión mutua para agrupar cada secuencia de audio con su secuencia de vídeo correspondiente y hacer que todos los grupos se excluyen mutuamente.

El lector selecciona automáticamente secuencias para todas las exclusiones mutuas. Para todos los tipos de exclusión mutua excepto MBR y exclusión mutua basada en lenguaje, el lector siempre selecciona la secuencia predeterminada, que es la primera secuencia agregada al objeto de exclusión mutua en el perfil. Para MBR, el lector selecciona la secuencia que mejor se adapte al ancho de banda disponible en el momento de la reproducción. Si no desea usar la secuencia predeterminada, puede establecer la selección de secuencias en manual antes de empezar a leer un archivo.

La selección manual de secuencias se aplica a todo el archivo. Pueden surgir dificultades cuando se tienen exclusiones mutuas de distintos tipos en el mismo archivo. Por ejemplo, un archivo puede contener tanto la exclusión mutua basada en velocidad de bits como la exclusión mutua personalizada. Para seleccionar una secuencia que no sea la predeterminada en la exclusión mutua personalizada, debe usar la selección manual de secuencias. Sin embargo, si usa la selección manual de secuencias, el lector no seleccionará automáticamente la secuencia de velocidad de bits múltiple. Debe planear esta eventualidad en la aplicación si tiene previsto admitir varios tipos de exclusión mutua en un solo archivo. Normalmente, esto significa crear sus propias rutinas de selección de secuencias para los tipos normalmente automáticos de exclusión mutua.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características del archivo ASF**](asf-file-features.md)
</dt> <dt>

[**Uso de la exclusión mutua**](using-mutual-exclusion.md)
</dt> </dl>

 

 




