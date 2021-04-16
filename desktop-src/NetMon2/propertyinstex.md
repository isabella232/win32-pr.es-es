---
description: La estructura PROPERTYINSTEX define una instancia de la propiedad extendida y de forma libre.
ms.assetid: a2316baf-07e2-4617-bb35-e20cfb11fbcb
title: Estructura PROPERTYINSTEX (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROPERTYINSTEX
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: f7b196d30e96f9d047f7f923d969d65a918aa4f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677329"
---
# <a name="propertyinstex-structure"></a><span data-ttu-id="aab71-103">Estructura PROPERTYINSTEX</span><span class="sxs-lookup"><span data-stu-id="aab71-103">PROPERTYINSTEX structure</span></span>

<span data-ttu-id="aab71-104">La estructura **PROPERTYINSTEX** define una instancia de la propiedad extendida y de forma libre.</span><span class="sxs-lookup"><span data-stu-id="aab71-104">The **PROPERTYINSTEX** structure defines a freeform, extended property instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="aab71-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aab71-105">Syntax</span></span>


```C++
typedef struct _PROPERTYINSTEX {
  WORD    Length;
  WORD    LengthEx;
  ULPVOID lpData;
  union {
    BYTE          Byte[];
    WORD          Word[];
    DWORD         Dword[];
    LARGE_INTEGER LargeInt[];
    SYSTEMTIME    SysTime[];
    TYPED_STRING  TypedString;
  };
} PROPERTYINSTEX;
```



## <a name="members"></a><span data-ttu-id="aab71-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="aab71-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="aab71-107">**Duración**</span><span class="sxs-lookup"><span data-stu-id="aab71-107">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="aab71-108">Longitud de los datos en bytes.</span><span class="sxs-lookup"><span data-stu-id="aab71-108">Length of the data in Bytes.</span></span>

</dd> <dt>

<span data-ttu-id="aab71-109">**LengthEx**</span><span class="sxs-lookup"><span data-stu-id="aab71-109">**LengthEx**</span></span>
</dt> <dd>

<span data-ttu-id="aab71-110">Longitud de los datos extendidos.</span><span class="sxs-lookup"><span data-stu-id="aab71-110">Length of the extended data.</span></span>

</dd> <dt>

<span data-ttu-id="aab71-111">**lpData**</span><span class="sxs-lookup"><span data-stu-id="aab71-111">**lpData**</span></span>
</dt> <dd>

<span data-ttu-id="aab71-112">Puntero a los datos extendidos.</span><span class="sxs-lookup"><span data-stu-id="aab71-112">Pointer to the extended data.</span></span>

</dd> <dt>

<span data-ttu-id="aab71-113">**Byte**</span><span class="sxs-lookup"><span data-stu-id="aab71-113">**Byte**</span></span>
</dt> <dd>

<span data-ttu-id="aab71-114">Puntero a los datos de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="aab71-114">Pointer to the **BYTE** data.</span></span>

</dd> <dt>

<span data-ttu-id="aab71-115">**Word**</span><span class="sxs-lookup"><span data-stu-id="aab71-115">**Word**</span></span>
</dt> <dd>

<span data-ttu-id="aab71-116">Puntero a los datos de la **palabra** .</span><span class="sxs-lookup"><span data-stu-id="aab71-116">Pointer to the **WORD** data.</span></span>

</dd> <dt>

<span data-ttu-id="aab71-117">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="aab71-117">**Dword**</span></span>
</dt> <dd>

<span data-ttu-id="aab71-118">Puntero a los datos **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="aab71-118">Pointer to the **DWORD** data.</span></span>

</dd> <dt>

<span data-ttu-id="aab71-119">**LargeInt**</span><span class="sxs-lookup"><span data-stu-id="aab71-119">**LargeInt**</span></span>
</dt> <dd>

<span data-ttu-id="aab71-120">Puntero a los datos de **LARGEINT** .</span><span class="sxs-lookup"><span data-stu-id="aab71-120">Pointer to the **LARGEINT** data.</span></span>

</dd> <dt>

<span data-ttu-id="aab71-121">**SysTime**</span><span class="sxs-lookup"><span data-stu-id="aab71-121">**SysTime**</span></span>
</dt> <dd>

<span data-ttu-id="aab71-122">Puntero a los datos **SYSTEMTIME** .</span><span class="sxs-lookup"><span data-stu-id="aab71-122">Pointer to the **SYSTEMTIME** data.</span></span>

</dd> <dt>

<span data-ttu-id="aab71-123">**TypedString**</span><span class="sxs-lookup"><span data-stu-id="aab71-123">**TypedString**</span></span>
</dt> <dd>

<span data-ttu-id="aab71-124">Cadena con tipo que puede tener datos extendidos.</span><span class="sxs-lookup"><span data-stu-id="aab71-124">A typed string that may have extended data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aab71-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aab71-125">Requirements</span></span>



| <span data-ttu-id="aab71-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="aab71-126">Requirement</span></span> | <span data-ttu-id="aab71-127">Value</span><span class="sxs-lookup"><span data-stu-id="aab71-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="aab71-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aab71-128">Minimum supported client</span></span><br/> | <span data-ttu-id="aab71-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="aab71-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="aab71-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aab71-130">Minimum supported server</span></span><br/> | <span data-ttu-id="aab71-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="aab71-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="aab71-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aab71-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="aab71-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="aab71-133"><dt>Netmon.h</dt></span></span> </dl> |



 

 




