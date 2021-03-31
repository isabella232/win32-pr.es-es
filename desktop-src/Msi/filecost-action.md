---
description: FileCostaction inicia las acciones de instalación estándar de forma dinámica.
ms.assetid: 1b3f2baf-6191-452e-955d-8ac903edc1b7
title: Acción FileCost
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b9d87cb73353ef80f956ce13ec1940f1a4adee2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083505"
---
# <a name="filecost-action"></a><span data-ttu-id="ade9e-103">Acción FileCost</span><span class="sxs-lookup"><span data-stu-id="ade9e-103">FileCost Action</span></span>

<span data-ttu-id="ade9e-104">FileCostaction inicia el [*costo*](c-gly.md)dinámico de las acciones de instalación estándar.</span><span class="sxs-lookup"><span data-stu-id="ade9e-104">The FileCostaction initiates dynamic [*costing*](c-gly.md)of standard installation actions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="ade9e-105">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="ade9e-105">ActionData Messages</span></span>

<span data-ttu-id="ade9e-106">No hay mensajes ActionData.</span><span class="sxs-lookup"><span data-stu-id="ade9e-106">There are no ActionData messages.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="ade9e-107">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="ade9e-107">Sequence Restrictions</span></span>

<span data-ttu-id="ade9e-108">Cualquier acción estándar o [personalizada](custom-actions.md) que afecte a los costos se debe secuenciar antes de la acción [CostInitialize](costinitialize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="ade9e-108">Any standard or [custom actions](custom-actions.md) that affect costing should sequenced before the [CostInitialize](costinitialize-action.md) action.</span></span> <span data-ttu-id="ade9e-109">Llame a la acción FileCost inmediatamente después de la acción CostInitialize.</span><span class="sxs-lookup"><span data-stu-id="ade9e-109">Call the FileCost action immediately following the CostInitialize action.</span></span> <span data-ttu-id="ade9e-110">Después, llame a la acción [CostFinalize](costfinalize-action.md) que sigue a la acción CostInitialize para que todos los cálculos de costos finales estén disponibles para el instalador a través de la tabla de [componentes](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="ade9e-110">Then call the [CostFinalize](costfinalize-action.md) action following the CostInitialize action to make all final cost calculations available to the installer through the [Component](component-table.md) table.</span></span>

<span data-ttu-id="ade9e-111">La acción [CostInitialize](costinitialize-action.md) se debe ejecutar antes de la acción FileCost.</span><span class="sxs-lookup"><span data-stu-id="ade9e-111">The [CostInitialize](costinitialize-action.md) action must be executed before the FileCost action.</span></span> <span data-ttu-id="ade9e-112">A continuación, el instalador determina el costo de espacio en disco de todos los archivos de la tabla de [archivos](file-table.md) , en función de cada componente (consulte [tabla de componentes](component-table.md)), que realiza la agrupación en clústeres de [*volúmenes*](v-gly.md) y la presencia de archivos existentes que es posible que deban sobrescribirse en la cuenta.</span><span class="sxs-lookup"><span data-stu-id="ade9e-112">The installer then determines the disk-space cost of every file in the [File](file-table.md) table, on a per-component basis (See [Component Table](component-table.md)), taking both [*volume*](v-gly.md) clustering and the presence of existing files that may need to be overwritten into account.</span></span> <span data-ttu-id="ade9e-113">También se consideran todas las acciones que consumen o liberan espacio en disco.</span><span class="sxs-lookup"><span data-stu-id="ade9e-113">All actions that consume or release disk space are also considered.</span></span> <span data-ttu-id="ade9e-114">Si se encuentra un archivo existente, se realiza una comprobación de la versión del archivo para determinar si realmente es necesario instalar el nuevo archivo o no.</span><span class="sxs-lookup"><span data-stu-id="ade9e-114">If an existing file is found, a file version check is performed to determine whether the new file actually needs to be installed or not.</span></span> <span data-ttu-id="ade9e-115">Si el archivo existente tiene un número de versión igual o mayor, el archivo existente no se sobrescribe y no se genera ningún costo de espacio en disco.</span><span class="sxs-lookup"><span data-stu-id="ade9e-115">If the existing file is of an equal or greater version number, the existing file is not overwritten and no disk-space cost is incurred.</span></span> <span data-ttu-id="ade9e-116">En todos los casos, el instalador utiliza los resultados de la comprobación del número de versión para establecer el estado de instalación de cada archivo.</span><span class="sxs-lookup"><span data-stu-id="ade9e-116">In all cases, the installer uses the results of version number checking to set the installation state of each file.</span></span>

<span data-ttu-id="ade9e-117">La acción FileCost inicializa el cálculo de costos con el instalador.</span><span class="sxs-lookup"><span data-stu-id="ade9e-117">The FileCost action initializes cost calculation with theinstaller.</span></span> <span data-ttu-id="ade9e-118">No se produce un [*costo*](c-gly.md) dinámico real hasta que se ejecuta la acción [CostFinalize](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="ade9e-118">Actual dynamic [*costing*](c-gly.md) does not occur until the [CostFinalize](costfinalize-action.md) action is executed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ade9e-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ade9e-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ade9e-120">Costo de archivos</span><span class="sxs-lookup"><span data-stu-id="ade9e-120">File Costing</span></span>](file-costing.md)
</dt> </dl>

 

 



