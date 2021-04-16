---
description: Gira un vector a la izquierda un número determinado de componentes de 32 bits e inserta los elementos seleccionados de ese resultado en otro vector.
ms.assetid: m:microsoft.directx_sdk.template.xmvectorinsert(xmvector,xmvector)
title: Plantilla XMVectorInsert (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3250ad52ab19a127b110b02ecf71543f44708681
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649898"
---
# <a name="xmvectorinsert-template"></a><span data-ttu-id="0512c-103">Plantilla XMVectorInsert</span><span class="sxs-lookup"><span data-stu-id="0512c-103">XMVectorInsert template</span></span>

<span data-ttu-id="0512c-104">Gira un vector a la izquierda un número determinado de componentes de 32 bits e inserta los elementos seleccionados de ese resultado en otro vector.</span><span class="sxs-lookup"><span data-stu-id="0512c-104">Rotates a vector left by a given number of 32-bit components and insert selected elements of that result into another vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="0512c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0512c-105">Syntax</span></span>

``` syntax
template<uint32_t VSLeftRotateElements, uint32_t Select0, uint32_t Select1, uint32_t Select2, uint32_t Select3> XMVECTOR XMVectorInsert(
  [in]  XMVECTOR VD,
  [in]  XMVECTOR VS
);
```

## <a name="parameters"></a><span data-ttu-id="0512c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0512c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0512c-107"><span id="VD"></span><span id="vd"></span>*VD*</span><span class="sxs-lookup"><span data-stu-id="0512c-107"><span id="VD"></span><span id="vd"></span>*VD*</span></span>
</dt> <dd>

<span data-ttu-id="0512c-108">\[en \] vector para insertar en.</span><span class="sxs-lookup"><span data-stu-id="0512c-108">\[in\] Vector to insert into.</span></span>

</dd> <dt>

<span data-ttu-id="0512c-109"><span id="VS"></span><span id="vs"></span>*VIRTUAL*</span><span class="sxs-lookup"><span data-stu-id="0512c-109"><span id="VS"></span><span id="vs"></span>*VS*</span></span>
</dt> <dd>

<span data-ttu-id="0512c-110">\[en \] vector para girar a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="0512c-110">\[in\] Vector to rotate left.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0512c-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0512c-111">Return Value</span></span>

<span data-ttu-id="0512c-112">Devuelve el [**XMVECTOR**](xmvector-data-type.md) resultante de la rotación y la inserción.</span><span class="sxs-lookup"><span data-stu-id="0512c-112">Returns the [**XMVECTOR**](xmvector-data-type.md) that results from the rotation and insertion.</span></span>

## <a name="remarks"></a><span data-ttu-id="0512c-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0512c-113">Remarks</span></span>

<span data-ttu-id="0512c-114">Esta función es una versión de plantilla de [**XMVectorInsert**](/windows/win32/api/directxmath/nf-directxmath-xmvectorinsert) en la que los argumentos *SELECT \** son valores de plantilla.</span><span class="sxs-lookup"><span data-stu-id="0512c-114">This function is a template version of [**XMVectorInsert**](/windows/win32/api/directxmath/nf-directxmath-xmvectorinsert) where the *Select\** arguments are template values.</span></span>

<span data-ttu-id="0512c-115">Para obtener el mejor rendimiento, el resultado de `XMVectorInsert` debe asignarse de nuevo a *Vd*.</span><span class="sxs-lookup"><span data-stu-id="0512c-115">For best performance, the result of `XMVectorInsert` should be assigned back to *VD*.</span></span>

> [!Note]  
> <span data-ttu-id="0512c-116">La `XMVectorInsert` plantilla es nueva para DirectXMath y no está disponible para XNAMath 2. x.</span><span class="sxs-lookup"><span data-stu-id="0512c-116">The `XMVectorInsert` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span>

 

<span data-ttu-id="0512c-117">**Espacio de nombres**: usar DirectX</span><span class="sxs-lookup"><span data-stu-id="0512c-117">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="0512c-118">Requisitos de la plataforma</span><span class="sxs-lookup"><span data-stu-id="0512c-118">Platform Requirements</span></span>

<span data-ttu-id="0512c-119">Microsoft Visual Studio 2010 o Microsoft Visual Studio 2012 con el Windows SDK para Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0512c-119">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="0512c-120">Se admite para aplicaciones de escritorio de Win32, aplicaciones de la tienda Windows y Windows Phone 8 aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="0512c-120">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="0512c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0512c-121">Requirements</span></span>



| <span data-ttu-id="0512c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="0512c-122">Requirement</span></span> | <span data-ttu-id="0512c-123">Value</span><span class="sxs-lookup"><span data-stu-id="0512c-123">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0512c-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0512c-124">Header</span></span><br/> | <dl> <span data-ttu-id="0512c-125"><dt>DirectXMath. h</dt></span><span class="sxs-lookup"><span data-stu-id="0512c-125"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0512c-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="0512c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0512c-127">Funciones de plantilla de la biblioteca de DirectXMath</span><span class="sxs-lookup"><span data-stu-id="0512c-127">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="0512c-128">**XMVectorPermute**</span><span class="sxs-lookup"><span data-stu-id="0512c-128">**XMVectorPermute**</span></span>](xmvectorpermute-template.md)
</dt> <dt>

[<span data-ttu-id="0512c-129">**XMVectorRotateLeft**</span><span class="sxs-lookup"><span data-stu-id="0512c-129">**XMVectorRotateLeft**</span></span>](xmvectorrotateleft-template.md)
</dt> <dt>

[<span data-ttu-id="0512c-130">**XMVectorRotateRight**</span><span class="sxs-lookup"><span data-stu-id="0512c-130">**XMVectorRotateRight**</span></span>](xmvectorrotateright-template.md)
</dt> <dt>

[<span data-ttu-id="0512c-131">**XMVectorShiftLeft**</span><span class="sxs-lookup"><span data-stu-id="0512c-131">**XMVectorShiftLeft**</span></span>](xmvectorshiftleft-template.md)
</dt> </dl>

 

 
