---
description: ICE28 se usa normalmente para validar que la acción ForceReboot se coloca antes o después y nunca dentro de un grupo específico de acciones en las tablas de secuencia de acciones. Consulte el tema de la acción ForceReboot para determinar las acciones que componen este grupo.
ms.assetid: 746d907a-33e1-479a-bcb0-93e7fd5dd975
title: ICE28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc65878bdc3db4f9b79ba95b4a170b694a4728ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808749"
---
# <a name="ice28"></a><span data-ttu-id="3cbdb-104">ICE28</span><span class="sxs-lookup"><span data-stu-id="3cbdb-104">ICE28</span></span>

<span data-ttu-id="3cbdb-105">ICE28 se usa normalmente para validar que la acción ForceReboot se coloca antes o después y nunca dentro de un grupo específico de acciones en las tablas de secuencia de acciones.</span><span class="sxs-lookup"><span data-stu-id="3cbdb-105">ICE28 is commonly used to validate that the ForceReboot action is placed before or after, and never within, a specific group of actions in the action sequence tables.</span></span> <span data-ttu-id="3cbdb-106">Consulte el tema de la [acción ForceReboot](forcereboot-action.md) para determinar las acciones que componen este grupo.</span><span class="sxs-lookup"><span data-stu-id="3cbdb-106">See the [ForceReboot action](forcereboot-action.md) topic to determine the actions that comprise this group.</span></span>

<span data-ttu-id="3cbdb-107">ICE28 valida las acciones en las siguientes tablas de secuencia:</span><span class="sxs-lookup"><span data-stu-id="3cbdb-107">ICE28 validates actions in the following sequence tables:</span></span>

[<span data-ttu-id="3cbdb-108">Tabla AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="3cbdb-108">AdminUISequence table</span></span>](adminuisequence-table.md)

[<span data-ttu-id="3cbdb-109">Tabla AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="3cbdb-109">AdminExecuteSequence table</span></span>](adminexecutesequence-table.md)

[<span data-ttu-id="3cbdb-110">Tabla InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="3cbdb-110">InstallUISequence table</span></span>](installuisequence-table.md)

[<span data-ttu-id="3cbdb-111">Tabla InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="3cbdb-111">InstallExecuteSequence table</span></span>](installexecutesequence-table.md)

## <a name="result"></a><span data-ttu-id="3cbdb-112">Resultado</span><span class="sxs-lookup"><span data-stu-id="3cbdb-112">Result</span></span>

<span data-ttu-id="3cbdb-113">ICE28 envía un mensaje de error si ForceReboot se secuencia en el grupo de acciones especificado.</span><span class="sxs-lookup"><span data-stu-id="3cbdb-113">ICE28 posts an error message if ForceReboot is sequenced within the specified action group.</span></span>

## <a name="example"></a><span data-ttu-id="3cbdb-114">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3cbdb-114">Example</span></span>

<span data-ttu-id="3cbdb-115">En el ejemplo mostrado, ICE28 envía el mensaje de error siguiente:</span><span class="sxs-lookup"><span data-stu-id="3cbdb-115">For the example shown, ICE28 posts the following error message:</span></span>

``` syntax
Action: 'ForceReboot' of table InstallExecuteSequence is not permitted in the range 5 to 15 because it cannot separate a set of actions contained in this range.
```

[<span data-ttu-id="3cbdb-116">Tabla InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="3cbdb-116">InstallExecuteSequence Table</span></span>](installexecutesequence-table.md)



| <span data-ttu-id="3cbdb-117">Acción</span><span class="sxs-lookup"><span data-stu-id="3cbdb-117">Action</span></span>             | <span data-ttu-id="3cbdb-118">Secuencia</span><span class="sxs-lookup"><span data-stu-id="3cbdb-118">Sequence</span></span> |
|--------------------|----------|
| <span data-ttu-id="3cbdb-119">ForceReboot</span><span class="sxs-lookup"><span data-stu-id="3cbdb-119">ForceReboot</span></span>        | <span data-ttu-id="3cbdb-120">10</span><span class="sxs-lookup"><span data-stu-id="3cbdb-120">10</span></span>       |
| <span data-ttu-id="3cbdb-121">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="3cbdb-121">RegisterMIMEInfo</span></span>   |   <span data-ttu-id="3cbdb-122">5</span><span class="sxs-lookup"><span data-stu-id="3cbdb-122">5</span></span>      |
| <span data-ttu-id="3cbdb-123">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="3cbdb-123">RegisterProgIdInfo</span></span> | <span data-ttu-id="3cbdb-124">15</span><span class="sxs-lookup"><span data-stu-id="3cbdb-124">15</span></span>       |



 

<span data-ttu-id="3cbdb-125">El número de secuencia de 10 que se proporciona a las interrupciones de ForceReboot genera el error, porque se encuentra entre los números de secuencia de RegisterMIMEInfo y RegisterProgIdInfo.</span><span class="sxs-lookup"><span data-stu-id="3cbdb-125">The sequence number of 10 given to ForceReboot breaks generates the error, because it comes between the sequence numbers of RegisterMIMEInfo and RegisterProgIdInfo.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3cbdb-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3cbdb-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3cbdb-127">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="3cbdb-127">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



