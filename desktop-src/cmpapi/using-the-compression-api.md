---
description: Muchas aplicaciones necesitan usar la compresión de datos sin pérdida y la descompresión. La API de compresión simplifica esto al exponer Windows algoritmos de compresión a través de una API pública.
ms.assetid: D603A7DE-D4A1-4515-9702-B03C81504661
title: Uso de compression API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fedc1d57ad48196290500383686b35f557c87c34099aad842b1e8ff18f00d318
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118551389"
---
# <a name="using-the-compression-api"></a>Uso de compression API

Muchas aplicaciones necesitan usar la compresión de datos sin pérdida y la descompresión. La API de compresión simplifica esto al exponer Windows algoritmos de compresión a través de una API pública. Cada algoritmo de compresión tiene un conjunto de propiedades que controla su comportamiento. Compression API expone una interfaz que permite al desarrollador establecer o consultar los valores de estas propiedades. Todas las propiedades de los algoritmos de compresión admitidos tienen valores predeterminados que representan los valores usados habitualmente de estas propiedades. Si se requiere una propiedad para la compresión y la descompresión, los valores predeterminados serán idénticos, lo que garantiza que se usan valores idénticos para la compresión y la descompresión.

## <a name="selecting-the-compression-algorithm"></a>Selección del algoritmo de compresión

Una vez que un desarrollador decide que una aplicación necesita comprimir o descomprimir datos, el siguiente paso es elegir un algoritmo de compresión. Esto puede depender de las pruebas para encontrar la combinación de mejor rendimiento de velocidad, relación de compresión y requisito de memoria para una aplicación determinada. En la lista siguiente se proporciona una comparación relativa de los algoritmos de compresión admitidos actualmente por compression API. No todas las opciones están disponibles para cada algoritmo de compresión y la comparación es aproximada porque el rendimiento puede depender de los datos de entrada.

XPRESS (**COMPRESS \_ ALGORITHM \_ XPRESS**)

-   Muy rápido con requisitos de recursos bajos
-   Proporción de compresión media
-   Velocidades de compresión y descompresión elevadas
-   Requisito de memoria baja
-   Admite la opción **COMPRESS INFORMATION CLASS LEVEL \_ \_ \_ disponible** en la [**enumeración COMPRESS INFORMATION \_ \_ CLASS.**](/windows/desktop/api/compressapi/ne-compressapi-compress_information_class) El valor predeterminado es **(DWORD)0.** Para algunos datos, el valor **(DWORD)1** puede mejorar la relación de compresión con una velocidad de compresión ligeramente más lenta.

XPRESS con codificación Huffman (**COMPRESS \_ ALGORITHM \_ XPRESS \_ HUFF**)

-   La proporción de compresión es mayor que **COMPRESS \_ ALGORITHM \_ XPRESS**
-   Proporción de compresión media
-   Velocidades de compresión y descompresión de media a alta
-   Requisito de memoria baja
-   Admite la **opción COMPRESS INFORMATION CLASS \_ \_ \_ LEVEL** en la [**enumeración COMPRESS INFORMATION \_ \_ CLASS.**](/windows/desktop/api/compressapi/ne-compressapi-compress_information_class) El valor predeterminado es **(DWORD)0.** Para algunos datos, el valor **(DWORD)1** puede mejorar la relación de compresión con una velocidad de compresión ligeramente más lenta.

MSZIP (**COMPRESS \_ ALGORITHM \_ MSZIP**)

-   Usa más recursos que **COMPRESS \_ ALGORITHM \_ XPRESS \_ HUFF**
-   Genera un bloque comprimido similar a RFC 1951.
-   Relación de compresión media a alta
-   Velocidad de compresión media y alta velocidad de descompresión
-   Requisito de memoria media

LZMS (**COMPRESS \_ ALGORITHM \_ LZMS**)

