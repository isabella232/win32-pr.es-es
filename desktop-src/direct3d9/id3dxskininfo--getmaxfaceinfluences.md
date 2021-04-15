---
description: Obtiene el número máximo de influencias de caras en una malla de triángulo con el búfer de índice especificado.
ms.assetid: 72dc2440-87df-461e-80d0-9ad9b1e4d8ee
title: 'ID3DXSkinInfo:: GetMaxFaceInfluences (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetMaxFaceInfluences
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 11724c50d5224f0bcb2c9ced25523b869f3e347f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424315"
---
# <a name="id3dxskininfogetmaxfaceinfluences-method"></a><span data-ttu-id="c0944-103">ID3DXSkinInfo:: GetMaxFaceInfluences (método)</span><span class="sxs-lookup"><span data-stu-id="c0944-103">ID3DXSkinInfo::GetMaxFaceInfluences method</span></span>

<span data-ttu-id="c0944-104">Obtiene el número máximo de influencias de caras en una malla de triángulo con el búfer de índice especificado.</span><span class="sxs-lookup"><span data-stu-id="c0944-104">Gets the maximum face influences in a triangle mesh with the specified index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0944-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c0944-105">Syntax</span></span>


```C++
HRESULT GetMaxFaceInfluences(
  [in] LPDIRECT3DINDEXBUFFER9 pIB,
  [in] DWORD                  NumFaces,
  [in] DWORD                  *maxFaceInfluences
);
```



## <a name="parameters"></a><span data-ttu-id="c0944-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c0944-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0944-107">*pIB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c0944-107">*pIB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0944-108">Tipo: **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)**</span><span class="sxs-lookup"><span data-stu-id="c0944-108">Type: **[**LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)**</span></span>

<span data-ttu-id="c0944-109">Puntero al búfer de índice que contiene los datos del índice de malla.</span><span class="sxs-lookup"><span data-stu-id="c0944-109">Pointer to the index buffer that contains the mesh index data.</span></span>

</dd> <dt>

<span data-ttu-id="c0944-110">*NumFaces* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c0944-110">*NumFaces* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0944-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c0944-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c0944-112">Número de caras en la malla.</span><span class="sxs-lookup"><span data-stu-id="c0944-112">Number of faces in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="c0944-113">*maxFaceInfluences* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c0944-113">*maxFaceInfluences* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0944-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c0944-114">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c0944-115">Puntero a las influencias máximas de la superficie.</span><span class="sxs-lookup"><span data-stu-id="c0944-115">Pointer to the maximum face influences.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0944-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c0944-116">Return value</span></span>

<span data-ttu-id="c0944-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c0944-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c0944-118">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c0944-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c0944-119">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="c0944-119">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0944-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0944-120">Requirements</span></span>



| <span data-ttu-id="c0944-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0944-121">Requirement</span></span> | <span data-ttu-id="c0944-122">Value</span><span class="sxs-lookup"><span data-stu-id="c0944-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0944-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c0944-123">Header</span></span><br/>  | <dl> <span data-ttu-id="c0944-124"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0944-124"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="c0944-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c0944-125">Library</span></span><br/> | <dl> <span data-ttu-id="c0944-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c0944-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c0944-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="c0944-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0944-128">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="c0944-128">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 
