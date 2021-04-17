---
description: Determina el producto de la matriz actual y la matriz de traslación calculada determinada por los factores especificados (x, y y z).
ms.assetid: e0ac72a2-9970-433e-9026-aa79edc8261c
title: 'ID3DXMATRIXStack:: translate (método) (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Translate
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 228b4302a512e96d5c009edcb3f0b673ee61e047
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708123"
---
# <a name="id3dxmatrixstacktranslate-method-d3dx9mathh"></a><span data-ttu-id="baedb-103">ID3DXMATRIXStack:: translate (método) (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="baedb-103">ID3DXMATRIXStack::Translate method (D3dx9math.h)</span></span>

<span data-ttu-id="baedb-104">Determina el producto de la matriz actual y la matriz de traslación calculada determinada por los factores especificados (x, y y z).</span><span class="sxs-lookup"><span data-stu-id="baedb-104">Determines the product of the current matrix and the computed translation matrix determined by the given factors (x, y, and z).</span></span>

## <a name="syntax"></a><span data-ttu-id="baedb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="baedb-105">Syntax</span></span>


```C++
HRESULT Translate(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="baedb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="baedb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="baedb-107">*x* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="baedb-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="baedb-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="baedb-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="baedb-109">Factor de traslación en la dirección x.</span><span class="sxs-lookup"><span data-stu-id="baedb-109">The translation factor in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="baedb-110">*y* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="baedb-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="baedb-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="baedb-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="baedb-112">Factor de traslación en la dirección y.</span><span class="sxs-lookup"><span data-stu-id="baedb-112">The translation factor in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="baedb-113">*z* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="baedb-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="baedb-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="baedb-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="baedb-115">Factor de traslación en la dirección z.</span><span class="sxs-lookup"><span data-stu-id="baedb-115">The translation factor in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="baedb-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="baedb-116">Return value</span></span>

<span data-ttu-id="baedb-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="baedb-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="baedb-118">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="baedb-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="baedb-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="baedb-119">Remarks</span></span>

<span data-ttu-id="baedb-120">Este método multiplica la matriz actual con la matriz de traslación calculada (la transformación es sobre el origen mundial actual).</span><span class="sxs-lookup"><span data-stu-id="baedb-120">This method right-multiplies the current matrix with the computed translation matrix (transformation is about the current world origin).</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixTranslation( &tmp, x, y, z );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



## <a name="requirements"></a><span data-ttu-id="baedb-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="baedb-121">Requirements</span></span>



| <span data-ttu-id="baedb-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="baedb-122">Requirement</span></span> | <span data-ttu-id="baedb-123">Value</span><span class="sxs-lookup"><span data-stu-id="baedb-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="baedb-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="baedb-124">Header</span></span><br/>  | <dl> <span data-ttu-id="baedb-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="baedb-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="baedb-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="baedb-126">Library</span></span><br/> | <dl> <span data-ttu-id="baedb-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="baedb-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="baedb-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="baedb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="baedb-129">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="baedb-129">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="baedb-130">**ID3DXMATRIXStack::TranslateLocal**</span><span class="sxs-lookup"><span data-stu-id="baedb-130">**ID3DXMATRIXStack::TranslateLocal**</span></span>](id3dxmatrixstack--translatelocal.md)
</dt> </dl>

 

 
