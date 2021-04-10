---
description: La acción RegisterComPlus registra las aplicaciones COM+.
ms.assetid: e42bb993-7079-4d5b-bb2e-c958e99e705e
title: Acción RegisterComPlus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb824d67e776a99f8cd05c56f73f171f436c71d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156464"
---
# <a name="registercomplus-action"></a><span data-ttu-id="be143-103">Acción RegisterComPlus</span><span class="sxs-lookup"><span data-stu-id="be143-103">RegisterComPlus Action</span></span>

<span data-ttu-id="be143-104">La acción RegisterComPlus registra las aplicaciones COM+.</span><span class="sxs-lookup"><span data-stu-id="be143-104">The RegisterComPlus action registers COM+ applications.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="be143-105">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="be143-105">Sequence Restrictions</span></span>

<span data-ttu-id="be143-106">La acción RegisterComPlus debe seguir la acción [InstallFiles](installfiles-action.md) y la [acción UnregisterComPlus](unregistercomplus-action.md).</span><span class="sxs-lookup"><span data-stu-id="be143-106">The RegisterComPlus action must follow the [InstallFiles action](installfiles-action.md) and the [UnregisterComPlus action](unregistercomplus-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="be143-107">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="be143-107">ActionData Messages</span></span>



| <span data-ttu-id="be143-108">Campo</span><span class="sxs-lookup"><span data-stu-id="be143-108">Field</span></span> | <span data-ttu-id="be143-109">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="be143-109">Description of action data</span></span>              |
|-------|-----------------------------------------|
| <span data-ttu-id="be143-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="be143-110">\[1\]</span></span> | <span data-ttu-id="be143-111">IDENTIFICADOR de la aplicación COM+.</span><span class="sxs-lookup"><span data-stu-id="be143-111">Application ID of the COM+ application.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="be143-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="be143-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be143-113">Tabla de ComPlus</span><span class="sxs-lookup"><span data-stu-id="be143-113">Complus table</span></span>](complus-table.md)
</dt> <dt>

[<span data-ttu-id="be143-114">Acción UnregisterComPlus</span><span class="sxs-lookup"><span data-stu-id="be143-114">UnregisterComPlus action</span></span>](unregistercomplus-action.md)
</dt> <dt>

[<span data-ttu-id="be143-115">Instalación de una aplicación COM+ con el Windows Installer</span><span class="sxs-lookup"><span data-stu-id="be143-115">Installing a COM+ Application with the Windows Installer</span></span>](installing-a-com--application-with-the-windows-installer.md)
</dt> </dl>

 

 



