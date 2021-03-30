---
title: Exclusión mutua
description: Exclusión mutua
ms.assetid: 3a3f6763-a241-4bbd-a6e8-62041b05622d
keywords:
- SDK de Windows Media Format, exclusión mutua
- Advanced Systems Format (ASF), exclusión mutua
- ASF (formato de sistemas avanzados), exclusión mutua
- SDK de Windows Media Format, exclusión mutua de MBR
- Advanced Systems Format (ASF), exclusión mutua de MBR
- ASF (formato de sistemas avanzados), exclusión mutua de MBR
- Windows Media Format SDK, velocidad de bits múltiple (MBR)
- Advanced Systems Format (ASF), velocidad de bits múltiple (MBR)
- ASF (formato de sistemas avanzados), velocidad de bits múltiple (MBR)
- exclusión mutua, acerca de
- velocidad de bits múltiple (MBR), exclusión mutua
- MBR (velocidad de varios bits), exclusión mutua
- exclusión mutua, velocidad de bits
- exclusión mutua, lenguaje
- exclusión mutua, presentación
- exclusión mutua, desconocida
- exclusión mutua, características
- exclusión mutua, características avanzadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd00bf5bcb544d2541a6bc5465171fe9bacc1b9c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903846"
---
# <a name="mutual-exclusion"></a>Exclusión mutua

Cada archivo ASF contiene una o más secuencias, cada una de las cuales contiene datos multimedia digitales. En circunstancias normales, cada flujo está asociado a una sola salida. En la reproducción, el objeto de lector proporciona ejemplos para cada salida. Por lo tanto, de forma predeterminada, el lector entrega cada secuencia en un archivo ASF en la reproducción.

Hay situaciones en las que no desea que cada flujo se entregue al cliente. Por ejemplo, si crea un archivo de vídeo con cinco flujos de audio, uno para cada uno de los cinco idiomas, querrá que solo se entregue uno de ellos a la vez. La exclusión mutua es una característica del SDK de Windows Media Format que le permite especificar un número de flujos mutuamente excluyentes que equivalen a la misma salida.

La exclusión mutua se define en el perfil que se usa para crear un archivo. La exclusión mutua se configura en un perfil mediante el uso de objetos de exclusión mutua. Las secuencias se agregan de una en una al objeto de exclusión mutua, se establece el tipo e incluyen el objeto en el perfil.

El SDK de Windows Media Format reconoce cuatro tipos de exclusión mutua:

-   Velocidad de bits
-   Idioma
-   Presentación
-   Unknown

## <a name="mutual-exclusion-by-bit-rate"></a>Exclusión mutua por velocidad de bits

La exclusión mutua de velocidad de bits es un tipo especial de exclusión mutua y se conoce más comúnmente como exclusión mutua de velocidad de bits múltiple (MBR). Una exclusión mutua de MBR contiene un número de flujos que se originan a partir de la misma entrada, pero se codifican a velocidades de bits diferentes. Al reproducir un archivo con MBR, el lector determina el mejor flujo que se va a usar en función del ancho de banda disponible.

El SDK de Windows Media Format admite MBR para secuencias de audio y vídeo. El SDK también admite un tipo especial de vídeo MBR denominado Multiple video size MBR. Esto es como el vídeo MBR normal, salvo que los flujos individuales pueden tener distintos tamaños de fotogramas. Por ejemplo, podría tener algunos flujos con el tamaño de vídeo de 320 x 240 predeterminado y otros con velocidades de bits más altas y un tamaño de vídeo de 640 x 480.

## <a name="mutual-exclusion-by-language"></a>Exclusión mutua por idioma

La exclusión mutua basada en el lenguaje está diseñada para su uso con contenido (normalmente audio) registrado en varios idiomas. Una exclusión mutua basada en el lenguaje incluye varios flujos que se originan a partir de entradas únicas. Cada entrada es el mismo contenido, pero en un lenguaje diferente.

Para que la exclusión mutua esté en funcionamiento, la aplicación de lectura debe incluir lógica para seleccionar el idioma adecuado. Si escribe una aplicación para reproducir archivos ASF y desea admitir archivos con exclusión mutua basada en el idioma, debe seleccionar la secuencia adecuada antes de comenzar la reproducción.

## <a name="mutual-exclusion-by-presentation"></a>Exclusión mutua por presentación

La exclusión mutua basada en la presentación se proporciona para admitir secuencias de vídeo que contienen el mismo contenido codificado con diferentes relaciones de aspecto. Normalmente, se usa cuando se proporciona vídeo en una versión de pantalla panorámica (relación de aspecto 16:9), así como con formato para pantallas de televisión (relación de aspecto 4:3).

La selección de una presentación para la reproducción suele estar determinada por el usuario. Si escribe una aplicación para reproducir archivos ASF y desea admitir archivos con exclusión mutua basada en la presentación, debe presentar al usuario la opción de seleccionar un tipo de presentación para su visualización.

## <a name="unknown-mutual-exclusion"></a>Exclusión mutua desconocida

Puede crear una exclusión mutua en función de los criterios que desee. Todos los tipos de exclusión mutua personalizados se deben crear con el tipo desconocido.

## <a name="advanced-mutual-exclusion-features"></a>Características avanzadas de exclusión mutua

También puede usar la exclusión mutua para asignar secuencias a grupos que se excluyen mutuamente entre sí. Por ejemplo, puede que desee tener secuencias de audio en varios idiomas y asignar un flujo de vídeo diferente a cada una. La exclusión mutua se usa para agrupar cada secuencia de audio con su secuencia de vídeo correspondiente y hacer que todos los grupos sean mutuamente excluyentes.

El lector selecciona automáticamente las secuencias para todas las exclusiones mutuas. Para todos los tipos de exclusión mutua, excepto el MBR y la exclusión mutua basada en el lenguaje, el lector selecciona siempre la secuencia predeterminada, que es la primera secuencia que se agrega al objeto de exclusión mutua en el perfil. En el caso de MBR, el lector selecciona la secuencia que mejor se adapta al ancho de banda disponible en el momento de la reproducción. Si no desea usar el flujo predeterminado, puede establecer la selección de la secuencia en manual antes de empezar a leer un archivo.

La selección de secuencias manual se aplica a todo el archivo. Pueden surgir dificultades si tiene exclusiones mutuas de diferentes tipos en el mismo archivo. Por ejemplo, un archivo puede contener la exclusión mutua basada en tasas de bits y la exclusión mutua personalizada. Para seleccionar una secuencia que no sea la predeterminada en la exclusión mutua personalizada, debe utilizar la selección de flujo manual. Sin embargo, si usa la selección de flujo manual, el lector no seleccionará automáticamente el flujo de velocidad de bits múltiple. Debe planear esta eventualidad en la aplicación si tiene previsto admitir varios tipos de exclusiones mutuas en un único archivo. Normalmente esto significa la creación de sus propias rutinas de selección de secuencias para tipos de exclusión mutua normalmente automáticos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de archivos ASF**](asf-file-features.md)
</dt> <dt>

[**Usar exclusión mutua**](using-mutual-exclusion.md)
</dt> </dl>

 

 




