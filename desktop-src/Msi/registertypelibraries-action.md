---
description: La acción RegisterTypeLibraries registra las bibliotecas de tipos con el sistema. Esta acción se aplica a cada archivo al que se hace referencia en la tabla TypeLib que está programada para instalarse.
ms.assetid: 374450bb-316c-4fe6-abb1-cd8a8a31f284
title: Acción RegisterTypeLibraries
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 469cc18fc2842a3258804fc012c48a49085f1598
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677759"
---
# <a name="registertypelibraries-action"></a><span data-ttu-id="8c24e-104">Acción RegisterTypeLibraries</span><span class="sxs-lookup"><span data-stu-id="8c24e-104">RegisterTypeLibraries Action</span></span>

<span data-ttu-id="8c24e-105">La acción RegisterTypeLibraries registra las bibliotecas de tipos con el sistema.</span><span class="sxs-lookup"><span data-stu-id="8c24e-105">The RegisterTypeLibraries action registers type libraries with the system.</span></span> <span data-ttu-id="8c24e-106">Esta acción se aplica a cada archivo al que se hace referencia en la [tabla typelib](typelib-table.md) que está programada para instalarse.</span><span class="sxs-lookup"><span data-stu-id="8c24e-106">This action is applied to each file referred to in the [TypeLib table](typelib-table.md) that is scheduled for install.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="8c24e-107">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="8c24e-107">Sequence Restrictions</span></span>

<span data-ttu-id="8c24e-108">La acción RegisterTypeLibraries debe aparecer después de la acción [InstallFiles](installfiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="8c24e-108">The RegisterTypeLibraries action must come after the [InstallFiles](installfiles-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="8c24e-109">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="8c24e-109">ActionData Messages</span></span>



| <span data-ttu-id="8c24e-110">Campo</span><span class="sxs-lookup"><span data-stu-id="8c24e-110">Field</span></span> | <span data-ttu-id="8c24e-111">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="8c24e-111">Description of action data</span></span>                   |
|-------|----------------------------------------------|
| <span data-ttu-id="8c24e-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="8c24e-112">\[1\]</span></span> | <span data-ttu-id="8c24e-113">[GUID](guid.md) de la biblioteca de tipos registrados.</span><span class="sxs-lookup"><span data-stu-id="8c24e-113">[GUID](guid.md) of registered type library.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="8c24e-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8c24e-114">Remarks</span></span>

<span data-ttu-id="8c24e-115">La acción RegisterTypeLibraries requiere que el idioma de la biblioteca de tipos se cree correctamente en el campo Language de la tabla TypeLib.</span><span class="sxs-lookup"><span data-stu-id="8c24e-115">The RegisterTypeLibraries action requires that the type library language be correctly authored in the Language field of the TypeLib table.</span></span> <span data-ttu-id="8c24e-116">La creación incorrecta del campo de idioma puede hacer que el instalador no pueda registrar una biblioteca de tipos válida de otro modo.</span><span class="sxs-lookup"><span data-stu-id="8c24e-116">Incorrect authoring of the Language field can cause the installer to fail to register an otherwise valid type library.</span></span>

 

 



