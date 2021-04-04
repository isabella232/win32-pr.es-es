---
description: Winlogon implementa dos operaciones de tiempo de espera, una para los cuadros de diálogo seguros y la otra para la activación y finalización del protector de pantalla.
ms.assetid: b1dfd7dc-cc00-4f1a-a157-c60b5d0f0b13
title: Cuadro de diálogo compatible Tiempo de servicio operaciones de salida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 274950cadd45cd4e7e3be890da0e4350a4d0c5ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809901"
---
# <a name="supported-dialog-box-service-time-out-operations"></a><span data-ttu-id="2cd7e-103">Cuadro de diálogo compatible Tiempo de servicio operaciones de salida</span><span class="sxs-lookup"><span data-stu-id="2cd7e-103">Supported Dialog Box Service Time-out Operations</span></span>

<span data-ttu-id="2cd7e-104">[*Winlogon*](../secgloss/w-gly.md) implementa dos operaciones de tiempo de espera, una para los cuadros de diálogo seguros y la otra para la activación y finalización del protector de pantalla.</span><span class="sxs-lookup"><span data-stu-id="2cd7e-104">[*Winlogon*](../secgloss/w-gly.md) implements two time-out operations, one for secure dialog boxes and the other for screen saver activation and termination.</span></span>

<span data-ttu-id="2cd7e-105">Al mostrar un cuadro de diálogo seguro, como el inicio de sesión o el desbloqueo de una estación de trabajo, Winlogon puede agotar el tiempo de espera de los cuadros de diálogo y devolver un código de resultado adecuado al procedimiento del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="2cd7e-105">While displaying a secure dialog box, such as logon or unlocking a workstation, Winlogon can time-out the dialog boxes and return an appropriate result code to the dialog box procedure.</span></span> <span data-ttu-id="2cd7e-106">Winlogon proporciona un conjunto de funciones de compatibilidad de cuadro de diálogo para [*Gina*](../secgloss/g-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2cd7e-106">Winlogon provides a set of dialog box support functions for the [*GINA*](../secgloss/g-gly.md).</span></span> <span data-ttu-id="2cd7e-107">GINA debe usar estas funciones en lugar de sus homólogos de Windows para asegurarse de que GINA y Winlogon mantienen el control adecuado sobre los cuadros de diálogo.</span><span class="sxs-lookup"><span data-stu-id="2cd7e-107">The GINA must use these functions instead of their Windows counterparts to ensure that the GINA and Winlogon maintain appropriate control over the dialog boxes.</span></span> <span data-ttu-id="2cd7e-108">Si no se utilizan las versiones de Winlogon de estas funciones, los usuarios no autorizados tendrán acceso al sistema.</span><span class="sxs-lookup"><span data-stu-id="2cd7e-108">Failure to use the Winlogon versions of these functions could result in unauthorized users gaining access to the system.</span></span>

<span data-ttu-id="2cd7e-109">Los servicios del cuadro de diálogo Winlogon se proporcionan mediante las siguientes funciones de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="2cd7e-109">Winlogon dialog box services are provided by the following support functions.</span></span>



| <span data-ttu-id="2cd7e-110">Función de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="2cd7e-110">Support function</span></span>                                               | <span data-ttu-id="2cd7e-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="2cd7e-111">Description</span></span>                                                                                      |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2cd7e-112">**WlxMessageBox**</span><span class="sxs-lookup"><span data-stu-id="2cd7e-112">**WlxMessageBox**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_message_box)                         | <span data-ttu-id="2cd7e-113">Similar a la función [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) de Windows.</span><span class="sxs-lookup"><span data-stu-id="2cd7e-113">Similar to the Windows [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) function.</span></span>                         |
| [<span data-ttu-id="2cd7e-114">**WlxDialogBox**</span><span class="sxs-lookup"><span data-stu-id="2cd7e-114">**WlxDialogBox**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box)                           | <span data-ttu-id="2cd7e-115">Similar a la función [**DialogBox**](/windows/win32/api/winuser/nf-winuser-dialogboxa) de Windows.</span><span class="sxs-lookup"><span data-stu-id="2cd7e-115">Similar to the Windows [**DialogBox**](/windows/win32/api/winuser/nf-winuser-dialogboxa) function.</span></span>                           |
| [<span data-ttu-id="2cd7e-116">**WlxDialogBoxIndirect**</span><span class="sxs-lookup"><span data-stu-id="2cd7e-116">**WlxDialogBoxIndirect**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_indirect)           | <span data-ttu-id="2cd7e-117">Similar a la función [**DialogBoxIndirect**](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta) de Windows.</span><span class="sxs-lookup"><span data-stu-id="2cd7e-117">Similar to the Windows [**DialogBoxIndirect**](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta) function.</span></span>           |
| [<span data-ttu-id="2cd7e-118">**WlxDialogBoxParam**</span><span class="sxs-lookup"><span data-stu-id="2cd7e-118">**WlxDialogBoxParam**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param)                 | <span data-ttu-id="2cd7e-119">Similar a la función [**DialogBoxParam**](/windows/win32/api/winuser/nf-winuser-dialogboxparama) de Windows.</span><span class="sxs-lookup"><span data-stu-id="2cd7e-119">Similar to the Windows [**DialogBoxParam**](/windows/win32/api/winuser/nf-winuser-dialogboxparama) function.</span></span>                 |
| [<span data-ttu-id="2cd7e-120">**WlxDialogBoxIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="2cd7e-120">**WlxDialogBoxIndirectParam**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_indirect_param) | <span data-ttu-id="2cd7e-121">Similar a la función [**DialogBoxIndirectParam**](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama) de Windows.</span><span class="sxs-lookup"><span data-stu-id="2cd7e-121">Similar to the Windows [**DialogBoxIndirectParam**](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama) function.</span></span> |



 

