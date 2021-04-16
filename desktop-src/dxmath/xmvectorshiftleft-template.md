---
description: Desplaza un vector a la izquierda de un número determinado de elementos de 32 bits y rellena los elementos vacantes con elementos de un segundo vector.
ms.assetid: m:microsoft.directx_sdk.template.xmvectorshiftleft(xmvector,xmvector)
title: Plantilla XMVectorShiftLeft (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 115604871d9e8402157a82bf3c420e5762b3a424
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649892"
---
# <a name="xmvectorshiftleft-template"></a><span data-ttu-id="ba8c8-103">Plantilla XMVectorShiftLeft</span><span class="sxs-lookup"><span data-stu-id="ba8c8-103">XMVectorShiftLeft template</span></span>

<span data-ttu-id="ba8c8-104">Desplaza un vector a la izquierda de un número determinado de elementos de 32 bits y rellena los elementos vacantes con elementos de un segundo vector.</span><span class="sxs-lookup"><span data-stu-id="ba8c8-104">Shifts a vector left by a given number of 32-bit elements, filling the vacated elements with elements from a second vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba8c8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ba8c8-105">Syntax</span></span>

``` syntax
template<uint32_t Elements> XMVECTOR XMVectorShiftLeft(
  [in]  XMVECTOR V1,
  [in]  XMVECTOR V2
);
```

## <a name="parameters"></a><span data-ttu-id="ba8c8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ba8c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba8c8-107"><span id="V1"></span><span id="v1"></span>*V1*</span><span class="sxs-lookup"><span data-stu-id="ba8c8-107"><span id="V1"></span><span id="v1"></span>*V1*</span></span>
</dt> <dd>

<span data-ttu-id="ba8c8-108">\[en \] vector para desplazarse a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="ba8c8-108">\[in\] Vector to shift left.</span></span>

</dd> <dt>

<span data-ttu-id="ba8c8-109"><span id="V2"></span><span id="v2"></span>*2*</span><span class="sxs-lookup"><span data-stu-id="ba8c8-109"><span id="V2"></span><span id="v2"></span>*V2*</span></span>
</dt> <dd>

<span data-ttu-id="ba8c8-110">\[en \] Vector se usa para rellenar los componentes vacantes de v1 después de desplazarse a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="ba8c8-110">\[in\] Vector used to fill in the vacated components of V1 after it is shifted left.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba8c8-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ba8c8-111">Return Value</span></span>

<span data-ttu-id="ba8c8-112">Devuelve el desplazado y rellenado en [**XMVECTOR**](xmvector-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="ba8c8-112">Returns the shifted and filled in [**XMVECTOR**](xmvector-data-type.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ba8c8-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ba8c8-113">Remarks</span></span>

<span data-ttu-id="ba8c8-114">Esta función es una versión de plantilla de [**XMVectorShiftLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorshiftleft) , donde el argumento *Elements* es un valor de plantilla.</span><span class="sxs-lookup"><span data-stu-id="ba8c8-114">This function is a template version of [**XMVectorShiftLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorshiftleft) where the *Elements* argument is a template value.</span></span>

> [!Note]  
> <span data-ttu-id="ba8c8-115">La `XMVectorShiftLeft` plantilla es nueva para DirectXMath y no está disponible para XNAMath 2. x.</span><span class="sxs-lookup"><span data-stu-id="ba8c8-115">The `XMVectorShiftLeft` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span>

 

<span data-ttu-id="ba8c8-116">**Espacio de nombres**: usar DirectX</span><span class="sxs-lookup"><span data-stu-id="ba8c8-116">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="ba8c8-117">Requisitos de la plataforma</span><span class="sxs-lookup"><span data-stu-id="ba8c8-117">Platform Requirements</span></span>

<span data-ttu-id="ba8c8-118">Microsoft Visual Studio 2010 o Microsoft Visual Studio 2012 con el Windows SDK para Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ba8c8-118">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="ba8c8-119">Se admite para aplicaciones de escritorio de Win32, aplicaciones de la tienda Windows y Windows Phone 8 aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="ba8c8-119">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba8c8-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba8c8-120">Requirements</span></span>



| <span data-ttu-id="ba8c8-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba8c8-121">Requirement</span></span> | <span data-ttu-id="ba8c8-122">Value</span><span class="sxs-lookup"><span data-stu-id="ba8c8-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba8c8-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ba8c8-123">Header</span></span><br/> | <dl> <span data-ttu-id="ba8c8-124"><dt>DirectXMath. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba8c8-124"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba8c8-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="ba8c8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba8c8-126">Funciones de plantilla de la biblioteca de DirectXMath</span><span class="sxs-lookup"><span data-stu-id="ba8c8-126">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="ba8c8-127">**XMVectorPermute**</span><span class="sxs-lookup"><span data-stu-id="ba8c8-127">**XMVectorPermute**</span></span>](xmvectorpermute-template.md)
</dt> <dt>

[<span data-ttu-id="ba8c8-128">**XMVectorRotateLeft**</span><span class="sxs-lookup"><span data-stu-id="ba8c8-128">**XMVectorRotateLeft**</span></span>](xmvectorrotateleft-template.md)
</dt> <dt>

[<span data-ttu-id="ba8c8-129">**XMVectorRotateRight**</span><span class="sxs-lookup"><span data-stu-id="ba8c8-129">**XMVectorRotateRight**</span></span>](xmvectorrotateright-template.md)
</dt> </dl>

 

 
