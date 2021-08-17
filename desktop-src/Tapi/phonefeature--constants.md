---
description: Las constantes PHONEFEATURE \_ enumera las operaciones que se pueden invocar en un teléfono mediante esta API. Cada uno de los valores de PHONEFEATURE \_ (excepto PHONEFEATURE GENERICPHONE) corresponde a una función TAPI con un nombre idéntico \_ o similar.
ms.assetid: 361b3080-3650-48a2-a1b7-f05d72777f9a
title: PHONEFEATURE_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78b074b2c02a1ceb8144d0d21ea5b8002d2a4612600072ce76254c8b38738ec4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060643"
---
# <a name="phonefeature_-constants"></a>Constantes PHONEFEATURE \_

Las **constantes PHONEFEATURE \_** enumera las operaciones que se pueden invocar en un teléfono mediante esta API. Cada uno de los valores de PHONEFEATURE \_ (excepto PHONEFEATURE GENERICPHONE) corresponde a una función TAPI con un nombre idéntico \_ o similar.



| Constante o valor                                                                                                                                                                                                                                                                            | Descripción                                                                             |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| <span id="PHONEFEATURE_GETBUTTONINFO"></span><span id="phonefeature_getbuttoninfo"></span><dl> <dt>**PHONEFEATURE \_ GetBUTTONINFO**</dt> <dt>0x00000001</dt> </dl>                      | [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo)<br/>                             |
| <span id="PHONEFEATURE_GETDATA"></span><span id="phonefeature_getdata"></span><dl> <dt>**PHONEFEATURE \_ GetDATA**</dt> <dt>0x00000002</dt> </dl>                                        | [**phoneGetData**](/windows/desktop/api/Tapi/nf-tapi-phonegetdata)<br/>                                         |
| <span id="PHONEFEATURE_GETDISPLAY"></span><span id="phonefeature_getdisplay"></span><dl> <dt>**PHONEFEATURE \_ GetDISPLAY**</dt> <dt>0x00000004</dt> </dl>                               | [**phoneGetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonegetdisplay)<br/>                                   |
| <span id="PHONEFEATURE_GETGAINHANDSET"></span><span id="phonefeature_getgainhandset"></span><dl> <dt>**PHONEFEATURE \_ GetGAINHANDSET**</dt> <dt>0x00000008</dt> </dl>                   | [**phoneGetGain**](/windows/desktop/api/Tapi/nf-tapi-phonegetgain) PHONEHOOKSWITCHDEV \_ HANDSET<br/>             |
| <span id="PHONEFEATURE_GETGAINSPEAKER"></span><span id="phonefeature_getgainspeaker"></span><dl> <dt>**PHONEFEATURE \_ GETGAINSPEAKER**</dt> <dt>0x00000010</dt> </dl>                   | [**phoneGetGain**](/windows/desktop/api/Tapi/nf-tapi-phonegetgain) PHONEHOOKSWITCHDEV \_ SPEAKER<br/>             |
| <span id="PHONEFEATURE_GETGAINHEADSET"></span><span id="phonefeature_getgainheadset"></span><dl> <dt>**PHONEFEATURE \_ GETGAINHEADSET**</dt> <dt>0x00000020</dt> </dl>                   | [**phoneGetGain**](/windows/desktop/api/Tapi/nf-tapi-phonegetgain) CASCO PHONEHOOKSWITCHDEV \_<br/>             |
| <span id="PHONEFEATURE_GETHOOKSWITCHHANDSET"></span><span id="phonefeature_gethookswitchhandset"></span><dl> <dt>**PHONEFEATURE \_ GetHOOKSWITCHHANDSET**</dt> <dt>0x00000040</dt> </dl> | [**phoneGetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) PHONEHOOKSWITCHDEV \_ HANDSET<br/> |
| <span id="PHONEFEATURE_GETHOOKSWITCHSPEAKER"></span><span id="phonefeature_gethookswitchspeaker"></span><dl> <dt>**PHONEFEATURE \_ GETHOOKSWITCHSPEAKER**</dt> <dt>0x00000080</dt> </dl> | [**phoneGetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) PHONEHOOKSWITCHDEV \_ HANDSET<br/> |
| <span id="PHONEFEATURE_GETHOOKSWITCHHEADSET"></span><span id="phonefeature_gethookswitchheadset"></span><dl> <dt>**PHONEFEATURE \_ GetHOOKSWITCHHEADSET**</dt> <dt>0x00000100</dt> </dl> | [**phoneGetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) PHONEHOOKSWITCHDEV \_ HANDSET<br/> |
| <span id="PHONEFEATURE_GETLAMP"></span><span id="phonefeature_getlamp"></span><dl> <dt>**PHONEFEATURE \_ GetLAMP**</dt> <dt>0x00000200</dt> </dl>                                        | [**phoneGetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonegetlamp)<br/>                                         |
| <span id="PHONEFEATURE_GETRING"></span><span id="phonefeature_getring"></span><dl> <dt>**PHONEFEATURE \_ GETRING**</dt> <dt>0x00000400</dt> </dl>                                        | [**phoneGetRing**](/windows/desktop/api/Tapi/nf-tapi-phonegetring)<br/>                                         |
| <span id="PHONEFEATURE_GETVOLUMEHANDSET"></span><span id="phonefeature_getvolumehandset"></span><dl> <dt>**PHONEFEATURE \_ GETVOLUMEHANDSET**</dt> <dt>0x00000800</dt> </dl>             | [**phoneGetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonegetvolume) PHONEHOOKSWITCHDEV \_ HANDSET<br/>         |
| <span id="PHONEFEATURE_GETVOLUMESPEAKER"></span><span id="phonefeature_getvolumespeaker"></span><dl> <dt>**PHONEFEATURE \_ GETVOLUMESPEAKER**</dt> <dt>0x00001000</dt> </dl>             | [**phoneGetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonegetvolume) PHONEHOOKSWITCHDEV \_ SPEAKER<br/>         |
| <span id="PHONEFEATURE_GETVOLUMEHEADSET"></span><span id="phonefeature_getvolumeheadset"></span><dl> <dt>**PHONEFEATURE \_ GETVOLUMEHEADSET**</dt> <dt>0x00002000</dt> </dl>             | [**phoneGetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonegetvolume) CASCO PHONEHOOKSWITCHDEV \_<br/>         |
| <span id="PHONEFEATURE_SETBUTTONINFO"></span><span id="phonefeature_setbuttoninfo"></span><dl> <dt>**PHONEFEATURE \_ SetBUTTONINFO**</dt> <dt>0x00004000</dt> </dl>                      | [**phoneSetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonesetbuttoninfo)<br/>                             |
| <span id="PHONEFEATURE_SETDATA"></span><span id="phonefeature_setdata"></span><dl> <dt>**PHONEFEATURE \_ SETDATA**</dt> <dt>0x00008000</dt> </dl>                                        | [**phoneSetData**](/windows/desktop/api/Tapi/nf-tapi-phonesetdata)<br/>                                         |
| <span id="PHONEFEATURE_SETDISPLAY"></span><span id="phonefeature_setdisplay"></span><dl> <dt>**PHONEFEATURE \_ Setdisplay**</dt> <dt>0x00010000</dt> </dl>                               | [**phoneSetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonesetdisplay)<br/>                                   |
| <span id="PHONEFEATURE_SETGAINHANDSET"></span><span id="phonefeature_setgainhandset"></span><dl> <dt>**PHONEFEATURE \_ SETGAINHANDSET**</dt> <dt>0x00020000</dt> </dl>                   | [**phoneSetGain**](/windows/desktop/api/Tapi/nf-tapi-phonesetgain) PHONEHOOKSWITCHDEV \_ HANDSET<br/>             |
| <span id="PHONEFEATURE_SETGAINSPEAKER"></span><span id="phonefeature_setgainspeaker"></span><dl> <dt>**PHONEFEATURE \_ SETGAINSPEAKER**</dt> <dt>0x00040000</dt> </dl>                   | [**phoneSetGain**](/windows/desktop/api/Tapi/nf-tapi-phonesetgain) PHONEHOOKSWITCHDEV \_ SPEAKER<br/>             |
| <span id="PHONEFEATURE_SETGAINHEADSET"></span><span id="phonefeature_setgainheadset"></span><dl> <dt>**PHONEFEATURE \_ SETGAINHEADSET**</dt> <dt>0x00080000</dt> </dl>                   | [**phoneSetGain**](/windows/desktop/api/Tapi/nf-tapi-phonesetgain) CASCO PHONEHOOKSWITCHDEV \_<br/>             |
| <span id="PHONEFEATURE_SETHOOKSWITCHHANDSET"></span><span id="phonefeature_sethookswitchhandset"></span><dl> <dt>**PHONEFEATURE \_ SETHOOKSWITCHHANDSET**</dt> <dt>0x00100000</dt> </dl> | [**phoneSetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) PHONEHOOKSWITCHDEV \_ HANDSET<br/> |
| <span id="PHONEFEATURE_SETHOOKSWITCHSPEAKER"></span><span id="phonefeature_sethookswitchspeaker"></span><dl> <dt>**PHONEFEATURE \_ SETHOOKSWITCHSPEAKER**</dt> <dt>0x00200000</dt> </dl> | [**phoneSetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) PHONEHOOKSWITCHDEV \_ SPEAKER<br/> |
| <span id="PHONEFEATURE_SETHOOKSWITCHHEADSET"></span><span id="phonefeature_sethookswitchheadset"></span><dl> <dt>**PHONEFEATURE \_ SETHOOKSWITCHHEADSET**</dt> <dt>0x00400000</dt> </dl> | [**phoneSetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) CASCO PHONEHOOKSWITCHDEV \_<br/> |
| <span id="PHONEFEATURE_SETLAMP"></span><span id="phonefeature_setlamp"></span><dl> <dt>**PHONEFEATURE \_ Setlamp**</dt> <dt>0x00800000</dt> </dl>                                        | [**phoneSetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonesetlamp)<br/>                                         |
| <span id="PHONEFEATURE_SETRING"></span><span id="phonefeature_setring"></span><dl> <dt>**PHONEFEATURE \_ SETRING**</dt> <dt>0x01000000</dt> </dl>                                        | [**phoneSetRing**](/windows/desktop/api/Tapi/nf-tapi-phonesetring)<br/>                                         |
| <span id="PHONEFEATURE_SETVOLUMEHANDSET"></span><span id="phonefeature_setvolumehandset"></span><dl> <dt>**PHONEFEATURE \_ SETVOLUMEHANDSET**</dt> <dt>0x02000000</dt> </dl>             | [**phoneSetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonesetvolume) PHONEHOOKSWITCHDEV \_ HANDSET<br/>         |
| <span id="PHONEFEATURE_SETVOLUMESPEAKER"></span><span id="phonefeature_setvolumespeaker"></span><dl> <dt>**PHONEFEATURE \_ SETVOLUMESPEAKER**</dt> <dt>0x04000000</dt> </dl>             | [**phoneSetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonesetvolume) PHONEHOOKSWITCHDEV \_ SPEAKER<br/>         |
| <span id="PHONEFEATURE_SETVOLUMEHEADSET"></span><span id="phonefeature_setvolumeheadset"></span><dl> <dt>**PHONEFEATURE \_ SETVOLUMEHEADSET**</dt> <dt>0x08000000</dt> </dl>             | [**phoneSetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonesetvolume) CASCO PHONEHOOKSWITCHDEV \_<br/>         |
| <span id="PHONEFEATURE_GENERICPHONE"></span><span id="phonefeature_genericphone"></span><dl> <dt>**PHONEFEATURE \_ GenericPhone**</dt> <dt>0x10000000</dt> </dl>                         | (relevante solo para las aplicaciones que usan TAPI 3.0 y versiones posteriores)<br/>                     |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




