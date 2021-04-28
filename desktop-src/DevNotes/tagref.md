---
description: 'TAGREF: contiene el índice de una entrada y su información DE ETIQUETA en una base de datos de correcciones de compatibilidad (shim).'
ms.assetid: e7d83dca-13a5-4396-b50b-0d068209c03c
title: TAGREF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34e27a60847630e7bbd8e07ccf005dfd7b474d7a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096633"
---
# <a name="tagref"></a><span data-ttu-id="312b2-103">TAGREF</span><span class="sxs-lookup"><span data-stu-id="312b2-103">TAGREF</span></span>

<span data-ttu-id="312b2-104">Contiene el índice de una entrada y su información tag en una base de datos de correcciones de compatibilidad (shim).</span><span class="sxs-lookup"><span data-stu-id="312b2-104">Contains the index of an entry and its TAG information in a shim database.</span></span>


```C++
typedef DWORD TAGREF;
```



## <a name="remarks"></a><span data-ttu-id="312b2-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="312b2-105">Remarks</span></span>

<span data-ttu-id="312b2-106">Un **TAGREF es específico** de una base de datos shim y es válido en varias bases de datos.</span><span class="sxs-lookup"><span data-stu-id="312b2-106">A **TAGREF** is specific to a shim database and valid across multiple databases.</span></span> <span data-ttu-id="312b2-107">Puede ser un valor entero que representa el índice o uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="312b2-107">It can be an integer value that represents the index, or one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="312b2-108"><span id="TAGREF_NULL__0_"></span><span id="tagref_null__0_"></span>TAGREF \_ NULL (0)</span><span class="sxs-lookup"><span data-stu-id="312b2-108"><span id="TAGREF_NULL__0_"></span><span id="tagref_null__0_"></span>TAGREF\_NULL (0)</span></span>
</dt> <dd>

<span data-ttu-id="312b2-109">**TAGREF** no existe.</span><span class="sxs-lookup"><span data-stu-id="312b2-109">The **TAGREF** does not exist.</span></span> <span data-ttu-id="312b2-110">Este valor se devuelve de una función cuando no puede devolver un **TAGREF válido.**</span><span class="sxs-lookup"><span data-stu-id="312b2-110">This value is returned from a function when it cannot return a valid **TAGREF**.</span></span>

</dd> <dt>

<span data-ttu-id="312b2-111"><span id="TAGREF_ROOT__0_"></span><span id="tagref_root__0_"></span>TAGREF \_ ROOT (0)</span><span class="sxs-lookup"><span data-stu-id="312b2-111"><span id="TAGREF_ROOT__0_"></span><span id="tagref_root__0_"></span>TAGREF\_ROOT (0)</span></span>
</dt> <dd>

<span data-ttu-id="312b2-112">Indica una etiqueta de lista raíz que se puede usar como elemento primario para obtener un **ELEMENTO TAGREF secundario.**</span><span class="sxs-lookup"><span data-stu-id="312b2-112">Indicates a root list TAG that can be used as a parent to obtain a child **TAGREF**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="312b2-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="312b2-113">Requirements</span></span>



| <span data-ttu-id="312b2-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="312b2-114">Requirement</span></span> | <span data-ttu-id="312b2-115">Valor</span><span class="sxs-lookup"><span data-stu-id="312b2-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="312b2-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="312b2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="312b2-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="312b2-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="312b2-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="312b2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="312b2-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="312b2-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="312b2-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="312b2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="312b2-121">**SdbTagRefToTagID**</span><span class="sxs-lookup"><span data-stu-id="312b2-121">**SdbTagRefToTagID**</span></span>](sdbtagreftotagid.md)
</dt> <dt>

[<span data-ttu-id="312b2-122">**etiqueta**</span><span class="sxs-lookup"><span data-stu-id="312b2-122">**TAG**</span></span>](tag.md)
</dt> <dt>

[<span data-ttu-id="312b2-123">Tipos TAG</span><span class="sxs-lookup"><span data-stu-id="312b2-123">TAG Types</span></span>](tag-types.md)
</dt> <dt>

[<span data-ttu-id="312b2-124">**TAGID**</span><span class="sxs-lookup"><span data-stu-id="312b2-124">**TAGID**</span></span>](tagid.md)
</dt> </dl>

 

 




