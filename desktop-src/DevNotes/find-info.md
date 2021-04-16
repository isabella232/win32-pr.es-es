---
description: Contiene información de contexto de búsqueda.
ms.assetid: 4b865563-98c2-459b-bb2b-75420d51d6a7
title: Estructura de FIND_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FIND_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 7d6b6dea42c008178c22f6e342a64b2f8d193ec5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659381"
---
# <a name="find_info-structure"></a><span data-ttu-id="cf61f-103">BUSCAR \_ estructura de información</span><span class="sxs-lookup"><span data-stu-id="cf61f-103">FIND\_INFO structure</span></span>

<span data-ttu-id="cf61f-104">Contiene información de contexto de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="cf61f-104">Contains search context information.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf61f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cf61f-105">Syntax</span></span>


```C++
typedef struct _FIND_INFO {
  TAGID     tiIndex;
  TAGID     tiCurrent;
  TAGID     tiEndIndex;
  TAG       tName;
  DWORD     dwIndexRec;
  DWORD     dwFlags;
  ULONGLONG ullKey;
  union {
    LPCTSTR szName;
    DWORD   dwName;
    GUID    *pguidName;
  };
} FIND_INFO, *PFIND_INFO;
```



## <a name="members"></a><span data-ttu-id="cf61f-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="cf61f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="cf61f-107">**tiIndex**</span><span class="sxs-lookup"><span data-stu-id="cf61f-107">**tiIndex**</span></span>
</dt> <dd>

<span data-ttu-id="cf61f-108">**TAGID** del índice que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="cf61f-108">The **TAGID** for the index to be searched.</span></span>

</dd> <dt>

<span data-ttu-id="cf61f-109">**tiCurrent**</span><span class="sxs-lookup"><span data-stu-id="cf61f-109">**tiCurrent**</span></span>
</dt> <dd>

<span data-ttu-id="cf61f-110">**TAGID** del elemento actual que se encontró.</span><span class="sxs-lookup"><span data-stu-id="cf61f-110">The **TAGID** for the current item that was located.</span></span>

</dd> <dt>

<span data-ttu-id="cf61f-111">**tiEndIndex**</span><span class="sxs-lookup"><span data-stu-id="cf61f-111">**tiEndIndex**</span></span>
</dt> <dd>

<span data-ttu-id="cf61f-112">El **TAGID** del último registro después de FindFirst si el índice es único.</span><span class="sxs-lookup"><span data-stu-id="cf61f-112">The **TAGID** for the last record after FindFirst if the index is UNIQUE.</span></span>

</dd> <dt>

<span data-ttu-id="cf61f-113">**tName**</span><span class="sxs-lookup"><span data-stu-id="cf61f-113">**tName**</span></span>
</dt> <dd>

<span data-ttu-id="cf61f-114">Tipo del elemento que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="cf61f-114">The type of the item to be located.</span></span> <span data-ttu-id="cf61f-115">Vea [tipos de etiqueta](tag-types.md).</span><span class="sxs-lookup"><span data-stu-id="cf61f-115">See [TAG Types](tag-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf61f-116">**dwIndexRec**</span><span class="sxs-lookup"><span data-stu-id="cf61f-116">**dwIndexRec**</span></span>
</dt> <dd>

<span data-ttu-id="cf61f-117">Contador interno que se usa para realizar un seguimiento del lugar en el que debe comenzar la siguiente operación de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="cf61f-117">An internal counter used to track where in the index the next find operation should start.</span></span>

</dd> <dt>

<span data-ttu-id="cf61f-118">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="cf61f-118">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="cf61f-119">Este miembro puede ser 0 o **SHIMDB \_ \_ Unique index \_ key** (0x00000001), lo que indica que se trata de un índice de clave única.</span><span class="sxs-lookup"><span data-stu-id="cf61f-119">This member can be 0 or **SHIMDB\_INDEX\_UNIQUE\_KEY** (0x00000001), which indicates that this is a unique-key index.</span></span>

</dd> <dt>

<span data-ttu-id="cf61f-120">**ullKey**</span><span class="sxs-lookup"><span data-stu-id="cf61f-120">**ullKey**</span></span>
</dt> <dd>

<span data-ttu-id="cf61f-121">Clave de la entrada actual.</span><span class="sxs-lookup"><span data-stu-id="cf61f-121">The key for the current entry.</span></span>

</dd> <dt>

<span data-ttu-id="cf61f-122">**szName**</span><span class="sxs-lookup"><span data-stu-id="cf61f-122">**szName**</span></span>
</dt> <dd>

<span data-ttu-id="cf61f-123">La cadena actual (si el tipo de etiqueta es el **tipo de etiqueta \_ \_ STRINGREF**).</span><span class="sxs-lookup"><span data-stu-id="cf61f-123">The current string (if the tag type is **TAG\_TYPE\_STRINGREF**).</span></span>

</dd> <dt>

<span data-ttu-id="cf61f-124">**dwName**</span><span class="sxs-lookup"><span data-stu-id="cf61f-124">**dwName**</span></span>
</dt> <dd>

<span data-ttu-id="cf61f-125">Valor **DWORD** actual (si el tipo de etiqueta es **el \_ tipo \_ de etiqueta DWORD**).</span><span class="sxs-lookup"><span data-stu-id="cf61f-125">The current **DWORD** value (if the tag type is **TAG\_TYPE\_DWORD**).</span></span>

</dd> <dt>

<span data-ttu-id="cf61f-126">**pguidName**</span><span class="sxs-lookup"><span data-stu-id="cf61f-126">**pguidName**</span></span>
</dt> <dd>

<span data-ttu-id="cf61f-127">El valor GUID actual (si el tipo de etiqueta es el **tipo de etiqueta \_ \_ Binary** y la etiqueta es **tag \_ Database \_ ID**).</span><span class="sxs-lookup"><span data-stu-id="cf61f-127">The current GUID value (if the tag type is **TAG\_TYPE\_BINARY** and the TAG is **TAG\_DATABASE\_ID**).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cf61f-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf61f-128">Requirements</span></span>



| <span data-ttu-id="cf61f-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf61f-129">Requirement</span></span> | <span data-ttu-id="cf61f-130">Value</span><span class="sxs-lookup"><span data-stu-id="cf61f-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cf61f-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cf61f-131">Minimum supported client</span></span><br/> | <span data-ttu-id="cf61f-132">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cf61f-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cf61f-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cf61f-133">Minimum supported server</span></span><br/> | <span data-ttu-id="cf61f-134">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="cf61f-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cf61f-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="cf61f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf61f-136">**SdbFindFirstDWORDIndexedTag**</span><span class="sxs-lookup"><span data-stu-id="cf61f-136">**SdbFindFirstDWORDIndexedTag**</span></span>](sdbfindfirstdwordindexedtag.md)
</dt> </dl>

 

 




