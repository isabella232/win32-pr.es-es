---
description: SpawnWaitDialog ControlEvent, desencadena el cuadro de diálogo especificado por la columna argument de la tabla ControlEvent,, si la expresión de la columna condition se evalúa como FALSE.
ms.assetid: 38a5d896-2c11-4ce9-b829-104a882723b6
title: SpawnWaitDialog ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b20059c936a8534d00799c93dfbe3408a19c6dbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001248"
---
# <a name="spawnwaitdialog-controlevent"></a><span data-ttu-id="7b9a9-103">SpawnWaitDialog ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="7b9a9-103">SpawnWaitDialog ControlEvent</span></span>

<span data-ttu-id="7b9a9-104">SpawnWaitDialog ControlEvent, desencadena el cuadro de diálogo especificado por la columna argument de la [tabla ControlEvent,](controlevent-table.md), si la expresión de la columna condition se evalúa como false.</span><span class="sxs-lookup"><span data-stu-id="7b9a9-104">The SpawnWaitDialog ControlEvent triggers the dialog box specified by the Argument column of the [ControlEvent table](controlevent-table.md), if the expression in the Condition column evaluates as FALSE.</span></span> <span data-ttu-id="7b9a9-105">El cuadro de diálogo permanece activo mientras la expresión condicional sigue siendo falsa y se quita en cuanto la condición se evalúa como TRUE.</span><span class="sxs-lookup"><span data-stu-id="7b9a9-105">The dialog box remains up for as long as the conditional expression remains FALSE and is removed as soon as the condition evaluates TRUE.</span></span>

<span data-ttu-id="7b9a9-106">Este evento puede ser publicado por un [control Pushbutton](pushbutton-control.md)o un [control SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="7b9a9-106">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="7b9a9-107">Este evento se debe crear en la [tabla ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="7b9a9-107">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="7b9a9-108">Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="7b9a9-108">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="7b9a9-109">Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida.</span><span class="sxs-lookup"><span data-stu-id="7b9a9-109">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="7b9a9-110">Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="7b9a9-110">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="7b9a9-111">Publicado por</span><span class="sxs-lookup"><span data-stu-id="7b9a9-111">Published By</span></span>

<span data-ttu-id="7b9a9-112">Este ControlEvent, lo publica el instalador.</span><span class="sxs-lookup"><span data-stu-id="7b9a9-112">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="7b9a9-113">Argumento</span><span class="sxs-lookup"><span data-stu-id="7b9a9-113">Argument</span></span>

<span data-ttu-id="7b9a9-114">Cuadro de diálogo en la [tabla del cuadro de diálogo](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="7b9a9-114">A dialog box in the [Dialog table](dialog-table.md).</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="7b9a9-115">Acción en los suscriptores</span><span class="sxs-lookup"><span data-stu-id="7b9a9-115">Action on Subscribers</span></span>

<span data-ttu-id="7b9a9-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7b9a9-116">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="7b9a9-117">Uso típico</span><span class="sxs-lookup"><span data-stu-id="7b9a9-117">Typical Use</span></span>

<span data-ttu-id="7b9a9-118">SpawnWaitDialog ControlEvent, se puede usar para esperar a cualquier tarea en segundo plano la finalización de la que se puede probar mediante una expresión condicional como el estado de una propiedad.</span><span class="sxs-lookup"><span data-stu-id="7b9a9-118">The SpawnWaitDialog ControlEvent can be used to wait for any background task the completion of which can be tested using a conditional expression such as the state of a property.</span></span> <span data-ttu-id="7b9a9-119">Para obtener un ejemplo del uso de SpawnWaitDialog ControlEvent,, consulte la sección [creación de una instrucción condicional "Wait..." Cuadro de mensaje](authoring-a-conditional-please-wait-------message-box.md).</span><span class="sxs-lookup"><span data-stu-id="7b9a9-119">For an example of using the SpawnWaitDialog ControlEvent, see the section [Authoring a Conditional "Please wait . . ." Message Box](authoring-a-conditional-please-wait-------message-box.md).</span></span>

 

 



