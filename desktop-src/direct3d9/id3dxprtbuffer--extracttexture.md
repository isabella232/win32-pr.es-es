---
description: Extrae los datos coeficientes de un canal de color del búfer para un intervalo de coeficientes especificado y agrega los datos a un objeto IDirect3DTexture9.
ms.assetid: 75854676-706a-4675-857e-4f2f8fc8365b
title: 'ID3DXPRTBuffer:: ExtractTexture (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ExtractTexture
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2ea6cfdc8fb6ec83f847ccf37d06972974ea4de8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003866"
---
# <a name="id3dxprtbufferextracttexture-method"></a><span data-ttu-id="dcddc-103">ID3DXPRTBuffer:: ExtractTexture (método)</span><span class="sxs-lookup"><span data-stu-id="dcddc-103">ID3DXPRTBuffer::ExtractTexture method</span></span>

<span data-ttu-id="dcddc-104">Extrae los datos coeficientes de un canal de color del búfer para un intervalo de coeficientes especificado y agrega los datos a un objeto [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .</span><span class="sxs-lookup"><span data-stu-id="dcddc-104">Extracts coefficient data from a color channel of the buffer for a specified range of coefficients, and adds the data to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcddc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dcddc-105">Syntax</span></span>


```C++
HRESULT ExtractTexture(
  [in] UINT               Channel,
  [in] UINT               StartCoefficient,
  [in] UINT               NumCoefficients,
  [in] LPDIRECT3DTEXTURE9 pTexture
);
```



## <a name="parameters"></a><span data-ttu-id="dcddc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dcddc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcddc-107">*Canal* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="dcddc-107">*Channel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcddc-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dcddc-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dcddc-109">Canal de color del búfer del que se van a extraer los datos de textura.</span><span class="sxs-lookup"><span data-stu-id="dcddc-109">Buffer color channel from which to extract texture data.</span></span>

</dd> <dt>

<span data-ttu-id="dcddc-110">*StartCoefficient* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dcddc-110">*StartCoefficient* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcddc-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dcddc-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dcddc-112">Valor inicial del coeficiente de búfer desde el que se van a extraer los datos de textura.</span><span class="sxs-lookup"><span data-stu-id="dcddc-112">Starting value of the buffer coefficient from which to extract texture data.</span></span>

</dd> <dt>

<span data-ttu-id="dcddc-113">*NumCoefficients* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dcddc-113">*NumCoefficients* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcddc-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dcddc-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dcddc-115">Número de escalares, a partir de StartCoefficient, del que se van a extraer los datos de textura.</span><span class="sxs-lookup"><span data-stu-id="dcddc-115">Number of scalars, beginning at StartCoefficient, from which to extract texture data.</span></span>

</dd> <dt>

<span data-ttu-id="dcddc-116">*pTexture* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dcddc-116">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcddc-117">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="dcddc-117">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="dcddc-118">Puntero a un objeto de textura [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que almacena coeficientes.</span><span class="sxs-lookup"><span data-stu-id="dcddc-118">Pointer to a [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) texture object that will store coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcddc-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dcddc-119">Return value</span></span>

<span data-ttu-id="dcddc-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dcddc-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dcddc-121">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="dcddc-121">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="dcddc-122">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="dcddc-122">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcddc-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dcddc-123">Requirements</span></span>



| <span data-ttu-id="dcddc-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcddc-124">Requirement</span></span> | <span data-ttu-id="dcddc-125">Value</span><span class="sxs-lookup"><span data-stu-id="dcddc-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dcddc-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dcddc-126">Header</span></span><br/>  | <dl> <span data-ttu-id="dcddc-127"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcddc-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="dcddc-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dcddc-128">Library</span></span><br/> | <dl> <span data-ttu-id="dcddc-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dcddc-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dcddc-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="dcddc-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcddc-131">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="dcddc-131">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 
