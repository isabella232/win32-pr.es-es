---
description: Las \_ \_ \_ constantes XXX de compatibilidad de hardware de punto de conexión son marcas de compatibilidad de hardware para un dispositivo de punto de conexión de audio.
ms.assetid: 54032f75-2287-4589-bda5-e005ee077c41
title: Constantes de ENDPOINT_HARDWARE_SUPPORT_XXX (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ffb5b2255330b205519ce3065ccb5f7eebb6b65
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153520"
---
# <a name="endpoint_hardware_support_xxx-constants"></a>Compatibilidad de hardware de punto de conexión \_ \_ \_ XXX constantes

Las \_ \_ \_ constantes XXX de compatibilidad de hardware de punto de conexión son marcas de compatibilidad de hardware para un dispositivo de punto de conexión de audio.



| Constante o valor                                                                                                                                                                                                                                                                           | Descripción                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| <span id="ENDPOINT_HARDWARE_SUPPORT_VOLUME"></span><span id="endpoint_hardware_support_volume"></span><dl> <dt>**Punto de conexión \_ \_ \_ Volumen de soporte de hardware**</dt> <dt>0x00000001</dt> </dl> | El dispositivo de punto de conexión de audio admite un control de volumen de hardware.<br/> |
| <span id="ENDPOINT_HARDWARE_SUPPORT_MUTE"></span><span id="endpoint_hardware_support_mute"></span><dl> <dt>**Punto de conexión \_ Compatibilidad de HARDWARE \_ \_ silenciar**</dt> <dt>0x00000002</dt> </dl>       | El dispositivo de punto de conexión de audio admite un control de silencio de hardware.<br/>   |
| <span id="ENDPOINT_HARDWARE_SUPPORT_METER"></span><span id="endpoint_hardware_support_meter"></span><dl> <dt>**Punto de conexión \_ \_ \_ Medidor de compatibilidad de hardware**</dt> <dt>0x00000004</dt> </dl>    | El dispositivo de punto de conexión de audio admite un medidor de picos de hardware.<br/>     |



## <a name="remarks"></a>Observaciones

Los métodos [**IAudioEndpointVolume:: QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-queryhardwaresupport) y [**IAudioMeterInformation:: QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-queryhardwaresupport) usan las \_ \_ constantes XXX de compatibilidad de hardware del punto de conexión \_ .

Una máscara de compatibilidad de hardware indica qué funciones implementa un dispositivo de punto de conexión de audio en el hardware. La máscara puede ser 0 o la combinación OR bit a bit de una o varias \_ constantes XXX de compatibilidad de hardware de extremo \_ \_ . Si un bit que corresponde a una \_ \_ \_ constante de compatibilidad de hardware de punto de conexión en particular se establece en la máscara, el significado es que el dispositivo implementa la función representada por esa constante en el hardware.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Mmdeviceapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de audio principales](core-audio-constants.md)
</dt> <dt>

[**IAudioEndpointVolume::QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-queryhardwaresupport)
</dt> <dt>

[**IAudioMeterInformation::QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-queryhardwaresupport)
</dt> </dl>

 

 




