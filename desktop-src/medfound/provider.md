---
description: Especifica un proveedor de seguimiento (ETW o WPP) para MFTrace.
ms.assetid: 692cce3b-ebf5-4a49-8c37-48c8ef6caee7
title: provider (elemento)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56ca319b686101766dacd79821ac6d9caf859cf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811575"
---
# <a name="provider-element"></a><span data-ttu-id="86c47-103">provider (elemento)</span><span class="sxs-lookup"><span data-stu-id="86c47-103">provider element</span></span>

<span data-ttu-id="86c47-104">Especifica un proveedor de seguimiento (ETW o WPP) para [MFTrace](mftrace.md).</span><span class="sxs-lookup"><span data-stu-id="86c47-104">Specifies a trace provider (ETW or WPP) for [MFTrace](mftrace.md).</span></span>

## <a name="usage"></a><span data-ttu-id="86c47-105">Uso</span><span class="sxs-lookup"><span data-stu-id="86c47-105">Usage</span></span>

``` syntax
<provider
  ID = "CDATA"
  level = "CDATA">
  child elements
</provider>
```

## <a name="attributes"></a><span data-ttu-id="86c47-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="86c47-106">Attributes</span></span>



| <span data-ttu-id="86c47-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="86c47-107">Attribute</span></span>            | <span data-ttu-id="86c47-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="86c47-108">Type</span></span>             | <span data-ttu-id="86c47-109">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="86c47-109">Required</span></span>       | <span data-ttu-id="86c47-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="86c47-110">Description</span></span>                                              |
|----------------------|------------------|----------------|----------------------------------------------------------|
| <span data-ttu-id="86c47-111">**Id**</span><span class="sxs-lookup"><span data-stu-id="86c47-111">**ID**</span></span><br/>    | <span data-ttu-id="86c47-112">CDATA</span><span class="sxs-lookup"><span data-stu-id="86c47-112">CDATA</span></span><br/> | <span data-ttu-id="86c47-113">Sí</span><span class="sxs-lookup"><span data-stu-id="86c47-113">Yes</span></span><br/> | <span data-ttu-id="86c47-114">El nombre o GUID del proveedor.</span><span class="sxs-lookup"><span data-stu-id="86c47-114">The name or GUID of the provider.</span></span><br/> <br/> |
| <span data-ttu-id="86c47-115">**level**</span><span class="sxs-lookup"><span data-stu-id="86c47-115">**level**</span></span><br/> | <span data-ttu-id="86c47-116">CDATA</span><span class="sxs-lookup"><span data-stu-id="86c47-116">CDATA</span></span><br/> | <span data-ttu-id="86c47-117">Sí</span><span class="sxs-lookup"><span data-stu-id="86c47-117">Yes</span></span><br/> | <span data-ttu-id="86c47-118">Nivel de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="86c47-118">The trace level.</span></span><br/> <br/>                  |



## <a name="child-elements"></a><span data-ttu-id="86c47-119">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="86c47-119">Child elements</span></span>



| <span data-ttu-id="86c47-120">Elemento</span><span class="sxs-lookup"><span data-stu-id="86c47-120">Element</span></span>                               |
|---------------------------------------|
| [<span data-ttu-id="86c47-121">**palabra clave**</span><span class="sxs-lookup"><span data-stu-id="86c47-121">**keyword**</span></span>](keyword.md)<br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="86c47-122">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="86c47-122">Child element sequence</span></span>

``` syntax
keyword+
```

## <a name="parent-elements"></a><span data-ttu-id="86c47-123">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="86c47-123">Parent elements</span></span>



| <span data-ttu-id="86c47-124">Elemento</span><span class="sxs-lookup"><span data-stu-id="86c47-124">Element</span></span>                                   |
|-------------------------------------------|
| [<span data-ttu-id="86c47-125">**providers**</span><span class="sxs-lookup"><span data-stu-id="86c47-125">**providers**</span></span>](providers.md)<br/> |



## <a name="element-information"></a><span data-ttu-id="86c47-126">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="86c47-126">Element information</span></span>



|              |     |
|--------------|-----|
| <span data-ttu-id="86c47-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="86c47-127">Can be empty</span></span> | <span data-ttu-id="86c47-128">No</span><span class="sxs-lookup"><span data-stu-id="86c47-128">No</span></span>  |



## <a name="see-also"></a><span data-ttu-id="86c47-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="86c47-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86c47-130">Archivo de configuración MFTrace</span><span class="sxs-lookup"><span data-stu-id="86c47-130">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)
</dt> </dl>

 

 




