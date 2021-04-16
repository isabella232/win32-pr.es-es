---
description: En las marcas de la tabla siguiente se especifica el estado de una sesión de Output Protection Manager (OPM).
ms.assetid: d6d85fd4-e735-4610-93e0-bb2b1782f11b
title: Marcas de estado de OPM (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cbf9d299d6d53a26a61d19372e56e42bd2cdf99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543854"
---
# <a name="opm-status-flags"></a>Marcas de estado de OPM

En las marcas de la tabla siguiente se especifica el estado de una sesión de Output Protection Manager (OPM).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante o valor</th>
<th style="text-align: left;">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="OPM_STATUS_NORMAL"></span><span id="opm_status_normal"></span><dl> <dt><strong>OPM_STATUS_NORMAL</strong></dt> <dt>0x00</dt> </dl></td>
<td style="text-align: left;">Estado normal.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="OPM_STATUS_LINK_LOST"></span><span id="opm_status_link_lost"></span><dl> <dt><strong>OPM_STATUS_LINK_LOST</strong></dt> <dt>0x01</dt> </dl></td>
<td style="text-align: left;">Se ha puesto en peligro la integridad de la conexión. Entre los ejemplos de eventos que hacen que el controlador establezca esta marca se incluyen:<br/>
<ul>
<li>El controlador ya no puede aplicar el nivel de protección actual.</li>
<li>El controlador ha detectado un error de integridad interno.</li>
<li>Se desconectó el conector entre el equipo y el dispositivo de pantalla.</li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="OPM_STATUS_RENEGOTIATION_REQUIRED"></span><span id="opm_status_renegotiation_required"></span><dl> <dt><strong>OPM_STATUS_RENEGOTIATION_REQUIRED</strong></dt> <dt>0x02</dt> </dl></td>
<td style="text-align: left;">La configuración de la conexión ha cambiado. Por ejemplo, el usuario ha cambiado el modo de presentación del escritorio.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="OPM_STATUS_TAMPERING_DETECTED"></span><span id="opm_status_tampering_detected"></span><dl> <dt><strong>OPM_STATUS_TAMPERING_DETECTED</strong></dt> <dt>0x04</dt> </dl></td>
<td style="text-align: left;">El adaptador de gráficos o el controlador se han alterado.<br/> Esta marca no se usa en el <em>modo de emulación de COPP</em>. En su lugar, la salida de vídeo establecerá la marca de OPM_STATUS_LINK_LOST si detecta alteraciones.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED"></span><span id="opm_status_revoked_hdcp_device_attached"></span><dl> <dt><strong>OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED</strong></dt> <dt>0x08</dt> </dl></td>
<td style="text-align: left;">Un dispositivo High-Bandwidth Digital Content Protection (HDCP) revocado se adjunta a la salida de vídeo.<br/> Esta marca de estado se puede devolver desde una <a href="opm-get-virtual-protection-level.md">OPM_GET_VIRTUAL_PROTECTION_LEVEL</a> o <a href="opm-get-actual-protection-level.md">OPM_GET_ACTUAL_PROTECTION_LEVEL</a> consulta. <br/> El dispositivo revocado puede estar conectado directamente a la salida de vídeo o indirectamente a través de un repetidor de HDCP. Se necesita una salida de vídeo para detectar esta condición mientras se habilita HDCP, pero no.<br/> Esta marca no se usa en el <em>modo de emulación de COPP</em>porque la salida de vídeo no detecta los dispositivos revocados en ese modo.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Observaciones

Algunas de estas constantes son equivalentes a los valores de la enumeración **COPP \_ StatusFlags** usada en el protocolo de protección de la salida certificada (COPP).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de OPM](opm-enumerations.md)
</dt> </dl>

 

 




