---
description: La acción CostFinalize finaliza el proceso de costo de instalación interna Iniciado por la acción CostInitialize.
ms.assetid: ae69ad03-5acc-4a62-ba71-3a4e477d34ab
title: Acción CostFinalize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a5423f1050f9c9d755d33e492b9b65cfcaa08b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669681"
---
# <a name="costfinalize-action"></a><span data-ttu-id="a9965-103">Acción CostFinalize</span><span class="sxs-lookup"><span data-stu-id="a9965-103">CostFinalize Action</span></span>

<span data-ttu-id="a9965-104">La acción CostFinalize finaliza el proceso de [*costo*](c-gly.md) de instalación interna Iniciado por la acción [CostInitialize](costinitialize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="a9965-104">The CostFinalize action ends the internal installation [*costing*](c-gly.md) process begun by the [CostInitialize](costinitialize-action.md) action.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="a9965-105">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="a9965-105">Sequence Restrictions</span></span>

<span data-ttu-id="a9965-106">Cualquier acción estándar o [personalizada](custom-actions.md) que afecte a los costos se debe secuenciar antes de la acción [CostInitialize](costinitialize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="a9965-106">Any standard or [custom actions](custom-actions.md) that affect costing should be sequenced before the [CostInitialize](costinitialize-action.md) action.</span></span> <span data-ttu-id="a9965-107">Llame a la acción [FileCost](filecost-action.md) inmediatamente después de la acción CostInitialize y, a continuación, llame a la acción CostFinalize para que todos los cálculos de costos finales estén disponibles para el instalador a través de la tabla de [componentes](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="a9965-107">Call the [FileCost](filecost-action.md) action immediately following the CostInitialize action and then call the CostFinalize action to make all final cost calculations available to the installer through the [Component](component-table.md) table.</span></span>

<span data-ttu-id="a9965-108">La acción CostFinalize se debe ejecutar antes de iniciar cualquier secuencia de interfaz de usuario que permita al usuario ver o modificar los directorios o las selecciones de las tablas de [características](feature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="a9965-108">The CostFinalize action must be executed before starting any user interface sequence which allows the user to view or modify [Feature](feature-table.md) table selections or directories.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="a9965-109">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="a9965-109">ActionData Messages</span></span>

<span data-ttu-id="a9965-110">No hay mensajes ActionData.</span><span class="sxs-lookup"><span data-stu-id="a9965-110">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9965-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a9965-111">Remarks</span></span>

<span data-ttu-id="a9965-112">La acción CostFinalize consulta la tabla de [condiciones](condition-table.md) para determinar qué características están programadas para instalarse.</span><span class="sxs-lookup"><span data-stu-id="a9965-112">The CostFinalize action queries the [Condition](condition-table.md) table to determine which features are scheduled to be installed.</span></span> <span data-ttu-id="a9965-113">El costo se realiza para cada componente de la tabla de [componentes](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="a9965-113">Costing is done for each component in the [Component](component-table.md) table.</span></span>

<span data-ttu-id="a9965-114">La acción CostFinalize también comprueba que se puedan escribir todos los directorios de destino antes de permitir que continúe la instalación.</span><span class="sxs-lookup"><span data-stu-id="a9965-114">The CostFinalize action also verifies that all the target directories are writable before allowing the installation to continue.</span></span>

> [!Note]  
> <span data-ttu-id="a9965-115">Durante una [instalación administrativa](administrative-installation.md), CostFinalize establece todas las características para la instalación, excepto las características que tienen 0 creado en la columna LEVEL de la [tabla de características](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="a9965-115">During an [administrative installation](administrative-installation.md), CostFinalize sets all features for installation except features having 0 authored in the Level column of the [Feature table](feature-table.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a9965-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a9965-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9965-117">Costo de archivos</span><span class="sxs-lookup"><span data-stu-id="a9965-117">File Costing</span></span>](file-costing.md)
</dt> </dl>

 

 



