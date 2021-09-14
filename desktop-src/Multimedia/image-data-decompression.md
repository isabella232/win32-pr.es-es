---
title: Image-Data descompresión
description: Image-Data descompresión
ms.assetid: 4bff02be-dac8-41f4-a3af-2da6a2693ffe
keywords:
- administrador de compresión de vídeo (VCM), descompresión de datos de imagen
- VCM (administrador de compresión de vídeo), descompresión de datos de imagen
- Funciones ICDecompressEx
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25614f157436056f7f24c340f6cc6f4dbc62d9ae
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246213"
---
# <a name="image-data-decompression"></a>Image-Data descompresión

La aplicación usa una serie de [**funciones ICDecompressEx**](/windows/desktop/api/Vfw/nf-vfw-icdecompressex) para controlar el descomprimidor. Las funciones pueden ayudarle a realizar las siguientes tareas:

-   Seleccione un descomprimidor.
-   Prepare el descomprimidor.
-   Descomprimir los datos.
-   Finalice la descompresión.

La aplicación controla la descompresión de forma similar a la forma en que controla la compresión, salvo que el formato de entrada es un formato comprimido y el formato de salida es un formato que se puede mostrar. El formato de entrada para la descompresión normalmente se obtiene del encabezado de flujo. Después de determinar el formato de entrada, la aplicación puede usar las funciones [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) o [**ICOpen**](/windows/desktop/api/Vfw/nf-vfw-icopen) para buscar un descomprimidor que pueda controlarlo.

Las funciones y macros [**ICDecompressEx**](/windows/desktop/api/Vfw/nf-vfw-icdecompressex) son un superconjunto del grupo de funciones [**ICDecompress**](/windows/desktop/api/Vfw/nf-vfw-icdecompress) y proporcionan más funcionalidades. La funcionalidad de **ICDecompressEx,** [**ICDecompressExBegin,**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexbegin) [**ICDecompressExEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexend)y [**ICDecompressExQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery) reemplaza a la de las funciones **ICDecompress,** [**ICDecompressBegin,**](/windows/desktop/api/Vfw/nf-vfw-icdecompressbegin) [**ICDecompressEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressend)y [**ICDecompressQuery.**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) Use las funciones y macros **ICDecompressEx** en lugar de los equivalentes **de ICDecompress.**

## <a name="decompressor-and-decompression-format-selection"></a>Selección de formato de descompresión y descompresión

Si desea descomprimir datos y la aplicación requiere un formato de salida específico, puede usar la función [**ICDecompressExQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery) para consultar el descomprimidor para determinar si admite los formatos de entrada y salida.

Si el formato de salida no es importante en la aplicación, solo necesita encontrar un descomprimidor que pueda controlar el formato de entrada. Para determinar si un descomprimidor puede controlar el formato de entrada, use [**ICDecompressExQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery) y especifique **NULL para** el *parámetro lpbiDst.* La aplicación puede determinar el tamaño de búfer necesario para los datos que especifican el formato de descompresión mediante el envío del mensaje GET FORMAT de [**ICM \_ \_ \_ DECOMPRESS**](icm-decompress-get-format.md) (o use la macro [**ICDecompressGetFormatSize).**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformatsize) También puede enviar ICM GET FORMAT de **\_ DECOMPRESS \_ \_** (o la macro [**ICDecompressGetFormat)**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformat) para recuperar los datos de formato. El descomprimidor devuelve su formato sugerido en una [**estructura BITMAPINFO.**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) Este formato suele conservar la mayor parte de la información durante la descompresión. La aplicación debe asegurarse de que el descompresor se devuelve correctamente antes de descomprimir la información.

Dado que la aplicación asigna la memoria necesaria para la descompresión, debe determinar la memoria máxima que el descompresor puede requerir para el formato de salida. El ICM get format de **\_ DECOMPRESS \_ \_** obtiene el número de bytes que usa el descompresor para el formato predeterminado.

Si la aplicación define su propio formato mediante [**ICDecompressExQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery), también debe obtener una paleta para el mapa de bits; **ICDecompressExQuery** no proporciona definiciones de paleta. (La mayoría de las aplicaciones usan formatos estándar y no necesitan obtener una paleta). La aplicación puede obtener la paleta mediante el envío ICM mensaje GET PALETTE de [**\_ DECOMPRESS \_ \_**](icm-decompress-get-palette.md) (o use la macro [**ICDecompressGetPalette).**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette)

## <a name="decompressor-initialization"></a>Inicialización del descomprimidor

Una vez que la aplicación selecciona un descompresión que puede controlar los formatos de entrada y salida que necesita, puede inicializar el descomprimidor mediante la [**función ICDecompressExBegin.**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexbegin) Esta función requiere el identificador de descompresión y los formatos de entrada y salida.

## <a name="data-decompression"></a>Descompresión de datos

Puede usar la [**función ICDecompressEx**](/windows/desktop/api/Vfw/nf-vfw-icdecompressex) para descomprimir un fotograma. La aplicación debe usar esta función repetidamente hasta que se descomprimen todos los fotogramas de una secuencia.

Si la secuencia de vídeo se queda atrás de otros componentes (por ejemplo, audio) durante la reproducción, la aplicación puede especificar la marca **ICDECOMPRESS \_ DENSEUP** para acelerar la descompresión. Para ello, un descomprimidor podría extraer solo la información que necesita para descomprimir el fotograma siguiente y no descomprimir completamente el marco actual. Por lo tanto, la aplicación no debe intentar dibujar los datos descomprimidos cuando usa esta marca.

Una vez que la aplicación ha descomprimido los datos, puede enviar el mensaje [**\_ end de DECOMPRESSEX \_**](icm-decompressex-end.md) de ICM (o usar la macro [**ICDecompressExEnd)**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexend) para notificar al descomprimidor que ha finalizado. Si desea reiniciar la descompresión después de usar esta función, la aplicación debe reinicializar el descomprimidor mediante [**ICDecompressExBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexbegin).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Servicios de VCM](vcm-services.md)
</dt> </dl>

 

 