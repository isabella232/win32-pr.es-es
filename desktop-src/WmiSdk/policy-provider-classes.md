---
description: El proveedor de directivas WMI proporciona extensiones a la Directiva de grupo a través de clases, lo que permite refinar la aplicación de la Directiva.
ms.assetid: 5d4d4fd2-ecd0-4546-b919-1e75199a403c
ms.tgt_platform: multiple
title: Clases de proveedor de directivas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f2e2a142cf677c8f0b14b41ceb5119e71bcfebe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659829"
---
# <a name="policy-provider-classes"></a><span data-ttu-id="b9ac9-103">Clases de proveedor de directivas</span><span class="sxs-lookup"><span data-stu-id="b9ac9-103">Policy Provider Classes</span></span>

<span data-ttu-id="b9ac9-104">El proveedor de directivas WMI proporciona extensiones a la Directiva de grupo a través de clases, lo que permite refinar la aplicación de la Directiva.</span><span class="sxs-lookup"><span data-stu-id="b9ac9-104">The WMI policy provider provides extensions to group policy through classes, permitting refinements in the application of policy.</span></span> <span data-ttu-id="b9ac9-105">La Directiva se establece mediante el lenguaje de consulta de WMI (WQL) y reside en el Active Directory para facilitar la implementación.</span><span class="sxs-lookup"><span data-stu-id="b9ac9-105">Policy is set using the WMI Query Language (WQL) and resides in the Active Directory for easy deployment.</span></span>

<span data-ttu-id="b9ac9-106">En la tabla siguiente se enumeran las clases del proveedor de directivas WMI.</span><span class="sxs-lookup"><span data-stu-id="b9ac9-106">The following table lists the classes for the WMI policy provider.</span></span>



| <span data-ttu-id="b9ac9-107">Clase</span><span class="sxs-lookup"><span data-stu-id="b9ac9-107">Class</span></span>                                               | <span data-ttu-id="b9ac9-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="b9ac9-108">Description</span></span>                                                       |
|-----------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="b9ac9-109">**Proveedores de MSFT \_**</span><span class="sxs-lookup"><span data-stu-id="b9ac9-109">**MSFT\_Providers**</span></span>](/previous-versions/windows/desktop/wmisystemprov/msft-providers) | <span data-ttu-id="b9ac9-110">Expone la configuración relacionada con las instancias del proveedor.</span><span class="sxs-lookup"><span data-stu-id="b9ac9-110">Exposes configuration relating to provider instances.</span></span>             |
| [<span data-ttu-id="b9ac9-111">**Regla de MSFT \_**</span><span class="sxs-lookup"><span data-stu-id="b9ac9-111">**MSFT\_Rule**</span></span>](/previous-versions/windows/desktop/policmanprov/msft-rule)                | <span data-ttu-id="b9ac9-112">Define una regla única dentro de un ámbito de administración (SOM).</span><span class="sxs-lookup"><span data-stu-id="b9ac9-112">Defines a single rule within a Scope of Management (SOM).</span></span>         |
| [<span data-ttu-id="b9ac9-113">**MSFT \_ SomFilter**</span><span class="sxs-lookup"><span data-stu-id="b9ac9-113">**MSFT\_SomFilter**</span></span>](/previous-versions/windows/desktop/policmanprov/msft-somfilter)      | <span data-ttu-id="b9ac9-114">Proporciona una lista de reglas que se evalúan en un equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="b9ac9-114">Provides a list of rules which are evaluated on a target machine.</span></span> |



 

 

 
