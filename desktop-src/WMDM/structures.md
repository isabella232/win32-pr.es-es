---
title: Estructuras WMDM
description: Estructuras
ms.assetid: 3068359f-5ac0-41e0-a09b-283b439527a0
keywords:
- Administrador de dispositivos de Windows Media, estructuras
- Administrador de dispositivos, estructuras
- referencia de programación, estructuras
- referencia de Windows Media Administrador de dispositivos, estructuras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 903aa07bbe3d01029eb2020b521523b545843f2a
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2019
ms.locfileid: "104420017"
---
# <a name="wmdm-structures"></a>Estructuras WMDM

Windows Media Administrador de dispositivos define las siguientes estructuras.



| Estructura                                                   | Descripción                                                                                                                                                                                                                                              |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_BITMAPINFOHEADER**](-bitmapinfoheader.md)             | Define el formato del fotograma de vídeo.                                                                                                                                                                                                                       |
| [**\_ \_ datos de comando MTP \_ en**](/windows/desktop/api/MtpExt/ns-mtpext-mtp_command_data_in)       | Contiene comandos personalizados del Protocolo de transporte multimedia (MTP) que se envían al dispositivo mediante el método [**IWMDMDevice3::D eviceiocontrol**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-deviceiocontrol) .                                                                           |
| [**\_datos de comando MTP \_ \_ out**](/windows/desktop/api/MtpExt/ns-mtpext-mtp_command_data_out)     | Contiene respuestas del Protocolo de transporte multimedia (MTP) que el controlador de dispositivo rellena.                                                                                                                                                                  |
| [**OPAQUECOMMAND**](opaquecommand.md)                      | Contiene datos para los comandos que se pasan a través de Windows Media Administrador de dispositivos a un dispositivo, pero que no están diseñados para ser actuados por Windows Media Administrador de dispositivos.                                                                                       |
| [**\_VIDEOINFOHEADER**](-videoinfoheader.md)               | Define el formato de una secuencia de vídeo.                                                                                                                                                                                                                    |
| [**\_WAVEFORMATEX**](-waveformatex.md)                     | Define el formato de los datos de audio de forma de onda.                                                                                                                                                                                                               |
| [**\_funcionalidad de formato WMDM \_**](wmdm-format-capability.md)  | Describe las capacidades de un dispositivo para un formato determinado. Esta estructura contiene un conjunto de configuraciones de propiedades en una matriz de estructuras de [**\_ \_ configuración de propiedades de WMDM**](wmdm-prop-config.md) .                                                       |
| [**\_configuración de propiedades de WMDM \_**](wmdm-prop-config.md)              | Describe un conjunto de valores de propiedad compatibles en todas las propiedades compatibles con el dispositivo para un formato determinado. Esta estructura contiene una serie de descripciones de propiedades en una matriz de estructuras de propiedades [**\_ \_ DESC de WMDM**](wmdm-prop-desc.md) . |
| [**Descripción de la Prop de WMDM \_ \_**](wmdm-prop-desc.md)                  | Describe los valores válidos de una propiedad en una configuración de propiedad determinada.                                                                                                                                                                             |
| [**\_ \_ enumeración de valores de propiedades de WMDM \_**](wmdm-prop-values-enum.md)   | Contiene un conjunto enumerado de valores válidos para una propiedad determinada en una configuración de propiedad determinada.                                                                                                                                             |
| [**\_intervalo de \_ valores de prop de WMDM \_**](wmdm-prop-values-range.md) | Describe el intervalo de valores válidos para una propiedad determinada en una configuración de propiedad determinada.                                                                                                                                                        |
| [**WMDMDATETIME**](wmdmdatetime.md)                        | Contiene una fecha y hora.                                                                                                                                                                                                                                |
| [**WMDMID**](wmdmid.md)                                    | Describe los números de serie y los ID. de grupo.                                                                                                                                                                                                                  |
| [**WMDMMetadataView**](wmdmmetadataview.md)                | Define la vista de metadatos.                                                                                                                                                                                                                               |
| [**WMDMRIGHTS**](wmdmrights.md)                            | Describe los derechos de uso de contenido.                                                                                                                                                                                                                            |
| [**WMFILECAPABILITIES**](wmfilecapabilities.md)            | Describe un tipo MIME.                                                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación**](programming-reference.md)
</dt> </dl>

 

 




