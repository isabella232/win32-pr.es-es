---
description: Establece un vector normal para cada textura de un objeto Texture. Este método se usa para almacenar vectores normales de vértices de una malla (o normales de vértice interpolados si se está calculando la transferencia de Radiance precalculada basada en píxeles).
ms.assetid: 165a3ef6-c142-4988-b4fb-5aafd8ff11fe
title: 'ID3DXPRTEngine:: SetPerTexelNormal (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetPerTexelNormal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5220ad500312792cd158967e9502381f49b0e3e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424432"
---
# <a name="id3dxprtenginesetpertexelnormal-method"></a><span data-ttu-id="f695a-104">ID3DXPRTEngine:: SetPerTexelNormal (método)</span><span class="sxs-lookup"><span data-stu-id="f695a-104">ID3DXPRTEngine::SetPerTexelNormal method</span></span>

<span data-ttu-id="f695a-105">Establece un vector normal para cada textura de un objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="f695a-105">Sets a normal vector for each texel in a texture object.</span></span> <span data-ttu-id="f695a-106">Este método se usa para almacenar vectores normales de vértices de una malla (o normales de vértice interpolados si se está calculando la transferencia de Radiance precalculada basada en píxeles).</span><span class="sxs-lookup"><span data-stu-id="f695a-106">This method is used to store vertex normal vectors from a mesh (or interpolated vertex normals if pixel-based precomputed radiance transfer (PRT) is being computed).</span></span>

## <a name="syntax"></a><span data-ttu-id="f695a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f695a-107">Syntax</span></span>


```C++
HRESULT SetPerTexelNormal(
  [in] LPDIRECT3DTEXTURE9 pNormalTexture
);
```



## <a name="parameters"></a><span data-ttu-id="f695a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f695a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f695a-109">*pNormalTexture* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f695a-109">*pNormalTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f695a-110">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="f695a-110">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="f695a-111">Puntero a un objeto de textura [**IDirect3DTexture9**](/windows/desktop/api) que actúa como mapa normal de espacio de objeto en el que se almacenan los vectores normales.</span><span class="sxs-lookup"><span data-stu-id="f695a-111">Pointer to an [**IDirect3DTexture9**](/windows/desktop/api) texture object that serves as an object space normal map in which to store normal vectors.</span></span> <span data-ttu-id="f695a-112">La textura debe tener las mismas dimensiones que [**ID3DXPRTBuffer**](id3dxprtbuffer.md) y debe poder almacenar formatos de textura firmados.</span><span class="sxs-lookup"><span data-stu-id="f695a-112">The texture must have the same dimensions as [**ID3DXPRTBuffer**](id3dxprtbuffer.md) and must be able to store signed texture formats.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f695a-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f695a-113">Return value</span></span>

<span data-ttu-id="f695a-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f695a-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f695a-115">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f695a-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="f695a-116">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="f695a-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="f695a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f695a-117">Requirements</span></span>



| <span data-ttu-id="f695a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f695a-118">Requirement</span></span> | <span data-ttu-id="f695a-119">Value</span><span class="sxs-lookup"><span data-stu-id="f695a-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f695a-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f695a-120">Header</span></span><br/>  | <dl> <span data-ttu-id="f695a-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="f695a-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="f695a-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f695a-122">Library</span></span><br/> | <dl> <span data-ttu-id="f695a-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f695a-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f695a-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="f695a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f695a-125">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="f695a-125">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
