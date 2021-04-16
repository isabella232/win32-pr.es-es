---
title: Mensajes en Active Directory Domain Services
description: Los mensajes de Active Directory Domain Services son funcionales en Windows 2000 y Windows NT 4,0 con Service Pack 6a (SP6a) y posterior con DSClient.
ms.assetid: 32a4724b-3182-4521-975c-cef33afee0b2
ms.tgt_platform: multiple
keywords:
- Active Directory mensajes de AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6895aee711af04778318cf42920d0b0416725205
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656221"
---
# <a name="messages-in-active-directory-domain-services"></a><span data-ttu-id="82cb3-104">Mensajes en Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="82cb3-104">Messages in Active Directory Domain Services</span></span>

<span data-ttu-id="82cb3-105">Los mensajes de Active Directory Domain Services son funcionales en Windows 2000 y Windows NT 4,0 con Service Pack 6a (SP6a) y posterior con DSClient.</span><span class="sxs-lookup"><span data-stu-id="82cb3-105">Messages in Active Directory Domain Services are functional in Windows 2000 and Windows NT 4.0 with Service Pack 6a (SP6a) and later with DSClient.</span></span> <span data-ttu-id="82cb3-106">También son funcionales en estaciones de trabajo de Windows 98/95 con IE 4.01 y versiones posteriores y DSClient.</span><span class="sxs-lookup"><span data-stu-id="82cb3-106">They are also functional in Windows 98/95 workstations with IE4.01 and later and DSClient.</span></span> <span data-ttu-id="82cb3-107">Sin embargo, si las páginas de propiedades de selección MultiSelect se inician desde el Shell, el mensaje de [**\_ \_ \_ error de notificaciones de WM ADSPROP**](wm-adsprop-notify-error.md) y sus funciones auxiliares correspondientes, [**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) y [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) , no estarán funcionales y no se mostrarán.</span><span class="sxs-lookup"><span data-stu-id="82cb3-107">However, if multiselect property pages are launched from the shell, then the [**WM\_ADSPROP\_NOTIFY\_ERROR**](wm-adsprop-notify-error.md) message and its corresponding helper functions, [**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) and [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) are not functional and will not be displayed.</span></span> <span data-ttu-id="82cb3-108">Si las páginas de propiedades de selección MultiSelect se inician en una herramienta de administración, por ejemplo, usuarios y equipos de AD, todos los mensajes estarán funcionales y estarán disponibles para que se muestren en las páginas de propiedades de selección MultiSelect.</span><span class="sxs-lookup"><span data-stu-id="82cb3-108">If multiselect property pages are launched within an admin tool, for example, AD Users and Computers, then all messages are functional and available to be displayed within the multiselect property pages.</span></span>

<span data-ttu-id="82cb3-109">Active Directory Domain Services usar los siguientes mensajes:</span><span class="sxs-lookup"><span data-stu-id="82cb3-109">Active Directory Domain Services use the following messages:</span></span>

-   [<span data-ttu-id="82cb3-110">**\_solicitud de ADSPROP de WM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="82cb3-110">**WM\_ADSPROP\_NOTIFY\_APPLY**</span></span>](wm-adsprop-notify-apply.md)
-   [<span data-ttu-id="82cb3-111">**\_ \_ notificar cambio de ADSPROP de WM \_**</span><span class="sxs-lookup"><span data-stu-id="82cb3-111">**WM\_ADSPROP\_NOTIFY\_CHANGE**</span></span>](wm-adsprop-notify-change.md)
-   [<span data-ttu-id="82cb3-112">**\_error de \_ notificación de ADSPROP de WM \_**</span><span class="sxs-lookup"><span data-stu-id="82cb3-112">**WM\_ADSPROP\_NOTIFY\_ERROR**</span></span>](wm-adsprop-notify-error.md)
-   [<span data-ttu-id="82cb3-113">**\_salida de \_ notificación de ADSPROP de WM \_**</span><span class="sxs-lookup"><span data-stu-id="82cb3-113">**WM\_ADSPROP\_NOTIFY\_EXIT**</span></span>](wm-adsprop-notify-exit.md)
-   [<span data-ttu-id="82cb3-114">**\_ \_ notificar a \_ primer plano ADSPROP de WM**</span><span class="sxs-lookup"><span data-stu-id="82cb3-114">**WM\_ADSPROP\_NOTIFY\_FOREGROUND**</span></span>](wm-adsprop-notify-foreground.md)
-   [<span data-ttu-id="82cb3-115">**\_ADSPROP \_ notificar a \_ PAGEHWND de WM**</span><span class="sxs-lookup"><span data-stu-id="82cb3-115">**WM\_ADSPROP\_NOTIFY\_PAGEHWND**</span></span>](wm-adsprop-notify-pagehwnd.md)
-   [<span data-ttu-id="82cb3-116">**\_ADSPROP \_ notificar a \_ PAGEINIT de WM**</span><span class="sxs-lookup"><span data-stu-id="82cb3-116">**WM\_ADSPROP\_NOTIFY\_PAGEINIT**</span></span>](wm-adsprop-notify-pageinit.md)
-   [<span data-ttu-id="82cb3-117">**\_ADSPROP \_ notificar \_ SETFOCUS de WM**</span><span class="sxs-lookup"><span data-stu-id="82cb3-117">**WM\_ADSPROP\_NOTIFY\_SETFOCUS**</span></span>](wm-adsprop-notify-setfocus.md)
-   [<span data-ttu-id="82cb3-118">**hoja de ADSPROP de WM \_ \_ \_ creación**</span><span class="sxs-lookup"><span data-stu-id="82cb3-118">**WM\_ADSPROP\_SHEET\_CREATE**</span></span>](wm-adsprop-sheet-create.md)
-   [<span data-ttu-id="82cb3-119">**\_notificación de \_ cierre de hoja DSA \_ de WM \_**</span><span class="sxs-lookup"><span data-stu-id="82cb3-119">**WM\_DSA\_SHEET\_CLOSE\_NOTIFY**</span></span>](wm-dsa-sheet-close-notify.md)
-   [<span data-ttu-id="82cb3-120">**\_ \_ \_ crear notificación de la hoja DSA de WM \_**</span><span class="sxs-lookup"><span data-stu-id="82cb3-120">**WM\_DSA\_SHEET\_CREATE\_NOTIFY**</span></span>](wm-dsa-sheet-create-notify.md)

 

 




