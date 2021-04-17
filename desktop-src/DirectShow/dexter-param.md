---
description: Especifica el valor que supone una propiedad en un momento dado.
ms.assetid: 117868b7-65e5-4b3b-9e50-4106ee6a65d0
title: DEXTER_PARAM estructura (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEXTER_PARAM
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 22b0f6ef0a91f9a6d9163a03c17f6e86ee8b5f4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653724"
---
# <a name="dexter_param-structure"></a><span data-ttu-id="40066-103">Estructura del parámetro DEXTERity \_</span><span class="sxs-lookup"><span data-stu-id="40066-103">DEXTER\_PARAM structure</span></span>

> [!Note]  
> <span data-ttu-id="40066-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="40066-104">\[Deprecated.</span></span> <span data-ttu-id="40066-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="40066-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="40066-106">Especifica el valor que supone una propiedad en un momento dado.</span><span class="sxs-lookup"><span data-stu-id="40066-106">Specifies the value that a property assumes at a given time.</span></span>

## <a name="syntax"></a><span data-ttu-id="40066-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="40066-107">Syntax</span></span>


```C++
typedef struct {
  BSTR   Name;
  DISPID dispID;
  LONG   nValues;
} DEXTER_PARAM;
```



## <a name="members"></a><span data-ttu-id="40066-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="40066-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="40066-109">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="40066-109">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="40066-110">Nombre de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="40066-110">Name of the property.</span></span>

</dd> <dt>

<span data-ttu-id="40066-111">**dispID**</span><span class="sxs-lookup"><span data-stu-id="40066-111">**dispID**</span></span>
</dt> <dd>

<span data-ttu-id="40066-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="40066-112">Reserved.</span></span> <span data-ttu-id="40066-113">Establecer en cero.</span><span class="sxs-lookup"><span data-stu-id="40066-113">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="40066-114">**Nvalores**</span><span class="sxs-lookup"><span data-stu-id="40066-114">**nValues**</span></span>
</dt> <dd>

<span data-ttu-id="40066-115">Número de valores que asume la propiedad.</span><span class="sxs-lookup"><span data-stu-id="40066-115">Number of values that the property assumes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="40066-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="40066-116">Remarks</span></span>

<span data-ttu-id="40066-117">El objeto debe admitir la interfaz **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="40066-117">The object must support the **IDispatch** interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="40066-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40066-118">Requirements</span></span>



| <span data-ttu-id="40066-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="40066-119">Requirement</span></span> | <span data-ttu-id="40066-120">Value</span><span class="sxs-lookup"><span data-stu-id="40066-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="40066-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="40066-121">Header</span></span><br/> | <dl> <span data-ttu-id="40066-122"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="40066-122"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40066-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="40066-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40066-124">**IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="40066-124">**IPropertySetter**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="40066-125">**valor de DEXTERity \_**</span><span class="sxs-lookup"><span data-stu-id="40066-125">**DEXTER\_VALUE**</span></span>](dexter-value.md)
</dt> </dl>

 

 




