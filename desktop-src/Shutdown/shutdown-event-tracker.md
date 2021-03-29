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
# <a name="shutdown-event-tracker"></a><span data-ttu-id="15f45-103">Rastreador de eventos de apagado</span><span class="sxs-lookup"><span data-stu-id="15f45-103">Shutdown Event Tracker</span></span>

<span data-ttu-id="15f45-104">El *rastreador de eventos de apagado* permite al usuario o a la aplicación documentar el motivo de apagar o reiniciar el sistema.</span><span class="sxs-lookup"><span data-stu-id="15f45-104">The *Shutdown Event Tracker* enables the user or application to document the reason for shutting down or restarting the system.</span></span> <span data-ttu-id="15f45-105">Al usuario se le pide que rellene la información al seleccionar **apagar** en el menú **Inicio** o al utilizar Shutdown.exe.</span><span class="sxs-lookup"><span data-stu-id="15f45-105">The user is prompted to fill in information when selecting **Shut Down** from the **Start** menu, or when using Shutdown.exe.</span></span> <span data-ttu-id="15f45-106">Los desarrolladores pueden incluir un código de motivo al llamar a las funciones [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) y [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) .</span><span class="sxs-lookup"><span data-stu-id="15f45-106">Developers can include a reason code when calling the [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) and [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) functions.</span></span> <span data-ttu-id="15f45-107">La información se almacena en el registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="15f45-107">The information is stored in the event log.</span></span>

<span data-ttu-id="15f45-108">**Windows XP:** Aunque esta característica está habilitada de forma predeterminada a partir de Windows Server 2003, debe habilitarla en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="15f45-108">**Windows XP:** While this feature is enabled by default starting with Windows Server 2003, you must enable it on Windows XP.</span></span> <span data-ttu-id="15f45-109">Para obtener más información, consulte la documentación del rastreador de eventos de apagado incluido en el sistema o en TechNet.</span><span class="sxs-lookup"><span data-stu-id="15f45-109">For more information, see the documentation for the Shutdown Event Tracker included in the system or on TechNet.</span></span>

<span data-ttu-id="15f45-110">Las funciones [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) y [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) se han actualizado para admitir códigos de motivo de apagado en el parámetro *dwReason* .</span><span class="sxs-lookup"><span data-stu-id="15f45-110">The [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) and [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) functions have been updated to support shutdown reason codes in the *dwReason* parameter.</span></span> <span data-ttu-id="15f45-111">Use los valores definidos en Reason. h para construir un código de motivo de apagado, o bien defina un código de motivo personalizado.</span><span class="sxs-lookup"><span data-stu-id="15f45-111">Use the values defined in Reason.h to construct a shutdown reason code, or define a custom reason code.</span></span> <span data-ttu-id="15f45-112">Un código de motivo de apagado se construye a partir de una marca principal, una marca secundaria y dos marcas opcionales.</span><span class="sxs-lookup"><span data-stu-id="15f45-112">A shutdown reason code is constructed from a major flag, a minor flag, and two optional flags.</span></span> <span data-ttu-id="15f45-113">Para obtener más información, consulte [códigos de motivo de apagado del sistema](system-shutdown-reason-codes.md).</span><span class="sxs-lookup"><span data-stu-id="15f45-113">For more information, see [System Shutdown Reason Codes](system-shutdown-reason-codes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="15f45-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="15f45-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="15f45-115">[Rastreador de eventos de apagado (TechNet)](/previous-versions/windows/it-pro/windows-server-2003/cc783475(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="15f45-115">[Shutdown Event Tracker (TechNet)](/previous-versions/windows/it-pro/windows-server-2003/cc783475(v=ws.10))</span></span>
</dt> </dl>

 

 
