---
title: Enumerar objetos Container
description: Por Convención, todos los elementos de una enumeración en ADSI deben tener el mismo tipo de datos de automatización. Por ejemplo, una enumeración no debe devolver algunos elementos como una variante de tipo VT \_ I4 y otros como una variante del tipo VT \_ BSTR.
ms.assetid: 155caa67-05db-432b-b813-0d891a502301
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5514596b02521fa869ffd7c712dcac2cacb40192
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656183"
---
# <a name="enumerating-container-objects"></a><span data-ttu-id="40340-104">Enumerar objetos Container</span><span class="sxs-lookup"><span data-stu-id="40340-104">Enumerating Container Objects</span></span>

<span data-ttu-id="40340-105">Por Convención, todos los elementos de una enumeración en ADSI deben tener el mismo tipo de datos de automatización.</span><span class="sxs-lookup"><span data-stu-id="40340-105">By convention, all items in an enumeration in ADSI must be of the same Automation data type.</span></span> <span data-ttu-id="40340-106">Por ejemplo, una enumeración no debe devolver algunos elementos como una **variante** de tipo **VT \_ I4** y otros como una **variante** del tipo **VT \_ BSTR**.</span><span class="sxs-lookup"><span data-stu-id="40340-106">For example, an enumeration should not return some items as a **VARIANT** of type **VT\_I4** and others as a **VARIANT** of type **VT\_BSTR**.</span></span>

<span data-ttu-id="40340-107">Para enumerar una lista de los elementos que mantiene un objeto, un cliente solicita la creación de un objeto de enumeración para el tipo de información específico que se muestra.</span><span class="sxs-lookup"><span data-stu-id="40340-107">To enumerate a list of items that an object maintains, a client requests the creation of an enumeration object for the specific type of information being listed.</span></span> <span data-ttu-id="40340-108">En ADSI, el cliente puede enumerar los objetos de objetos de espacio de nombres, objetos de contenedor genéricos, objetos de colección, objetos de miembro o objetos de esquema.</span><span class="sxs-lookup"><span data-stu-id="40340-108">In ADSI, the client may list the objects in namespace objects, generic container objects, collection objects, member objects, or schema objects.</span></span> <span data-ttu-id="40340-109">ADSI proporciona un filtro que se puede establecer y modificar para limitar las coincidencias en cualquier enumeración a través de la propiedad [**IADsContainer. Filter**](iadscontainer-property-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="40340-109">ADSI provides a filter that can be set and modified to limit the matches in any enumeration though the [**IADsContainer.Filter**](iadscontainer-property-methods.md) property.</span></span> <span data-ttu-id="40340-110">Puede encontrar ejemplos de implementaciones de objetos de enumerador en el código de componente de proveedor de ejemplo para los siguientes objetos de contenedor de ADs.</span><span class="sxs-lookup"><span data-stu-id="40340-110">Examples of implementations of enumerator objects can be found in the example provider component code for the following ADs container objects.</span></span>



| <span data-ttu-id="40340-111">Tipo de objeto</span><span class="sxs-lookup"><span data-stu-id="40340-111">Object type</span></span>         | <span data-ttu-id="40340-112">código</span><span class="sxs-lookup"><span data-stu-id="40340-112">code</span></span>         |
|---------------------|--------------|
| <span data-ttu-id="40340-113">Contenedor genérico</span><span class="sxs-lookup"><span data-stu-id="40340-113">Generic Container</span></span>   | <span data-ttu-id="40340-114">cenumobj. cpp</span><span class="sxs-lookup"><span data-stu-id="40340-114">cenumobj.cpp</span></span> |
| <span data-ttu-id="40340-115">Contenedor de espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="40340-115">Namespace Container</span></span> | <span data-ttu-id="40340-116">cenumns. cpp</span><span class="sxs-lookup"><span data-stu-id="40340-116">cenumns.cpp</span></span>  |
| <span data-ttu-id="40340-117">Contenedor de esquema</span><span class="sxs-lookup"><span data-stu-id="40340-117">Schema Container</span></span>    | <span data-ttu-id="40340-118">cenumsch. cpp</span><span class="sxs-lookup"><span data-stu-id="40340-118">cenumsch.cpp</span></span> |



 

<span data-ttu-id="40340-119">Para obtener información del lado cliente, vea [colecciones y grupos](collections-and-groups.md).</span><span class="sxs-lookup"><span data-stu-id="40340-119">For client-side information, see [Collections and Groups](collections-and-groups.md).</span></span>

 

 




