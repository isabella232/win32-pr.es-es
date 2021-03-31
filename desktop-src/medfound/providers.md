---
description: Contiene una lista de proveedores de seguimiento para MFTrace.
ms.assetid: ee483f0a-5a90-4150-ada4-0b63ae312523
title: elemento Providers
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04e5aaedcd14d840cfdc0d85559f6a7981943593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275822"
---
# <a name="providers-element"></a><span data-ttu-id="2233c-103">elemento Providers</span><span class="sxs-lookup"><span data-stu-id="2233c-103">providers element</span></span>

<span data-ttu-id="2233c-104">Contiene una lista de proveedores de seguimiento para [MFTrace](mftrace.md).</span><span class="sxs-lookup"><span data-stu-id="2233c-104">Contains a list of trace providers for [MFTrace](mftrace.md).</span></span>

## <a name="usage"></a><span data-ttu-id="2233c-105">Uso</span><span class="sxs-lookup"><span data-stu-id="2233c-105">Usage</span></span>

``` syntax
<providers>
  child elements
</providers>
```

## <a name="attributes"></a><span data-ttu-id="2233c-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="2233c-106">Attributes</span></span>

<span data-ttu-id="2233c-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="2233c-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="2233c-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2233c-108">Child elements</span></span>



| <span data-ttu-id="2233c-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="2233c-109">Element</span></span>                                   | <span data-ttu-id="2233c-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="2233c-110">Description</span></span>                                                                                                      |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2233c-111">**mfdetours**</span><span class="sxs-lookup"><span data-stu-id="2233c-111">**mfdetours**</span></span>](mfdetours.md)<br/> | <span data-ttu-id="2233c-112">Especifica el proveedor de desvío de Media Foundation, que realiza un seguimiento de las llamadas a la API Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="2233c-112">Specifies the Media Foundation Detours provider, which traces Media Foundation API calls.</span></span><br/> <br/> |
| [<span data-ttu-id="2233c-113">**presta**</span><span class="sxs-lookup"><span data-stu-id="2233c-113">**provider**</span></span>](provider.md)<br/>   | <span data-ttu-id="2233c-114">Especifica un proveedor de seguimiento (ETW o WPP).</span><span class="sxs-lookup"><span data-stu-id="2233c-114">Specifies a trace provider (ETW or WPP).</span></span><br/> <br/>                                                  |



### <a name="child-element-sequence"></a><span data-ttu-id="2233c-115">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2233c-115">Child element sequence</span></span>

``` syntax
(
  mfdetours?, 
  provider*
)
```

## <a name="parent-elements"></a><span data-ttu-id="2233c-116">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="2233c-116">Parent elements</span></span>

<span data-ttu-id="2233c-117">No hay elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2233c-117">There are no parent elements.</span></span>

## <a name="element-information"></a><span data-ttu-id="2233c-118">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="2233c-118">Element information</span></span>



|              |     |
|--------------|-----|
| <span data-ttu-id="2233c-119">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2233c-119">Can be empty</span></span> | <span data-ttu-id="2233c-120">Sí</span><span class="sxs-lookup"><span data-stu-id="2233c-120">Yes</span></span> |



## <a name="see-also"></a><span data-ttu-id="2233c-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2233c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2233c-122">Archivo de configuración MFTrace</span><span class="sxs-lookup"><span data-stu-id="2233c-122">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)
</dt> </dl>

 

 




