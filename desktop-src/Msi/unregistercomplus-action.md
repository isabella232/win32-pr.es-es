---
description: La acción UnregisterComPlus quita las aplicaciones COM+ del registro.
ms.assetid: bcedc436-a048-487e-9a84-e766da57a0b3
title: Acción UnregisterComPlus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e32d39255229151757f7d6be0ada871f555f77e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003132"
---
# <a name="unregistercomplus-action"></a><span data-ttu-id="c16ce-103">Acción UnregisterComPlus</span><span class="sxs-lookup"><span data-stu-id="c16ce-103">UnregisterComPlus Action</span></span>

<span data-ttu-id="c16ce-104">La acción UnregisterComPlus quita las aplicaciones COM+ del registro.</span><span class="sxs-lookup"><span data-stu-id="c16ce-104">The UnregisterComPlus action removes COM+ applications from the registry.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="c16ce-105">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="c16ce-105">Sequence Restrictions</span></span>

<span data-ttu-id="c16ce-106">La [acción RegisterComPlus](registercomplus-action.md) debe seguir la acción [InstallFiles](installfiles-action.md) y la acción UnregisterComPlus.</span><span class="sxs-lookup"><span data-stu-id="c16ce-106">The [RegisterComPlus action](registercomplus-action.md) must follow the [InstallFiles action](installfiles-action.md) and the UnregisterComPlus action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="c16ce-107">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="c16ce-107">ActionData Messages</span></span>



| <span data-ttu-id="c16ce-108">Campo</span><span class="sxs-lookup"><span data-stu-id="c16ce-108">Field</span></span> | <span data-ttu-id="c16ce-109">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="c16ce-109">Description of action data</span></span>                                    |
|-------|---------------------------------------------------------------|
| <span data-ttu-id="c16ce-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="c16ce-110">\[1\]</span></span> | <span data-ttu-id="c16ce-111">Identificador de la aplicación COM+ que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="c16ce-111">Application identifier of the COM+ application being removed.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="c16ce-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c16ce-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c16ce-113">Acción RegisterComPlus</span><span class="sxs-lookup"><span data-stu-id="c16ce-113">RegisterComPlus action</span></span>](registercomplus-action.md)
</dt> <dt>

[<span data-ttu-id="c16ce-114">Tabla de ComPlus</span><span class="sxs-lookup"><span data-stu-id="c16ce-114">Complus table</span></span>](complus-table.md)
</dt> <dt>

[<span data-ttu-id="c16ce-115">Instalación de una aplicación COM+ con el Windows Installer</span><span class="sxs-lookup"><span data-stu-id="c16ce-115">Installing a COM+ Application with the Windows Installer</span></span>](installing-a-com--application-with-the-windows-installer.md)
</dt> </dl>

 

 



