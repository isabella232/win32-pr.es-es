---
title: Elemento ButtonTip
description: Tenga en cuenta que en esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. | Elemento ButtonTip
ms.assetid: 93e5d0c8-8d2d-45c1-9d47-bbd0b6eb8b88
keywords:
- Elemento ButtonTip Media Player Windows
topic_type:
- apiref
api_name:
- ButtonTip Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56ab94794232ade6f924b87fd3f4d73d4452d544
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698655"
---
# <a name="buttontip-element"></a><span data-ttu-id="b8cb5-105">Elemento ButtonTip</span><span class="sxs-lookup"><span data-stu-id="b8cb5-105">ButtonTip Element</span></span>

> [!Note]  
> <span data-ttu-id="b8cb5-106">En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="b8cb5-106">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="b8cb5-107">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="b8cb5-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="b8cb5-108">El elemento **ButtonTip** especifica la cadena de texto que se muestra cuando el usuario apunta a un botón del panel de tareas.</span><span class="sxs-lookup"><span data-stu-id="b8cb5-108">The **ButtonTip** element specifies the text string that is displayed when the user points to a task pane button.</span></span>

``` syntax
<ButtonTip>
   text string
</ButtonTip>
```

## <a name="attributes"></a><span data-ttu-id="b8cb5-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="b8cb5-109">Attributes</span></span>

<span data-ttu-id="b8cb5-110">Este elemento no tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="b8cb5-110">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="b8cb5-111">Elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="b8cb5-111">Parent/Child Elements</span></span>



| <span data-ttu-id="b8cb5-112">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="b8cb5-112">Hierarchy</span></span>       | <span data-ttu-id="b8cb5-113">Elemento</span><span class="sxs-lookup"><span data-stu-id="b8cb5-113">Element</span></span>                                              |
|-----------------|------------------------------------------------------|
| <span data-ttu-id="b8cb5-114">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="b8cb5-114">Parent elements</span></span> | <span data-ttu-id="b8cb5-115">**ServiceTask1**, **ServiceTask2**, **ServiceTask3**</span><span class="sxs-lookup"><span data-stu-id="b8cb5-115">**ServiceTask1**, **ServiceTask2**, **ServiceTask3**</span></span> |
| <span data-ttu-id="b8cb5-116">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b8cb5-116">Child elements</span></span>  | <span data-ttu-id="b8cb5-117">Ninguno</span><span class="sxs-lookup"><span data-stu-id="b8cb5-117">None</span></span>                                                 |



 

## <a name="remarks"></a><span data-ttu-id="b8cb5-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b8cb5-118">Remarks</span></span>

<span data-ttu-id="b8cb5-119">Este elemento es opcional para cada instancia de **ServiceTask1**, **ServiceTask2** o **ServiceTask3**.</span><span class="sxs-lookup"><span data-stu-id="b8cb5-119">This element is optional for each instance of **ServiceTask1**, **ServiceTask2**, or **ServiceTask3**.</span></span> <span data-ttu-id="b8cb5-120">Si no se proporciona este elemento, Windows Media Player usa el texto del botón como valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="b8cb5-120">If this element is not supplied, Windows Media Player uses the button text as the default value.</span></span>

> [!Note]  
> <span data-ttu-id="b8cb5-121">Windows Media Player 10 tiene tres paneles de tareas en los que una tienda en línea puede mostrar sus páginas Web.</span><span class="sxs-lookup"><span data-stu-id="b8cb5-121">Windows Media Player 10 has three task panes where an online store can display its webpages.</span></span> <span data-ttu-id="b8cb5-122">La tienda en línea puede elegir usar uno, dos o los tres paneles de tareas.</span><span class="sxs-lookup"><span data-stu-id="b8cb5-122">The online store can choose to use one, two, or all three of the task panes.</span></span> <span data-ttu-id="b8cb5-123">Windows Media Player 11 solo tiene un panel de tareas, que el usuario puede ver haciendo clic en la pestaña **tiendas en línea** . Windows Media Player 11 omite los elementos **ServiceTask2** y **ServiceTask3** .</span><span class="sxs-lookup"><span data-stu-id="b8cb5-123">Windows Media Player 11 has only one task pane, which the user can view by clicking on the **Online Stores** tab. Windows Media Player 11 ignores the **ServiceTask2** and **ServiceTask3** elements.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b8cb5-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8cb5-124">Requirements</span></span>



| <span data-ttu-id="b8cb5-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8cb5-125">Requirement</span></span> | <span data-ttu-id="b8cb5-126">Value</span><span class="sxs-lookup"><span data-stu-id="b8cb5-126">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="b8cb5-127">Versión</span><span class="sxs-lookup"><span data-stu-id="b8cb5-127">Version</span></span><br/> | <span data-ttu-id="b8cb5-128">Windows Media Player 10 o posterior.</span><span class="sxs-lookup"><span data-stu-id="b8cb5-128">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b8cb5-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="b8cb5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8cb5-130">**Ejemplo de documento ServiceInfo para una tienda en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="b8cb5-130">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="b8cb5-131">**Ejemplo de documento ServiceInfo para una tienda en línea de tipo 2**</span><span class="sxs-lookup"><span data-stu-id="b8cb5-131">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="b8cb5-132">**Documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="b8cb5-132">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





