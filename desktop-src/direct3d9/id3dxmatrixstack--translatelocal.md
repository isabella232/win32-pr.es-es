---
description: 'Método ID3DXMATRIXStack::TranslateLocal (D3dx9math.h): determina el producto de la matriz de traducción calculada determinada por los factores especificados (x, y y z) y la matriz actual.'
ms.assetid: d4752a6c-2114-4016-a69f-dcc561d2c76b
title: Método ID3DXMATRIXStack::TranslateLocal (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.TranslateLocal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b9badd4b01d1245247766c750e2a2ea1f266d9e1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107373"
---
# <a name="id3dxmatrixstacktranslatelocal-method-d3dx9mathh"></a><span data-ttu-id="66c3a-103">Método ID3DXMATRIXStack::TranslateLocal (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="66c3a-103">ID3DXMATRIXStack::TranslateLocal method (D3dx9math.h)</span></span>

<span data-ttu-id="66c3a-104">Determina el producto de la matriz de traducción calculada determinada por los factores especificados (x, y y z) y la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="66c3a-104">Determines the product of the computed translation matrix determined by the given factors (x, y, and z) and the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="66c3a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="66c3a-105">Syntax</span></span>


```C++
HRESULT TranslateLocal(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="66c3a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="66c3a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66c3a-107">*x* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="66c3a-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66c3a-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="66c3a-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="66c3a-109">Factor de traducción en la dirección X.</span><span class="sxs-lookup"><span data-stu-id="66c3a-109">The translation factor in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="66c3a-110">*y* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="66c3a-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66c3a-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="66c3a-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="66c3a-112">Factor de traducción en la dirección y.</span><span class="sxs-lookup"><span data-stu-id="66c3a-112">The translation factor in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="66c3a-113">*z* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="66c3a-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66c3a-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="66c3a-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="66c3a-115">Factor de traducción en la dirección Z.</span><span class="sxs-lookup"><span data-stu-id="66c3a-115">The translation factor in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66c3a-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="66c3a-116">Return value</span></span>

<span data-ttu-id="66c3a-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="66c3a-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="66c3a-118">Si el método se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="66c3a-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="66c3a-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="66c3a-119">Remarks</span></span>

<span data-ttu-id="66c3a-120">Este método multiplica a la izquierda la matriz actual con la matriz de traducción calculada (la transformación trata sobre el origen local del objeto).</span><span class="sxs-lookup"><span data-stu-id="66c3a-120">This method left-multiplies the current matrix with the computed translation matrix (transformation is about the local origin of the object).</span></span>


```
    
D3DXMATRIX tmp;
D3DXMatrixTranslation( &tmp, x, y, z );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



## <a name="requirements"></a><span data-ttu-id="66c3a-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66c3a-121">Requirements</span></span>



| <span data-ttu-id="66c3a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="66c3a-122">Requirement</span></span> | <span data-ttu-id="66c3a-123">Value</span><span class="sxs-lookup"><span data-stu-id="66c3a-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="66c3a-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="66c3a-124">Header</span></span><br/>  | <dl> <span data-ttu-id="66c3a-125"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="66c3a-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="66c3a-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="66c3a-126">Library</span></span><br/> | <dl> <span data-ttu-id="66c3a-127"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="66c3a-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="66c3a-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="66c3a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66c3a-129">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="66c3a-129">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="66c3a-130">**ID3DXMATRIXStack::Translate**</span><span class="sxs-lookup"><span data-stu-id="66c3a-130">**ID3DXMATRIXStack::Translate**</span></span>](id3dxmatrixstack--translate.md)
</dt> </dl>

 

 
