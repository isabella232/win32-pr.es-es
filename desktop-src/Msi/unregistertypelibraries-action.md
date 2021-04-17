---
description: La acción UnregisterTypeLibraries anula el registro de las bibliotecas de tipos del sistema. Esta acción se aplica a cada archivo que aparece en la tabla TypeLib que se desencadena para desinstalarse.
ms.assetid: fea5bdc1-ac27-4d02-bcea-5c97366dd394
title: Acción UnregisterTypeLibraries
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b399f80d940839c5e94028a9c32e706f4826341a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653073"
---
# <a name="unregistertypelibraries-action"></a><span data-ttu-id="741e2-104">Acción UnregisterTypeLibraries</span><span class="sxs-lookup"><span data-stu-id="741e2-104">UnregisterTypeLibraries Action</span></span>

<span data-ttu-id="741e2-105">La acción UnregisterTypeLibraries anula el registro de las bibliotecas de tipos del sistema.</span><span class="sxs-lookup"><span data-stu-id="741e2-105">The UnregisterTypeLibraries action unregisters type libraries from the system.</span></span> <span data-ttu-id="741e2-106">Esta acción se aplica a cada archivo que aparece en la tabla [typelib](typelib-table.md) que se desencadena para desinstalarse.</span><span class="sxs-lookup"><span data-stu-id="741e2-106">This action is applied to each file listed in the [TypeLib](typelib-table.md) table that is triggered to be uninstalled.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="741e2-107">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="741e2-107">Sequence Restrictions</span></span>

<span data-ttu-id="741e2-108">La acción UnregisterTypeLibraries debe ser anterior a la acción [RemoveFiles](removefiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="741e2-108">The UnregisterTypeLibraries action must come before the [RemoveFiles](removefiles-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="741e2-109">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="741e2-109">ActionData Messages</span></span>



| <span data-ttu-id="741e2-110">Campo</span><span class="sxs-lookup"><span data-stu-id="741e2-110">Field</span></span> | <span data-ttu-id="741e2-111">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="741e2-111">Description of action data</span></span>                        |
|-------|---------------------------------------------------|
| <span data-ttu-id="741e2-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="741e2-112">\[1\]</span></span> | <span data-ttu-id="741e2-113">[GUID](guid.md) de una biblioteca de tipos no registrada.</span><span class="sxs-lookup"><span data-stu-id="741e2-113">[GUID](guid.md) of an unregistered type library.</span></span> |



 

 

 



