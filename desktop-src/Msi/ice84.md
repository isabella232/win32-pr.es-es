---
description: ICE84 comprueba la tabla AdvtExecuteSequence, la tabla AdminExecuteSequence y la tabla InstallExecuteSequence para comprobar que no se han establecido las siguientes acciones estándar con condiciones en el campo condición.
ms.assetid: 0d1bbf4b-ffab-409e-a292-891dfa823433
title: ICE84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8960f53f5a01e9bec95a02bb3241487aa31aaae5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361154"
---
# <a name="ice84"></a><span data-ttu-id="3e829-103">ICE84</span><span class="sxs-lookup"><span data-stu-id="3e829-103">ICE84</span></span>

<span data-ttu-id="3e829-104">ICE84 comprueba la tabla [AdvtExecuteSequence](advtexecutesequence-table.md), la [tabla AdminExecuteSequence](adminexecutesequence-table.md)y la [tabla InstallExecuteSequence](installexecutesequence-table.md) para comprobar que no se han establecido las siguientes [acciones estándar](standard-actions.md) con condiciones en el campo condición.</span><span class="sxs-lookup"><span data-stu-id="3e829-104">ICE84 checks the [AdvtExecuteSequence table](advtexecutesequence-table.md), [AdminExecuteSequence table](adminexecutesequence-table.md), and the [InstallExecuteSequence table](installexecutesequence-table.md) to verify that the following [standard actions](standard-actions.md) have not been set with conditions in the Condition field.</span></span>

-   [<span data-ttu-id="3e829-105">Acción CostInitialize</span><span class="sxs-lookup"><span data-stu-id="3e829-105">CostInitialize action</span></span>](costinitialize-action.md)
-   [<span data-ttu-id="3e829-106">Acción CostFinalize</span><span class="sxs-lookup"><span data-stu-id="3e829-106">CostFinalize action</span></span>](costfinalize-action.md)
-   [<span data-ttu-id="3e829-107">Acción FileCost</span><span class="sxs-lookup"><span data-stu-id="3e829-107">FileCost action</span></span>](filecost-action.md)
-   [<span data-ttu-id="3e829-108">Acción InstallValidate</span><span class="sxs-lookup"><span data-stu-id="3e829-108">InstallValidate action</span></span>](installvalidate-action.md)
-   [<span data-ttu-id="3e829-109">Acción InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="3e829-109">InstallInitialize action</span></span>](installinitialize-action.md)
-   [<span data-ttu-id="3e829-110">Acción InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="3e829-110">InstallFinalize action</span></span>](installfinalize-action.md)
-   [<span data-ttu-id="3e829-111">Acción ProcessComponents</span><span class="sxs-lookup"><span data-stu-id="3e829-111">ProcessComponents action</span></span>](processcomponents-action.md)
-   [<span data-ttu-id="3e829-112">Acción PublishFeatures</span><span class="sxs-lookup"><span data-stu-id="3e829-112">PublishFeatures action</span></span>](publishfeatures-action.md)
-   [<span data-ttu-id="3e829-113">Acción PublishProduct</span><span class="sxs-lookup"><span data-stu-id="3e829-113">PublishProduct action</span></span>](publishproduct-action.md)
-   [<span data-ttu-id="3e829-114">Acción RegisterProduct</span><span class="sxs-lookup"><span data-stu-id="3e829-114">RegisterProduct action</span></span>](registerproduct-action.md)
-   [<span data-ttu-id="3e829-115">Acción UnpublishFeatures</span><span class="sxs-lookup"><span data-stu-id="3e829-115">UnpublishFeatures action</span></span>](unpublishfeatures-action.md)

<span data-ttu-id="3e829-116">Si se encuentran condiciones, ICE84 publica una advertencia.</span><span class="sxs-lookup"><span data-stu-id="3e829-116">If conditions are found, ICE84 posts a warning.</span></span>

## <a name="result"></a><span data-ttu-id="3e829-117">Resultado</span><span class="sxs-lookup"><span data-stu-id="3e829-117">Result</span></span>

<span data-ttu-id="3e829-118">ICE84 envía la siguiente advertencia.</span><span class="sxs-lookup"><span data-stu-id="3e829-118">ICE84 posts the following warning.</span></span>



| <span data-ttu-id="3e829-119">Error ICE84</span><span class="sxs-lookup"><span data-stu-id="3e829-119">ICE84 error</span></span>                                                             | <span data-ttu-id="3e829-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="3e829-120">Description</span></span>                                           |
|-------------------------------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="3e829-121">La acción ' \[ 1 ' que se \] encuentra en la tabla% s es una acción necesaria con una condición.</span><span class="sxs-lookup"><span data-stu-id="3e829-121">Action '\[1\]' found in %s table is a required action with a condition.</span></span> | <span data-ttu-id="3e829-122">Se ha creado una acción necesaria con una condición.</span><span class="sxs-lookup"><span data-stu-id="3e829-122">A required action has been authored with a condition.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="3e829-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3e829-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e829-124">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="3e829-124">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



