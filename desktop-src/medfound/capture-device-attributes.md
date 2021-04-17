---
description: Capturar atributos de dispositivo
ms.assetid: dd24671a-0689-4490-8d18-2a33ed461e9d
title: Capturar atributos de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43dd8dbcdf0a441ddb8a5ef2794526e961c22033
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696180"
---
# <a name="capture-device-attributes"></a>Capturar atributos de dispositivo

Los siguientes atributos están relacionados con los dispositivos de captura:



| Atributo                                                                                                                     | Descripción                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [\_ \_ nombre descriptivo del atributo MF DEVSOURCE \_ \_](mf-devsource-attribute-friendly-name.md)                                          | Nombre para mostrar del dispositivo.                                                          |
| [\_tipo de \_ medio de atributo MF DEVSOURCE \_ \_](mf-devsource-attribute-media-type.md)                                                | El formato de salida del dispositivo.                                                         |
| [\_tipo de \_ origen de atributo MF DEVSOURCE \_ \_](mf-devsource-attribute-source-type.md)                                              | El tipo de dispositivo, como captura de audio o captura de vídeo.                         |
| [\_Type DEVSOURCE \_ tipo de origen de atributo \_ \_ \_ AUDCAP \_ ID. de punto de conexión \_](mf-devsource-attribute-source-type-audcap-endpoint-id.md)     | IDENTIFICADOR del punto de conexión de un dispositivo de captura de audio.                                        |
| [\_ \_ \_ \_ \_ AUDCAP rol de tipo de origen de atributo MF DEVSOURCE \_](mf-devsource-attribute-source-type-audcap-role.md)                    | El rol de dispositivo para un dispositivo de captura de audio.                                        |
| [\_tipo de origen de atributo MF DEVSOURCE \_ \_ \_ \_ \_ categoría VIDCAP](mf-devsource-attribute-source-type-vidcap-category.md)            | La categoría de dispositivos para un dispositivo de vídeo.                                             |
| [tipo de origen de atributo de MF \_ DEVSOURCE \_ \_ origen de \_ \_ HW de VIDCAP \_ \_](mf-devsource-attribute-source-type-vidcap-hw-source.md)         | Especifica si un origen de captura de vídeo es un dispositivo de hardware o un dispositivo de software. |
| [\_tipo de origen de atributo MF DEVSOURCE \_ \_ \_ \_ \_ búferes de VIDCAP máx \_ .](mf-devsource-attribute-source-type-vidcap-max-buffers.md)     | Especifica el número máximo de fotogramas que el origen de captura de vídeo almacenará en búfer.   |
| [\_tipo de origen de atributo MF DEVSOURCE \_ \_ \_ \_ vínculo de VIDCAP \_ simbólico \_](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) | El vínculo simbólico de un controlador de captura de vídeo.                                       |
| [\_ \_ Marca de tiempo \_ de HW de MFT con el \_ \_ atributo QPC](mft-hw-timestamp-with-qpc-attribute.md)                                           | Especifica si el origen del dispositivo utiliza la hora del sistema para las marcas de tiempo.           |



 

Estos atributos se utilizan con las siguientes funciones:

-   [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource)
-   [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Atributos de Media Foundation](media-foundation-attributes.md)
</dt> </dl>

 

 



