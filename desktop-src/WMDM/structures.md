---
title: Estructuras WMDM
description: En este artículo se incluyen artículos de referencia sobre las estructuras definidas por Windows Media Administrador de dispositivos, como _BITMAPINFOHEADER y MTP_COMMAND_DATA_IN.
ms.assetid: 3068359f-5ac0-41e0-a09b-283b439527a0
keywords:
- Windows Media Administrador de dispositivos,structures
- Administrador de dispositivos,structures
- referencia de programación, estructuras
- referencia de Windows media Administrador de dispositivos,structures
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cc49deb3f4dd28695f5e0e7c3a871c53fa96300
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127242007"
---
# <a name="wmdm-structures"></a>Estructuras WMDM

Windows El Administrador de dispositivos define las estructuras siguientes.



| Estructura                                                   | Descripción                                                                                                                                                                                                                                              |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_BITMAPINFOHEADER**](-bitmapinfoheader.md)             | Define el formato del fotograma de vídeo.                                                                                                                                                                                                                       |
| [**DATOS DE COMANDOS DE MTP \_ \_ \_ EN**](/windows/desktop/api/MtpExt/ns-mtpext-mtp_command_data_in)       | Contiene comandos personalizados del Protocolo de transporte multimedia (MTP) que se envían al dispositivo mediante el método [**IWMDMDevice3::D eviceIoControl.**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-deviceiocontrol)                                                                           |
| [**SALIDA DE \_ DATOS DE COMANDOS DE \_ \_ MTP**](/windows/desktop/api/MtpExt/ns-mtpext-mtp_command_data_out)     | Contiene respuestas del Protocolo de transporte multimedia (MTP) rellenadas por el controlador de dispositivo.                                                                                                                                                                  |
| [**OPAQUECOMMAND**](opaquecommand.md)                      | Contiene datos para los comandos que se pasan a través de Windows Media Administrador de dispositivos a un dispositivo, pero que no están diseñados para que los actúe Windows Media Administrador de dispositivos.                                                                                       |
| [**\_VIDEOINFOHEADER**](-videoinfoheader.md)               | Define el formato de una secuencia de vídeo.                                                                                                                                                                                                                    |
| [**\_FORMA DE ONDAATEX**](-waveformatex.md)                     | Define el formato de los datos de audio de forma de onda.                                                                                                                                                                                                               |
| [**FUNCIONALIDAD DE \_ FORMATO \_ WMDM**](wmdm-format-capability.md)  | Describe las funcionalidades de un dispositivo para un formato determinado. Esta estructura contiene un conjunto de configuraciones de propiedades en una matriz de estructuras [**DE CONFIGURACIÓN DE PROP \_ \_ de WMDM.**](wmdm-prop-config.md)                                                       |
| [**CONFIGURACIÓN DE PROP DE WMDM \_ \_**](wmdm-prop-config.md)              | Describe un conjunto de valores de propiedad compatibles en todas las propiedades admitidas por el dispositivo para un formato determinado. Esta estructura contiene una serie de descripciones de propiedades en una matriz de estructuras [**\_ \_ DESC PROP de WMDM.**](wmdm-prop-desc.md) |
| [**WMDM \_ PROP \_ DESC**](wmdm-prop-desc.md)                  | Describe los valores válidos de una propiedad en una configuración de propiedad determinada.                                                                                                                                                                             |
| [**ENUMERACIÓN DE \_ VALORES PROP \_ \_ DE WMDM**](wmdm-prop-values-enum.md)   | Contiene un conjunto enumerado de valores válidos para una propiedad determinada en una configuración de propiedad determinada.                                                                                                                                             |
| [**INTERVALO DE VALORES \_ DE PROPIEDAD \_ DE WMDM \_**](wmdm-prop-values-range.md) | Describe el intervalo de valores válidos para una propiedad determinada en una configuración de propiedad determinada.                                                                                                                                                        |
| [**WMDMDATETIME**](wmdmdatetime.md)                        | Contiene una fecha y hora.                                                                                                                                                                                                                                |
| [**WMDMID**](wmdmid.md)                                    | Describe los números de serie y los identificaciónes de grupo.                                                                                                                                                                                                                  |
| [**WMDMMetadataView**](wmdmmetadataview.md)                | Define la vista de metadatos.                                                                                                                                                                                                                               |
| [**WMDMRIGHTS**](wmdmrights.md)                            | Describe los derechos de uso de contenido.                                                                                                                                                                                                                            |
| [**WMFILECAPABILITIES**](wmfilecapabilities.md)            | Describe un tipo MIME.                                                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación**](programming-reference.md)
</dt> </dl>

 

 




