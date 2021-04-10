---
description: Muchas aplicaciones necesitan usar la compresión y descompresión de datos sin pérdida de información. La API de compresión simplifica esto al exponer algoritmos de compresión de Windows a través de una API pública.
ms.assetid: D603A7DE-D4A1-4515-9702-B03C81504661
title: Uso de la API de compresión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01eff163f4ea1ccf03e1cd4ac9cb16a26afeb265
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153394"
---
# <a name="using-the-compression-api"></a>Uso de la API de compresión

Muchas aplicaciones necesitan usar la compresión y descompresión de datos sin pérdida de información. La API de compresión simplifica esto al exponer algoritmos de compresión de Windows a través de una API pública. Cada algoritmo de compresión tiene un conjunto de propiedades que controla su comportamiento. La API de compresión expone una interfaz que permite al desarrollador establecer o consultar los valores de estas propiedades. Todas las propiedades de los algoritmos de compresión admitidos tienen valores predeterminados que representan los valores de estas propiedades que se usan habitualmente. Si se requiere una propiedad para la compresión y la descompresión, los valores predeterminados serán idénticos, asegurándose de que se usan valores idénticos para la compresión y la descompresión.

## <a name="selecting-the-compression-algorithm"></a>Seleccionar el algoritmo de compresión

Después de que un desarrollador decida que una aplicación necesita comprimir o descomprimir datos, el paso siguiente consiste en elegir un algoritmo de compresión. Esto puede depender de las pruebas para encontrar la mejor combinación de velocidad, razón de compresión y requisito de memoria para una aplicación determinada. La lista siguiente proporciona una comparación relativa de los algoritmos de compresión que admite actualmente la API de compresión. No todas las opciones están disponibles para todos los algoritmos de compresión y la comparación es aproximada, ya que el rendimiento puede depender de los datos de entrada.

XPRESS (**compress \_ algorithm \_ Xpress**)

-   Muy rápido con pocos requisitos de recursos
-   Razón de compresión media
-   Velocidades de compresión y descompresión elevadas
-   Requisito de memoria insuficiente
-   Admite la **opción \_ comprimir \_ \_ nivel de clase de información** disponible en la enumeración [**comprimir \_ \_ clase de información**](/windows/desktop/api/compressapi/ne-compressapi-compress_information_class) . El valor predeterminado es **(DWORD) 0**. En algunos datos, el valor **(DWORD) 1** puede mejorar la razón de compresión con una velocidad de compresión ligeramente más lenta.

XPRESS con codificación Huffman (**compress \_ algorithm \_ Xpress \_ García**)

-   La razón de compresión es mayor que **compress \_ algorithm \_ Xpress**
-   Razón de compresión media
-   Velocidades de compresión y descompresión medianos alta
-   Requisito de memoria insuficiente
-   Admite la **opción \_ comprimir \_ \_ nivel de clase de información** en la enumeración [**comprimir \_ \_ clase de información**](/windows/desktop/api/compressapi/ne-compressapi-compress_information_class) . El valor predeterminado es **(DWORD) 0**. En algunos datos, el valor **(DWORD) 1** puede mejorar la razón de compresión con una velocidad de compresión ligeramente más lenta.

MSZIP (**comprimir \_ algoritmo \_ MSZIP**)

-   Usa más recursos que **compress \_ algorithm \_ Xpress \_ García**
-   Genera un bloque comprimido similar a RFC 1951.
-   Razón de compresión media a alta
-   Velocidad de compresión media y velocidad de descompresión alta
-   Requisito de memoria media

LZMS (**comprimir \_ algoritmo \_ LZMS**)

