---
description: Gira el vector a la izquierda un número determinado de elementos de 32 bits.
ms.assetid: ba3698ed-212d-4ef0-846a-4099d0e1abec
title: Plantilla XMVectorRotateLeft (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e5b52fccebeb93803fdc33346fa4ee5e873c1d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649896"
---
# <a name="xmvectorrotateleft-template"></a><span data-ttu-id="3df96-103">Plantilla XMVectorRotateLeft</span><span class="sxs-lookup"><span data-stu-id="3df96-103">XMVectorRotateLeft template</span></span>

<span data-ttu-id="3df96-104">Gira el vector a la izquierda un número determinado de elementos de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="3df96-104">Rotates the vector left by a given number of 32-bit elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="3df96-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3df96-105">Syntax</span></span>

``` syntax
template<uint32_t Elements> XMVECTOR XMVectorRotateLeft(
  [in]  XMVECTOR V
);
```

## <a name="parameters"></a><span data-ttu-id="3df96-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3df96-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3df96-107"><span id="V"></span><span id="v"></span>*V*</span><span class="sxs-lookup"><span data-stu-id="3df96-107"><span id="V"></span><span id="v"></span>*V*</span></span>
</dt> <dd>

<span data-ttu-id="3df96-108">\[en \] vector para girar a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="3df96-108">\[in\] Vector to rotate left.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3df96-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3df96-109">Return Value</span></span>

<span data-ttu-id="3df96-110">Devuelve el [**XMVECTOR**](xmvector-data-type.md)girado.</span><span class="sxs-lookup"><span data-stu-id="3df96-110">Returns the rotated [**XMVECTOR**](xmvector-data-type.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3df96-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3df96-111">Remarks</span></span>

<span data-ttu-id="3df96-112">Esta función es una versión de plantilla de [**XMVectorRotateLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateleft) , donde el argumento *Elements* es un valor de plantilla.</span><span class="sxs-lookup"><span data-stu-id="3df96-112">This function is a template version of [**XMVectorRotateLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateleft) where the *Elements* argument is a template value.</span></span>

> [!Note]  
> <span data-ttu-id="3df96-113">La `XMVectorRotateLeft` plantilla es nueva para DirectXMath y no está disponible para XNAMath 2. x.</span><span class="sxs-lookup"><span data-stu-id="3df96-113">The `XMVectorRotateLeft` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span>

 

<span data-ttu-id="3df96-114">**Espacio de nombres**: usar DirectX</span><span class="sxs-lookup"><span data-stu-id="3df96-114">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="3df96-115">Requisitos de la plataforma</span><span class="sxs-lookup"><span data-stu-id="3df96-115">Platform Requirements</span></span>

<span data-ttu-id="3df96-116">Microsoft Visual Studio 2010 o Microsoft Visual Studio 2012 con el Windows SDK para Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3df96-116">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="3df96-117">Se admite para aplicaciones de escritorio de Win32, aplicaciones de la tienda Windows y Windows Phone 8 aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="3df96-117">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="3df96-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3df96-118">Requirements</span></span>



| <span data-ttu-id="3df96-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3df96-119">Requirement</span></span> | <span data-ttu-id="3df96-120">Value</span><span class="sxs-lookup"><span data-stu-id="3df96-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3df96-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3df96-121">Header</span></span><br/> | <dl> <span data-ttu-id="3df96-122"><dt>DirectXMath. h</dt></span><span class="sxs-lookup"><span data-stu-id="3df96-122"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3df96-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="3df96-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3df96-124">Funciones de plantilla de la biblioteca de DirectXMath</span><span class="sxs-lookup"><span data-stu-id="3df96-124">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="3df96-125">**XMVectorPermute**</span><span class="sxs-lookup"><span data-stu-id="3df96-125">**XMVectorPermute**</span></span>](xmvectorpermute-template.md)
</dt> <dt>

[<span data-ttu-id="3df96-126">**XMVectorRotateRight**</span><span class="sxs-lookup"><span data-stu-id="3df96-126">**XMVectorRotateRight**</span></span>](xmvectorrotateright-template.md)
</dt> <dt>

[<span data-ttu-id="3df96-127">**XMVectorShiftLeft**</span><span class="sxs-lookup"><span data-stu-id="3df96-127">**XMVectorShiftLeft**</span></span>](xmvectorshiftleft-template.md)
</dt> </dl>

 

 
