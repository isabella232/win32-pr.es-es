---
description: Determina el producto de la matriz de traducción calculada determinada por los factores especificados (x, y y z) y la matriz actual.
ms.assetid: d4752a6c-2114-4016-a69f-dcc561d2c76b
title: 'ID3DXMATRIXStack:: TranslateLocal (método) (D3dx9math. h)'
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
ms.openlocfilehash: 784e623ae47dfece9b395d423437fb6ce661b223
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280400"
---
# <a name="id3dxmatrixstacktranslatelocal-method-d3dx9mathh"></a><span data-ttu-id="d82ef-103">ID3DXMATRIXStack:: TranslateLocal (método) (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="d82ef-103">ID3DXMATRIXStack::TranslateLocal method (D3dx9math.h)</span></span>

<span data-ttu-id="d82ef-104">Determina el producto de la matriz de traducción calculada determinada por los factores especificados (x, y y z) y la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="d82ef-104">Determines the product of the computed translation matrix determined by the given factors (x, y, and z) and the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="d82ef-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d82ef-105">Syntax</span></span>


```C++
HRESULT TranslateLocal(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="d82ef-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d82ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d82ef-107">*x* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="d82ef-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d82ef-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d82ef-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d82ef-109">Factor de traslación en la dirección x.</span><span class="sxs-lookup"><span data-stu-id="d82ef-109">The translation factor in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="d82ef-110">*y* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="d82ef-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d82ef-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d82ef-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d82ef-112">Factor de traslación en la dirección y.</span><span class="sxs-lookup"><span data-stu-id="d82ef-112">The translation factor in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="d82ef-113">*z* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="d82ef-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d82ef-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d82ef-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d82ef-115">Factor de traslación en la dirección z.</span><span class="sxs-lookup"><span data-stu-id="d82ef-115">The translation factor in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d82ef-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d82ef-116">Return value</span></span>

<span data-ttu-id="d82ef-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d82ef-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d82ef-118">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d82ef-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="d82ef-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d82ef-119">Remarks</span></span>

<span data-ttu-id="d82ef-120">Este método multiplica a la izquierda la matriz actual con la matriz de conversión calculada (la transformación es sobre el origen local del objeto).</span><span class="sxs-lookup"><span data-stu-id="d82ef-120">This method left-multiplies the current matrix with the computed translation matrix (transformation is about the local origin of the object).</span></span>


```
    
D3DXMATRIX tmp;
D3DXMatrixTranslation( &tmp, x, y, z );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



## <a name="requirements"></a><span data-ttu-id="d82ef-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d82ef-121">Requirements</span></span>



| <span data-ttu-id="d82ef-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d82ef-122">Requirement</span></span> | <span data-ttu-id="d82ef-123">Value</span><span class="sxs-lookup"><span data-stu-id="d82ef-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d82ef-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d82ef-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d82ef-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d82ef-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="d82ef-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d82ef-126">Library</span></span><br/> | <dl> <span data-ttu-id="d82ef-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d82ef-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d82ef-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="d82ef-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d82ef-129">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="d82ef-129">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="d82ef-130">**ID3DXMATRIXStack:: translate**</span><span class="sxs-lookup"><span data-stu-id="d82ef-130">**ID3DXMATRIXStack::Translate**</span></span>](id3dxmatrixstack--translate.md)
</dt> </dl>

 

 
