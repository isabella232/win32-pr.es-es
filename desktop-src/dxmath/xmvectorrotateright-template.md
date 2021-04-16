---
description: Gira el vector a la derecha un número determinado de elementos de 32 bits.
ms.assetid: 7493c1fe-2c3d-4eb6-bec1-02c066a70b9f
title: Plantilla XMVectorRotateRight (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa2c4e623a75015e8051a5a9ccf32f4715016b73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650179"
---
# <a name="xmvectorrotateright-template"></a><span data-ttu-id="fb888-103">Plantilla XMVectorRotateRight</span><span class="sxs-lookup"><span data-stu-id="fb888-103">XMVectorRotateRight template</span></span>

<span data-ttu-id="fb888-104">Gira el vector a la derecha un número determinado de elementos de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="fb888-104">Rotates the vector right by a given number of 32-bit elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb888-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fb888-105">Syntax</span></span>

``` syntax
template<uint32_t Elements> XMVECTOR XMVectorRotateRight(
  [in]  XMVECTOR V
);
```

## <a name="parameters"></a><span data-ttu-id="fb888-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fb888-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb888-107"><span id="V"></span><span id="v"></span>*V*</span><span class="sxs-lookup"><span data-stu-id="fb888-107"><span id="V"></span><span id="v"></span>*V*</span></span>
</dt> <dd>

<span data-ttu-id="fb888-108">\[en \] vector para girar a la derecha.</span><span class="sxs-lookup"><span data-stu-id="fb888-108">\[in\] Vector to rotate right.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb888-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fb888-109">Return Value</span></span>

<span data-ttu-id="fb888-110">Devuelve el [**XMVECTOR**](xmvector-data-type.md)girado.</span><span class="sxs-lookup"><span data-stu-id="fb888-110">Returns the rotated [**XMVECTOR**](xmvector-data-type.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fb888-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fb888-111">Remarks</span></span>

<span data-ttu-id="fb888-112">Esta función es una versión de plantilla de [**XMVectorRotateRight**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateright) , donde el argumento *Elements* es un valor de plantilla.</span><span class="sxs-lookup"><span data-stu-id="fb888-112">This function is a template version of [**XMVectorRotateRight**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateright) where the *Elements* argument is a template value.</span></span>

> [!Note]  
> <span data-ttu-id="fb888-113">La `XMVectorRotateRight` plantilla es nueva para DirectXMath y no está disponible para XNAMath 2. x.</span><span class="sxs-lookup"><span data-stu-id="fb888-113">The `XMVectorRotateRight` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span>

 

<span data-ttu-id="fb888-114">**Espacio de nombres**: usar DirectX</span><span class="sxs-lookup"><span data-stu-id="fb888-114">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="fb888-115">Requisitos de la plataforma</span><span class="sxs-lookup"><span data-stu-id="fb888-115">Platform Requirements</span></span>

<span data-ttu-id="fb888-116">Microsoft Visual Studio 2010 o Microsoft Visual Studio 2012 con el Windows SDK para Windows 8.</span><span class="sxs-lookup"><span data-stu-id="fb888-116">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="fb888-117">Se admite para aplicaciones de escritorio de Win32, aplicaciones de la tienda Windows y Windows Phone 8 aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="fb888-117">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb888-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb888-118">Requirements</span></span>



| <span data-ttu-id="fb888-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb888-119">Requirement</span></span> | <span data-ttu-id="fb888-120">Value</span><span class="sxs-lookup"><span data-stu-id="fb888-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb888-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fb888-121">Header</span></span><br/> | <dl> <span data-ttu-id="fb888-122"><dt>DirectXMath. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb888-122"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb888-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="fb888-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb888-124">Funciones de plantilla de la biblioteca de DirectXMath</span><span class="sxs-lookup"><span data-stu-id="fb888-124">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="fb888-125">**XMVectorPermute**</span><span class="sxs-lookup"><span data-stu-id="fb888-125">**XMVectorPermute**</span></span>](xmvectorpermute-template.md)
</dt> <dt>

[<span data-ttu-id="fb888-126">**XMVectorRotateLeft**</span><span class="sxs-lookup"><span data-stu-id="fb888-126">**XMVectorRotateLeft**</span></span>](xmvectorrotateleft-template.md)
</dt> <dt>

[<span data-ttu-id="fb888-127">**XMVectorShiftLeft**</span><span class="sxs-lookup"><span data-stu-id="fb888-127">**XMVectorShiftLeft**</span></span>](xmvectorshiftleft-template.md)
</dt> </dl>

 

 
