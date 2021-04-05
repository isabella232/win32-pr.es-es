---
description: ICE63 comprueba la secuenciación correcta de la acción RemoveExistingProducts.
ms.assetid: 4dd67bb0-c08a-4a44-b687-0394a3afc2c4
title: ICE63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5faa6f2ddbcb95cdf12966c2887fe9438a5d610
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911337"
---
# <a name="ice63"></a><span data-ttu-id="97967-103">ICE63</span><span class="sxs-lookup"><span data-stu-id="97967-103">ICE63</span></span>

<span data-ttu-id="97967-104">ICE63 comprueba la secuenciación correcta de la [acción RemoveExistingProducts](removeexistingproducts-action.md).</span><span class="sxs-lookup"><span data-stu-id="97967-104">ICE63 checks for proper sequencing of the [RemoveExistingProducts action](removeexistingproducts-action.md).</span></span> <span data-ttu-id="97967-105">La acción RemoveExistingProducts se puede colocar:</span><span class="sxs-lookup"><span data-stu-id="97967-105">The RemoveExistingProducts action may be placed:</span></span>

1.  <span data-ttu-id="97967-106">Entre InstallValidate y InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="97967-106">Between InstallValidate and InstallInitialize</span></span>
2.  <span data-ttu-id="97967-107">Inmediatamente después de InstallInitialize o después de InstallInitialize si las acciones entre InstallInitialize y RemoveExistingProducts no generan ninguna acción de script.</span><span class="sxs-lookup"><span data-stu-id="97967-107">Immediately after InstallInitialize, or after InstallInitialize if the actions between InstallInitialize and RemoveExistingProducts do not generate any script actions.</span></span>
3.  <span data-ttu-id="97967-108">Inmediatamente después de InstallExecute o InstallExecuteAgain y antes de InstallFinalize (se aplica la misma restricción que antes).</span><span class="sxs-lookup"><span data-stu-id="97967-108">Immediately after InstallExecute or InstallExecuteAgain and before InstallFinalize (the same restriction as above applies).</span></span>
4.  <span data-ttu-id="97967-109">Después de InstallFinalize.</span><span class="sxs-lookup"><span data-stu-id="97967-109">After InstallFinalize.</span></span>

<span data-ttu-id="97967-110">Si no se corrige una advertencia o un error informados por ICE63, se producirá un error en la actualización.</span><span class="sxs-lookup"><span data-stu-id="97967-110">Failure to fix a warning or error reported by ICE63 leads to failure of the upgrade.</span></span>

## <a name="result"></a><span data-ttu-id="97967-111">Resultado</span><span class="sxs-lookup"><span data-stu-id="97967-111">Result</span></span>

<span data-ttu-id="97967-112">ICE63 expone una advertencia o un error si la secuenciación de la acción RemoveExistingProducts no es correcta.</span><span class="sxs-lookup"><span data-stu-id="97967-112">ICE63 posts a warning or error if the sequencing of the RemoveExistingProducts action is not correct.</span></span>

## <a name="example"></a><span data-ttu-id="97967-113">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="97967-113">Example</span></span>

<span data-ttu-id="97967-114">ICE63 notifica el siguiente error para el ejemplo que se muestra.</span><span class="sxs-lookup"><span data-stu-id="97967-114">ICE63 reports the following error for the example shown.</span></span>

``` syntax
WARNING: Some action falls between InstallInitialize and RemoveExistingProducts.
```

<span data-ttu-id="97967-115">La acción "MyCustomAction" se produce entre InstallInitialize y RemoveExistingProducts.</span><span class="sxs-lookup"><span data-stu-id="97967-115">The action 'MyCustomAction' occurs between InstallInitialize and RemoveExistingProducts.</span></span> <span data-ttu-id="97967-116">Si MyCustomAction genera acciones en el script, esto provoca problemas en la instalación.</span><span class="sxs-lookup"><span data-stu-id="97967-116">If MyCustomAction generates any actions in the script, this causes problems in the installation.</span></span>

<span data-ttu-id="97967-117">Para corregir este error, compruebe que MyCustomAction no genera ninguna acción de script ni resecuenciar las acciones.</span><span class="sxs-lookup"><span data-stu-id="97967-117">To fix this error, verify that MyCustomAction does not generate any script actions or resequence the actions.</span></span>

[<span data-ttu-id="97967-118">Tabla InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="97967-118">InstallExecuteSequence Table</span></span>](installexecutesequence-table.md)



| <span data-ttu-id="97967-119">Acción</span><span class="sxs-lookup"><span data-stu-id="97967-119">Action</span></span>                 | <span data-ttu-id="97967-120">Condición</span><span class="sxs-lookup"><span data-stu-id="97967-120">Condition</span></span> | <span data-ttu-id="97967-121">Secuencia</span><span class="sxs-lookup"><span data-stu-id="97967-121">Sequence</span></span> |
|------------------------|-----------|----------|
| <span data-ttu-id="97967-122">InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="97967-122">InstallInitialize</span></span>      |           | <span data-ttu-id="97967-123">1000</span><span class="sxs-lookup"><span data-stu-id="97967-123">1000</span></span>     |
| <span data-ttu-id="97967-124">MyCustomAction</span><span class="sxs-lookup"><span data-stu-id="97967-124">MyCustomAction</span></span>         |           | <span data-ttu-id="97967-125">1010</span><span class="sxs-lookup"><span data-stu-id="97967-125">1010</span></span>     |
| <span data-ttu-id="97967-126">RemoveExistingProducts</span><span class="sxs-lookup"><span data-stu-id="97967-126">RemoveExistingProducts</span></span> |           | <span data-ttu-id="97967-127">1020</span><span class="sxs-lookup"><span data-stu-id="97967-127">1020</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="97967-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="97967-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97967-129">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="97967-129">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



