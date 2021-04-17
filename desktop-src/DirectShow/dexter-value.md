---
description: Identifica una propiedad que se va a establecer en una transición o efecto, junto con el número de valores distintos que la propiedad asume a lo largo de la transición o efecto.
ms.assetid: 3b1c35cf-f1f7-4f2c-8d94-1aaae4116833
title: DEXTER_VALUE estructura (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEXTER_VALUE
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 930b828e1b715cfcb53275192ed76a7df7d116ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680420"
---
# <a name="dexter_value-structure"></a><span data-ttu-id="bb506-103">Estructura del valor de DEXTERity \_</span><span class="sxs-lookup"><span data-stu-id="bb506-103">DEXTER\_VALUE structure</span></span>

> [!Note]  
> <span data-ttu-id="bb506-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="bb506-104">\[Deprecated.</span></span> <span data-ttu-id="bb506-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bb506-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="bb506-106">Identifica una propiedad que se va a establecer en una transición o efecto, junto con el número de valores distintos que la propiedad asume a lo largo de la transición o efecto.</span><span class="sxs-lookup"><span data-stu-id="bb506-106">Identifies a property that is to be set on a transition or effect, along with the number of distinct values that the property assumes over the duration of the transition or effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb506-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bb506-107">Syntax</span></span>


```C++
typedef struct {
  VARIANT        v;
  REFERENCE_TIME rt;
  DWORD          dwInterp;
} DEXTER_VALUE;
```



## <a name="members"></a><span data-ttu-id="bb506-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="bb506-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="bb506-109">**v**</span><span class="sxs-lookup"><span data-stu-id="bb506-109">**v**</span></span>
</dt> <dd>

<span data-ttu-id="bb506-110">Valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="bb506-110">Value of the property.</span></span>

</dd> <dt>

<span data-ttu-id="bb506-111">**RT**</span><span class="sxs-lookup"><span data-stu-id="bb506-111">**rt**</span></span>
</dt> <dd>

<span data-ttu-id="bb506-112">Hora a la que la propiedad asume el valor, en relación con el inicio de la transición o efecto.</span><span class="sxs-lookup"><span data-stu-id="bb506-112">Time at which the property assumes the value, relative to the start of the transition or effect.</span></span>

</dd> <dt>

<span data-ttu-id="bb506-113">**dwInterp**</span><span class="sxs-lookup"><span data-stu-id="bb506-113">**dwInterp**</span></span>
</dt> <dd>

<span data-ttu-id="bb506-114">Marca que indica cómo progresa la propiedad desde el valor anterior a este valor.</span><span class="sxs-lookup"><span data-stu-id="bb506-114">Flag indicating how the property progresses from the previous value to this value.</span></span> <span data-ttu-id="bb506-115">Debe ser una de las siguientes:</span><span class="sxs-lookup"><span data-stu-id="bb506-115">Must be one of the following:</span></span>



| <span data-ttu-id="bb506-116">Value</span><span class="sxs-lookup"><span data-stu-id="bb506-116">Value</span></span>                                                                                                                                                                           | <span data-ttu-id="bb506-117">Significado</span><span class="sxs-lookup"><span data-stu-id="bb506-117">Meaning</span></span>                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="DEXTERF_JUMP"></span><span id="dexterf_jump"></span><dl> <span data-ttu-id="bb506-118"><dt>**salto de DEXTERF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bb506-118"><dt>**DEXTERF\_JUMP**</dt></span></span> </dl>                      | <span data-ttu-id="bb506-119">La propiedad salta inmediatamente al nuevo valor en el momento especificado.</span><span class="sxs-lookup"><span data-stu-id="bb506-119">The property jumps instantly to the new value at the specified time.</span></span><br/>     |
| <span id="DEXTERF_INTERPOLATE"></span><span id="dexterf_interpolate"></span><dl> <span data-ttu-id="bb506-120"><dt>**DEXTERF \_ interpolación**</dt></span><span class="sxs-lookup"><span data-stu-id="bb506-120"><dt>**DEXTERF\_INTERPOLATE**</dt></span></span> </dl> | <span data-ttu-id="bb506-121">La propiedad se interpola linealmente a lo largo del tiempo desde el valor anterior.</span><span class="sxs-lookup"><span data-stu-id="bb506-121">The property is interpolated linearly over time from the previous value.</span></span><br/> |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bb506-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb506-122">Requirements</span></span>



| <span data-ttu-id="bb506-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb506-123">Requirement</span></span> | <span data-ttu-id="bb506-124">Value</span><span class="sxs-lookup"><span data-stu-id="bb506-124">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bb506-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bb506-125">Header</span></span><br/> | <dl> <span data-ttu-id="bb506-126"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb506-126"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb506-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb506-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb506-128">**IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="bb506-128">**IPropertySetter**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="bb506-129">**parámetro DEXTERity \_**</span><span class="sxs-lookup"><span data-stu-id="bb506-129">**DEXTER\_PARAM**</span></span>](dexter-param.md)
</dt> </dl>

 

 




