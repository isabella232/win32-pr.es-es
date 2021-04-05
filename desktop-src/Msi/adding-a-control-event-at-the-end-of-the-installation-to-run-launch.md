---
description: El instalador ejecuta la secuencia del Asistente para la instalación de ejemplo solo si se usa el nivel de interfaz de usuario completo para instalar la aplicación.
ms.assetid: 323d62ae-333b-49fd-96a1-55b228c8ab2c
title: Agregar un evento de control al final de la instalación para ejecutar el inicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 545901c4cfd0936f63078d5ad56586022fb4ec4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001763"
---
# <a name="adding-a-control-event-at-the-end-of-the-installation-to-run-launch"></a><span data-ttu-id="68384-103">Agregar un evento de control al final de la instalación para ejecutar el inicio</span><span class="sxs-lookup"><span data-stu-id="68384-103">Adding a Control Event at the End of the Installation to Run Launch</span></span>

<span data-ttu-id="68384-104">El instalador ejecuta la secuencia del Asistente para la instalación de ejemplo solo si se usa el nivel de [*interfaz de usuario completo*](f-gly.md) para instalar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="68384-104">The installer runs the sample's installation wizard sequence only if the [*full UI*](f-gly.md) level is used to install the application.</span></span> <span data-ttu-id="68384-105">El último cuadro de diálogo de la secuencia de diálogo de ejemplo es un cuadro de [diálogo de salida](exit-dialog.md) denominado ExitDialog.</span><span class="sxs-lookup"><span data-stu-id="68384-105">The last dialog box of the sample dialog sequence is an [Exit Dialog](exit-dialog.md) named ExitDialog.</span></span> <span data-ttu-id="68384-106">Cuando un usuario interactúa con el botón Aceptar en ExitDialog, primero publica un [ControlEvent, EndDialog](enddialog-controlevent.md) que devuelve el control al instalador.</span><span class="sxs-lookup"><span data-stu-id="68384-106">When a user interacts with the OK button on ExitDialog, this first publishes an [EndDialog ControlEvent](enddialog-controlevent.md) that returns control to the installer.</span></span> <span data-ttu-id="68384-107">Después, el control publica una [ControlEvent, de acción](doaction-controlevent.md) que ejecuta la acción personalizada Launch.</span><span class="sxs-lookup"><span data-stu-id="68384-107">The control then publishes a [DoAction ControlEvent](doaction-controlevent.md) that runs the Launch custom action.</span></span> <span data-ttu-id="68384-108">Cada evento de control requiere un registro en la [tabla ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="68384-108">Each control event requires a record in the [ControlEvent table](controlevent-table.md).</span></span> <span data-ttu-id="68384-109">Consulte [información general de ControlEvent,](controlevent-overview.md).</span><span class="sxs-lookup"><span data-stu-id="68384-109">See [ControlEvent Overview](controlevent-overview.md).</span></span>

[<span data-ttu-id="68384-110">Tabla ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="68384-110">ControlEvent Table</span></span>](controlevent-table.md)



| <span data-ttu-id="68384-111">Diálogo</span><span class="sxs-lookup"><span data-stu-id="68384-111">Dialog</span></span>     | <span data-ttu-id="68384-112">control\_</span><span class="sxs-lookup"><span data-stu-id="68384-112">Control\_</span></span> | <span data-ttu-id="68384-113">Evento</span><span class="sxs-lookup"><span data-stu-id="68384-113">Event</span></span>     | <span data-ttu-id="68384-114">Argumento</span><span class="sxs-lookup"><span data-stu-id="68384-114">Argument</span></span> | <span data-ttu-id="68384-115">Condición</span><span class="sxs-lookup"><span data-stu-id="68384-115">Condition</span></span>                     | <span data-ttu-id="68384-116">Ordenación</span><span class="sxs-lookup"><span data-stu-id="68384-116">Ordering</span></span> |
|------------|-----------|-----------|----------|-------------------------------|----------|
| <span data-ttu-id="68384-117">ExitDialog</span><span class="sxs-lookup"><span data-stu-id="68384-117">ExitDialog</span></span> | <span data-ttu-id="68384-118">Aceptar</span><span class="sxs-lookup"><span data-stu-id="68384-118">OK</span></span>        | <span data-ttu-id="68384-119">EndDialog</span><span class="sxs-lookup"><span data-stu-id="68384-119">EndDialog</span></span> | <span data-ttu-id="68384-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="68384-120">Return</span></span>   | <span data-ttu-id="68384-121">1</span><span class="sxs-lookup"><span data-stu-id="68384-121">1</span></span>                             | <span data-ttu-id="68384-122">1</span><span class="sxs-lookup"><span data-stu-id="68384-122">1</span></span>        |
| <span data-ttu-id="68384-123">ExitDialog</span><span class="sxs-lookup"><span data-stu-id="68384-123">ExitDialog</span></span> | <span data-ttu-id="68384-124">Aceptar</span><span class="sxs-lookup"><span data-stu-id="68384-124">OK</span></span>        | <span data-ttu-id="68384-125">DoAction</span><span class="sxs-lookup"><span data-stu-id="68384-125">DoAction</span></span>  | <span data-ttu-id="68384-126">Launch</span><span class="sxs-lookup"><span data-stu-id="68384-126">Launch</span></span>   | <span data-ttu-id="68384-127">NO instalado y $Tutorial = 3</span><span class="sxs-lookup"><span data-stu-id="68384-127">NOT Installed AND $Tutorial=3</span></span> | <span data-ttu-id="68384-128">2</span><span class="sxs-lookup"><span data-stu-id="68384-128">2</span></span>        |



 

<span data-ttu-id="68384-129">La condición en el control de la acción garantiza que la acción personalizada se ejecute solo durante la primera instalación de la aplicación y que se instale localmente.</span><span class="sxs-lookup"><span data-stu-id="68384-129">The condition on the DoAction control ensures the custom action only runs during the first installation of the application and that it is being installed locally.</span></span> <span data-ttu-id="68384-130">La frase $Tutorial = 3 significa que el estado de acción del componente tutorial está establecido en local.</span><span class="sxs-lookup"><span data-stu-id="68384-130">The phrase $Tutorial=3 means the action state of the Tutorial component is set to local.</span></span> <span data-ttu-id="68384-131">Consulte [Sintaxis de la instrucción condicional](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="68384-131">See [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

<span data-ttu-id="68384-132">Esto completa el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="68384-132">This completes the sample.</span></span>

 

 



