---
description: El evento SetInstallLevel cambia el nivel de instalación al valor especificado por el argumento.
ms.assetid: 71cfd516-4a92-446c-bd8f-a3a04dba0bb2
title: SetInstallLevel ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 347f54cee1494b2ff91f7dc1701f0b7749d47e4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275665"
---
# <a name="setinstalllevel-controlevent"></a><span data-ttu-id="b1acd-103">SetInstallLevel ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="b1acd-103">SetInstallLevel ControlEvent</span></span>

<span data-ttu-id="b1acd-104">El evento SetInstallLevel cambia el nivel de instalación al valor especificado por el argumento.</span><span class="sxs-lookup"><span data-stu-id="b1acd-104">The SetInstallLevel event changes the installation level to the value specified by the argument.</span></span>

<span data-ttu-id="b1acd-105">Este evento puede ser publicado por un [control Pushbutton](pushbutton-control.md)o un [control SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="b1acd-105">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="b1acd-106">Este evento se debe crear en la [tabla ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="b1acd-106">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="b1acd-107">Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="b1acd-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="b1acd-108">Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida.</span><span class="sxs-lookup"><span data-stu-id="b1acd-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="b1acd-109">Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="b1acd-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="b1acd-110">Publicado por</span><span class="sxs-lookup"><span data-stu-id="b1acd-110">Published By</span></span>

<span data-ttu-id="b1acd-111">Este ControlEvent, lo publica el instalador.</span><span class="sxs-lookup"><span data-stu-id="b1acd-111">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="b1acd-112">Argumento</span><span class="sxs-lookup"><span data-stu-id="b1acd-112">Argument</span></span>

<span data-ttu-id="b1acd-113">Un entero que es el nuevo valor del nivel de instalación.</span><span class="sxs-lookup"><span data-stu-id="b1acd-113">An integer that is the new value of the installation level.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="b1acd-114">Acción en los suscriptores</span><span class="sxs-lookup"><span data-stu-id="b1acd-114">Action on Subscribers</span></span>

<span data-ttu-id="b1acd-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b1acd-115">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="b1acd-116">Uso típico</span><span class="sxs-lookup"><span data-stu-id="b1acd-116">Typical Use</span></span>

<span data-ttu-id="b1acd-117">Un control [Pushbutton](pushbutton-control.md) en un cuadro de diálogo modal está asociado a este evento en la tabla [ControlEvent,](controlevent-table.md) para cambiar el nivel de instalación.</span><span class="sxs-lookup"><span data-stu-id="b1acd-117">A [PushButton](pushbutton-control.md) control on a modal dialog box is tied to this event in the [ControlEvent](controlevent-table.md) table to change the installation level.</span></span>

 

 