<span data-ttu-id="2cd7e-122">Los archivos dll de GINA también pueden recibir \_ \_ mensajes SAS de WLX WM desde Winlogon.</span><span class="sxs-lookup"><span data-stu-id="2cd7e-122">GINA DLLs can also receive WLX\_WM\_SAS messages from Winlogon.</span></span> <span data-ttu-id="2cd7e-123">Estos mensajes se envían a los cuadros de diálogo activos si se recibe una [*secuencia de atención segura*](../secgloss/s-gly.md) (SAS).</span><span class="sxs-lookup"><span data-stu-id="2cd7e-123">These messages are sent to active dialog boxes if an [*secure attention sequence*](../secgloss/s-gly.md) (SAS) is received.</span></span> <span data-ttu-id="2cd7e-124">Esto resulta útil si GINA está en proceso de solicitar el PIN correspondiente para una [*tarjeta inteligente*](../secgloss/s-gly.md)y la tarjeta se quita del [*lector*](../secgloss/r-gly.md)de tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="2cd7e-124">This is useful if the GINA is in the process of prompting for the matching PIN for a [*smart card*](../secgloss/s-gly.md), and the card is removed from the smart card [*reader*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="2cd7e-125">Winlogon usa \_ SAS WLX Dlg \_ como código de resultado EndDialog cuando se produce un evento de SAS durante una operación de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="2cd7e-125">Winlogon uses WLX\_DLG\_SAS as the EndDialog result code when an SAS event occurs during a dialog box operation.</span></span>

<span data-ttu-id="2cd7e-126">Los tiempos de espera también se entregan de esta manera.</span><span class="sxs-lookup"><span data-stu-id="2cd7e-126">Time-outs are also delivered in this manner.</span></span> <span data-ttu-id="2cd7e-127">\_Se envía un mensaje SAS de WLX WM con el tiempo de espera de \_ WLX de \_ \_ tipo SAS \_ SCRNSVR o de \_ WLX \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2cd7e-127">A WLX\_WM\_SAS message is sent with WLX\_SAS\_TYPE\_SCRNSVR\_TIMEOUT or WLX\_SAS\_TYPE\_TIMEOUT.</span></span> <span data-ttu-id="2cd7e-128">El cuadro de diálogo finalizará con un código de salida adecuado para permitir a los desarrolladores de GINA enlazar las notificaciones de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="2cd7e-128">The dialog box will end with an appropriate exit code to allow GINA developers to hook the time-out notifications.</span></span>

<span data-ttu-id="2cd7e-129">Winlogon puede finalizar los cuadros de diálogo de GINA mediante el código de \_ cierre de sesión de usuario WLX Dlg \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2cd7e-129">GINA dialog boxes can be terminated by Winlogon by using the code WLX\_DLG\_USER\_LOGOFF.</span></span> <span data-ttu-id="2cd7e-130">Esto indica que el usuario ha cerrado la sesión durante la ejecución del cuadro de diálogo (por ejemplo, mediante una llamada a la función [**ExitWindowsEx**](/windows/win32/api/winuser/nf-winuser-exitwindowsex) desde otro subproceso).</span><span class="sxs-lookup"><span data-stu-id="2cd7e-130">This indicates that the user has logged off during the running of the dialog box (for example, by calling the [**ExitWindowsEx**](/windows/win32/api/winuser/nf-winuser-exitwindowsex) function from another thread).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2cd7e-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2cd7e-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2cd7e-132">Inicializando Winlogon</span><span class="sxs-lookup"><span data-stu-id="2cd7e-132">Initializing Winlogon</span></span>](initializing-winlogon.md)
</dt> <dt>

[<span data-ttu-id="2cd7e-133">Estados de Winlogon</span><span class="sxs-lookup"><span data-stu-id="2cd7e-133">Winlogon States</span></span>](winlogon-states.md)
</dt> <dt>

[<span data-ttu-id="2cd7e-134">Envío de mensajes a GINA</span><span class="sxs-lookup"><span data-stu-id="2cd7e-134">Sending Messages to the GINA</span></span>](sending-messages-to-the-gina.md)
</dt> <dt>

[<span data-ttu-id="2cd7e-135">Funciones de compatibilidad con Winlogon</span><span class="sxs-lookup"><span data-stu-id="2cd7e-135">Winlogon Support Functions</span></span>](authentication-functions.md)
</dt> </dl>

 

 
