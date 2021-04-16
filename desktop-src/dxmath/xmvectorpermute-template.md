---
description: Permute los componentes de dos vectores para crear un nuevo vector.
ms.assetid: m:microsoft.directx_sdk.template.xmvectorpermute(xmvector,xmvector)
title: Plantilla XMVectorPermute (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37271cbb165f1e9c1769ef3a55e47f1e07310a81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650180"
---
# <a name="xmvectorpermute-template"></a><span data-ttu-id="a3abf-103">Plantilla XMVectorPermute</span><span class="sxs-lookup"><span data-stu-id="a3abf-103">XMVectorPermute template</span></span>

<span data-ttu-id="a3abf-104">Permute los componentes de dos vectores para crear un nuevo vector.</span><span class="sxs-lookup"><span data-stu-id="a3abf-104">Permutes the components of two vectors to create a new vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3abf-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a3abf-105">Syntax</span></span>

``` syntax
template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW> XMVECTOR XMVectorPermute(
  [in]  XMVECTOR V1,
  [in]  XMVECTOR V2
);
```

## <a name="parameters"></a><span data-ttu-id="a3abf-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a3abf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3abf-107"><span id="V1"></span><span id="v1"></span>*V1*</span><span class="sxs-lookup"><span data-stu-id="a3abf-107"><span id="V1"></span><span id="v1"></span>*V1*</span></span>
</dt> <dd>

<span data-ttu-id="a3abf-108">\[en el \] primer vector.</span><span class="sxs-lookup"><span data-stu-id="a3abf-108">\[in\] First vector.</span></span>

</dd> <dt>

<span data-ttu-id="a3abf-109"><span id="V2"></span><span id="v2"></span>*2*</span><span class="sxs-lookup"><span data-stu-id="a3abf-109"><span id="V2"></span><span id="v2"></span>*V2*</span></span>
</dt> <dd>

<span data-ttu-id="a3abf-110">\[en el \] segundo vector.</span><span class="sxs-lookup"><span data-stu-id="a3abf-110">\[in\] Second vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3abf-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a3abf-111">Return Value</span></span>

<span data-ttu-id="a3abf-112">Devuelve el vector permuted que resultó de combinar los vectores de origen.</span><span class="sxs-lookup"><span data-stu-id="a3abf-112">Returns the permuted vector that resulted from combining the source vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3abf-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a3abf-113">Remarks</span></span>

<span data-ttu-id="a3abf-114">Si los 4 índices solo hacen referencia a un único vector (es decir, están todos en el intervalo 0-3 o todos en el intervalo 4-7), use [**XMVectorSwizzle**](xmvectorswizzle-template.md) en su lugar para mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="a3abf-114">If all 4 indices reference only a single vector (i.e. they are all in the range 0-3 or all in the range 4-7), use [**XMVectorSwizzle**](xmvectorswizzle-template.md) instead for better performance.</span></span>

<span data-ttu-id="a3abf-115">Tenga en cuenta que la biblioteca utiliza especializaciones de plantilla en algunas plataformas para mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="a3abf-115">Note the library makes use of template specializations on some platforms to improve performance.</span></span> <span data-ttu-id="a3abf-116">No se implementan todos los casos de reflejo posibles en estos casos especiales, por lo que es preferible que el elemento X del vector resultante proceda del parámetro V1 en lugar del parámetro V2.</span><span class="sxs-lookup"><span data-stu-id="a3abf-116">Not every possible mirror case is implemented for these special cases, so prefer permutes where the X element of the resulting vector comes from the V1 parameter rather than the V2 parameter.</span></span> <span data-ttu-id="a3abf-117">Por ejemplo, prefiere usar `XMVectorPermute<0,1,4,5>(A,B);` para `XMVectorPermute(4,5,0,1)(B,A);` .</span><span class="sxs-lookup"><span data-stu-id="a3abf-117">For example, prefer using `XMVectorPermute<0,1,4,5>(A,B);` to `XMVectorPermute(4,5,0,1)(B,A);`.</span></span>

<span data-ttu-id="a3abf-118">Esta función es una versión de plantilla de [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) en la que los argumentos *permute \** son valores de plantilla.</span><span class="sxs-lookup"><span data-stu-id="a3abf-118">This function is a template version of [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) where the *Permute\** arguments are template values.</span></span>

<span data-ttu-id="a3abf-119">Las constantes de [ \_ permute \_ de XM](ovw-xnamath-reference-constants.md) se proporcionan para usar como valores de entrada para *PERMUTEX*,*permutey*,*PermuteZ* y *PermuteW*.</span><span class="sxs-lookup"><span data-stu-id="a3abf-119">The [XM\_PERMUTE\_](ovw-xnamath-reference-constants.md) constants are provided to use as input values for *PermuteX*,*PermuteY*,*PermuteZ*, and *PermuteW*.</span></span>

> [!Note]  
> <span data-ttu-id="a3abf-120">La `XMVectorPermute` plantilla es nueva para DirectXMath y no está disponible para XNAMath 2. x.</span><span class="sxs-lookup"><span data-stu-id="a3abf-120">The `XMVectorPermute` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span>

 

<span data-ttu-id="a3abf-121">**Espacio de nombres**: usar DirectX</span><span class="sxs-lookup"><span data-stu-id="a3abf-121">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="a3abf-122">Requisitos de la plataforma</span><span class="sxs-lookup"><span data-stu-id="a3abf-122">Platform Requirements</span></span>

<span data-ttu-id="a3abf-123">Microsoft Visual Studio 2010 o Microsoft Visual Studio 2012 con el Windows SDK para Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a3abf-123">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="a3abf-124">Se admite para aplicaciones de escritorio de Win32, aplicaciones de la tienda Windows y Windows Phone 8 aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="a3abf-124">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3abf-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3abf-125">Requirements</span></span>



| <span data-ttu-id="a3abf-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3abf-126">Requirement</span></span> | <span data-ttu-id="a3abf-127">Value</span><span class="sxs-lookup"><span data-stu-id="a3abf-127">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3abf-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a3abf-128">Header</span></span><br/> | <dl> <span data-ttu-id="a3abf-129"><dt>DirectXMath. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3abf-129"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3abf-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="a3abf-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3abf-131">Funciones de plantilla de la biblioteca de DirectXMath</span><span class="sxs-lookup"><span data-stu-id="a3abf-131">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="a3abf-132">**XMVectorSwizzle**</span><span class="sxs-lookup"><span data-stu-id="a3abf-132">**XMVectorSwizzle**</span></span>](xmvectorswizzle-template.md)
</dt> </dl>

 

 
