---
description: Swizzles un vector.
ms.assetid: 75608e80-5911-45a8-beca-ceac1f4d2c1c
title: Plantilla XMVectorSwizzle (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8e872d76f3251eccc8616c143c645b388e2dca4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709238"
---
# <a name="xmvectorswizzle-template"></a><span data-ttu-id="07f41-103">Plantilla XMVectorSwizzle</span><span class="sxs-lookup"><span data-stu-id="07f41-103">XMVectorSwizzle template</span></span>

<span data-ttu-id="07f41-104">Swizzles un vector.</span><span class="sxs-lookup"><span data-stu-id="07f41-104">Swizzles a vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="07f41-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="07f41-105">Syntax</span></span>

``` syntax
template<uint32_t SwizzleX, uint32_t SwizzleY, uint32_t SwizzleZ, uint32_t SwizzleW> XMVECTOR XMVectorSwizzle(
  [in]  XMVECTOR V
);
```

## <a name="parameters"></a><span data-ttu-id="07f41-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="07f41-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07f41-107"><span id="V"></span><span id="v"></span>*V*</span><span class="sxs-lookup"><span data-stu-id="07f41-107"><span id="V"></span><span id="v"></span>*V*</span></span>
</dt> <dd>

<span data-ttu-id="07f41-108">\[en \] Vector a swizzle.</span><span class="sxs-lookup"><span data-stu-id="07f41-108">\[in\] Vector to swizzle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07f41-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="07f41-109">Return Value</span></span>

<span data-ttu-id="07f41-110">Devuelve swizzled [**XMVECTOR**](xmvector-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="07f41-110">Returns the swizzled [**XMVECTOR**](xmvector-data-type.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="07f41-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="07f41-111">Remarks</span></span>

<span data-ttu-id="07f41-112">Esta función es una versión de plantilla de [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) en la que los argumentos de *swizzle \** son valores de plantilla.</span><span class="sxs-lookup"><span data-stu-id="07f41-112">This function is a template version of [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) where the *Swizzle\** arguments are template values.</span></span>

<span data-ttu-id="07f41-113">`XM_SWIZZLE_X`, `XM_SWIZZLE_Y` , `XM_SWIZZLE_Z` y `XM_SWIZZLE_W` son constantes que se evalúan como 0, 1, 2 y 3, respectivamente, para su uso con `XMVectorSwizzle` .</span><span class="sxs-lookup"><span data-stu-id="07f41-113">`XM_SWIZZLE_X`, `XM_SWIZZLE_Y`, `XM_SWIZZLE_Z`, and `XM_SWIZZLE_W` are constants which evaluate to 0, 1, 2, and 3 respectively for use with `XMVectorSwizzle`.</span></span> <span data-ttu-id="07f41-114">Es idéntico a `XM_PERMUTE_0X` , `XM_PERMUTE_0Y` , `XM_PERMUTE_0Z` y `XM_PERMUTE_0W` .</span><span class="sxs-lookup"><span data-stu-id="07f41-114">This is identical to `XM_PERMUTE_0X`, `XM_PERMUTE_0Y`, `XM_PERMUTE_0Z`, and `XM_PERMUTE_0W`.</span></span>

> [!Note]  
> <span data-ttu-id="07f41-115">La `XMVectorSwizzle` plantilla es nueva para DirectXMath y no está disponible para XNAMath 2. x.</span><span class="sxs-lookup"><span data-stu-id="07f41-115">The `XMVectorSwizzle` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span>

 

<span data-ttu-id="07f41-116">**Espacio de nombres**: usar DirectX</span><span class="sxs-lookup"><span data-stu-id="07f41-116">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="07f41-117">Requisitos de la plataforma</span><span class="sxs-lookup"><span data-stu-id="07f41-117">Platform Requirements</span></span>

<span data-ttu-id="07f41-118">Microsoft Visual Studio 2010 o Microsoft Visual Studio 2012 con el Windows SDK para Windows 8.</span><span class="sxs-lookup"><span data-stu-id="07f41-118">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="07f41-119">Se admite para aplicaciones de escritorio de Win32, aplicaciones de la tienda Windows y Windows Phone 8 aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="07f41-119">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="07f41-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07f41-120">Requirements</span></span>



| <span data-ttu-id="07f41-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="07f41-121">Requirement</span></span> | <span data-ttu-id="07f41-122">Value</span><span class="sxs-lookup"><span data-stu-id="07f41-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="07f41-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="07f41-123">Header</span></span><br/> | <dl> <span data-ttu-id="07f41-124"><dt>DirectXMath. h</dt></span><span class="sxs-lookup"><span data-stu-id="07f41-124"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07f41-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="07f41-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07f41-126">Funciones de plantilla de la biblioteca de DirectXMath</span><span class="sxs-lookup"><span data-stu-id="07f41-126">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="07f41-127">**XMVectorPermute**</span><span class="sxs-lookup"><span data-stu-id="07f41-127">**XMVectorPermute**</span></span>](xmvectorpermute-template.md)
</dt> </dl>

 

 
