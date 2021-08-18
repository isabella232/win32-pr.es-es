---
description: Winlogon y GINA deben comunicar la información de inicialización, controlar la supervisión y notificación de la secuencia de atención segura (SAS) y permitir las actividades de cierre y cierre de sesión.
ms.assetid: ea45cd5f-9cb0-41bb-99bf-f84781ae9604
title: 'Interacción entre Winlogon y GINA '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 824c658e4f19b14de339b569a8c9d17992c1b60bb5d4d526de949ce76cd1554d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482365"
---
# <a name="interaction-between-winlogon-and-gina"></a>Interacción entre Winlogon y GINA 

[*Winlogon y*](../secgloss/w-gly.md) [*GINA*](../secgloss/g-gly.md) deben comunicar la información de inicialización, controlar la supervisión y notificación de la secuencia de atención segura [*(SAS)*](../secgloss/s-gly.md) y permitir las actividades de cierre y cierre de sesión. El estado de Winlogon determina qué función GINA se llama para procesar cualquier evento SAS determinado. Las comunicaciones se producen en el orden que se muestra aquí.

> [!Note]  
> Los archivos DLL de GINA se omiten Windows Vista.

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Evento</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Arranque de estación de trabajo</td>
<td><ol>
<li>Winlogon llama a la función <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate"><strong>WlxNegotiate</strong></a> de GINA para notificar a la GINA la versión de Winlogon en uso.</li>
<li>Winlogon llama a la función <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize"><strong>WlxInitialize</strong></a> de la GINA para proporcionar a la GINA las <a href="/windows/desktop/SecGloss/c-gly"><em></em></a> direcciones de las funciones de soporte técnico, un identificador para Winlogon y para obtener la información de contexto de la GINA (que se usará en todas las llamadas futuras a la GINA).<br/> Winlogon está en el estado de la sesión iniciada.<br/></li>
</ol></td>
</tr>
<tr class="even">
<td>Nadie ha iniciado sesión</td>
<td>(La GINA supervisa los dispositivos en busca de eventos SAS).
<ol>
<li>La GINA llama a la función <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> de Winlogon cuando se recibe un evento SAS.</li>
<li>Winlogon llama a la función <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas"><strong>WlxLoggedOutSAS</strong></a> de GINA, lo que permite que la GINA procese la información de identificación y autenticación de un usuario.<br/> Cuando el inicio de sesión se realiza correctamente, Winlogon está en estado de inicio de sesión.<br/></li>
</ol></td>
</tr>
<tr class="odd">
<td>El usuario ha iniciado sesión</td>
<td>(La GINA supervisa los dispositivos en busca de eventos SAS).
<ol>
<li>La GINA llama a la función <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> de Winlogon cuando se recibe un evento SAS.</li>
<li>Winlogon llama a la función <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> de GINA, lo que permite que la GINA presente opciones al usuario que ha iniciado sesión actualmente.</li>
</ol></td>
</tr>
<tr class="even">
<td>El usuario ha iniciado sesión y quiere bloquear el equipo</td>
<td>(La GINA supervisa los dispositivos en busca de eventos SAS).
<ol>
<li>La GINA llama a <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>la función WlxSasNotify.</strong></a></li>
<li>Winlogon llama a la función <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS de</strong></a> GINA.</li>
<li>La GINA devuelve WLX_SAS_ACTION_LOCK_WKSTA.<br/> Winlogon está en estado bloqueado en la estación de trabajo.<br/></li>
</ol></td>
</tr>
<tr class="odd">
<td>El usuario ha iniciado sesión, la estación de trabajo está bloqueada y el usuario quiere desbloquear el equipo.</td>
<td>(La GINA supervisa los dispositivos en busca de eventos SAS).
<ol>
<li>La GINA llama a <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>la función WlxSasNotify.</strong></a></li>
<li>Winlogon llama a la función <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxwkstalockedsas"><strong>WlxWkstaLockedSAS de</strong></a> GINA.</li>
<li>La GINA devuelve WLX_SAS_ACTION_UNLOCK_WKSTA.</li>
</ol></td>
</tr>
<tr class="even">
<td>El usuario ha iniciado sesión y el programa llama a <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"><strong>la función ExitWindowsEx.</strong></a></td>
<td>Winlogon llama a la función <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> de la GINA.</td>
</tr>
<tr class="odd">
<td>El usuario ha iniciado sesión y desea cerrar la sesión mediante SAS.</td>
<td>(La GINA supervisa los dispositivos en busca de eventos SAS).
<ol>
<li>La GINA llama a <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>la función WlxSasNotify.</strong></a></li>
<li>Winlogon llama a la función <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS de</strong></a> GINA.</li>
<li>La GINA devuelve WLX_SAS_ACTION_LOGOFF.</li>
<li>Winlogon llama a la función <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> de la GINA.</li>
</ol></td>
</tr>
<tr class="even">
<td>El usuario ha iniciado sesión y desea cerrar la sesión y apagarla mediante <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"> <strong>ExitWindowsEx.</strong></a></td>
<td><ol>
<li>Winlogon llama a la función <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> de la GINA.</li>
<li>Winlogon llama a la función <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>WlxShutdown</strong></a> de GINA.</li>
</ol></td>
</tr>
<tr class="odd">
<td>El usuario ha iniciado sesión y desea cerrar la sesión y apagarla mediante SAS.</td>
<td>(La GINA supervisa los dispositivos en busca de eventos SAS).
<ol>
<li>La GINA llama a <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>la función WlxSasNotify.</strong></a></li>
<li>Winlogon llama a la función <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS de</strong></a> GINA.</li>
<li>La GINA devuelve WLX_SAS_ACTION_SHUTDOWN.</li>
<li>Winlogon llama a la función <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> de la GINA.</li>
<li>Winlogon llama a la función <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>WlxShutdown</strong></a> de GINA.</li>
</ol></td>
</tr>
</tbody>
</table>



 

 

 
