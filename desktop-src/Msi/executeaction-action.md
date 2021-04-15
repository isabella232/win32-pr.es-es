---
description: La acción ExecuteAction inicia la secuencia de ejecución mediante la propiedad EXECUTEACTION para determinar el tipo de instalación que se va a realizar.
ms.assetid: 61878317-ac87-4f6e-9375-12a78969e29e
title: Acción ExecuteAction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2970a0fb4e9297264071769ac7415cd2acf866b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497794"
---
# <a name="executeaction-action"></a><span data-ttu-id="eea50-103">Acción ExecuteAction</span><span class="sxs-lookup"><span data-stu-id="eea50-103">ExecuteAction Action</span></span>

<span data-ttu-id="eea50-104">La acción ExecuteAction inicia la secuencia de ejecución mediante la propiedad [**ExecuteAction**](executeaction.md) para determinar el tipo de instalación que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="eea50-104">The ExecuteAction action initiates the execution sequence using the [**EXECUTEACTION**](executeaction.md) property to determine which type of installation to perform.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="eea50-105">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="eea50-105">Sequence Restrictions</span></span>

<span data-ttu-id="eea50-106">Esta acción se debe secuenciar después de que se complete toda la recopilación de información necesaria para iniciar la instalación.</span><span class="sxs-lookup"><span data-stu-id="eea50-106">This action should be sequenced after all information collection necessary to begin the installation is complete.</span></span> <span data-ttu-id="eea50-107">Se pueden secuenciar acciones adicionales después de la acción ExecuteAction en la [tabla InstallUISequence](installuisequence-table.md)y la [tabla AdminUISequence](adminuisequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="eea50-107">Additional actions may be sequenced after ExecuteAction action in the [InstallUISequence table](installuisequence-table.md), and [AdminUISequence table](adminuisequence-table.md).</span></span> <span data-ttu-id="eea50-108">Normalmente, una secuencia comienza con acciones de [*costo*](c-gly.md) , como la [acción CostInitialize](costinitialize-action.md), seguida de las acciones de la interfaz de usuario y, a continuación, la acción ExecuteAction.</span><span class="sxs-lookup"><span data-stu-id="eea50-108">A sequence will typically begin with [*costing*](c-gly.md) actions, such as the [CostInitialize action](costinitialize-action.md), followed by the user interface actions, and then the ExecuteAction action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="eea50-109">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="eea50-109">ActionData Messages</span></span>

<span data-ttu-id="eea50-110">No hay mensajes ActionData.</span><span class="sxs-lookup"><span data-stu-id="eea50-110">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="eea50-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eea50-111">Remarks</span></span>

<span data-ttu-id="eea50-112">La acción ExecuteAction se ejecuta con privilegios del sistema si está habilitado el servicio de instalador.</span><span class="sxs-lookup"><span data-stu-id="eea50-112">The ExecuteAction action is run with system privileges if the installer service is enabled.</span></span> <span data-ttu-id="eea50-113">Las acciones de nivel superior, como la [acción de instalación](install-action.md), la [acción de anuncio](advertise-action.md)y la acción de [Administrador](admin-action.md) incluyen lógica interna que determina si la llamada a la acción de ExecuteAction requiere la secuencia de ejecución o la secuencia de interfaz de usuario para ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="eea50-113">The top-level actions, such as the [INSTALL action](install-action.md), [ADVERTISE action](advertise-action.md), and [ADMIN action](admin-action.md) include internal logic that determines whether calling the ExecuteAction action requires either the execution sequence or the user interface sequence to run.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eea50-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="eea50-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eea50-115">Tabla InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="eea50-115">InstallUISequence table</span></span>](installuisequence-table.md)
</dt> <dt>

[<span data-ttu-id="eea50-116">Tabla AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="eea50-116">AdminUISequence table</span></span>](adminuisequence-table.md)
</dt> <dt>

[<span data-ttu-id="eea50-117">Acción CostInitialize</span><span class="sxs-lookup"><span data-stu-id="eea50-117">CostInitialize action</span></span>](costinitialize-action.md)
</dt> </dl>

 

 



