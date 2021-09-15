---
description: Las marcas de la tabla siguiente especifican el estado de una sesión de Output Protection Manager (OPM).
ms.assetid: d6d85fd4-e735-4610-93e0-bb2b1782f11b
title: Marcas de estado de OPM (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edc044d9159ad6e6a6e957c4be0228a8e2531164
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579813"
---
# <a name="opm-status-flags"></a>Marcas de estado de OPM

Las marcas de la tabla siguiente especifican el estado de una sesión de Output Protection Manager (OPM).




| Constante o valor | Descripción | 
|----------------|-------------|
| <span id="OPM_STATUS_NORMAL"></span><span id="opm_status_normal"></span><dl><dt><strong>OPM_STATUS_NORMAL</strong></dt><dt>0x00</dt></dl> | Estado normal.<br /> | 
| <span id="OPM_STATUS_LINK_LOST"></span><span id="opm_status_link_lost"></span><dl><dt><strong>OPM_STATUS_LINK_LOST</strong></dt><dt>0x01</dt></dl> | La integridad de la conexión se ha puesto en peligro. Entre los ejemplos de eventos que hacen que el controlador establezca esta marca se incluyen:<br /><ul><li>El controlador ya no puede aplicar el nivel de protección actual.</li><li>El controlador detectó un error de integridad interna.</li><li>El conector entre el equipo y el dispositivo de pantalla se ha desconectado.</li></ul> | 
| <span id="OPM_STATUS_RENEGOTIATION_REQUIRED"></span><span id="opm_status_renegotiation_required"></span><dl><dt><strong>OPM_STATUS_RENEGOTIATION_REQUIRED</strong></dt><dt>0x02</dt></dl> | La configuración de conexión ha cambiado. Por ejemplo, el usuario ha cambiado el modo de visualización del escritorio.<br /> | 
| <span id="OPM_STATUS_TAMPERING_DETECTED"></span><span id="opm_status_tampering_detected"></span><dl><dt><strong>OPM_STATUS_TAMPERING_DETECTED</strong></dt><dt>0x04</dt></dl> | El adaptador de gráficos o el controlador se han alterado.<br /> Esta marca no se usa en el <em>modo de emulación copp</em>. En su lugar, la salida de vídeo establecerá la OPM_STATUS_LINK_LOST si detecta la manipulación.<br /> | 
| <span id="OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED"></span><span id="opm_status_revoked_hdcp_device_attached"></span><dl><dt><strong>OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED</strong></dt><dt>0x08</dt></dl> | Se ha revocado High-Bandwidth dispositivo Content Protection Digital Content Protection (HDCP) se adjunta a la salida de vídeo.<br /> Esta marca de estado se puede devolver desde una <a href="opm-get-virtual-protection-level.md">OPM_GET_VIRTUAL_PROTECTION_LEVEL</a> o <a href="opm-get-actual-protection-level.md">OPM_GET_ACTUAL_PROTECTION_LEVEL</a> consulta. <br /> El dispositivo revocado podría estar conectado directamente a la salida de vídeo o indirectamente a través de un repetidor HDCP. Se requiere una salida de vídeo para detectar esta condición mientras HDCP está habilitado, pero no de lo contrario.<br /> Esta marca no se usa en el modo <em>de emulación copp</em>, porque la salida de vídeo no detecta dispositivos revocados en ese modo.<br /> | 




## <a name="remarks"></a>Observaciones

Algunas de estas constantes son equivalentes a los valores de la enumeración **COPP \_ StatusFlags** que se usa en el Protocolo de protección de salida certificado (COPP).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Opmapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de OPM](opm-enumerations.md)
</dt> </dl>

 

 




