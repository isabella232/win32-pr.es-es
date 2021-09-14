---
title: Image-Data compresión
description: Image-Data compresión
ms.assetid: 689cf403-cbb5-4ccb-a05b-0caa617430ed
keywords:
- administrador de compresión de vídeo (VCM), compresión de datos de imagen
- VCM (administrador de compresión de vídeo), compresión de datos de imagen
- Función ICCompress
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b8f59a163a9b5a74d2d2fe984417069985fa86a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246218"
---
# <a name="image-data-compression"></a>Image-Data compresión

La aplicación puede usar una serie de funciones y macros [**de ICCompress**](/windows/desktop/api/Vfw/nf-vfw-iccompress) para comprimir los datos. Las funciones y macros pueden ayudarle a realizar las siguientes tareas:

-   Determine el formato de compresión que se usará para un formato de entrada especificado.
-   Prepare el resalte.
-   Comprima los datos.
-   Compresión final.

La aplicación puede aumentar el control sobre el proceso de compresión mediante las funciones y macros [**iccompress.**](/windows/desktop/api/Vfw/nf-vfw-iccompress) Este grupo de funciones y macros controla fotogramas individuales, en lugar de la secuencia en su conjunto. Por ejemplo, la aplicación puede identificar los fotogramas que se comprimirán como fotogramas clave mediante la **función ICCompress.**

Un objeto recibe datos en un formato, los comprime y devuelve una versión comprimida de los datos con un formato especificado. El formato de entrada típico especifica dibs mediante la [**estructura BITMAPINFO.**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) El formato de salida típico especifica dibs comprimidos, usando también la **estructura BITMAPINFO.**

> [!Note]  
> Para minimizar la degradación de imágenes y audio durante la reproducción, evite comprimir un archivo AVI más de una vez. Combine fragmentos de vídeo sin comprimir en el sistema de edición y, a continuación, comprima el producto final.

 

## <a name="compressor-and-compression-format-selection"></a>Selección de formato de compresión y compresión

Si desea comprimir los datos y la aplicación requiere un formato de salida específico, envíe el mensaje [**\_ de consulta \_ COMPRESS**](icm-compress-query.md) de ICM (o use la macro [**ICCompressQuery)**](/windows/desktop/api/Vfw/nf-vfw-iccompressquery) para consultar el objeto para determinar si admite los formatos de entrada y salida.

Si el formato de salida no es importante para la aplicación, solo necesita encontrar un elemento que pueda controlar el formato de entrada. Para determinar si un objeto puede controlar el formato de entrada, puede enviar ICM **\_ COMPRESS \_ QUERY**, especificando **NULL para** el *parámetro lParam.* Este mensaje no devuelve el formato de salida a la aplicación. La aplicación puede determinar el tamaño de búfer necesario para los datos que especifican el formato de compresión enviando el mensaje [**\_ ICM COMPRESS GET \_ \_ FORMAT**](icm-compress-get-format.md) (o use la macro [**ICCompressGetFormatSize).**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformatsize) También puede recuperar los datos de formato enviando ICM \_ COMPRESS \_ GET FORMAT \_ (o la macro [**ICCompressGetFormat).**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat)

Si desea determinar el búfer más grande que podría requerir el objeto para la compresión, envíe el mensaje [**\_ ICM COMPRESS GET \_ \_ SIZE**](icm-compress-get-size.md) (o use la macro [**ICCompressGetSize).**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) Puede usar el número de bytes devueltos por la [**función ICSendMessage**](/windows/desktop/api/Vfw/nf-vfw-icsendmessage) para asignar un búfer para las siguientes compresiónes de imagen.

## <a name="compressor-initialization"></a>Inicialización de inicialización de inicialización

Después de que la aplicación seleccione un objeto que pueda controlar los formatos de entrada y salida que necesita, puede inicializar el objeto mediante el mensaje [**\_ COMPRESS \_ BEGIN**](icm-compress-begin.md) de ICM (o usar la macro [**ICCompressBegin).**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) Este mensaje requiere el identificador del controlador y los formatos de entrada y salida.

## <a name="data-compression"></a>Data Compression

Puede usar la [**función ICCompress**](/windows/desktop/api/Vfw/nf-vfw-iccompress) para comprimir un marco. La aplicación debe usar esta función repetidamente hasta que se comprimen todos los fotogramas de una secuencia. La aplicación también debe realizar un seguimiento e incrementar el número de cada fotograma comprimido con **ICCompress**. El objeto utiliza este valor para comprobar si los fotogramas se envían fuera de orden durante la compresión temporal rápida (almacenando las diferencias entre fotogramas sucesivos). Si la aplicación vuelve a comprimir un marco, debe usar el mismo número de fotograma que cuando se comprimió por primera vez. Si la aplicación comprime una imagen de fotogramas todavía, puede especificar un número de fotograma de cero.

La aplicación puede usar la marca **ICCOMPRESS \_ KEYFRAME** para que el marco se comprima [**mediante ICCompress**](/windows/desktop/api/Vfw/nf-vfw-iccompress) como un fotograma clave.

Cuando VCM devuelve el control a la aplicación después de comprimir un marco, VCM almacena los datos comprimidos en las estructuras a las que hacen referencia los parámetros *lpbiOutput* y *lpData.* Si la aplicación necesita mover los datos comprimidos, puede encontrar su tamaño en el *miembro biSizeImage* de la estructura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) especificada en *lpbiOutput*.

> [!Note]  
> La aplicación debe asignar las estructuras y búferes que almacenan los datos sin comprimir y comprimidos. Si el objeto admite la compresión temporal, la aplicación también debe asignar una estructura y un búfer para contener el formato y los datos del marco de información anterior.

 

## <a name="ending-compression"></a>Compresión final

Una vez que la aplicación haya comprimido los datos, puede usar la macro [**ICCompressEnd**](/windows/desktop/api/Vfw/nf-vfw-iccompressend) para notificar al reenvío que ha finalizado. Si desea reiniciar la compresión después de usar esta función, la aplicación debe reinicializar el servicio enviando el mensaje BEGIN de [**\_ ICM COMPRESS \_**](icm-compress-begin.md) (o use la macro [**ICCompressBegin).**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin)

 

 