-   Buen algoritmo si el tamaño de los datos que se van a comprimir es superior a 2 MB.
-   Razón de compresión alta
-   Velocidad de compresión baja y velocidad de descompresión alta
-   Requisitos de memoria media y alta
-   Admite la opción de **tamaño de bloque comprimir \_ \_ clase \_ \_ de información** en la enumeración [**comprimir \_ \_ clase de información**](/windows/desktop/api/compressapi/ne-compressapi-compress_information_class) . Se sugiere un tamaño mínimo de 1 MB para obtener una mejor relación de compresión.

## <a name="deciding-which-compression-api-mode-to-use"></a>Decidir qué modo de API de compresión usar

Después de que un desarrollador Seleccione el algoritmo de compresión, la siguiente decisión es cuál de los dos modos de la API de compresión usar: modo de búfer o modo de bloque. El modo de búfer se desarrolló para facilitar su uso y se recomienda para la mayoría de los casos.

El modo de búfer divide automáticamente el búfer de entrada en bloques de un tamaño adecuado para el algoritmo de compresión seleccionado. El modo de búfer aplica formato y almacena automáticamente el tamaño de búfer sin comprimir en el búfer comprimido. El tamaño del búfer comprimido no se guarda automáticamente y la aplicación tiene que guardarlo para la descompresión. No incluya la marca **compress \_ raw** en el parámetro *algorithm* cuando llame a [**CreateCompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) y [**CreateDecompressor**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor) para usar el modo de búfer. Para obtener un ejemplo de código de una aplicación de modo de búfer, consulte la sección [uso de la API de compresión en modo de búfer](using-the-compression-api-in-buffer-mode.md) .

El modo de bloqueo permite al desarrollador controlar el tamaño de bloque, pero la aplicación requiere más trabajo. Al usar el modo de bloqueo, la aplicación tiene que interrumpir los datos de entrada en piezas de tamaño adecuado al comprimir y, a continuación, volver a colocar los fragmentos al descomprimir. El modo de bloqueo produce un error si el tamaño del búfer de entrada es mayor que el tamaño de bloque interno del algoritmo de compresión. El tamaño de bloque interno es de 32 KB para MSZIP y 1 GB para los algoritmos de compresión XPRESS. El tamaño de bloque interno para LZMS es configurable hasta 64 GB con un aumento de uso de memoria correspondiente. El tamaño del búfer comprimido no se guarda automáticamente y la aplicación también necesita guardarlo para la descompresión. El valor del parámetro *UncompressedBufferSize* de [**descomprimir**](/windows/desktop/api/compressapi/nf-compressapi-decompress) debe ser exactamente igual al tamaño original de los datos sin comprimir y no solo al tamaño del búfer de salida. Esto significa que la aplicación debe guardar el tamaño original exacto de los datos sin comprimir, así como los datos comprimidos y el tamaño comprimido, al usar el modo de bloqueo. Incluya la **marca compress \_ raw** en el parámetro *algorithm* cuando llame a [**CreateCompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) y [**CreateDecompressor**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor) para usar el modo de bloqueo. Para obtener un ejemplo de código de una aplicación en modo de bloque, consulte la sección [uso de la API de compresión en modo de bloqueo](using-the-compression-api-in-block-mode.md) .

## <a name="custom-memory-allocation"></a>Asignación de memoria personalizada

Las aplicaciones en modo de búfer y de bloque tienen la opción de especificar una rutina de asignación de memoria personalizada cuando llaman a [**CreateCompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) y [**CreateDecompressor**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor). El parámetro *AllocationRoutines* especifica la estructura de [**\_ \_ rutinas de asignación de compresión**](/windows/desktop/api/compressapi/ns-compressapi-compress_allocation_routines) que contiene la rutina de asignación de memoria. A continuación, la aplicación puede establecer el tamaño de bloque para el compresor mediante [**SetCompressorInformation**](/windows/desktop/api/compressapi/nf-compressapi-setcompressorinformation). Consulte la sección [uso de la API de compresión en modo de bloqueo](using-the-compression-api-in-block-mode.md) para ver un ejemplo de una rutina de asignación personalizada simple.

 

 



