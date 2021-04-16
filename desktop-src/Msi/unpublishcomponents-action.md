---
description: La acción UnpublishComponents administra el desanuncio de los componentes enumerados en la tabla PublishComponent.
ms.assetid: 3e50f668-6d08-405e-a5a4-f422041ef0b1
title: Acción UnpublishComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f58d9fff862295bcc06e61e1b35c05cdddb58daa
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "104424307"
---
# <a name="unpublishcomponents-action"></a><span data-ttu-id="1b15a-103">Acción UnpublishComponents</span><span class="sxs-lookup"><span data-stu-id="1b15a-103">UnpublishComponents Action</span></span>

<span data-ttu-id="1b15a-104">La acción UnpublishComponents administra el desanuncio de los componentes enumerados en la tabla PublishComponent.</span><span class="sxs-lookup"><span data-stu-id="1b15a-104">The UnpublishComponents action manages the unadvertisement of components listed in the PublishComponent table.</span></span> <span data-ttu-id="1b15a-105">Se trata de componentes que pueden ser errores en otros productos.</span><span class="sxs-lookup"><span data-stu-id="1b15a-105">These are components that may be faulted in by other products.</span></span> <span data-ttu-id="1b15a-106">Esta acción quita información sobre los componentes publicados de la [tabla PublishComponent](publishcomponent-table.md) para los que la característica correspondiente está seleccionada actualmente para desinstalarse.</span><span class="sxs-lookup"><span data-stu-id="1b15a-106">This action removes information about published components from the [PublishComponent table](publishcomponent-table.md) for which the corresponding feature is currently selected to be uninstalled.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="1b15a-107">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="1b15a-107">Sequence Restrictions</span></span>

<span data-ttu-id="1b15a-108">No hay restricciones de secuencia.</span><span class="sxs-lookup"><span data-stu-id="1b15a-108">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="1b15a-109">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="1b15a-109">ActionData Messages</span></span>



| <span data-ttu-id="1b15a-110">Campo</span><span class="sxs-lookup"><span data-stu-id="1b15a-110">Field</span></span> | <span data-ttu-id="1b15a-111">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="1b15a-111">Description of action data</span></span>                                   |
|-------|--------------------------------------------------------------|
| <span data-ttu-id="1b15a-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="1b15a-112">\[1\]</span></span> | <span data-ttu-id="1b15a-113">GUID que representa el identificador de componente de una característica anunciada.</span><span class="sxs-lookup"><span data-stu-id="1b15a-113">GUID representing the component ID of an advertised feature.</span></span> |
| <span data-ttu-id="1b15a-114">\[2\]</span><span class="sxs-lookup"><span data-stu-id="1b15a-114">\[2\]</span></span> | <span data-ttu-id="1b15a-115">Calificador del ID. de componente.</span><span class="sxs-lookup"><span data-stu-id="1b15a-115">Qualifier of the component ID.</span></span>                               |



 

