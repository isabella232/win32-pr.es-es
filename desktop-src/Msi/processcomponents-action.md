---
description: La acción ProcessComponents registra y anula el registro de componentes, sus rutas de acceso clave y los clientes de componentes.
ms.assetid: 8ad418c0-9bba-41d0-a96c-2c7b1c2467d9
title: Acción ProcessComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aef1f71e9a50b714a12848fc9f923d1866c2e40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652943"
---
# <a name="processcomponents-action"></a><span data-ttu-id="ea17c-103">Acción ProcessComponents</span><span class="sxs-lookup"><span data-stu-id="ea17c-103">ProcessComponents Action</span></span>

<span data-ttu-id="ea17c-104">La acción ProcessComponents registra y anula el registro de componentes, sus rutas de acceso clave y los clientes de componentes.</span><span class="sxs-lookup"><span data-stu-id="ea17c-104">The ProcessComponents action registers and unregisters components, their key paths, and the component clients.</span></span> <span data-ttu-id="ea17c-105">La acción ProcessComponents consulta la columna de la ruta de la [tabla de componentes](component-table.md) para determinar keypaths.</span><span class="sxs-lookup"><span data-stu-id="ea17c-105">The ProcessComponents action queries the KeyPath column of the [Component table](component-table.md) to determine keypaths.</span></span> <span data-ttu-id="ea17c-106">[**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) usa este registro para devolver la ruta de acceso de un componente para un cliente del producto.</span><span class="sxs-lookup"><span data-stu-id="ea17c-106">This registration is used by [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) to return the path of a component for a product client.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="ea17c-107">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="ea17c-107">Sequence Restrictions</span></span>

<span data-ttu-id="ea17c-108">La acción ProcessComponents debe aparecer después de la acción [InstallInitialize](installinitialize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="ea17c-108">The ProcessComponents action must come after the [InstallInitialize](installinitialize-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="ea17c-109">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="ea17c-109">ActionData Messages</span></span>

<span data-ttu-id="ea17c-110">Para cada componente que se va a registrar.</span><span class="sxs-lookup"><span data-stu-id="ea17c-110">For each component being registered.</span></span>



| <span data-ttu-id="ea17c-111">Campo</span><span class="sxs-lookup"><span data-stu-id="ea17c-111">Field</span></span> | <span data-ttu-id="ea17c-112">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="ea17c-112">Description of action data</span></span>      |
|-------|---------------------------------|
| <span data-ttu-id="ea17c-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="ea17c-113">\[1\]</span></span> | <span data-ttu-id="ea17c-114">ProductId</span><span class="sxs-lookup"><span data-stu-id="ea17c-114">ProductId</span></span>                       |
| <span data-ttu-id="ea17c-115">\[2\]</span><span class="sxs-lookup"><span data-stu-id="ea17c-115">\[2\]</span></span> | <span data-ttu-id="ea17c-116">ComponentId</span><span class="sxs-lookup"><span data-stu-id="ea17c-116">ComponentId</span></span>                     |
| <span data-ttu-id="ea17c-117">\[3\]</span><span class="sxs-lookup"><span data-stu-id="ea17c-117">\[3\]</span></span> | <span data-ttu-id="ea17c-118">Ruta de acceso de la clave del componente.</span><span class="sxs-lookup"><span data-stu-id="ea17c-118">The key path for the component.</span></span> |



 

<span data-ttu-id="ea17c-119">Para cada componente del que se va a anular el registro.</span><span class="sxs-lookup"><span data-stu-id="ea17c-119">For each component being unregistered.</span></span>



| <span data-ttu-id="ea17c-120">Campo</span><span class="sxs-lookup"><span data-stu-id="ea17c-120">Field</span></span> | <span data-ttu-id="ea17c-121">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="ea17c-121">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="ea17c-122">\[1\]</span><span class="sxs-lookup"><span data-stu-id="ea17c-122">\[1\]</span></span> | <span data-ttu-id="ea17c-123">ProductId</span><span class="sxs-lookup"><span data-stu-id="ea17c-123">ProductId</span></span>                  |
| <span data-ttu-id="ea17c-124">\[2\]</span><span class="sxs-lookup"><span data-stu-id="ea17c-124">\[2\]</span></span> | <span data-ttu-id="ea17c-125">ComponentId</span><span class="sxs-lookup"><span data-stu-id="ea17c-125">ComponentId</span></span>                |



 

 

 



