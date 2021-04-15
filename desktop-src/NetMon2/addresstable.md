---
description: La estructura ADDRESSTABLE contiene una tabla de pares de direcciones.
ms.assetid: 84577b6c-9d43-4e53-9f8d-33685329b11d
title: Estructura ADDRESSTABLE (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDRESSTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 41acab19f83fdcc88a384c0407b666a7f641a598
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497806"
---
# <a name="addresstable-structure"></a><span data-ttu-id="c2992-103">Estructura ADDRESSTABLE</span><span class="sxs-lookup"><span data-stu-id="c2992-103">ADDRESSTABLE structure</span></span>

<span data-ttu-id="c2992-104">La estructura **ADDRESSTABLE** contiene una tabla de pares de direcciones.</span><span class="sxs-lookup"><span data-stu-id="c2992-104">The **ADDRESSTABLE** structure contains a table of address pairs.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2992-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c2992-105">Syntax</span></span>


```C++
typedef struct _ADDRESSTABLE {
  DWORD       nAddressPairs;
  DWORD       nNonMacAddressPairs;
  ADDRESSPAIR AddressPair[MAX_ADDRESS_PAIRS];
} ADDRESSTABLE, *LPADDRESSTABLE;
```



## <a name="members"></a><span data-ttu-id="c2992-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="c2992-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c2992-107">**nAddressPairs**</span><span class="sxs-lookup"><span data-stu-id="c2992-107">**nAddressPairs**</span></span>
</dt> <dd>

<span data-ttu-id="c2992-108">Número de pares de direcciones en la matriz **AddressPair** .</span><span class="sxs-lookup"><span data-stu-id="c2992-108">Number of address pairs in the **AddressPair** array.</span></span>

</dd> <dt>

<span data-ttu-id="c2992-109">**nNonMacAddressPairs**</span><span class="sxs-lookup"><span data-stu-id="c2992-109">**nNonMacAddressPairs**</span></span>
</dt> <dd>

<span data-ttu-id="c2992-110">Número de pares de direcciones que no son MAC.</span><span class="sxs-lookup"><span data-stu-id="c2992-110">Number of non-MAC address pairs.</span></span>

</dd> <dt>

<span data-ttu-id="c2992-111">**AddressPair**</span><span class="sxs-lookup"><span data-stu-id="c2992-111">**AddressPair**</span></span>
</dt> <dd>

<span data-ttu-id="c2992-112">Matriz de pares de direcciones.</span><span class="sxs-lookup"><span data-stu-id="c2992-112">Array of address pairs.</span></span> <span data-ttu-id="c2992-113">Tenga en cuenta que solo puede almacenar hasta ocho pares de direcciones por estructura ADDRESSTABLE.</span><span class="sxs-lookup"><span data-stu-id="c2992-113">Note that you may only store up to eight address pairs per ADDRESSTABLE structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c2992-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c2992-114">Remarks</span></span>

<span data-ttu-id="c2992-115">Use esta estructura como parte del proceso de construcción del filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="c2992-115">Use this structure as part of the capture filter construction process.</span></span> <span data-ttu-id="c2992-116">Para obtener más información sobre la implementación de esta estructura, vea [Capture filters](capture-filters.md).</span><span class="sxs-lookup"><span data-stu-id="c2992-116">For more information about implementing this structure, see [Capture Filters](capture-filters.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c2992-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2992-117">Requirements</span></span>



| <span data-ttu-id="c2992-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2992-118">Requirement</span></span> | <span data-ttu-id="c2992-119">Value</span><span class="sxs-lookup"><span data-stu-id="c2992-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c2992-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2992-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c2992-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c2992-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c2992-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2992-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c2992-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c2992-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c2992-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c2992-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2992-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2992-125"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2992-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="c2992-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2992-127">ADDRESSPAIR</span><span class="sxs-lookup"><span data-stu-id="c2992-127">ADDRESSPAIR</span></span>](addresspair.md)
</dt> <dt>

[<span data-ttu-id="c2992-128">CAPTUREFILTER</span><span class="sxs-lookup"><span data-stu-id="c2992-128">CAPTUREFILTER</span></span>](capturefilter.md)
</dt> </dl>

 

 




