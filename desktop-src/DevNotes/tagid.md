---
description: Contiene el índice de una entrada y su información de etiqueta en una base de datos de correcciones de compatibilidad (shim).
ms.assetid: 2ff58e01-cc47-4612-a3bc-a87ccb343bd2
title: TAGID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e7d8b8a25633d3505936d105b0eef7ed38746ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998177"
---
# <a name="tagid"></a><span data-ttu-id="e868f-103">TAGID</span><span class="sxs-lookup"><span data-stu-id="e868f-103">TAGID</span></span>

<span data-ttu-id="e868f-104">Contiene el índice de una entrada y su información de etiqueta en una base de datos de correcciones de compatibilidad (shim).</span><span class="sxs-lookup"><span data-stu-id="e868f-104">Contains the index of an entry and its TAG information in a shim database.</span></span>


```C++
typedef DWORD TAGID;
```



## <a name="remarks"></a><span data-ttu-id="e868f-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e868f-105">Remarks</span></span>

<span data-ttu-id="e868f-106">Un **TAGID** es específico de una base de datos.</span><span class="sxs-lookup"><span data-stu-id="e868f-106">A **TAGID** is specific to a database.</span></span> <span data-ttu-id="e868f-107">Puede ser un valor entero que represente el índice, o uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="e868f-107">It can be an integer value that represents the index, or one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="e868f-108"><span id="TAGID_NULL__0_"></span><span id="tagid_null__0_"></span>TAGID \_ null (0)</span><span class="sxs-lookup"><span data-stu-id="e868f-108"><span id="TAGID_NULL__0_"></span><span id="tagid_null__0_"></span>TAGID\_NULL (0)</span></span>
</dt> <dd>

<span data-ttu-id="e868f-109">El **TAGID** no existe.</span><span class="sxs-lookup"><span data-stu-id="e868f-109">The **TAGID** does not exist.</span></span> <span data-ttu-id="e868f-110">Este valor se devuelve de una función cuando no puede devolver un valor de **TAGID** válido.</span><span class="sxs-lookup"><span data-stu-id="e868f-110">This value is returned from a function when it cannot return a valid **TAGID**.</span></span>

</dd> <dt>

<span data-ttu-id="e868f-111"><span id="TAGID_ROOT__0_"></span><span id="tagid_root__0_"></span>Carpeta de TAGID \_ (0)</span><span class="sxs-lookup"><span data-stu-id="e868f-111"><span id="TAGID_ROOT__0_"></span><span id="tagid_root__0_"></span>TAGID\_ROOT (0)</span></span>
</dt> <dd>

<span data-ttu-id="e868f-112">Indica una etiqueta de lista raíz que se puede usar como elemento primario para obtener un **TAGID** secundario.</span><span class="sxs-lookup"><span data-stu-id="e868f-112">Indicates a root list TAG that can be used as a parent to obtain a child **TAGID**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e868f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e868f-113">Requirements</span></span>



| <span data-ttu-id="e868f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e868f-114">Requirement</span></span> | <span data-ttu-id="e868f-115">Value</span><span class="sxs-lookup"><span data-stu-id="e868f-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e868f-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e868f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e868f-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e868f-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e868f-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e868f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e868f-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e868f-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e868f-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="e868f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e868f-121">**ETIQUETA**</span><span class="sxs-lookup"><span data-stu-id="e868f-121">**TAG**</span></span>](tag.md)
</dt> <dt>

[<span data-ttu-id="e868f-122">Tipos de etiquetas</span><span class="sxs-lookup"><span data-stu-id="e868f-122">TAG Types</span></span>](tag-types.md)
</dt> <dt>

[<span data-ttu-id="e868f-123">**TAGREF**</span><span class="sxs-lookup"><span data-stu-id="e868f-123">**TAGREF**</span></span>](tagref.md)
</dt> </dl>

 

 




