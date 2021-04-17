---
description: ICE44 valida que NewDialog, SpawnDialog y SpawnWaitDialog ControlEvents hacen referencia a cuadros de diálogo válidos en la tabla del cuadro de diálogo.
ms.assetid: 401bae25-a361-45f6-af3f-0f31be463c84
title: ICE44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16354ac435979d830ff14c33a846e97757b64962
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667752"
---
# <a name="ice44"></a><span data-ttu-id="6d32d-103">ICE44</span><span class="sxs-lookup"><span data-stu-id="6d32d-103">ICE44</span></span>

<span data-ttu-id="6d32d-104">ICE44 valida que [NewDialog](newdialog-controlevent.md), [SpawnDialog](spawndialog-controlevent.md)y [SpawnWaitDialog](spawnwaitdialog-controlevent.md) ControlEvents hacen referencia a cuadros de diálogo válidos en la tabla del [cuadro de diálogo](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="6d32d-104">ICE44 validates that the [NewDialog](newdialog-controlevent.md), [SpawnDialog](spawndialog-controlevent.md), and [SpawnWaitDialog](spawnwaitdialog-controlevent.md) ControlEvents reference valid dialog boxes in the [Dialog table](dialog-table.md).</span></span>

## <a name="result"></a><span data-ttu-id="6d32d-105">Resultado</span><span class="sxs-lookup"><span data-stu-id="6d32d-105">Result</span></span>

<span data-ttu-id="6d32d-106">ICE44 envía un mensaje de error si hay un evento de control de diálogo que no hace referencia a un cuadro de diálogo que aparece en la tabla del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="6d32d-106">ICE44 posts an error message if there is a dialog control event that does not reference a dialog box listed in the Dialog table.</span></span>

## <a name="example"></a><span data-ttu-id="6d32d-107">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6d32d-107">Example</span></span>

<span data-ttu-id="6d32d-108">ICE44 notificaría los siguientes errores para el ejemplo que se muestra.</span><span class="sxs-lookup"><span data-stu-id="6d32d-108">ICE44 would report the following errors for the example shown.</span></span>



| <span data-ttu-id="6d32d-109">Error ICE44</span><span class="sxs-lookup"><span data-stu-id="6d32d-109">ICE44 error</span></span>                                                                                                                               | <span data-ttu-id="6d32d-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="6d32d-110">Description</span></span>                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d32d-111">Evento de control para el control ' Dialog1 '. ' Control1 ' es de tipo SpawnDialog, pero su argumento Dialog2 no es una entrada válida en la tabla del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="6d32d-111">Control Event for Control 'Dialog1'.'Control1' is of type SpawnDialog, but its argument Dialog2 is not a valid entry in the Dialog Table.</span></span> | <span data-ttu-id="6d32d-112">Hay una acción SpawnDialog, SpawnWaitDialog o NewDialog que tiene un argumento que no hace referencia a un cuadro de diálogo en la tabla del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="6d32d-112">There is a SpawnDialog, SpawnWaitDialog, or NewDialog actions that has an argument that does not refer to a dialog box in the Dialog table.</span></span> <span data-ttu-id="6d32d-113">Para corregir este error, agregue un argumento que sea una clave en la tabla del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="6d32d-113">To fix this error, add an argument that is a key in the Dialog Table.</span></span><br/> |



 

<span data-ttu-id="6d32d-114">[Tabla de cuadro de diálogo](dialog-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="6d32d-114">[Dialog Table](dialog-table.md) (partial)</span></span>



| <span data-ttu-id="6d32d-115">Diálogo</span><span class="sxs-lookup"><span data-stu-id="6d32d-115">Dialog</span></span>  | <span data-ttu-id="6d32d-116">Title</span><span class="sxs-lookup"><span data-stu-id="6d32d-116">Title</span></span> |
|---------|-------|
| <span data-ttu-id="6d32d-117">Dialog1</span><span class="sxs-lookup"><span data-stu-id="6d32d-117">Dialog1</span></span> |       |



 

<span data-ttu-id="6d32d-118">[Tabla ControlEvent,](controlevent-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="6d32d-118">[ControlEvent Table](controlevent-table.md) (partial)</span></span>



| <span data-ttu-id="6d32d-119">Diálogo\_</span><span class="sxs-lookup"><span data-stu-id="6d32d-119">Dialog\_</span></span> | <span data-ttu-id="6d32d-120">control\_</span><span class="sxs-lookup"><span data-stu-id="6d32d-120">Control\_</span></span> | <span data-ttu-id="6d32d-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="6d32d-121">Type</span></span>        | <span data-ttu-id="6d32d-122">Argumento</span><span class="sxs-lookup"><span data-stu-id="6d32d-122">Argument</span></span> |
|----------|-----------|-------------|----------|
| <span data-ttu-id="6d32d-123">Dialog1</span><span class="sxs-lookup"><span data-stu-id="6d32d-123">Dialog1</span></span>  | <span data-ttu-id="6d32d-124">Control1</span><span class="sxs-lookup"><span data-stu-id="6d32d-124">Control1</span></span>  | <span data-ttu-id="6d32d-125">SpawnDialog</span><span class="sxs-lookup"><span data-stu-id="6d32d-125">SpawnDialog</span></span> | <span data-ttu-id="6d32d-126">Dialog2</span><span class="sxs-lookup"><span data-stu-id="6d32d-126">Dialog2</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="6d32d-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6d32d-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d32d-128">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="6d32d-128">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




