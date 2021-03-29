---
description: El rastreador de eventos de apagado permite al usuario o a la aplicación documentar el motivo de apagar o reiniciar el sistema.
ms.assetid: 860c014e-1fde-45d1-b366-c279bfcf4079
title: Rastreador de eventos de apagado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4208914149bb84df34e67cca71b40cde66363211
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360740"
---
# <a name="shutdown-event-tracker"></a>Rastreador de eventos de apagado

El *rastreador de eventos de apagado* permite al usuario o a la aplicación documentar el motivo de apagar o reiniciar el sistema. Al usuario se le pide que rellene la información al seleccionar **apagar** en el menú **Inicio** o al utilizar Shutdown.exe. Los desarrolladores pueden incluir un código de motivo al llamar a las funciones [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) y [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) . La información se almacena en el registro de eventos.

**Windows XP:** Aunque esta característica está habilitada de forma predeterminada a partir de Windows Server 2003, debe habilitarla en Windows XP. Para obtener más información, consulte la documentación del rastreador de eventos de apagado incluido en el sistema o en TechNet.

Las funciones [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) y [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) se han actualizado para admitir códigos de motivo de apagado en el parámetro *dwReason* . Use los valores definidos en Reason. h para construir un código de motivo de apagado, o bien defina un código de motivo personalizado. Un código de motivo de apagado se construye a partir de una marca principal, una marca secundaria y dos marcas opcionales. Para obtener más información, consulte [códigos de motivo de apagado del sistema](system-shutdown-reason-codes.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Rastreador de eventos de apagado (TechNet)](/previous-versions/windows/it-pro/windows-server-2003/cc783475(v=ws.10))
</dt> </dl>

 

 
