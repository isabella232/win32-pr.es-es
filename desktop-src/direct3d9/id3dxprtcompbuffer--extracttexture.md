---
description: Extrae los coeficientes de proyección de análisis de componentes principales por ejemplo (PCA) de un búfer de datos comprimidos ID3DXPRTCompBuffer y agrega los datos a un objeto IDirect3DTexture9.
ms.assetid: 2159e57d-b8e5-421f-b20a-ac58b29e3c45
title: 'ID3DXPRTCompBuffer:: ExtractTexture (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractTexture
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a6a2200c680c19019375a5e33d2d8b675992dc38
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083752"
---
# <a name="id3dxprtcompbufferextracttexture-method"></a><span data-ttu-id="1d1c6-103">ID3DXPRTCompBuffer:: ExtractTexture (método)</span><span class="sxs-lookup"><span data-stu-id="1d1c6-103">ID3DXPRTCompBuffer::ExtractTexture method</span></span>

<span data-ttu-id="1d1c6-104">Extrae los coeficientes de proyección de análisis de componentes principales por ejemplo (PCA) de un búfer de datos comprimidos [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) y agrega los datos a un objeto [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .</span><span class="sxs-lookup"><span data-stu-id="1d1c6-104">Extracts the per-sample principal component analysis (PCA) projection coefficients from an [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) compressed data buffer and adds the data to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d1c6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1d1c6-105">Syntax</span></span>


```C++
HRESULT ExtractTexture(
  [in] UINT               StartPCA,
  [in] UINT               NumPCA,
  [in] LPDIRECT3DTEXTURE9 pTexture
);
```



## <a name="parameters"></a><span data-ttu-id="1d1c6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1d1c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d1c6-107">*StartPCA* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1d1c6-107">*StartPCA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d1c6-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1d1c6-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1d1c6-109">Valor inicial del coeficiente de búfer desde el que se van a extraer los datos de textura.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-109">Starting value of the buffer coefficient from which to extract texture data.</span></span>

</dd> <dt>

<span data-ttu-id="1d1c6-110">*NumPCA* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1d1c6-110">*NumPCA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d1c6-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1d1c6-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1d1c6-112">Número de coeficientes de PCA que se van a extraer del búfer.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-112">Number of PCA coefficients to extract from the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="1d1c6-113">*pTexture* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1d1c6-113">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d1c6-114">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="1d1c6-114">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="1d1c6-115">Puntero a un objeto de textura [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que almacenará los coeficientes del PCA.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-115">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) texture object that will store PCA coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d1c6-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1d1c6-116">Return value</span></span>

<span data-ttu-id="1d1c6-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1d1c6-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1d1c6-118">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-118">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="1d1c6-119">Si se produce un error en el método, se devolverá el valor siguiente.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-119">If the method fails, the following value will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d1c6-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d1c6-120">Requirements</span></span>



| <span data-ttu-id="1d1c6-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d1c6-121">Requirement</span></span> | <span data-ttu-id="1d1c6-122">Value</span><span class="sxs-lookup"><span data-stu-id="1d1c6-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d1c6-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1d1c6-123">Header</span></span><br/>  | <dl> <span data-ttu-id="1d1c6-124"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d1c6-124"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="1d1c6-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1d1c6-125">Library</span></span><br/> | <dl> <span data-ttu-id="1d1c6-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1d1c6-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1d1c6-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="1d1c6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d1c6-128">ID3DXPRTCompBuffer</span><span class="sxs-lookup"><span data-stu-id="1d1c6-128">ID3DXPRTCompBuffer</span></span>](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
