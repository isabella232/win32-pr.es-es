---
description: Capturar atributos de dispositivo
ms.assetid: dd24671a-0689-4490-8d18-2a33ed461e9d
title: Capturar atributos de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43dd8dbcdf0a441ddb8a5ef2794526e961c22033
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241167"
---
# <a name="capture-device-attributes"></a>Capturar atributos de dispositivo

Los atributos siguientes están relacionados con los dispositivos de captura:



| Atributo                                                                                                                     | Descripción                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [NOMBRE DESCRIPTIVO DEL ATRIBUTO MF \_ DEVSOURCE \_ \_ \_](mf-devsource-attribute-friendly-name.md)                                          | Nombre para mostrar del dispositivo.                                                          |
| [TIPO \_ DE MEDIO DE ATRIBUTO MF DEVSOURCE \_ \_ \_](mf-devsource-attribute-media-type.md)                                                | Formato de salida del dispositivo.                                                         |
| [TIPO DE ORIGEN DEL ATRIBUTO MF \_ DEVSOURCE \_ \_ \_](mf-devsource-attribute-source-type.md)                                              | El tipo de dispositivo, como la captura de audio o la captura de vídeo.                         |
| [MF \_ DEVSOURCE \_ ATTRIBUTE \_ SOURCE \_ TYPE \_ AUDCAP \_ ENDPOINT \_ ID](mf-devsource-attribute-source-type-audcap-endpoint-id.md)     | Identificador del punto de conexión de un dispositivo de captura de audio.                                        |
| [MF \_ DEVSOURCE \_ ATTRIBUTE \_ SOURCE \_ TYPE \_ AUDCAP \_ ROLE](mf-devsource-attribute-source-type-audcap-role.md)                    | Rol de dispositivo para un dispositivo de captura de audio.                                        |
| [CATEGORÍA VIDCAP DEL TIPO DE \_ ORIGEN DEL ATRIBUTO MF DEVSOURCE \_ \_ \_ \_ \_](mf-devsource-attribute-source-type-vidcap-category.md)            | Categoría de dispositivo para un dispositivo de vídeo.                                             |
| [MF \_ DEVSOURCE \_ ATTRIBUTE \_ SOURCE \_ TYPE \_ VIDCAP \_ HW \_ SOURCE](mf-devsource-attribute-source-type-vidcap-hw-source.md)         | Especifica si un origen de captura de vídeo es un dispositivo de hardware o un dispositivo de software. |
| [BÚFERES \_ MÁXIMOS DE \_ \_ VIDCAP MAX DEL \_ TIPO DE ORIGEN \_ \_ \_ DEL ATRIBUTO MF DEVSOURCE](mf-devsource-attribute-source-type-vidcap-max-buffers.md)     | Especifica el número máximo de fotogramas que almacenará en búfer el origen de captura de vídeo.   |
| [VÍNCULO SIMBÓLICO DEL TIPO DE ORIGEN DEL ATRIBUTO MF \_ DEVSOURCE \_ \_ \_ \_ VIDCAP \_ \_](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) | Vínculo simbólico para un controlador de captura de vídeo.                                       |
| [MARCA DE \_ TIEMPO DE MFT \_ HW CON atributo \_ \_ \_ QPC](mft-hw-timestamp-with-qpc-attribute.md)                                           | Especifica si el origen del dispositivo usa la hora del sistema para las marcas de tiempo.           |



 

Estos atributos se usan con las siguientes funciones:

-   [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource)
-   [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Media Foundation atributos](media-foundation-attributes.md)
</dt> </dl>

 

 



