---
title: Modos de acceso de almacenamiento estructurado
description: Los mecanismos para controlar el acceso simultáneo a un objeto, por parte de varios procesos y usuarios, son esenciales.
ms.assetid: 2d524c2b-f2b4-49f2-9be8-2037846eb9e9
keywords:
- Almacenamiento estructurado Strctd STG, Fundamentals, funciones de API, marcas de acceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e46a231cb5168d15564f0b86b064c8bfd19e38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665597"
---
# <a name="structured-storage-access-modes"></a><span data-ttu-id="1bdf5-104">Modos de acceso de almacenamiento estructurado</span><span class="sxs-lookup"><span data-stu-id="1bdf5-104">Structured Storage Access Modes</span></span>

<span data-ttu-id="1bdf5-105">Los mecanismos para controlar el acceso simultáneo a un objeto, por parte de varios procesos y usuarios, son esenciales.</span><span class="sxs-lookup"><span data-stu-id="1bdf5-105">Mechanisms for controlling simultaneous access to an object, by multiple processes and users, are essential.</span></span> <span data-ttu-id="1bdf5-106">COM proporciona estos mecanismos definiendo modos de acceso para los objetos de almacenamiento y de secuencia.</span><span class="sxs-lookup"><span data-stu-id="1bdf5-106">COM provides these mechanisms by defining access modes for both storage and stream objects.</span></span> <span data-ttu-id="1bdf5-107">Los elementos secundarios heredan el modo de acceso especificado para un objeto de almacenamiento primario, aunque se pueden colocar restricciones adicionales en el almacenamiento o la secuencia secundaria.</span><span class="sxs-lookup"><span data-stu-id="1bdf5-107">The access mode specified for a parent storage object is inherited by its children, though you can place additional restrictions on the child storage or stream.</span></span> <span data-ttu-id="1bdf5-108">Un objeto de flujo o almacenamiento anidado se puede abrir en el mismo modo o en un modo más restringido que el de su elemento primario, pero no se puede abrir en un modo menos restringido que el de su elemento primario.</span><span class="sxs-lookup"><span data-stu-id="1bdf5-108">A nested storage or stream object can be opened in the same mode or in a more restricted mode than that of its parent, but it cannot be opened in a less restricted mode than that of its parent.</span></span>

<span data-ttu-id="1bdf5-109">Los modos de acceso se especifican mediante los valores enumerados en [**constantes de STGM**](stgm-constants.md).</span><span class="sxs-lookup"><span data-stu-id="1bdf5-109">You specify access modes by using the values listed in [**STGM Constants**](stgm-constants.md).</span></span> <span data-ttu-id="1bdf5-110">Estos valores sirven como marcas para pasar como argumentos a métodos en la interfaz [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) y las funciones de API asociadas.</span><span class="sxs-lookup"><span data-stu-id="1bdf5-110">These values serve as flags to be passed as arguments to methods in the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface and associated API functions.</span></span> <span data-ttu-id="1bdf5-111">Normalmente, se combinan varias marcas en el parámetro *grfMode*, mediante una operación **or** booleana.</span><span class="sxs-lookup"><span data-stu-id="1bdf5-111">Typically, several flags are combined in the parameter *grfMode*, using a Boolean **OR** operation.</span></span>

<span data-ttu-id="1bdf5-112">Las marcas se dividen en seis grupos.</span><span class="sxs-lookup"><span data-stu-id="1bdf5-112">The flags fall into six groups.</span></span> <span data-ttu-id="1bdf5-113">Solo se puede especificar una marca de cada grupo a la vez:</span><span class="sxs-lookup"><span data-stu-id="1bdf5-113">Only one flag from each group can be specified at a time:</span></span>

-   [<span data-ttu-id="1bdf5-114">Marcas de transacción</span><span class="sxs-lookup"><span data-stu-id="1bdf5-114">Transaction Flags</span></span>](transaction-flags.md)
-   [<span data-ttu-id="1bdf5-115">Marcas de creación de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="1bdf5-115">Storage Creation Flags</span></span>](storage-creation-flags.md)
-   [<span data-ttu-id="1bdf5-116">Marcas de creación temporales</span><span class="sxs-lookup"><span data-stu-id="1bdf5-116">Temporary Creation Flags</span></span>](temporary-creation-flags.md)
-   [<span data-ttu-id="1bdf5-117">Marcas de prioridad</span><span class="sxs-lookup"><span data-stu-id="1bdf5-117">Priority Flags</span></span>](priority-flags.md)
-   [<span data-ttu-id="1bdf5-118">Marcas de permisos de acceso</span><span class="sxs-lookup"><span data-stu-id="1bdf5-118">Access Permission Flags</span></span>](access-permission-flags.md)
-   [<span data-ttu-id="1bdf5-119">Marcas de acceso compartido</span><span class="sxs-lookup"><span data-stu-id="1bdf5-119">Shared Access Flags</span></span>](shared-access-flags.md)

 

 




