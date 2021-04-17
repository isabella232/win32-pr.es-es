---
title: Image-Data compresión
description: Image-Data compresión
ms.assetid: 689cf403-cbb5-4ccb-a05b-0caa617430ed
keywords:
- Administrador de compresión de vídeo (VCM), compresión de datos de imagen
- VCM (Administrador de compresión de vídeo), compresión de datos de imagen
- ICCompress función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b8f59a163a9b5a74d2d2fe984417069985fa86a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420596"
---
# <a name="image-data-compression"></a>Image-Data compresión

La aplicación puede usar una serie de funciones y macros de [**ICCompress**](/windows/desktop/api/Vfw/nf-vfw-iccompress) para comprimir los datos. Las funciones y macros pueden ayudarle a realizar las siguientes tareas:

-   Determina el formato de compresión que se va a usar para un formato de entrada especificado.
-   Prepare el compresor.
-   Comprimir los datos.
-   Finalizar compresión.

La aplicación puede aumentar el control sobre el proceso de compresión mediante el uso de las funciones y macros de [**ICCompress**](/windows/desktop/api/Vfw/nf-vfw-iccompress) . Este grupo de funciones y macros controla fotogramas individuales, en lugar de la secuencia en conjunto. Por ejemplo, la aplicación puede identificar los fotogramas que se van a comprimir como fotogramas clave mediante la función **ICCompress** .

Un compresor recibe los datos en un formato, comprime los datos y devuelve una versión comprimida de los mismos usando un formato especificado. El formato de entrada típico especifica DIB mediante la estructura [**bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) . El formato de salida típico especifica DIB comprimidos, también mediante la estructura **bitmapinfo (** .

> [!Note]  
> Para minimizar la degradación del audio y la imagen durante la reproducción, evite comprimir un archivo AVI más de una vez. Combine piezas sin comprimir de vídeo en el sistema de edición y, a continuación, comprima el producto final.

 

## <a name="compressor-and-compression-format-selection"></a>Selección del compresor y del formato de compresión

Si desea comprimir los datos y la aplicación requiere un formato de salida específico, envíe el mensaje de [**\_ \_ consulta de compresión ICM**](icm-compress-query.md) (o use la macro [**ICCompressQuery**](/windows/desktop/api/Vfw/nf-vfw-iccompressquery) ) para consultar el compresor y determinar si admite los formatos de entrada y salida.

Si el formato de salida no es importante para la aplicación, solo necesita buscar un compresor que pueda controlar el formato de entrada. Para determinar si un compresor puede controlar el formato de entrada, puede enviar **la \_ \_ consulta de compresión ICM**, especificando **null** para el parámetro *lParam* . Este mensaje no devuelve el formato de salida a la aplicación. La aplicación puede determinar el tamaño de búfer necesario para los datos que especifican el formato de compresión mediante el envío del mensaje de compresión [**ICM \_ \_ Get \_ Format**](icm-compress-get-format.md) (o use la macro [**ICCompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformatsize) ). También puede recuperar los datos de formato mediante el envío del \_ formato de compresión ICM \_ Get \_ (o la macro [**ICCompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat) ).

Si desea determinar el búfer más grande que el compresor podría requerir para la compresión, envíe el mensaje de [**\_ \_ \_ tamaño**](icm-compress-get-size.md) de compresión ICM para el usuario (o use la macro [**ICCompressGetSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) ). Puede usar el número de bytes devueltos por la función [**ICSendMessage**](/windows/desktop/api/Vfw/nf-vfw-icsendmessage) para asignar un búfer para las comparaciones de imagen posteriores.

## <a name="compressor-initialization"></a>Inicialización del compresor

Una vez que la aplicación selecciona un compresor que puede controlar los formatos de entrada y salida que necesita, puede inicializar el compresor mediante el mensaje de [**\_ \_ Inicio de compresión ICM**](icm-compress-begin.md) (o utilizar la macro [**ICCompressBegin**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) ). Este mensaje requiere el controlador del compresor y los formatos de entrada y salida.

## <a name="data-compression"></a>Data Compression

Puede usar la función [**ICCompress**](/windows/desktop/api/Vfw/nf-vfw-iccompress) para comprimir un fotograma. La aplicación debe usar esta función repetidamente hasta que se compriman todos los marcos de una secuencia. La aplicación también debe realizar un seguimiento e incrementar el número de cada fotograma comprimido con **ICCompress**. El compresor usa este valor para comprobar si los fotogramas se envían fuera de orden durante la compresión temporal rápida (lo que almacena las diferencias entre los fotogramas sucesivos). Si la aplicación vuelve a comprimir un fotograma, debe utilizar el mismo número de fotograma que cuando el fotograma se comprimió por primera vez. Si la aplicación comprime una imagen de marco fijo, puede especificar un número de fotogramas de cero.

La aplicación puede usar la marca de **\_ fotogramas clave ICCOMPRESS** para que el fotograma esté comprimido por [**ICCOMPRESS**](/windows/desktop/api/Vfw/nf-vfw-iccompress) en un fotograma clave.

Cuando VCM devuelve el control a la aplicación después de comprimir un fotograma, VCM almacena los datos comprimidos en las estructuras a las que hacen referencia los parámetros *lpbiOutput* y *lpData* . Si la aplicación necesita trasladar los datos comprimidos, puede encontrar su tamaño en el miembro *biSizeImage* de la estructura [**Bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) especificada en *lpbiOutput*.

> [!Note]  
> La aplicación debe asignar las estructuras y los búferes que almacenan los datos sin comprimir y comprimidos. Si el compresor admite la compresión temporal, la aplicación también debe asignar una estructura y un búfer para contener el formato y los datos del marco de información anterior.

 

## <a name="ending-compression"></a>Finalización de la compresión

Una vez que la aplicación haya comprimido los datos, puede usar la macro [**ICCompressEnd**](/windows/desktop/api/Vfw/nf-vfw-iccompressend) para notificar al compresor que ha finalizado. Si desea reiniciar la compresión después de usar esta función, la aplicación debe reinicializar el compresor mediante el envío del mensaje de [**\_ \_ Inicio de compresión ICM**](icm-compress-begin.md) (o use la macro [**ICCompressBegin**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) ).

 

 