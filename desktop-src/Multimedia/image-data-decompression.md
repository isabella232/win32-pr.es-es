---
title: Descompresión de Image-Data
description: Descompresión de Image-Data
ms.assetid: 4bff02be-dac8-41f4-a3af-2da6a2693ffe
keywords:
- Administrador de compresión de vídeo (VCM), descompresión de datos de imagen
- VCM (Administrador de compresión de vídeo), descompresión de datos de imagen
- Funciones de ICDecompressEx
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25614f157436056f7f24c340f6cc6f4dbc62d9ae
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358885"
---
# <a name="image-data-decompression"></a>Descompresión de Image-Data

La aplicación usa una serie de funciones [**ICDecompressEx**](/windows/desktop/api/Vfw/nf-vfw-icdecompressex) para controlar el descompresor. Las funciones pueden ayudarle a realizar las siguientes tareas:

-   Seleccione un descompresor.
-   Prepare el descompresor.
-   Descomprimir los datos.
-   Descompresión final.

La aplicación controla la descompresión de forma similar a la forma en que controla la compresión, salvo que el formato de entrada es un formato comprimido y el formato de salida es un formato que se pueda mostrar. El formato de entrada para la descompresión se suele obtener del encabezado de flujo. Después de determinar el formato de entrada, la aplicación puede usar las funciones [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) o [**ICOpen**](/windows/desktop/api/Vfw/nf-vfw-icopen) para buscar un descompresor que pueda controlarlo.

Las funciones y macros de [**ICDecompressEx**](/windows/desktop/api/Vfw/nf-vfw-icdecompressex) son un supraconjunto del grupo de funciones [**ICDecompress**](/windows/desktop/api/Vfw/nf-vfw-icdecompress) y proporcionan más capacidades. La funcionalidad de **ICDecompressEx**, [**ICDecompressExBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexbegin), [**ICDecompressExEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexend)y [**ICDecompressExQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery) reemplaza a las funciones **ICDecompress**, [**ICDecompressBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressbegin), [**ICDecompressEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressend)y [**ICDecompressQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) . Use las funciones y macros de **ICDecompressEx** en lugar de los equivalentes de **ICDecompress** .

## <a name="decompressor-and-decompression-format-selection"></a>Selección de descompresor y descompresión de formato

Si desea descomprimir datos y la aplicación requiere un formato de salida específico, puede usar la función [**ICDecompressExQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery) para consultar el descompresor y determinar si admite los formatos de entrada y salida.

Si el formato de salida no es importante en la aplicación, solo necesita buscar un descompresor que pueda controlar el formato de entrada. Para determinar si un descompresor puede controlar el formato de entrada, use [**ICDecompressExQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery) y especifique **null** para el parámetro *lpbiDst* . La aplicación puede determinar el tamaño de búfer necesario para los datos que especifican el formato de descompresión mediante el envío del mensaje de descompresión [**ICM \_ \_ Get \_ Format**](icm-decompress-get-format.md) (o use la macro [**ICDecompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformatsize) ). También puede enviar el **\_ formato de \_ obtención \_ descomprime ICM** (o la macro [**ICDecompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformat) ) para recuperar los datos de formato. El descompresor devuelve su formato sugerido en una estructura [**bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) . Este formato normalmente conserva más información durante la descompresión. La aplicación debe asegurarse de que el descompresor se devuelve correctamente antes de descomprimir la información.

Dado que la aplicación asigna la memoria necesaria para la descompresión, debe determinar la cantidad máxima de memoria que puede requerir el descompresor para el formato de salida. El mensaje de **\_ descompresión ICM \_ Get \_ Format** obtiene el número de bytes que usa el descompresor para el formato predeterminado.

Si la aplicación define su propio formato mediante [**ICDecompressExQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery), también debe obtener una paleta para el mapa de bits; **ICDecompressExQuery** no proporciona definiciones de paleta. (La mayoría de las aplicaciones usan formatos estándar y no necesitan obtener una paleta). La aplicación puede obtener la paleta mediante el envío del mensaje de la [**\_ paleta de descompresión ICM \_ Get \_**](icm-decompress-get-palette.md) (o usar la macro [**ICDecompressGetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette) ).

## <a name="decompressor-initialization"></a>Inicialización descompresor

Una vez que la aplicación selecciona un descompresor que puede controlar los formatos de entrada y salida que necesita, puede inicializar el descompresor mediante la función [**ICDecompressExBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexbegin) . Esta función requiere el controlador de descompresor y los formatos de entrada y salida.

## <a name="data-decompression"></a>Descompresión de datos

Puede usar la función [**ICDecompressEx**](/windows/desktop/api/Vfw/nf-vfw-icdecompressex) para descomprimir un fotograma. La aplicación debe usar esta función repetidamente hasta que se descomprimen todos los marcos de una secuencia.

Si el flujo de vídeo se encuentra detrás de otros componentes (como audio) durante la reproducción, la aplicación puede especificar la marca **ICDECOMPRESS \_ HURRYUP** para acelerar la descompresión. Para ello, un descompresor podría extraer solo la información que necesita para descomprimir el fotograma siguiente y no descomprimir completamente el fotograma actual. Por lo tanto, la aplicación no debe intentar dibujar los datos descomprimidos cuando usa esta marca.

Una vez que la aplicación haya descomprimido los datos, puede enviar el mensaje de [**\_ \_ finalización de DECOMPRESSEX ICM**](icm-decompressex-end.md) (o usar la macro [**ICDecompressExEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexend) ) para notificar al descompresor que ha finalizado. Si desea reiniciar la descompresión después de usar esta función, la aplicación debe reinicializar el descompresor mediante [**ICDecompressExBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexbegin).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[VCM servicios](vcm-services.md)
</dt> </dl>

 

 