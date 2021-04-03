---
description: Winlogon y GINA deben comunicar la información de inicialización, controlar la supervisión y notificación de la secuencia de atención segura (SAS) y permitir las actividades de cierre de sesión y cierre.
ms.assetid: ea45cd5f-9cb0-41bb-99bf-f84781ae9604
title: 'Interacción entre Winlogon y GINA '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 759d9171bca02e0a00fd35b77a4514d7438d43f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083257"
---
# <a name="interaction-between-winlogon-and-gina"></a>Interacción entre Winlogon y GINA 

[*Winlogon*](../secgloss/w-gly.md) y [*Gina*](../secgloss/g-gly.md) deben comunicar la información de inicialización, controlar la supervisión y notificación de la [*secuencia de atención segura*](../secgloss/s-gly.md) (SAS) y permitir las actividades de cierre de sesión y cierre. El estado de Winlogon determina la función GINA a la que se llama para procesar cualquier evento SAS determinado. Las comunicaciones se producen en el orden que se muestra aquí.

> [!Note]  
> Los archivos dll de GINA se omiten en Windows Vista.

 



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
<li>Winlogon llama a la función <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate"><strong>WlxNegotiate</strong></a> de Gina para notificar a Gina la versión de Winlogon en uso.</li>
<li>Winlogon llama a la función <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize"><strong>WlxInitialize</strong></a> de Gina para proporcionar a Gina las direcciones de las funciones de soporte, un identificador a Winlogon, y para obtener la información de <a href="/windows/desktop/SecGloss/c-gly"><em>contexto</em></a> para Gina (que se usará en todas las llamadas futuras a Gina).<br/> Winlogon está en el estado de salida de sesión.<br/></li>
</ol></td>
</tr>
<tr class="even">
<td>No hay una sesión iniciada</td>
<td>(El GINA supervisa los dispositivos para los eventos de SAS).
<ol>
<li>GINA llama a la función <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> de Winlogon cuando se ha recibido un evento de SAS.</li>
<li>Winlogon llama a la función <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas"><strong>WlxLoggedOutSAS</strong></a> de Gina, lo que permite que Gina procese la información de autenticación e identificación de un usuario.<br/> Cuando el inicio de sesión se realiza correctamente, Winlogon está en estado conectado.<br/></li>
</ol></td>
</tr>
<tr class="odd">
<td>El usuario ha iniciado sesión</td>
<td>(El GINA supervisa los dispositivos para los eventos de SAS).
<ol>
<li>GINA llama a la función <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> de Winlogon cuando se ha recibido un evento de SAS.</li>
<li>Winlogon llama a la función <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> de Gina, lo que permite que Gina presente opciones al usuario que ha iniciado sesión actualmente.</li>
</ol></td>
</tr>
<tr class="even">
<td>El usuario ha iniciado sesión y desea bloquear el equipo</td>
<td>(El GINA supervisa los dispositivos para los eventos de SAS).
<ol>
<li>GINA llama a la función <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> .</li>
<li>Winlogon llama a la función <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> de Gina.</li>
<li>GINA devuelve WLX_SAS_ACTION_LOCK_WKSTA.<br/> Winlogon está en el estado de la estación de trabajo bloqueada.<br/></li>
</ol></td>
</tr>
<tr class="odd">
<td>El usuario ha iniciado sesión, la estación de trabajo está bloqueada y el usuario desea desbloquear el equipo</td>
<td>(El GINA supervisa los dispositivos para los eventos de SAS).
<ol>
<li>GINA llama a la función <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> .</li>
<li>Winlogon llama a la función <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxwkstalockedsas"><strong>WlxWkstaLockedSAS</strong></a> de Gina.</li>
<li>GINA devuelve WLX_SAS_ACTION_UNLOCK_WKSTA.</li>
</ol></td>
</tr>
<tr class="even">
<td>El usuario ha iniciado sesión y el programa llama a la función <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"><strong>ExitWindowsEx</strong></a></td>
<td>Winlogon llama a la función <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> de Gina.</td>
</tr>
<tr class="odd">
<td>El usuario ha iniciado sesión y desea cerrar sesión con SAS</td>
<td>(El GINA supervisa los dispositivos para los eventos de SAS).
<ol>
<li>GINA llama a la función <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> .</li>
<li>Winlogon llama a la función <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> de Gina.</li>
<li>GINA devuelve WLX_SAS_ACTION_LOGOFF.</li>
<li>Winlogon llama a la función <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> de Gina.</li>
</ol></td>
</tr>
<tr class="even">
<td>El usuario ha iniciado sesión y desea cerrar sesión y apagarlo mediante <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"> <strong>ExitWindowsEx</strong></a></td>
<td><ol>
<li>Winlogon llama a la función <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> de Gina.</li>
<li>Winlogon llama a la función <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>WlxShutdown</strong></a> de Gina.</li>
</ol></td>
</tr>
<tr class="odd">
<td>El usuario ha iniciado sesión y desea cerrar sesión y cerrarla con SAS</td>
<td>(El GINA supervisa los dispositivos para los eventos de SAS).
<ol>
<li>GINA llama a la función <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> .</li>
<li>Winlogon llama a la función <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> de Gina.</li>
<li>GINA devuelve WLX_SAS_ACTION_SHUTDOWN.</li>
<li>Winlogon llama a la función <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> de Gina.</li>
<li>Winlogon llama a la función <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>WlxShutdown</strong></a> de Gina.</li>
</ol></td>
</tr>
</tbody>
</table>



 

 

 
