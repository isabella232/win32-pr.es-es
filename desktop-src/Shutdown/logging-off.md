---
description: La función ExitWindows cierra la sesión del usuario actual. También puede llamar a la función ExitWindowsEx con la \_ marca de cierre de sesión EXW.
ms.assetid: 906d92f1-7cbe-454e-9c71-34b4383aebab
title: Cerrando sesión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0571c0522c494acd763d57dcae8d200125cd53d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913850"
---
# <a name="logging-off"></a><span data-ttu-id="e35d7-104">Cerrando sesión</span><span class="sxs-lookup"><span data-stu-id="e35d7-104">Logging Off</span></span>

<span data-ttu-id="e35d7-105">La función [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) cierra la sesión del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="e35d7-105">The [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) function logs off the current user.</span></span> <span data-ttu-id="e35d7-106">También puede llamar a la función [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) con la \_ marca de cierre de sesión EXW.</span><span class="sxs-lookup"><span data-stu-id="e35d7-106">You can also call the [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) function with the EXW\_LOGOFF flag.</span></span>

<span data-ttu-id="e35d7-107">De forma predeterminada, cuando una aplicación usa [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) o [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) para cerrar la sesión, el sistema envía el mensaje de [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) a cada ventana.</span><span class="sxs-lookup"><span data-stu-id="e35d7-107">By default, when an application uses [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) or [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) to log off, the system sends the [**WM\_QUERYENDSESSION**](wm-queryendsession.md) message to each window.</span></span> <span data-ttu-id="e35d7-108">Las aplicaciones aceptan finalizar devolviendo **true** cuando reciben este mensaje.</span><span class="sxs-lookup"><span data-stu-id="e35d7-108">Applications agree to terminate by returning **TRUE** when they receive this message.</span></span> <span data-ttu-id="e35d7-109">Si alguna aplicación devuelve **false** al procesar este mensaje, se cancela la operación de cierre de sesión.</span><span class="sxs-lookup"><span data-stu-id="e35d7-109">If any application returns **FALSE** when processing this message, the log-off operation is canceled.</span></span> <span data-ttu-id="e35d7-110">Si la aplicación controla el mensaje de **\_ QUERYENDSESSION de WM** , puede permitir que el usuario cancele la operación de cierre de sesión, incluso si otra aplicación o el sistema originó la solicitud de la sesión final.</span><span class="sxs-lookup"><span data-stu-id="e35d7-110">If your application handles the **WM\_QUERYENDSESSION** message, you can allow the user to cancel the log-off operation, even if another application or the system originated the end-session request.</span></span> <span data-ttu-id="e35d7-111">Para obtener un ejemplo, consulte [cómo cerrar la sesión del usuario actual](how-to-log-off-the-current-user.md).</span><span class="sxs-lookup"><span data-stu-id="e35d7-111">For an example, see [How to Log Off the Current User](how-to-log-off-the-current-user.md).</span></span>

<span data-ttu-id="e35d7-112">Cuando una aplicación devuelve **true** para [**WM \_ QUERYENDSESSION**](wm-queryendsession.md), recibe el mensaje de [**WM \_ ENDSESSION**](wm-endsession.md) y se termina, independientemente de cómo respondan las otras aplicaciones al mensaje **de \_ QUERYENDSESSION de WM** .</span><span class="sxs-lookup"><span data-stu-id="e35d7-112">When an application returns **TRUE** for [**WM\_QUERYENDSESSION**](wm-queryendsession.md), it receives the [**WM\_ENDSESSION**](wm-endsession.md) message and it is terminated, regardless of how the other applications respond to the **WM\_QUERYENDSESSION** message.</span></span>

<span data-ttu-id="e35d7-113">Para forzar la finalización de todas las aplicaciones, use [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex)y especifique la \_ marca Force de EXW.</span><span class="sxs-lookup"><span data-stu-id="e35d7-113">To force all applications to terminate, use [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex), and specify the EXW\_FORCE flag.</span></span> <span data-ttu-id="e35d7-114">Esto impide que el sistema envíe mensajes de [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) .</span><span class="sxs-lookup"><span data-stu-id="e35d7-114">This prevents the system from sending [**WM\_QUERYENDSESSION**](wm-queryendsession.md) messages.</span></span>

<span data-ttu-id="e35d7-115">El sistema también envía la \_ señal de control de evento Ctrl Logoff \_ a todos los procesos durante una operación de cierre de sesión.</span><span class="sxs-lookup"><span data-stu-id="e35d7-115">The system also sends the CTRL\_LOGOFF\_EVENT control signal to every process during a log-off operation.</span></span> <span data-ttu-id="e35d7-116">Una aplicación de consola puede registrar un [**HandlerRoutine**](/windows/console/handlerroutine) para procesar estos mensajes.</span><span class="sxs-lookup"><span data-stu-id="e35d7-116">A console application can register a [**HandlerRoutine**](/windows/console/handlerroutine) to process these messages.</span></span>

<span data-ttu-id="e35d7-117">Si el proceso que llamó a [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) se está ejecutando en la sesión de inicio de sesión del usuario interactivo, se finalizan todos los procesos de la sesión de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="e35d7-117">If the process that called [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) is running in the logon session of the interactive user, all processes in the logon session are terminated.</span></span> <span data-ttu-id="e35d7-118">Si el proceso que llama a **ExitWindowsEx** está en otra sesión de inicio de sesión, solo se realizan las notificaciones; no se termina ningún proceso.</span><span class="sxs-lookup"><span data-stu-id="e35d7-118">If the process calling **ExitWindowsEx** is in some other logon session, only the notifications are made; no processes are terminated.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e35d7-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e35d7-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e35d7-120">Cómo cerrar la sesión del usuario actual</span><span class="sxs-lookup"><span data-stu-id="e35d7-120">How to Log Off the Current User</span></span>](how-to-log-off-the-current-user.md)
</dt> </dl>

 

 
