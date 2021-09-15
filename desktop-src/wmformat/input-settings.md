---
title: Entrada Configuración
description: Entrada Configuración
ms.assetid: 23adbb64-5733-4198-8f2b-d02052ddb848
keywords:
- Windows SDK de formato multimedia, constantes globales
- Formato de sistemas avanzados (ASF), constantes globales
- ASF (formato de sistemas avanzados), constantes globales
- constantes globales, lista de
- Windows SDK de formato multimedia, constantes
- Formato de sistemas avanzados (ASF),constantes
- ASF (formato de sistemas avanzados),constantes
- constants,list of
- Windows SDK de formato multimedia, configuración de entrada
- Formato de sistemas avanzados (ASF), configuración de entrada
- ASF (formato de sistemas avanzados), configuración de entrada
- configuración de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f70ef0db6a3d9371bd1c8e9a20157f5f0ac73b3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466708"
---
# <a name="input-settings"></a>Entrada Configuración

Las siguientes constantes globales se usan para identificar la configuración de entrada para el escritor.



| Constante global                        | TIPO DE \_ DATOS ATTR DE WMT \_                                                                                                                       | Descripción de *pValue*                                                                                                                                                                                                                                                 |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| g \_ wszDeinterlaceMode                  | **WMT \_ ESCRIBA \_ DWORD** establecido en uno de los valores de la tabla mode del tema [To Deinterlace Video](to-deinterlace-video.md).            | Cuando se establece, especifica el tipo de contenido entrelazado de la entrada. Para obtener más información, vea [To Deinterlace Video](to-deinterlace-video.md).                                                                                                                            |
| g \_ wszFixedFrameRate                   | **TIPO WMT \_ \_ BOOL**                                                                                                                       | Cuando se establece en True, indica al códec que no coloque ningún fotograma durante la codificación. Esto hará que la [*velocidad de fotogramas*](wmformat-glossary.md) de la secuencia de vídeo de salida sea constante. No es necesario que la velocidad de fotogramas del flujo de entrada sea constante. |
| g \_ wszInitialPatternForInverseTeleversión | **WMT \_ ESCRIBA \_ DWORD** establecido en uno de los valores de la tabla de patrones inicial del tema [To Deinterlace Video](to-deinterlace-video.md). | Cuando el modo de desinterlace se establece en WM \_ DM \_ DEINTERLACE \_ INVERSETELEVERSIÓN, se puede establecer para especificar el patrón de la [*entrada de televisa.*](wmformat-glossary.md) Para obtener más información, vea [To Deinterlace Video](to-deinterlace-video.md).        |
| g \_ wszInterlacedCoding                 | **TIPO WMT \_ \_ BOOL**                                                                                                                       | Cuando se establece en True, especifica que el códec debe codificar la secuencia como contenido entrelazado. Para obtener más información, [vea To Use Interlaced Video](to-use-interlaced-video.md).                                                                                       |
| g \_ wszQUALEGCompressionQuality           | **DWORD \_ DE TIPO \_ WMT**                                                                                                                      | Especifica el nivel de calidad JPEG (de 1 a 100) que se usará en la entrada.                                                                                                                                                                                               |
| g \_ wszWatermarkCLSID                   | **GUID DE \_ TIPO \_ WMT**                                                                                                                       | El valor se establece en el GUID de marca de agua.                                                                                                                                                                                                                                 |
| g \_ wszWatermarkConfig                  | **CADENA DE \_ TIPO \_ WMT**                                                                                                                     | El valor se establece en la configuración de marca de agua. Este valor variará en función de la marca de agua DMO. Consulte la documentación del sistema de marca de agua para obtener más información.                                                                                   |



 

> [!Note]  
> La configuración de entrada configurada para una secuencia no se conserva en el archivo escrito. Si desea que el lector personalizado tenga acceso a estos parámetros de codificación, debe crear atributos personalizados para almacenarlos en el encabezado de archivo.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMWriterAdvanced2::GetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-getinputsetting)
</dt> <dt>

[**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting)
</dt> </dl>

 

 




