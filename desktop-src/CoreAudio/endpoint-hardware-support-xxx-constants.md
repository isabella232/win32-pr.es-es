---
description: Las constantes ENDPOINT \_ HARDWARE SUPPORT XXX son marcas de compatibilidad de hardware para un dispositivo de punto de conexión de \_ \_ audio.
ms.assetid: 54032f75-2287-4589-bda5-e005ee077c41
title: ENDPOINT_HARDWARE_SUPPORT_XXX constantes (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ffb5b2255330b205519ce3065ccb5f7eebb6b65
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165009"
---
# <a name="endpoint_hardware_support_xxx-constants"></a>COMPATIBILIDAD \_ CON HARDWARE DE PUNTO DE CONEXIÓN XXX \_ \_ Constantes

Las constantes ENDPOINT \_ HARDWARE SUPPORT XXX son marcas de compatibilidad de hardware para un dispositivo de punto de conexión de \_ \_ audio.



| Constante o valor                                                                                                                                                                                                                                                                           | Descripción                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| <span id="ENDPOINT_HARDWARE_SUPPORT_VOLUME"></span><span id="endpoint_hardware_support_volume"></span><dl> <dt>**PUNTO DE CONEXIÓN \_ COMPATIBILIDAD \_ DE HARDWARE CON \_ EL**</dt> <dt>VOLUMEN 0x00000001</dt> </dl> | El dispositivo de punto de conexión de audio admite un control de volumen de hardware.<br/> |
| <span id="ENDPOINT_HARDWARE_SUPPORT_MUTE"></span><span id="endpoint_hardware_support_mute"></span><dl> <dt>**PUNTO DE CONEXIÓN \_ Compatibilidad con \_ la \_ exclusión mutua**</dt> de hardware <dt>0x00000002</dt> </dl>       | El dispositivo de punto de conexión de audio admite un control de exclusión mutua de hardware.<br/>   |
| <span id="ENDPOINT_HARDWARE_SUPPORT_METER"></span><span id="endpoint_hardware_support_meter"></span><dl> <dt>**PUNTO DE CONEXIÓN \_ MEDIDOR \_ DE COMPATIBILIDAD \_ DE HARDWARE**</dt> <dt>0x00000004</dt> </dl>    | El dispositivo de punto de conexión de audio admite un medidor máximo de hardware.<br/>     |



## <a name="remarks"></a>Observaciones

Los [**métodos IAudioEndpointVolume::QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-queryhardwaresupport) e [**IAudioMeterInformation::QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-queryhardwaresupport) usan las constantes XXX ENDPOINT \_ HARDWARE \_ \_ SUPPORT.

Una máscara de compatibilidad de hardware indica qué funciones implementa un dispositivo de punto de conexión de audio en el hardware. La máscara puede ser 0 o la combinación or bit a bit de una o varias constantes DE COMPATIBILIDAD CON HARDWARE DE PUNTO DE CONEXIÓN \_ \_ \_ XXX. Si se establece un bit que corresponde a una constante XXX de COMPATIBILIDAD CON HARDWARE DE PUNTO DE CONEXIÓN determinada en la máscara, el significado es que el dispositivo implementa la función representada por esa constante en \_ \_ el \_ hardware.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Mmdeviceapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Constantes de audio principales](core-audio-constants.md)
</dt> <dt>

[**IAudioEndpointVolume::QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-queryhardwaresupport)
</dt> <dt>

[**IAudioMeterInformation::QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-queryhardwaresupport)
</dt> </dl>

 

 




