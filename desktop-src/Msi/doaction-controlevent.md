---
description: La ControlEvent, de la acción notifica al instalador que ejecute una acción personalizada. Este evento puede ser publicado por un control PushButton, un control CheckBox o un control SelectionTree. Este evento se debe crear en la tabla ControlEvent,.
ms.assetid: 9a855330-8241-4912-84da-4fca43f1d240
title: ControlEvent, de acción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74cc16c918522408e4cdf046e95d3d822ba3ac5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153881"
---
# <a name="doaction-controlevent"></a><span data-ttu-id="95a97-105">ControlEvent, de acción</span><span class="sxs-lookup"><span data-stu-id="95a97-105">DoAction ControlEvent</span></span>

<span data-ttu-id="95a97-106">La ControlEvent, de la acción notifica al instalador que ejecute una acción personalizada.</span><span class="sxs-lookup"><span data-stu-id="95a97-106">The DoAction ControlEvent notifies the installer to execute a custom action.</span></span> <span data-ttu-id="95a97-107">Este evento puede ser publicado por un control [Pushbutton](pushbutton-control.md) , un control [CheckBox](checkbox-control.md) o un control [SelectionTree](selectiontree-control.md) .</span><span class="sxs-lookup"><span data-stu-id="95a97-107">This event can be published by a [PushButton](pushbutton-control.md) control, [CheckBox](checkbox-control.md) control, or a [SelectionTree](selectiontree-control.md) control.</span></span> <span data-ttu-id="95a97-108">Este evento se debe crear en la tabla [ControlEvent,](controlevent-table.md) .</span><span class="sxs-lookup"><span data-stu-id="95a97-108">This event should be authored into the [ControlEvent](controlevent-table.md) table.</span></span>

<span data-ttu-id="95a97-109">Tenga en cuenta que las acciones personalizadas iniciadas por un ControlEvent, de acción pueden enviar un mensaje con el [**método de mensaje**](session-message.md), pero no puede enviar un mensaje con [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage).</span><span class="sxs-lookup"><span data-stu-id="95a97-109">Note that custom actions launched by a DoAction ControlEvent can send a message with the [**Message Method**](session-message.md), but cannot send a message with [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage).</span></span> <span data-ttu-id="95a97-110">En sistemas anteriores a Windows Server 2003, las acciones personalizadas iniciadas por una acción ControlEvent, no pueden enviar mensajes con **MsiProcessMessage** o un **método de mensaje**.</span><span class="sxs-lookup"><span data-stu-id="95a97-110">On systems prior to Windows Server 2003, custom actions launched by a DoAction ControlEvent cannot send messages with **MsiProcessMessage** or **Message Method**.</span></span> <span data-ttu-id="95a97-111">Para obtener más información, consulte [envío de mensajes a Windows Installer mediante MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).</span><span class="sxs-lookup"><span data-stu-id="95a97-111">For more information, see [Sending Messages to Windows Installer Using MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).</span></span>

<span data-ttu-id="95a97-112">Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="95a97-112">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="95a97-113">Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida.</span><span class="sxs-lookup"><span data-stu-id="95a97-113">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="95a97-114">Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="95a97-114">For more information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="95a97-115">Publicado por</span><span class="sxs-lookup"><span data-stu-id="95a97-115">Published By</span></span>

<span data-ttu-id="95a97-116">Este ControlEvent, lo publica el instalador.</span><span class="sxs-lookup"><span data-stu-id="95a97-116">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="95a97-117">Argumento</span><span class="sxs-lookup"><span data-stu-id="95a97-117">Argument</span></span>

<span data-ttu-id="95a97-118">Una cadena, el nombre de la acción personalizada que se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="95a97-118">A string, the name of the custom action to be executed.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="95a97-119">Acción en los suscriptores</span><span class="sxs-lookup"><span data-stu-id="95a97-119">Action on Subscribers</span></span>

<span data-ttu-id="95a97-120">Este ControlEvent, no realiza ninguna acción en los suscriptores.</span><span class="sxs-lookup"><span data-stu-id="95a97-120">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="95a97-121">Uso típico</span><span class="sxs-lookup"><span data-stu-id="95a97-121">Typical Use</span></span>

<span data-ttu-id="95a97-122">Un control [Pushbutton](pushbutton-control.md) en un cuadro de diálogo está asociado a este evento en la tabla [ControlEvent,](controlevent-table.md) para invocar una acción personalizada.</span><span class="sxs-lookup"><span data-stu-id="95a97-122">A [PushButton](pushbutton-control.md) control on a dialog box is tied to this event in the [ControlEvent](controlevent-table.md) table to invoke a custom action.</span></span>

 

 



