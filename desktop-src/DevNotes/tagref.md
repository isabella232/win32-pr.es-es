---
description: Contiene el índice de una entrada y su información de etiqueta en una base de datos de correcciones de compatibilidad (shim).
ms.assetid: e7d83dca-13a5-4396-b50b-0d068209c03c
title: TAGREF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8631811f101850b68bdbad1097c19b9a41737bd2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538517"
---
# <a name="tagref"></a><span data-ttu-id="24f67-103">TAGREF</span><span class="sxs-lookup"><span data-stu-id="24f67-103">TAGREF</span></span>

<span data-ttu-id="24f67-104">Contiene el índice de una entrada y su información de etiqueta en una base de datos de correcciones de compatibilidad (shim).</span><span class="sxs-lookup"><span data-stu-id="24f67-104">Contains the index of an entry and its TAG information in a shim database.</span></span>


```C++
typedef DWORD TAGREF;
```



## <a name="remarks"></a><span data-ttu-id="24f67-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="24f67-105">Remarks</span></span>

<span data-ttu-id="24f67-106">Una **TAGREF** es específica de una base de datos de corrección de compatibilidad y es válida en varias bases de datos.</span><span class="sxs-lookup"><span data-stu-id="24f67-106">A **TAGREF** is specific to a shim database and valid across multiple databases.</span></span> <span data-ttu-id="24f67-107">Puede ser un valor entero que represente el índice, o uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="24f67-107">It can be an integer value that represents the index, or one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="24f67-108"><span id="TAGREF_NULL__0_"></span><span id="tagref_null__0_"></span>TAGREF \_ null (0)</span><span class="sxs-lookup"><span data-stu-id="24f67-108"><span id="TAGREF_NULL__0_"></span><span id="tagref_null__0_"></span>TAGREF\_NULL (0)</span></span>
</dt> <dd>

<span data-ttu-id="24f67-109">El **TAGREF** no existe.</span><span class="sxs-lookup"><span data-stu-id="24f67-109">The **TAGREF** does not exist.</span></span> <span data-ttu-id="24f67-110">Este valor se devuelve de una función cuando no puede devolver un **TAGREF** válido.</span><span class="sxs-lookup"><span data-stu-id="24f67-110">This value is returned from a function when it cannot return a valid **TAGREF**.</span></span>

</dd> <dt>

<span data-ttu-id="24f67-111"><span id="TAGREF_ROOT__0_"></span><span id="tagref_root__0_"></span>\_Raíz TAGREF (0)</span><span class="sxs-lookup"><span data-stu-id="24f67-111"><span id="TAGREF_ROOT__0_"></span><span id="tagref_root__0_"></span>TAGREF\_ROOT (0)</span></span>
</dt> <dd>

<span data-ttu-id="24f67-112">Indica una etiqueta de lista raíz que se puede usar como elemento primario para obtener un **TAGREF** secundario.</span><span class="sxs-lookup"><span data-stu-id="24f67-112">Indicates a root list TAG that can be used as a parent to obtain a child **TAGREF**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="24f67-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24f67-113">Requirements</span></span>



| <span data-ttu-id="24f67-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="24f67-114">Requirement</span></span> | <span data-ttu-id="24f67-115">Value</span><span class="sxs-lookup"><span data-stu-id="24f67-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="24f67-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="24f67-116">Minimum supported client</span></span><br/> | <span data-ttu-id="24f67-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="24f67-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="24f67-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="24f67-118">Minimum supported server</span></span><br/> | <span data-ttu-id="24f67-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="24f67-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="24f67-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="24f67-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24f67-121">**SdbTagRefToTagID**</span><span class="sxs-lookup"><span data-stu-id="24f67-121">**SdbTagRefToTagID**</span></span>](sdbtagreftotagid.md)
</dt> <dt>

[<span data-ttu-id="24f67-122">**ETIQUETA**</span><span class="sxs-lookup"><span data-stu-id="24f67-122">**TAG**</span></span>](tag.md)
</dt> <dt>

[<span data-ttu-id="24f67-123">Tipos de etiquetas</span><span class="sxs-lookup"><span data-stu-id="24f67-123">TAG Types</span></span>](tag-types.md)
</dt> <dt>

[<span data-ttu-id="24f67-124">**TAGID**</span><span class="sxs-lookup"><span data-stu-id="24f67-124">**TAGID**</span></span>](tagid.md)
</dt> </dl>

 

 




