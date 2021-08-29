---
description: Los siguientes identificadores únicos globales (GUID) definen tipos de nodo para los filtros en modo kernel. Para buscar el tipo de nodo, consulte el filtro de la interfaz IKsTopologyInfo.
ms.assetid: 0e133ce3-8815-47d1-a5c3-577a98963912
title: Tipos de nodo KS (Ksmedia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KSNODETYPE_DEV_SPECIFIC
- KSNODETYPE_VIDEO_CAMERA_TERMINAL
- KSNODETYPE_VIDEO_INPUT_MTT
- KSNODETYPE_VIDEO_INPUT_TERMINAL
- KSNODETYPE_VIDEO_OUTPUT_MTT
- KSNODETYPE_VIDEO_OUTPUT_TERMINAL
- KSNODETYPE_VIDEO_PROCESSING
- KSNODETYPE_VIDEO_SELECTOR
- KSNODETYPE_VIDEO_STREAMING
api_type:
- HeaderDef
api_location:
- Ksmedia.h
ms.openlocfilehash: 76c201451a4f747190cf586fd51ba60ee43dbbf8c97e55a50da0fee4e9802a82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791755"
---
# <a name="ks-node-types"></a>Tipos de nodo KS

Los siguientes identificadores únicos globales (GUID) definen tipos de nodo para los filtros en modo kernel. Para buscar el tipo de nodo, consulte el filtro de la [**interfaz IKsTopologyInfo.**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-ikstopologyinfo)



| GUID                                                                                                                                                                                                                     | Descripción                                                                                                                                                                                                                                                                                              |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="KSNODETYPE_DEV_SPECIFIC"></span><span id="ksnodetype_dev_specific"></span><dl> <dt>**KSNODETYPE \_ DEV \_ ESPECÍFICO**</dt> </dl>                             | Representa una o varias funciones de procesamiento específicas del dispositivo. El nodo tiene una conexión de entrada y una conexión de salida.<br/> El nodo puede exponer una interfaz COM personalizada a través de un complemento KsProxy, si lo proporciona el fabricante del dispositivo.<br/>                                            |
| <span id="KSNODETYPE_VIDEO_CAMERA_TERMINAL"></span><span id="ksnodetype_video_camera_terminal"></span><dl> <dt>**TERMINAL DE CÁMARA \_ DE \_ \_ VÍDEO KSNODETYPE**</dt> </dl> | Representa los datos que se mueven al dispositivo desde un sensor de cámara, independientemente del bus USB. El nodo tiene una conexión de salida.<br/> El nodo expone las [**interfaces IAMCameraControl**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol) [**e ICameraControl**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-icameracontrol) para controlar la cámara.<br/> |
| <span id="KSNODETYPE_VIDEO_INPUT_MTT"></span><span id="ksnodetype_video_input_mtt"></span><dl> <dt>**MTT DE ENTRADA \_ \_ DE VÍDEO \_ KSNODETYPE**</dt> </dl>                   | Representa los datos que se mueven al dispositivo desde un transporte multimedia secuencial, como una cinta VTR, independientemente del bus USB. El nodo tiene una conexión de salida.<br/> El nodo expone la interfaz [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) para controlar el mecanismo de transporte.<br/>   |
| <span id="KSNODETYPE_VIDEO_INPUT_TERMINAL"></span><span id="ksnodetype_video_input_terminal"></span><dl> <dt>**TERMINAL DE ENTRADA DE VÍDEO KSNODETYPE \_ \_ \_**</dt> </dl>    | Representa los datos que se mueven al dispositivo, independientemente del bus USB. Por ejemplo, este nodo puede representar un conector de audio análogo o un conector S/PDIF. El nodo tiene una conexión de salida.<br/>                                                                                                             |
| <span id="KSNODETYPE_VIDEO_OUTPUT_MTT"></span><span id="ksnodetype_video_output_mtt"></span><dl> <dt>**MTT DE SALIDA \_ \_ DE VÍDEO \_ KSNODETYPE**</dt> </dl>                | Representa los datos que se mueven desde el dispositivo a un transporte multimedia secuencial, como una cinta VTR, independientemente del bus USB. El nodo tiene una conexión de entrada.<br/> El nodo expone la interfaz [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) para controlar el mecanismo de transporte.<br/>      |
| <span id="KSNODETYPE_VIDEO_OUTPUT_TERMINAL"></span><span id="ksnodetype_video_output_terminal"></span><dl> <dt>**TERMINAL DE SALIDA DE VÍDEO KSNODETYPE \_ \_ \_**</dt> </dl> | Representa los datos que se mueven desde el dispositivo, independientemente del bus USB. Por ejemplo, este nodo puede representar un conector de audio análogo o un conector S/PDIF. El nodo tiene una conexión de entrada.<br/>                                                                                                              |
| <span id="KSNODETYPE_VIDEO_PROCESSING"></span><span id="ksnodetype_video_processing"></span><dl> <dt>**PROCESAMIENTO DE VÍDEO KSNODETYPE \_ \_**</dt> </dl>                 | Representa una o varias funciones de procesamiento de vídeo. El nodo tiene una conexión de entrada y una conexión de salida.<br/> El nodo expone las interfaces [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) [**e IVideoProcAmp**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-ivideoprocamp) para ajustar las calidades de la señal de vídeo.<br/> |
| <span id="KSNODETYPE_VIDEO_SELECTOR"></span><span id="ksnodetype_video_selector"></span><dl> <dt>**SELECTOR DE VÍDEO KSNODETYPE \_ \_**</dt> </dl>                       | Representa un mecanismo para seleccionar la ruta de acceso de entrada de dos o más orígenes posibles. El nodo tiene dos o más conexiones de entrada y una conexión de salida.<br/> El nodo expone la interfaz [**ISelector**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-iselector) para seleccionar entre entradas.<br/>                               |
| <span id="KSNODETYPE_VIDEO_STREAMING"></span><span id="ksnodetype_video_streaming"></span><dl> <dt>**STREAMING DE VÍDEO KSNODETYPE \_ \_**</dt> </dl>                    | Representa los datos que se mueven entre el host y el dispositivo. En el caso de los dispositivos UVC, este nodo representa un punto de conexión USB. Los puntos de conexión de entrada tienen una conexión de entrada; los puntos de conexión de salida tienen una conexión de salida.<br/>                                                                                         |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Ksmedia.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes y GUID](constants-and-guids.md)
</dt> </dl>

 

 




