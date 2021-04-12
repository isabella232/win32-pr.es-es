---
description: Establece el índice de la superficie de la malla a la que pertenece cada textura.
ms.assetid: 45d931bc-fb8b-48da-b30d-99d5dc183494
title: 'ID3DXTextureGutterHelper:: SetFaceMap (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.SetFaceMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8ba0472052d5e2e06d759c83a404a197ecda148f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280463"
---
# <a name="id3dxtexturegutterhelpersetfacemap-method"></a><span data-ttu-id="e974e-103">ID3DXTextureGutterHelper:: SetFaceMap (método)</span><span class="sxs-lookup"><span data-stu-id="e974e-103">ID3DXTextureGutterHelper::SetFaceMap method</span></span>

<span data-ttu-id="e974e-104">Establece el índice de la superficie de la malla a la que pertenece cada textura.</span><span class="sxs-lookup"><span data-stu-id="e974e-104">Sets the index of the mesh face to which each texel belongs.</span></span>

## <a name="syntax"></a><span data-ttu-id="e974e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e974e-105">Syntax</span></span>


```C++
HRESULT SetFaceMap(
  [in] UINT *pFaceData
);
```



## <a name="parameters"></a><span data-ttu-id="e974e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e974e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e974e-107">*pFaceData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e974e-107">*pFaceData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e974e-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="e974e-108">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e974e-109">Puntero al índice de la superficie de la malla a la que pertenece cada textura.</span><span class="sxs-lookup"><span data-stu-id="e974e-109">Pointer to the index of the mesh face to which each texel belongs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e974e-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e974e-110">Return value</span></span>

<span data-ttu-id="e974e-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e974e-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e974e-112">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e974e-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e974e-113">Si se produce un error en el método, se devolverá el valor siguiente. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="e974e-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="e974e-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e974e-114">Remarks</span></span>

<span data-ttu-id="e974e-115">La entrada de datos de la superficie de la malla para este método solo es válida para textura válido (que no es de clase 0).</span><span class="sxs-lookup"><span data-stu-id="e974e-115">The mesh face data input to this method is valid only for valid (non-class 0) texels.</span></span> <span data-ttu-id="e974e-116">[**ID3DXTextureGutterHelper:: GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) devolverá valores distintos de cero para textura válidos.</span><span class="sxs-lookup"><span data-stu-id="e974e-116">[**ID3DXTextureGutterHelper::GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) will return non-zero values for valid texels.</span></span>

## <a name="requirements"></a><span data-ttu-id="e974e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e974e-117">Requirements</span></span>



| <span data-ttu-id="e974e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e974e-118">Requirement</span></span> | <span data-ttu-id="e974e-119">Value</span><span class="sxs-lookup"><span data-stu-id="e974e-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e974e-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e974e-120">Header</span></span><br/>  | <dl> <span data-ttu-id="e974e-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e974e-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="e974e-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e974e-122">Library</span></span><br/> | <dl> <span data-ttu-id="e974e-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e974e-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e974e-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="e974e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e974e-125">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="e974e-125">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
