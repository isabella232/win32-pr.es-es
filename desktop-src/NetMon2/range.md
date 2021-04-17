---
description: La estructura RANGE define un intervalo de valores de propiedad válidos.
ms.assetid: 7bd14410-f5c1-487b-8776-405567991e5a
title: Estructura de intervalo (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RANGE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: bf465636f315e60e43350bb370e2002b8a96e635
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666989"
---
# <a name="range-structure"></a><span data-ttu-id="8c109-103">Estructura de rango</span><span class="sxs-lookup"><span data-stu-id="8c109-103">RANGE structure</span></span>

<span data-ttu-id="8c109-104">La estructura **Range** define un intervalo de valores de propiedad válidos.</span><span class="sxs-lookup"><span data-stu-id="8c109-104">The **RANGE** structure defines a range of valid property values.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c109-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8c109-105">Syntax</span></span>


```C++
typedef struct range {
  DWORD MinValue;
  DWORD MaxValue;
} RANGE, *LPRANGE;
```



## <a name="members"></a><span data-ttu-id="8c109-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="8c109-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8c109-107">**MinValue**</span><span class="sxs-lookup"><span data-stu-id="8c109-107">**MinValue**</span></span>
</dt> <dd>

<span data-ttu-id="8c109-108">Menor valor posible de un intervalo.</span><span class="sxs-lookup"><span data-stu-id="8c109-108">Lowest possible value in a range.</span></span>

</dd> <dt>

<span data-ttu-id="8c109-109">**MaxValue**</span><span class="sxs-lookup"><span data-stu-id="8c109-109">**MaxValue**</span></span>
</dt> <dd>

<span data-ttu-id="8c109-110">Mayor valor posible de un intervalo.</span><span class="sxs-lookup"><span data-stu-id="8c109-110">Highest possible value in a range.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8c109-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8c109-111">Remarks</span></span>

<span data-ttu-id="8c109-112">La estructura de **intervalo** se usa para especificar un intervalo válido de números para una propiedad de protocolo.</span><span class="sxs-lookup"><span data-stu-id="8c109-112">The **RANGE** structure is used to specify a valid range of numbers for a protocol property.</span></span> <span data-ttu-id="8c109-113">Si el miembro de **Qualifier** de la estructura **PropertyInfo** está establecido en **props \_ \_ Range**, el miembro **lpRange** de la estructura [PropertyInfo](propertyinfo.md) debe proporcionar un puntero a una estructura de **intervalo** .</span><span class="sxs-lookup"><span data-stu-id="8c109-113">If the **DataQualifier** member of the **PROPERTYINFO** structure is set to **PROP\_QUAL\_RANGE**, the **lpRange** member of the [PROPERTYINFO](propertyinfo.md) structure must provide a pointer to a **RANGE** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c109-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c109-114">Requirements</span></span>



| <span data-ttu-id="8c109-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c109-115">Requirement</span></span> | <span data-ttu-id="8c109-116">Value</span><span class="sxs-lookup"><span data-stu-id="8c109-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8c109-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c109-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8c109-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8c109-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8c109-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c109-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8c109-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8c109-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8c109-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8c109-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c109-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c109-122"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c109-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c109-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c109-124">PROPERTYINFO</span><span class="sxs-lookup"><span data-stu-id="8c109-124">PROPERTYINFO</span></span>](propertyinfo.md)
</dt> </dl>

 

 




