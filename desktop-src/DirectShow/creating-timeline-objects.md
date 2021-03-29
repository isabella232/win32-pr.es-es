---
description: Crear objetos Timeline
ms.assetid: fb369b32-a54b-4d8a-8358-5f05aa48f853
title: Crear objetos Timeline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 929fffb6a953e198b6e7ed9b17250d45e84f7932
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105666107"
---
# <a name="creating-timeline-objects"></a><span data-ttu-id="edb7f-103">Crear objetos Timeline</span><span class="sxs-lookup"><span data-stu-id="edb7f-103">Creating Timeline Objects</span></span>

<span data-ttu-id="edb7f-104">\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]</span><span class="sxs-lookup"><span data-stu-id="edb7f-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="edb7f-105">El código de ejemplo que se presenta en este artículo comienza con una escala de tiempo vacía, pero se aplican los mismos pasos si carga un proyecto existente y desea agregarle objetos.</span><span class="sxs-lookup"><span data-stu-id="edb7f-105">The sample code presented in this article starts with an empty timeline, but the same steps apply if you load an existing project and want to add objects to it.</span></span>

<span data-ttu-id="edb7f-106">Para crear cualquier tipo de objeto en la escala de tiempo, llame al método [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) .</span><span class="sxs-lookup"><span data-stu-id="edb7f-106">To create any type of object in the timeline, call the [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) method.</span></span> <span data-ttu-id="edb7f-107">Por ejemplo, el código siguiente crea un nuevo Grupo:</span><span class="sxs-lookup"><span data-stu-id="edb7f-107">For example, the following code creates a new group:</span></span>


```C++
IAMTimelineObj *pGroupObj = NULL;
pTL->CreateEmptyNode(&pGroupObj, TIMELINE_MAJOR_TYPE_GROUP);
```



<span data-ttu-id="edb7f-108">El segundo parámetro es un miembro de la enumeración de [**\_ \_ tipo principal**](timeline-major-type.md) de la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="edb7f-108">The second parameter is a member of the [**TIMELINE\_MAJOR\_TYPE**](timeline-major-type.md) enumeration.</span></span> <span data-ttu-id="edb7f-109">Especifica el tipo de objeto de escala de tiempo que se va a crear, como un grupo o una pista.</span><span class="sxs-lookup"><span data-stu-id="edb7f-109">It specifies the type of timeline object to create, such as a group or a track.</span></span>

<span data-ttu-id="edb7f-110">El método **CreateEmptyNode** crea el objeto y devuelve un puntero a la interfaz [**IAMTimelineObj**](iamtimelineobj.md) del objeto.</span><span class="sxs-lookup"><span data-stu-id="edb7f-110">The **CreateEmptyNode** method creates the object and returns a pointer to the object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span> <span data-ttu-id="edb7f-111">También incrementa el recuento de referencias en la interfaz **IAMTimelineObj** , por lo que debe liberar la interfaz cuando termine de usarla.</span><span class="sxs-lookup"><span data-stu-id="edb7f-111">It also increments the reference count on the **IAMTimelineObj** interface, so you must release the interface when you finish using it.</span></span> <span data-ttu-id="edb7f-112">No llame a la función [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="edb7f-112">Do not call the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function.</span></span> <span data-ttu-id="edb7f-113">En su lugar, use siempre **CreateEmptyNode** para crear un objeto Timeline, ya que inicializa el nuevo objeto para su uso en una escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="edb7f-113">Instead, always use **CreateEmptyNode** to create a timeline object, because it initializes the new object for use in a timeline.</span></span>

<span data-ttu-id="edb7f-114">La interfaz [**IAMTimelineObj**](iamtimelineobj.md) es una interfaz genérica.</span><span class="sxs-lookup"><span data-stu-id="edb7f-114">The [**IAMTimelineObj**](iamtimelineobj.md) interface is a generic interface.</span></span> <span data-ttu-id="edb7f-115">Proporciona métodos comunes a todos los tipos de objeto Timeline.</span><span class="sxs-lookup"><span data-stu-id="edb7f-115">It provides methods that are common to all types of timeline object.</span></span> <span data-ttu-id="edb7f-116">Cada tipo de objeto expone también otras interfaces.</span><span class="sxs-lookup"><span data-stu-id="edb7f-116">Each type of object exposes other interfaces as well.</span></span> <span data-ttu-id="edb7f-117">Por ejemplo, los grupos exponen la interfaz [**IAMTimelineGroup**](iamtimelinegroup.md) , entre otros.</span><span class="sxs-lookup"><span data-stu-id="edb7f-117">For example, groups expose the [**IAMTimelineGroup**](iamtimelinegroup.md) interface, among others.</span></span> <span data-ttu-id="edb7f-118">Puede obtener punteros a las otras interfaces llamando a **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="edb7f-118">You can obtain pointers to the other interfaces by calling **QueryInterface**.</span></span>

<span data-ttu-id="edb7f-119">Después de crear un objeto, todavía no es parte de la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="edb7f-119">After you create an object, it is not yet a part of the timeline.</span></span> <span data-ttu-id="edb7f-120">El método para agregar un objeto a la escala de tiempo depende del tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="edb7f-120">The method to add an object to the timeline depends on the object type.</span></span> <span data-ttu-id="edb7f-121">En la sección siguiente se describe cómo agregar grupos, composiciones y pistas a la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="edb7f-121">The following section describes how to add groups, compositions, and tracks to the timeline.</span></span>

## <a name="related-topics"></a><span data-ttu-id="edb7f-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="edb7f-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="edb7f-123">Construir una escala de tiempo</span><span class="sxs-lookup"><span data-stu-id="edb7f-123">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 
