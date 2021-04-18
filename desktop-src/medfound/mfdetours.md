---
description: Especifica el proveedor de desvío de Microsoft Media Foundation, que realiza un seguimiento de las llamadas a la API Media Foundation.
ms.assetid: 7c9abda9-7968-463c-b4a9-19b54012ef56
title: elemento mfdetours
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c09d39d6f8a7c7ff1d88471e71c6fc58aa49bd62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715368"
---
# <a name="mfdetours-element"></a><span data-ttu-id="22496-103">elemento mfdetours</span><span class="sxs-lookup"><span data-stu-id="22496-103">mfdetours element</span></span>

<span data-ttu-id="22496-104">Especifica el proveedor de desvío de Microsoft Media Foundation, que realiza un seguimiento de las llamadas a la API Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="22496-104">Specifies the Microsoft Media Foundation Detours provider, which traces Media Foundation API calls.</span></span>

## <a name="usage"></a><span data-ttu-id="22496-105">Uso</span><span class="sxs-lookup"><span data-stu-id="22496-105">Usage</span></span>

``` syntax
<mfdetours
  level = "CDATA">
  child elements
</mfdetours>
```

## <a name="attributes"></a><span data-ttu-id="22496-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="22496-106">Attributes</span></span>



| <span data-ttu-id="22496-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="22496-107">Attribute</span></span>            | <span data-ttu-id="22496-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="22496-108">Type</span></span>             | <span data-ttu-id="22496-109">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="22496-109">Required</span></span>       | <span data-ttu-id="22496-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="22496-110">Description</span></span>                             |
|----------------------|------------------|----------------|-----------------------------------------|
| <span data-ttu-id="22496-111">**level**</span><span class="sxs-lookup"><span data-stu-id="22496-111">**level**</span></span><br/> | <span data-ttu-id="22496-112">CDATA</span><span class="sxs-lookup"><span data-stu-id="22496-112">CDATA</span></span><br/> | <span data-ttu-id="22496-113">Sí</span><span class="sxs-lookup"><span data-stu-id="22496-113">Yes</span></span><br/> | <span data-ttu-id="22496-114">Nivel de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="22496-114">The trace level.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="22496-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="22496-115">Child elements</span></span>



| <span data-ttu-id="22496-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="22496-116">Element</span></span>                               |
|---------------------------------------|
| [<span data-ttu-id="22496-117">**palabra clave**</span><span class="sxs-lookup"><span data-stu-id="22496-117">**keyword**</span></span>](keyword.md)<br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="22496-118">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="22496-118">Child element sequence</span></span>

``` syntax
keyword+
```

## <a name="parent-elements"></a><span data-ttu-id="22496-119">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="22496-119">Parent elements</span></span>



| <span data-ttu-id="22496-120">Elemento</span><span class="sxs-lookup"><span data-stu-id="22496-120">Element</span></span>                                   |
|-------------------------------------------|
| [<span data-ttu-id="22496-121">**providers**</span><span class="sxs-lookup"><span data-stu-id="22496-121">**providers**</span></span>](providers.md)<br/> |



## <a name="element-information"></a><span data-ttu-id="22496-122">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="22496-122">Element information</span></span>



|              |     |
|--------------|-----|
| <span data-ttu-id="22496-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="22496-123">Can be empty</span></span> | <span data-ttu-id="22496-124">No</span><span class="sxs-lookup"><span data-stu-id="22496-124">No</span></span>  |



## <a name="see-also"></a><span data-ttu-id="22496-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="22496-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22496-126">Archivo de configuración MFTrace</span><span class="sxs-lookup"><span data-stu-id="22496-126">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)
</dt> </dl>

 

 




