---
title: Elemento Navigate
description: Tenga en cuenta que en esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. El elemento Navigate especifica una dirección URL que usan las llamadas a external. NavigateTaskPaneURL.
ms.assetid: 3898e381-baf8-481a-90ee-d64e55b319a0
keywords:
- Desplazarse por las ventanas de elementos Media Player
topic_type:
- apiref
api_name:
- Navigate Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ab3a76fba522332f1414b02d3e317f2793e88292
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649823"
---
# <a name="navigate-element"></a><span data-ttu-id="9b447-106">Elemento Navigate</span><span class="sxs-lookup"><span data-stu-id="9b447-106">Navigate Element</span></span>

> [!Note]  
> <span data-ttu-id="9b447-107">En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="9b447-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="9b447-108">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="9b447-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="9b447-109">El elemento **Navigate** especifica una dirección URL que usan las llamadas a **external. NavigateTaskPaneURL**.</span><span class="sxs-lookup"><span data-stu-id="9b447-109">The **Navigate** element specifies a URL used by calls to **External.NavigateTaskPaneURL**.</span></span>

``` syntax
<Navigate
    BaseURL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="9b447-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="9b447-110">Attributes</span></span>



| <span data-ttu-id="9b447-111">Término</span><span class="sxs-lookup"><span data-stu-id="9b447-111">Term</span></span>                                                                                                                                             | <span data-ttu-id="9b447-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b447-112">Description</span></span>                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b447-113"><span id="BaseURL__required_"></span><span id="baseurl__required_"></span><span id="BASEURL__REQUIRED_"></span>**Baseurl** (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="9b447-113"><span id="BaseURL__required_"></span><span id="baseurl__required_"></span><span id="BASEURL__REQUIRED_"></span>**BaseURL** (required)</span></span><br/> | <span data-ttu-id="9b447-114">Dirección URL completa de la página web a la que se va a navegar.</span><span class="sxs-lookup"><span data-stu-id="9b447-114">Fully qualified URL for the webpage to which to navigate.</span></span> <span data-ttu-id="9b447-115">**NavigateTaskPaneURL** puede anexar una cadena de consulta a esta dirección URL.</span><span class="sxs-lookup"><span data-stu-id="9b447-115">**NavigateTaskPaneURL** can append a query string to this URL.</span></span><br/> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="9b447-116">Elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="9b447-116">Parent/Child Elements</span></span>



| <span data-ttu-id="9b447-117">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="9b447-117">Hierarchy</span></span>       | <span data-ttu-id="9b447-118">Elemento</span><span class="sxs-lookup"><span data-stu-id="9b447-118">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="9b447-119">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="9b447-119">Parent elements</span></span> | <span data-ttu-id="9b447-120">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="9b447-120">**ServiceInfo**</span></span> |
| <span data-ttu-id="9b447-121">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9b447-121">Child elements</span></span>  | <span data-ttu-id="9b447-122">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9b447-122">None</span></span>            |



 

## <a name="requirements"></a><span data-ttu-id="9b447-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b447-123">Requirements</span></span>



| <span data-ttu-id="9b447-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b447-124">Requirement</span></span> | <span data-ttu-id="9b447-125">Value</span><span class="sxs-lookup"><span data-stu-id="9b447-125">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="9b447-126">Versión</span><span class="sxs-lookup"><span data-stu-id="9b447-126">Version</span></span><br/> | <span data-ttu-id="9b447-127">Windows Media Player 10 o posterior.</span><span class="sxs-lookup"><span data-stu-id="9b447-127">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9b447-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="9b447-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b447-129">**Ejemplo de documento ServiceInfo para una tienda en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="9b447-129">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="9b447-130">**Ejemplo de documento ServiceInfo para una tienda en línea de tipo 2**</span><span class="sxs-lookup"><span data-stu-id="9b447-130">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="9b447-131">**External. NavigateTaskPaneURL**</span><span class="sxs-lookup"><span data-stu-id="9b447-131">**External.NavigateTaskPaneURL**</span></span>](external-navigatetaskpaneurl.md)
</dt> <dt>

[<span data-ttu-id="9b447-132">**Documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="9b447-132">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





