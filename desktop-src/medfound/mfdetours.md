---
description: Especifica el proveedor Microsoft Media Foundation Detours, que hace un seguimiento Media Foundation llamadas API.
ms.assetid: 7c9abda9-7968-463c-b4a9-19b54012ef56
title: elemento mfdetours
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cd03711c74c21a9a6ff33d2cc2560e4b6d6e0a3
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119340"
---
# <a name="mfdetours-element"></a><span data-ttu-id="6f38f-103">elemento mfdetours</span><span class="sxs-lookup"><span data-stu-id="6f38f-103">mfdetours element</span></span>

<span data-ttu-id="6f38f-104">Especifica el proveedor Microsoft Media Foundation Detours, que hace un seguimiento Media Foundation llamadas API.</span><span class="sxs-lookup"><span data-stu-id="6f38f-104">Specifies the Microsoft Media Foundation Detours provider, which traces Media Foundation API calls.</span></span>

## <a name="usage"></a><span data-ttu-id="6f38f-105">Uso</span><span class="sxs-lookup"><span data-stu-id="6f38f-105">Usage</span></span>

``` syntax
<mfdetours
  level = "CDATA">
  child elements
</mfdetours>
```

## <a name="attributes"></a><span data-ttu-id="6f38f-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="6f38f-106">Attributes</span></span>



| <span data-ttu-id="6f38f-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="6f38f-107">Attribute</span></span>            | <span data-ttu-id="6f38f-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="6f38f-108">Type</span></span>             | <span data-ttu-id="6f38f-109">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="6f38f-109">Required</span></span>       | <span data-ttu-id="6f38f-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="6f38f-110">Description</span></span>                             |
|----------------------|------------------|----------------|-----------------------------------------|
| <span data-ttu-id="6f38f-111">**level**</span><span class="sxs-lookup"><span data-stu-id="6f38f-111">**level**</span></span><br/> | <span data-ttu-id="6f38f-112">CDATA</span><span class="sxs-lookup"><span data-stu-id="6f38f-112">CDATA</span></span><br/> | <span data-ttu-id="6f38f-113">Sí</span><span class="sxs-lookup"><span data-stu-id="6f38f-113">Yes</span></span><br/> | <span data-ttu-id="6f38f-114">Nivel de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="6f38f-114">The trace level.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="6f38f-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6f38f-115">Child elements</span></span>



| <span data-ttu-id="6f38f-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="6f38f-116">Element</span></span>                               |
|---------------------------------------|
| [<span data-ttu-id="6f38f-117">**Palabra clave**</span><span class="sxs-lookup"><span data-stu-id="6f38f-117">**keyword**</span></span>](keyword.md)<br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="6f38f-118">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6f38f-118">Child element sequence</span></span>

``` syntax
keyword+
```

## <a name="parent-elements"></a><span data-ttu-id="6f38f-119">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="6f38f-119">Parent elements</span></span>

| <span data-ttu-id="6f38f-120">Elemento</span><span class="sxs-lookup"><span data-stu-id="6f38f-120">Element</span></span>                                   |
|-------------------------------------------|
| [<span data-ttu-id="6f38f-121">**Proveedores**</span><span class="sxs-lookup"><span data-stu-id="6f38f-121">**providers**</span></span>](providers.md)<br/> |



## <a name="element-information"></a><span data-ttu-id="6f38f-122">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="6f38f-122">Element information</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="6f38f-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6f38f-123">Can be empty</span></span>
    :::column-end:::
    :::column span="2":::
        <span data-ttu-id="6f38f-124">No</span><span class="sxs-lookup"><span data-stu-id="6f38f-124">No</span></span>
    :::column-end:::
:::row-end:::

## <a name="see-also"></a><span data-ttu-id="6f38f-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6f38f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f38f-126">Archivo de configuración de MFTrace</span><span class="sxs-lookup"><span data-stu-id="6f38f-126">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)
</dt> </dl>

 

 




