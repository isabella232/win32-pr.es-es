---
description: SpawnDialog ControlEvent, notifica al instalador que cree un elemento secundario de un cuadro de diálogo modal mientras mantiene el cuadro de diálogo presente en ejecución.
ms.assetid: 2a341039-60dd-4e6c-9ef3-bf482ca53917
title: SpawnDialog ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71aec632332a87d047913b618aa2c39843849e5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677301"
---
# <a name="spawndialog-controlevent"></a><span data-ttu-id="84846-103">SpawnDialog ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="84846-103">SpawnDialog ControlEvent</span></span>

<span data-ttu-id="84846-104">SpawnDialog ControlEvent, notifica al instalador que cree un elemento secundario de un cuadro de diálogo modal mientras mantiene el cuadro de diálogo presente en ejecución.</span><span class="sxs-lookup"><span data-stu-id="84846-104">The SpawnDialog ControlEvent notifies the installer to create a child of a modal dialog box while keeping the present dialog box running.</span></span>

<span data-ttu-id="84846-105">Este evento puede ser publicado por un [control Pushbutton](pushbutton-control.md)o un [control SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="84846-105">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="84846-106">Este evento se debe crear en la [tabla ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="84846-106">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="84846-107">Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="84846-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="84846-108">Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida.</span><span class="sxs-lookup"><span data-stu-id="84846-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="84846-109">Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="84846-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="84846-110">Publicado por</span><span class="sxs-lookup"><span data-stu-id="84846-110">Published By</span></span>

<span data-ttu-id="84846-111">Este ControlEvent, lo publica el instalador.</span><span class="sxs-lookup"><span data-stu-id="84846-111">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="84846-112">Argumento</span><span class="sxs-lookup"><span data-stu-id="84846-112">Argument</span></span>

<span data-ttu-id="84846-113">Cadena que es el nombre del nuevo cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="84846-113">A string that is the name of the new dialog box.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="84846-114">Acción en los suscriptores</span><span class="sxs-lookup"><span data-stu-id="84846-114">Action on Subscribers</span></span>

<span data-ttu-id="84846-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="84846-115">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="84846-116">Uso típico</span><span class="sxs-lookup"><span data-stu-id="84846-116">Typical Use</span></span>

<span data-ttu-id="84846-117">Un control [Pushbutton](pushbutton-control.md) en un cuadro de diálogo modal está asociado a este evento en la tabla [ControlEvent,](controlevent-table.md) para crear un cuadro de diálogo secundario, como "¿está seguro de que desea cancelar?"</span><span class="sxs-lookup"><span data-stu-id="84846-117">A [PushButton](pushbutton-control.md) control on a modal dialog is tied to this event in the [ControlEvent](controlevent-table.md) table to create a child dialog, such as an "Are you sure you want to cancel?"</span></span> <span data-ttu-id="84846-118">.</span><span class="sxs-lookup"><span data-stu-id="84846-118">dialog box.</span></span>

 

 



