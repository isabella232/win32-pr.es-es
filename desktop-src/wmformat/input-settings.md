---
title: Configuración de entrada
description: Configuración de entrada
ms.assetid: 23adbb64-5733-4198-8f2b-d02052ddb848
keywords:
- SDK de Windows Media Format, constantes globales
- Advanced Systems Format (ASF), constantes globales
- ASF (formato de sistemas avanzados), constantes globales
- constantes globales, lista de
- SDK de Windows Media Format, constantes
- Advanced Systems Format (ASF), constantes
- ASF (formato de sistemas avanzados), constantes
- constantes, lista de
- SDK de Windows Media Format, configuración de entrada
- Advanced Systems Format (ASF), configuración de entrada
- ASF (formato de sistemas avanzados), configuración de entrada
- configuración de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f70ef0db6a3d9371bd1c8e9a20157f5f0ac73b3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077283"
---
# <a name="input-settings"></a>Configuración de entrada

Las constantes globales siguientes se utilizan para identificar la configuración de entrada del escritor.



| Constante global                        | tipo de DataType del \_ atributo WMT \_                                                                                                                       | Descripción de *pValue*                                                                                                                                                                                                                                                 |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| g \_ wszDeinterlaceMode                  | **WMT \_ Escriba \_ DWORD** establecido en uno de los valores de la tabla modo del tema [para Desentrelazar vídeo](to-deinterlace-video.md).            | Cuando se establece, especifica el tipo de contenido entrelazado de la entrada. Para obtener más información, vea [para Desentrelazar vídeo](to-deinterlace-video.md).                                                                                                                            |
| g \_ wszFixedFrameRate                   | **tipo de WMT \_ \_ bool**                                                                                                                       | Cuando se establece en true, indica al códec que no quite ningún fotograma durante la codificación. Esto hará que la [*velocidad de fotogramas*](wmformat-glossary.md) de la secuencia de vídeo de salida sea constante. No es necesario que la velocidad de fotogramas del flujo de entrada sea constante. |
| g \_ wszInitialPatternForInverseTelecine | **WMT \_ Escriba \_ DWORD** establecido en uno de los valores de la tabla patrón inicial del tema [para Desentrelazar vídeo](to-deinterlace-video.md). | Cuando el modo de desentrelazado se establece en el \_ \_ desentrelazado de WM DM \_ INVERSETELECINE, se puede establecer para especificar el patrón de la entrada de [*telecine*](wmformat-glossary.md) . Para obtener más información, vea [para Desentrelazar vídeo](to-deinterlace-video.md).        |
| g \_ wszInterlacedCoding                 | **tipo de WMT \_ \_ bool**                                                                                                                       | Cuando se establece en true, especifica que el códec debe codificar el flujo como contenido entrelazado. Para obtener más información, consulte [uso de vídeo entrelazado](to-use-interlaced-video.md).                                                                                       |
| g \_ wszJPEGCompressionQuality           | **tipo de WMT \_ \_ DWORD**                                                                                                                      | Especifica el nivel de calidad JPEG (de 1 a 100) que se va a usar en la entrada.                                                                                                                                                                                               |
| g \_ wszWatermarkCLSID                   | **\_GUID de tipo WMT \_**                                                                                                                       | El valor se establece en el GUID de marca de agua.                                                                                                                                                                                                                                 |
| g \_ wszWatermarkConfig                  | **\_cadena de tipo WMT \_**                                                                                                                     | El valor se establece en la configuración de marca de agua. Este valor variará en función del DMO de marca de agua. Consulte la documentación del sistema de marcas de agua para obtener más información.                                                                                   |



 

> [!Note]  
> Los valores de entrada configurados para una secuencia no se conservan en el archivo escrito. Si desea que el lector personalizado tenga acceso a estos parámetros de codificación, debe crear atributos personalizados para almacenarlos en el encabezado del archivo.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMWriterAdvanced2::GetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-getinputsetting)
</dt> <dt>

[**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting)
</dt> </dl>

 

 




