---
description: Contiene una lista de proveedores de seguimiento para MFTrace.
ms.assetid: ee483f0a-5a90-4150-ada4-0b63ae312523
title: providers, elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d38a86bf3ca8ffa1ea9e3da20e0244e7abec8513
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118490"
---
# <a name="providers-element"></a><span data-ttu-id="54eb5-103">providers, elemento</span><span class="sxs-lookup"><span data-stu-id="54eb5-103">providers element</span></span>

<span data-ttu-id="54eb5-104">Contiene una lista de proveedores de seguimiento [para MFTrace.](mftrace.md)</span><span class="sxs-lookup"><span data-stu-id="54eb5-104">Contains a list of trace providers for [MFTrace](mftrace.md).</span></span>

## <a name="usage"></a><span data-ttu-id="54eb5-105">Uso</span><span class="sxs-lookup"><span data-stu-id="54eb5-105">Usage</span></span>

``` syntax
<providers>
  child elements
</providers>
```

## <a name="attributes"></a><span data-ttu-id="54eb5-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="54eb5-106">Attributes</span></span>

<span data-ttu-id="54eb5-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="54eb5-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="54eb5-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="54eb5-108">Child elements</span></span>



| <span data-ttu-id="54eb5-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="54eb5-109">Element</span></span>                                   | <span data-ttu-id="54eb5-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="54eb5-110">Description</span></span>                                                                                                      |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="54eb5-111">**mfdetours**</span><span class="sxs-lookup"><span data-stu-id="54eb5-111">**mfdetours**</span></span>](mfdetours.md)<br/> | <span data-ttu-id="54eb5-112">Especifica el proveedor Media Foundation Detours, que hace un seguimiento Media Foundation llamadas API.</span><span class="sxs-lookup"><span data-stu-id="54eb5-112">Specifies the Media Foundation Detours provider, which traces Media Foundation API calls.</span></span><br/> <br/> |
| [<span data-ttu-id="54eb5-113">**Proveedor**</span><span class="sxs-lookup"><span data-stu-id="54eb5-113">**provider**</span></span>](provider.md)<br/>   | <span data-ttu-id="54eb5-114">Especifica un proveedor de seguimiento (ETW o WPP).</span><span class="sxs-lookup"><span data-stu-id="54eb5-114">Specifies a trace provider (ETW or WPP).</span></span><br/> <br/>                                                  |



### <a name="child-element-sequence"></a><span data-ttu-id="54eb5-115">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="54eb5-115">Child element sequence</span></span>

``` syntax
(
  mfdetours?, 
  provider*
)
```

## <a name="parent-elements"></a><span data-ttu-id="54eb5-116">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="54eb5-116">Parent elements</span></span>

<span data-ttu-id="54eb5-117">No hay elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="54eb5-117">There are no parent elements.</span></span>

## <a name="element-information"></a><span data-ttu-id="54eb5-118">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="54eb5-118">Element information</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="54eb5-119">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="54eb5-119">Can be empty</span></span>
    :::column-end:::
    :::column span="2":::
        <span data-ttu-id="54eb5-120">Sí</span><span class="sxs-lookup"><span data-stu-id="54eb5-120">Yes</span></span>
    :::column-end:::
:::row-end:::

## <a name="see-also"></a><span data-ttu-id="54eb5-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="54eb5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54eb5-122">Archivo de configuración de MFTrace</span><span class="sxs-lookup"><span data-stu-id="54eb5-122">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)
</dt> </dl>

 

 




