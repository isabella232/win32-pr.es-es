---
description: Contiene los datos de atributo de un archivo.
ms.assetid: f23f801c-826c-4269-bf96-0e01430484f4
title: Estructura ATTRINFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ATTRINFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 01c061330db3e97989e0700452fd4a205488a9fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103906964"
---
# <a name="attrinfo-structure"></a><span data-ttu-id="1f046-103">Estructura ATTRINFO</span><span class="sxs-lookup"><span data-stu-id="1f046-103">ATTRINFO structure</span></span>

<span data-ttu-id="1f046-104">Contiene los datos de atributo de un archivo.</span><span class="sxs-lookup"><span data-stu-id="1f046-104">Contains the attribute data for a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f046-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1f046-105">Syntax</span></span>


```C++
typedef struct tagATTRINFO {
  TAG   tAttrID;
  DWORD dwFlags;
  union {
    ULONGLONG ullAttr;
    DWORD     dwAttr;
    TCHAR     *lpAttr;
  };
} ATTRINFO, *PATTRINFO;
```



## <a name="members"></a><span data-ttu-id="1f046-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="1f046-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1f046-107">**tAttrID**</span><span class="sxs-lookup"><span data-stu-id="1f046-107">**tAttrID**</span></span>
</dt> <dd>

<span data-ttu-id="1f046-108">Tipo de atributo.</span><span class="sxs-lookup"><span data-stu-id="1f046-108">The attribute type.</span></span> <span data-ttu-id="1f046-109">Vea [tipos de etiqueta](tag-types.md).</span><span class="sxs-lookup"><span data-stu-id="1f046-109">See [TAG Types](tag-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f046-110">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="1f046-110">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="1f046-111">Marcas para este atributo.</span><span class="sxs-lookup"><span data-stu-id="1f046-111">The flags for this attribute.</span></span>



| <span data-ttu-id="1f046-112">Value</span><span class="sxs-lookup"><span data-stu-id="1f046-112">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="1f046-113">Significado</span><span class="sxs-lookup"><span data-stu-id="1f046-113">Meaning</span></span>                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="ATTRIBUTE_AVAILABLE"></span><span id="attribute_available"></span><dl> <span data-ttu-id="1f046-114"><dt>**Atributo \_ de DISPONIBLE**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="1f046-114"><dt>**ATTRIBUTE\_AVAILABLE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="1f046-115">El atributo está disponible.</span><span class="sxs-lookup"><span data-stu-id="1f046-115">The attribute is available.</span></span><br/>                             |
| <span id="ATTRIBUTE_FAILED"></span><span id="attribute_failed"></span><dl> <span data-ttu-id="1f046-116"><dt>**Atributo \_ de ERROR**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="1f046-116"><dt>**ATTRIBUTE\_FAILED**</dt> <dt>0x00000002</dt></span></span> </dl>          | <span data-ttu-id="1f046-117">Error en la llamada porque el atributo no está disponible.</span><span class="sxs-lookup"><span data-stu-id="1f046-117">The call failed because the attribute is not available.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1f046-118">**ullAttr**</span><span class="sxs-lookup"><span data-stu-id="1f046-118">**ullAttr**</span></span>
</dt> <dd>

<span data-ttu-id="1f046-119">Un valor **QWord** (si el tipo de etiqueta es el **tipo de etiqueta \_ \_ QWord**).</span><span class="sxs-lookup"><span data-stu-id="1f046-119">A **QWORD** value (if the tag type is **TAG\_TYPE\_QWORD**).</span></span>

</dd> <dt>

<span data-ttu-id="1f046-120">**dwAttr**</span><span class="sxs-lookup"><span data-stu-id="1f046-120">**dwAttr**</span></span>
</dt> <dd>

<span data-ttu-id="1f046-121">Valor **DWORD** (si el tipo de etiqueta es **el \_ tipo \_ de etiqueta DWORD**).</span><span class="sxs-lookup"><span data-stu-id="1f046-121">A **DWORD** value (if the tag type is **TAG\_TYPE\_DWORD**).</span></span>

</dd> <dt>

<span data-ttu-id="1f046-122">**lpAttr**</span><span class="sxs-lookup"><span data-stu-id="1f046-122">**lpAttr**</span></span>
</dt> <dd>

<span data-ttu-id="1f046-123">Un puntero a una cadena (si el tipo de etiqueta es el **tipo de etiqueta \_ \_ STRINGREF**).</span><span class="sxs-lookup"><span data-stu-id="1f046-123">A pointer to a string (if the tag type is **TAG\_TYPE\_STRINGREF**).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1f046-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f046-124">Requirements</span></span>



| <span data-ttu-id="1f046-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f046-125">Requirement</span></span> | <span data-ttu-id="1f046-126">Value</span><span class="sxs-lookup"><span data-stu-id="1f046-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1f046-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1f046-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1f046-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1f046-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1f046-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1f046-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1f046-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1f046-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1f046-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="1f046-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f046-132">**SdbFormatAttribute**</span><span class="sxs-lookup"><span data-stu-id="1f046-132">**SdbFormatAttribute**</span></span>](sdbformatattribute.md)
</dt> <dt>

[<span data-ttu-id="1f046-133">**SdbFreeFileAttributes**</span><span class="sxs-lookup"><span data-stu-id="1f046-133">**SdbFreeFileAttributes**</span></span>](sdbfreefileattributes.md)
</dt> <dt>

[<span data-ttu-id="1f046-134">**SdbGetFileAttributes**</span><span class="sxs-lookup"><span data-stu-id="1f046-134">**SdbGetFileAttributes**</span></span>](sdbgetfileattributes.md)
</dt> </dl>

 

 