-   Algoritmo correcto si el tamaño de los datos que se va a comprimir es de más de 2 MB.
-   Relación de compresión alta
-   Baja velocidad de compresión y alta velocidad de descompresión
-   Requisito de memoria media a alta
-   Admite la opción **COMPRESS INFORMATION CLASS BLOCK \_ \_ \_ \_ SIZE** en la [**enumeración COMPRESS INFORMATION \_ \_ CLASS.**](/windows/desktop/api/compressapi/ne-compressapi-compress_information_class) Se recomienda un tamaño mínimo de 1 MB para obtener una mejor relación de compresión.

## <a name="deciding-which-compression-api-mode-to-use"></a>Decidir qué modo de API de compresión usar

Después de que un desarrollador seleccione el algoritmo de compresión, la siguiente decisión es cuál de los dos modos de la API de compresión debe usar: modo de búfer o modo de bloque. El modo de búfer se desarrolló para facilitar su uso y se recomienda en la mayoría de los casos.

El modo de búfer divide automáticamente el búfer de entrada en bloques de un tamaño adecuado para el algoritmo de compresión seleccionado. El modo de búfer da formato y almacena automáticamente el tamaño de búfer sin comprimir en el búfer comprimido. El tamaño del búfer comprimido no se guarda automáticamente y la aplicación debe guardarlo para la descompresión. No incluya la marca **COMPRESS \_ RAW** en el parámetro *Algorithm* cuando llame a [**CreateCompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) y [**CreateDecompressor**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor) para usar el modo de búfer. Para obtener un ejemplo de código de una aplicación en modo búfer, consulte la sección Uso de [la API de compresión en modo de](using-the-compression-api-in-buffer-mode.md) búfer.

El modo de bloque permite al desarrollador controlar el tamaño del bloque, pero requiere que la aplicación haga más trabajo. Cuando se usa el modo de bloque, la aplicación tiene que dividir los datos de entrada en partes con el tamaño adecuado al comprimir y, a continuación, volver a unir las piezas al descomprimir. Se produce un error en el modo de bloque si el tamaño del búfer de entrada es mayor que el tamaño de bloque interno del algoritmo de compresión. El tamaño de bloque interno es de 32 KB para MSZIP y 1 GB para los algoritmos de compresión XPRESS. El tamaño de bloque interno de LZMS se puede configurar hasta 64 GB con un aumento correspondiente en el uso de memoria. El tamaño del búfer comprimido no se guarda automáticamente y la aplicación también debe guardarlo para la descompresión. El valor del *parámetro UncompressedBufferSize* de [**Decompress**](/windows/desktop/api/compressapi/nf-compressapi-decompress) debe ser exactamente igual al tamaño original de los datos sin comprimir y no solo al tamaño del búfer de salida. Esto significa que la aplicación debe guardar el tamaño original exacto de los datos sin comprimir, así como los datos comprimidos y el tamaño comprimido, cuando se usa el modo de bloque. Incluya la **marca COMPRESS \_ RAW** en el parámetro *Algorithm* cuando llame a [**CreateCompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) y [**CreateDecompressor**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor) para usar el modo de bloque. Para obtener un ejemplo de código de una aplicación en modo de bloque, consulte la sección Uso de [compression API en modo de](using-the-compression-api-in-block-mode.md) bloque.

## <a name="custom-memory-allocation"></a>Asignación de memoria personalizada

Las aplicaciones en modo de búfer y de bloque tienen la opción de especificar una rutina de asignación de memoria personalizada cuando llaman a [**CreateCompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) [**y CreateDecompressor.**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor) El *parámetro AllocationRoutines* especifica la estructura [**COMPRESS ALLOCATION \_ \_ ROUTINES**](/windows/desktop/api/compressapi/ns-compressapi-compress_allocation_routines) que contiene la rutina de asignación de memoria. A continuación, la aplicación puede establecer el tamaño de bloque para el objeto con [**SetCompressorInformation**](/windows/desktop/api/compressapi/nf-compressapi-setcompressorinformation). Consulte la [sección Using the Compression API in block mode](using-the-compression-api-in-block-mode.md) (Uso de la API de compresión en modo de bloque) para obtener un ejemplo de una rutina de asignación personalizada simple.

 

 



