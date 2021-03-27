---
title: Función D3DX11SaveTextureToMemory (D3DX11tex. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Tenga en cuenta que, en lugar de usar esta función, se recomienda usar la biblioteca DirectXTex, CaptureTexture then SaveToXXXMemory (donde XXX es WIC, DDS o TGA; WIC no admite DDS ni TGA; D3DX 9 admitía TGA como formato de fuente de arte común para juegos. Guardar una textura en la memoria.
ms.assetid: 3b54d8e1-6474-48fd-8348-a3baac406101
keywords:
- Función D3DX11SaveTextureToMemory Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11SaveTextureToMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4718f32f8d8288f83b30e3d742ebbe619421dc48
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280432"
---
# <a name="d3dx11savetexturetomemory-function"></a><span data-ttu-id="04e5f-106">D3DX11SaveTextureToMemory función)</span><span class="sxs-lookup"><span data-stu-id="04e5f-106">D3DX11SaveTextureToMemory function</span></span>

> [!Note]  
> <span data-ttu-id="04e5f-107">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="04e5f-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="04e5f-108">En lugar de usar esta función, se recomienda usar la biblioteca [DirectXTex](https://github.com/Microsoft/DirectXTex) , **CaptureTexture** then **SAVETOXXXMEMORY** (donde xxx es WIC, DDS o TGA; WIC no admite DDS ni TGA; D3DX 9 admitía TGA como formato de fuente de arte común para juegos.</span><span class="sxs-lookup"><span data-stu-id="04e5f-108">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **CaptureTexture** then **SaveToXXXMemory** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span>

 

<span data-ttu-id="04e5f-109">Guardar una textura en la memoria.</span><span class="sxs-lookup"><span data-stu-id="04e5f-109">Save a texture to memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="04e5f-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="04e5f-110">Syntax</span></span>


```C++
HRESULT D3DX11SaveTextureToMemory(
        ID3D11DeviceContext      *pContext,
  _In_  ID3D11Resource           *pSrcTexture,
  _In_  D3DX11_IMAGE_FILE_FORMAT DestFormat,
  _Out_ LPD3D10BLOB              *ppDestBuf,
  _In_  UINT                     Flags
);
```



## <a name="parameters"></a><span data-ttu-id="04e5f-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="04e5f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04e5f-112">*pContext*</span><span class="sxs-lookup"><span data-stu-id="04e5f-112">*pContext*</span></span> 
</dt> <dd>

<span data-ttu-id="04e5f-113">Tipo: **[ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="04e5f-113">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="04e5f-114">Un puntero a un objeto [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="04e5f-114">A pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>

</dd> <dt>

<span data-ttu-id="04e5f-115">*pSrcTexture* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="04e5f-115">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04e5f-116">Tipo: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span><span class="sxs-lookup"><span data-stu-id="04e5f-116">Type: **[**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span></span>

<span data-ttu-id="04e5f-117">Puntero a la textura que se va a guardar.</span><span class="sxs-lookup"><span data-stu-id="04e5f-117">Pointer to the texture to be saved.</span></span> <span data-ttu-id="04e5f-118">Vea [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span><span class="sxs-lookup"><span data-stu-id="04e5f-118">See [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span></span>

</dd> <dt>

<span data-ttu-id="04e5f-119">*DestFormat* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="04e5f-119">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04e5f-120">Tipo: **[ **\_ formato de \_ archivo \_ de imagen D3DX11**](d3dx11-image-file-format.md)**</span><span class="sxs-lookup"><span data-stu-id="04e5f-120">Type: **[**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md)**</span></span>

<span data-ttu-id="04e5f-121">Formato en el que se guardará la textura.</span><span class="sxs-lookup"><span data-stu-id="04e5f-121">The format the texture will be saved as.</span></span> <span data-ttu-id="04e5f-122">Consulte [**\_ formato de \_ archivo \_ de imagen D3DX11**](d3dx11-image-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="04e5f-122">See [**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md).</span></span>

</dd> <dt>

<span data-ttu-id="04e5f-123">*ppDestBuf* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="04e5f-123">*ppDestBuf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04e5f-124">Tipo: **[ **LPD3D10BLOB**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\***</span><span class="sxs-lookup"><span data-stu-id="04e5f-124">Type: **[**LPD3D10BLOB**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\***</span></span>

<span data-ttu-id="04e5f-125">Dirección de un puntero a la memoria que contiene la textura guardada.</span><span class="sxs-lookup"><span data-stu-id="04e5f-125">Address of a pointer to the memory containing the saved texture.</span></span>

</dd> <dt>

<span data-ttu-id="04e5f-126">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="04e5f-126">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04e5f-127">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="04e5f-127">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="04e5f-128">Opcional.</span><span class="sxs-lookup"><span data-stu-id="04e5f-128">Optional.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04e5f-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="04e5f-129">Return value</span></span>

<span data-ttu-id="04e5f-130">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="04e5f-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="04e5f-131">El valor devuelto es uno de los valores que se muestran en [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="04e5f-131">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="04e5f-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04e5f-132">Requirements</span></span>



| <span data-ttu-id="04e5f-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="04e5f-133">Requirement</span></span> | <span data-ttu-id="04e5f-134">Value</span><span class="sxs-lookup"><span data-stu-id="04e5f-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="04e5f-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="04e5f-135">Header</span></span><br/>  | <dl> <span data-ttu-id="04e5f-136"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="04e5f-136"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="04e5f-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="04e5f-137">Library</span></span><br/> | <dl> <span data-ttu-id="04e5f-138"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="04e5f-138"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="04e5f-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="04e5f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04e5f-140">Funciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="04e5f-140">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

