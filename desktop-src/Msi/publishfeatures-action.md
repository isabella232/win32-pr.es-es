---
description: La acción PublishFeatures escribe el estado de cada característica en el registro del sistema.
ms.assetid: 8205e865-e625-43b9-8ce9-cff8026b2717
title: Acción PublishFeatures
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f5356ef89aa2651c470917a9b8d81b79ee83d01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677772"
---
# <a name="publishfeatures-action"></a><span data-ttu-id="f6c33-103">Acción PublishFeatures</span><span class="sxs-lookup"><span data-stu-id="f6c33-103">PublishFeatures Action</span></span>

<span data-ttu-id="f6c33-104">La acción PublishFeatures escribe el estado de cada característica en el registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="f6c33-104">The PublishFeatures action writes each feature's state into the system registry.</span></span> <span data-ttu-id="f6c33-105">El estado de la característica puede estar ausente, anunciado o instalado.</span><span class="sxs-lookup"><span data-stu-id="f6c33-105">The feature state may be either absent, advertised, or installed.</span></span> <span data-ttu-id="f6c33-106">La acción PublishFeatures también escribe la asignación del componente de característica en el registro del sistema para cada característica instalada.</span><span class="sxs-lookup"><span data-stu-id="f6c33-106">The PublishFeatures action also writes the feature-component mapping into the system registry for each installed feature.</span></span>

<span data-ttu-id="f6c33-107">La acción PublishFeatures consulta la tabla de [FeatureComponents](featurecomponents-table.md), la [tabla de características](feature-table.md)y la [tabla de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="f6c33-107">The PublishFeatures action queries the [FeatureComponents table](featurecomponents-table.md), [Feature table](feature-table.md), and [Component table](component-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="f6c33-108">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="f6c33-108">Sequence Restrictions</span></span>

<span data-ttu-id="f6c33-109">La acción PublishFeatures debe ser anterior a [PublishProduct](publishproduct-action.md).</span><span class="sxs-lookup"><span data-stu-id="f6c33-109">The PublishFeatures action must come before [PublishProduct](publishproduct-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="f6c33-110">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="f6c33-110">ActionData Messages</span></span>



| <span data-ttu-id="f6c33-111">Campo</span><span class="sxs-lookup"><span data-stu-id="f6c33-111">Field</span></span> | <span data-ttu-id="f6c33-112">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="f6c33-112">Description of action data</span></span>        |
|-------|-----------------------------------|
| <span data-ttu-id="f6c33-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="f6c33-113">\[1\]</span></span> | <span data-ttu-id="f6c33-114">Identificador de la característica anunciada.</span><span class="sxs-lookup"><span data-stu-id="f6c33-114">Identifier of advertised feature.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f6c33-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f6c33-115">Remarks</span></span>

<span data-ttu-id="f6c33-116">La acción PublishFeatures publica la composición de todas las características que se seleccionan para ser anunciadas o instaladas.</span><span class="sxs-lookup"><span data-stu-id="f6c33-116">The PublishFeatures action publishes the composition of all features that are selected to be advertised or installed.</span></span>

 

 



