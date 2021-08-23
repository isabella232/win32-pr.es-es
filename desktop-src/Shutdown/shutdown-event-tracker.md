---
description: Shutdown Event Tracker permite al usuario o a la aplicación documentar el motivo para apagar o reiniciar el sistema.
ms.assetid: 860c014e-1fde-45d1-b366-c279bfcf4079
title: Rastreador de eventos de apagado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee2deaebde736ed2e0ba72f38e8849cf815b167da68fdddbecb92e713083699b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664365"
---
# <a name="shutdown-event-tracker"></a>Rastreador de eventos de apagado

Shutdown *Event Tracker permite* al usuario o a la aplicación documentar el motivo para apagar o reiniciar el sistema. Se pide al usuario que rellene la información  al seleccionar **Apagar** en el menú Inicio o al usar Shutdown.exe. Los desarrolladores pueden incluir un código de motivo al llamar a las [**funciones ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) e [**InitiateSystemShutdownEx.**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) La información se almacena en el registro de eventos.

**Windows XP:** Aunque esta característica está habilitada de forma predeterminada a partir de Windows Server 2003, debe habilitarla en Windows XP. Para obtener más información, consulte la documentación del seguimiento de eventos de apagado incluido en el sistema o en TechNet.

Las [**funciones ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) e [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) se han actualizado para admitir códigos de motivo de apagado en el *parámetro dwReason.* Use los valores definidos en Reason.h para construir un código de motivo de apagado o definir un código de motivo personalizado. Un código de motivo de apagado se construye a partir de una marca principal, una marca secundaria y dos marcas opcionales. Para obtener más información, vea [Códigos de motivo de apagado del sistema.](system-shutdown-reason-codes.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Shutdown Event Tracker (TechNet)](/previous-versions/windows/it-pro/windows-server-2003/cc783475(v=ws.10))
</dt> </dl>

 

 
