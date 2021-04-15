---
description: Agrega una salida de animación al controlador de animación y registra punteros para las transformaciones de escala, rotación y traducción (SRT).
ms.assetid: 8c3197bc-9d03-40ba-869b-151f9c8e96ba
title: 'ID3DXAnimationController:: RegisterAnimationOutput (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.RegisterAnimationOutput
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7670f8b311532d096b9957ebbefcf1f6fb15d952
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708017"
---
# <a name="id3dxanimationcontrollerregisteranimationoutput-method"></a><span data-ttu-id="f3b7b-103">ID3DXAnimationController:: RegisterAnimationOutput (método)</span><span class="sxs-lookup"><span data-stu-id="f3b7b-103">ID3DXAnimationController::RegisterAnimationOutput method</span></span>

<span data-ttu-id="f3b7b-104">Agrega una salida de animación al controlador de animación y registra punteros para las transformaciones de escala, rotación y traducción (SRT).</span><span class="sxs-lookup"><span data-stu-id="f3b7b-104">Adds an animation output to the animation controller and registers pointers for scale, rotate, and translate (SRT) transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3b7b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f3b7b-105">Syntax</span></span>


```C++
HRESULT RegisterAnimationOutput(
  [in] LPCSTR         Name,
  [in] D3DXMATRIX     *pMatrix,
  [in] D3DXVECTOR3    *pScale,
  [in] D3DXQUATERNION *pRotation,
  [in] D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="f3b7b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f3b7b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3b7b-107">*Nombre* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="f3b7b-107">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3b7b-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f3b7b-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f3b7b-109">Nombre del resultado de la animación.</span><span class="sxs-lookup"><span data-stu-id="f3b7b-109">Name of the animation output.</span></span>

</dd> <dt>

<span data-ttu-id="f3b7b-110">*pMatrix* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f3b7b-110">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3b7b-111">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="f3b7b-111">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f3b7b-112">Puntero a una estructura [**D3DXMATRIX**](d3dxmatrix.md) que contiene datos de transformación de SRT.</span><span class="sxs-lookup"><span data-stu-id="f3b7b-112">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure containing SRT transformation data.</span></span> <span data-ttu-id="f3b7b-113">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="f3b7b-113">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f3b7b-114">*pScale* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f3b7b-114">*pScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3b7b-115">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="f3b7b-115">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="f3b7b-116">Puntero a un vector [**D3DXVECTOR3**](d3dxvector3.md) que describe la escala del conjunto de animaciones.</span><span class="sxs-lookup"><span data-stu-id="f3b7b-116">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) vector that describes the scale of the animation set.</span></span> <span data-ttu-id="f3b7b-117">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="f3b7b-117">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f3b7b-118">*Prot.* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f3b7b-118">*pRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3b7b-119">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="f3b7b-119">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="f3b7b-120">Puntero a un cuaternión [**D3DXQUATERNION**](d3dxquaternion.md) que describe el giro del conjunto de animaciones.</span><span class="sxs-lookup"><span data-stu-id="f3b7b-120">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) quaternion that describes the rotation of the animation set.</span></span> <span data-ttu-id="f3b7b-121">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="f3b7b-121">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f3b7b-122">*pTranslation* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f3b7b-122">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3b7b-123">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="f3b7b-123">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="f3b7b-124">Puntero a un vector [**D3DXVECTOR3**](d3dxvector3.md) que describe la traducción del conjunto de animaciones.</span><span class="sxs-lookup"><span data-stu-id="f3b7b-124">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) vector that describes the translation of the animation set.</span></span> <span data-ttu-id="f3b7b-125">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="f3b7b-125">Can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3b7b-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f3b7b-126">Return value</span></span>

<span data-ttu-id="f3b7b-127">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f3b7b-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f3b7b-128">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f3b7b-128">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="f3b7b-129">Si se produce un error en el método, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="f3b7b-129">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3b7b-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f3b7b-130">Remarks</span></span>

<span data-ttu-id="f3b7b-131">Si el resultado de la animación ya está registrado, pMatrix se rellenará con los datos de transformación de entrada.</span><span class="sxs-lookup"><span data-stu-id="f3b7b-131">If the animation output is already registered, pMatrix will be filled with the input transformation data.</span></span>

<span data-ttu-id="f3b7b-132">Los conjuntos de animaciones creados con [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) registran automáticamente todos los conjuntos de animaciones cargados.</span><span class="sxs-lookup"><span data-stu-id="f3b7b-132">Animation sets created with [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) automatically register all loaded animation sets.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3b7b-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3b7b-133">Requirements</span></span>



| <span data-ttu-id="f3b7b-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3b7b-134">Requirement</span></span> | <span data-ttu-id="f3b7b-135">Value</span><span class="sxs-lookup"><span data-stu-id="f3b7b-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3b7b-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f3b7b-136">Header</span></span><br/>  | <dl> <span data-ttu-id="f3b7b-137"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3b7b-137"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="f3b7b-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f3b7b-138">Library</span></span><br/> | <dl> <span data-ttu-id="f3b7b-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f3b7b-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f3b7b-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="f3b7b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3b7b-141">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="f3b7b-141">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
