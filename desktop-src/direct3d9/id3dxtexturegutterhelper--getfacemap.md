---
description: Recupera el índice de la superficie de la malla a la que pertenece cada textura.
ms.assetid: 3eb3461c-4e16-4c89-9ca9-fc9c6b5638c7
title: 'ID3DXTextureGutterHelper:: GetFaceMap (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetFaceMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8164ec35c3b3596914577287ecc6b9285142fca8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707949"
---
# <a name="id3dxtexturegutterhelpergetfacemap-method"></a><span data-ttu-id="6c615-103">ID3DXTextureGutterHelper:: GetFaceMap (método)</span><span class="sxs-lookup"><span data-stu-id="6c615-103">ID3DXTextureGutterHelper::GetFaceMap method</span></span>

<span data-ttu-id="6c615-104">Recupera el índice de la superficie de la malla a la que pertenece cada textura.</span><span class="sxs-lookup"><span data-stu-id="6c615-104">Retrieves the index of the mesh face to which each texel belongs.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c615-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6c615-105">Syntax</span></span>


```C++
HRESULT GetFaceMap(
  [in] UINT *pFaceData
);
```



## <a name="parameters"></a><span data-ttu-id="6c615-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6c615-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c615-107">*pFaceData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6c615-107">*pFaceData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c615-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6c615-108">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6c615-109">Puntero al índice de la superficie de la malla a la que pertenece cada textura.</span><span class="sxs-lookup"><span data-stu-id="6c615-109">Pointer to the index of the mesh face to which each texel belongs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c615-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6c615-110">Return value</span></span>

<span data-ttu-id="6c615-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6c615-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6c615-112">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6c615-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="6c615-113">Si se produce un error en el método, se devolverá el valor siguiente. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="6c615-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="6c615-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6c615-114">Remarks</span></span>

<span data-ttu-id="6c615-115">Los datos de la superficie de la malla devueltos por este método solo son válidos para textura válido (que no es de clase 0).</span><span class="sxs-lookup"><span data-stu-id="6c615-115">The mesh face data returned by this method is valid only for valid (non-class 0) texels.</span></span> <span data-ttu-id="6c615-116">[**ID3DXTextureGutterHelper:: GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) devolverá valores distintos de cero para textura válido (que no es de clase 0).</span><span class="sxs-lookup"><span data-stu-id="6c615-116">[**ID3DXTextureGutterHelper::GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) will return nonzero values for valid (non-class 0) texels.</span></span>

<span data-ttu-id="6c615-117">En el caso de la [**clase 2 textura**](id3dxtexturegutterhelper.md), este método recupera la superficie más cercana.</span><span class="sxs-lookup"><span data-stu-id="6c615-117">For [**class 2 texels**](id3dxtexturegutterhelper.md), this method retrieves the closest face.</span></span>

<span data-ttu-id="6c615-118">La aplicación debe asignar y administrar pFaceData.</span><span class="sxs-lookup"><span data-stu-id="6c615-118">The application must allocate and manage pFaceData.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c615-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c615-119">Requirements</span></span>



| <span data-ttu-id="6c615-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c615-120">Requirement</span></span> | <span data-ttu-id="6c615-121">Value</span><span class="sxs-lookup"><span data-stu-id="6c615-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c615-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6c615-122">Header</span></span><br/>  | <dl> <span data-ttu-id="6c615-123"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c615-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="6c615-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6c615-124">Library</span></span><br/> | <dl> <span data-ttu-id="6c615-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6c615-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6c615-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c615-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c615-127">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="6c615-127">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
