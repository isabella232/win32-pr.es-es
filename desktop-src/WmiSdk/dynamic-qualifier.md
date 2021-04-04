---
description: El calificador dinámico indica una clase cuyas instancias se crean dinámicamente. El valor de este calificador debe establecerse en TRUE.
ms.assetid: 63286687-abbf-49f0-8061-3b47fba75806
ms.tgt_platform: multiple
title: Calificador dinámico
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Dynamic
api_type:
- NA
api_location: ''
ms.openlocfilehash: f6530942859c8c3de571ba9ddb94e9b1ce78cc0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908677"
---
# <a name="dynamic-qualifier"></a><span data-ttu-id="49852-104">Calificador dinámico</span><span class="sxs-lookup"><span data-stu-id="49852-104">Dynamic Qualifier</span></span>

<span data-ttu-id="49852-105">El calificador **dinámico** indica una clase cuyas instancias se crean dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="49852-105">The **Dynamic** qualifier indicates a class whose instances are created dynamically.</span></span> <span data-ttu-id="49852-106">El valor de este calificador debe establecerse en **true**.</span><span class="sxs-lookup"><span data-stu-id="49852-106">The value of this qualifier must be set to **TRUE**.</span></span>

<span data-ttu-id="49852-107">El calificador **dinámico** debe especificarse en todas las clases que contienen datos y cuyas instancias se crean dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="49852-107">The **Dynamic** qualifier must be specified on all classes that contain data and for which instances are created dynamically.</span></span> <span data-ttu-id="49852-108">El calificador de [**proveedor**](/windows/desktop/api/Provider/nl-provider-provider) se suele especificar también para identificar el proveedor responsable de proporcionar los datos.</span><span class="sxs-lookup"><span data-stu-id="49852-108">The [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier is typically also specified to identify the provider responsible for supplying the data.</span></span>

<span data-ttu-id="49852-109">Las clases que solo contienen métodos que necesitan implementación no requieren el calificador **dinámico** .</span><span class="sxs-lookup"><span data-stu-id="49852-109">Classes that contain only methods that need implementation do not require the **Dynamic** qualifier.</span></span> <span data-ttu-id="49852-110">Solo se requiere el calificador de [**proveedor**](/windows/desktop/api/Provider/nl-provider-provider) para especificar el nombre del proveedor para proporcionar la implementación.</span><span class="sxs-lookup"><span data-stu-id="49852-110">Only the [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier is required to specify the name of the provider to supply the implementation.</span></span>

<span data-ttu-id="49852-111">Todas las clases derivadas de una clase dinámica deben ser dinámicas.</span><span class="sxs-lookup"><span data-stu-id="49852-111">All classes derived from a dynamic class must be dynamic.</span></span> <span data-ttu-id="49852-112">No se puede derivar una clase estática de una clase dinámica.</span><span class="sxs-lookup"><span data-stu-id="49852-112">You cannot derive a static class from a dynamic class.</span></span>

<span data-ttu-id="49852-113">Cuando se especifica **Dynamic** en una propiedad de una instancia de, también se debe especificar el calificador **PropertyContext** .</span><span class="sxs-lookup"><span data-stu-id="49852-113">When **Dynamic** is specified on a property of an instance, the **PropertyContext** qualifier must also be specified.</span></span>

## <a name="requirements"></a><span data-ttu-id="49852-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49852-114">Requirements</span></span>



| <span data-ttu-id="49852-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="49852-115">Requirement</span></span> | <span data-ttu-id="49852-116">Value</span><span class="sxs-lookup"><span data-stu-id="49852-116">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="49852-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49852-117">Minimum supported client</span></span><br/> | <span data-ttu-id="49852-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="49852-118">Windows Vista</span></span><br/>       |
| <span data-ttu-id="49852-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49852-119">Minimum supported server</span></span><br/> | <span data-ttu-id="49852-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="49852-120">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="49852-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="49852-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49852-122">**Calificadores WMI estándar**</span><span class="sxs-lookup"><span data-stu-id="49852-122">**Standard WMI Qualifiers**</span></span>](standard-wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="49852-123">Calificadores WMI</span><span class="sxs-lookup"><span data-stu-id="49852-123">WMI Qualifiers</span></span>](wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="49852-124">Adición de un calificador</span><span class="sxs-lookup"><span data-stu-id="49852-124">Adding a Qualifier</span></span>](adding-a-qualifier.md)
</dt> </dl>

 

 




