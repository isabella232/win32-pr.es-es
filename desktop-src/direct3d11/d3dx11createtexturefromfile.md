---
title: Función D3DX11CreateTextureFromFile (D3DX11. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Tenga en cuenta que, en lugar de usar esta función, se recomienda usar esta biblioteca DirectXTK (Runtime), CreateXXXTextureFromFile (donde XXX es DDS o WIC) DirectXTex Library (Tools), LoadFromXXXFile (donde XXX es WIC, DDS o TGA; WIC no admite DDS ni TGA; D3DX 9 admitía TGA como formato de código fuente común para juegos) y CreateTexture crear un recurso de textura a partir de un archivo.
ms.assetid: a84ea166-2296-48d9-a028-b65fd68f2371
keywords:
- Función D3DX11CreateTextureFromFile Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateTextureFromFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6ab9bedcfe44238938e47ccb402738d2694b061
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998515"
---
# <a name="d3dx11createtexturefromfile-function"></a><span data-ttu-id="d8d09-105">D3DX11CreateTextureFromFile función)</span><span class="sxs-lookup"><span data-stu-id="d8d09-105">D3DX11CreateTextureFromFile function</span></span>

> [!Note]  
> <span data-ttu-id="d8d09-106">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="d8d09-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="d8d09-107">En lugar de usar esta función, se recomienda usar estas:</span><span class="sxs-lookup"><span data-stu-id="d8d09-107">Instead of using this function, we recommend that you use these:</span></span>
>
> -   <span data-ttu-id="d8d09-108">Biblioteca [DirectXTK](https://github.com/Microsoft/DirectXTK) (Runtime), **CREATEXXXTEXTUREFROMFILE** (donde xxx es DDS o WIC)</span><span class="sxs-lookup"><span data-stu-id="d8d09-108">[DirectXTK](https://github.com/Microsoft/DirectXTK) library (runtime), **CreateXXXTextureFromFile** (where XXX is DDS or WIC)</span></span>
> -   <span data-ttu-id="d8d09-109">Biblioteca [DirectXTex](https://github.com/Microsoft/DirectXTex) (herramientas), **LOADFROMXXXFILE** (donde xxx es WIC, DDS o TGA; WIC no admite DDS ni TGA; D3DX 9 admitía TGA como formato de fuente de arte común para juegos) y luego **CreateTexture**</span><span class="sxs-lookup"><span data-stu-id="d8d09-109">[DirectXTex](https://github.com/Microsoft/DirectXTex) library (tools), **LoadFromXXXFile** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then **CreateTexture**</span></span>

 

<span data-ttu-id="d8d09-110">Cree un recurso de textura a partir de un archivo.</span><span class="sxs-lookup"><span data-stu-id="d8d09-110">Create a texture resource from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8d09-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d8d09-111">Syntax</span></span>


```C++
HRESULT D3DX11CreateTextureFromFile(
  _In_  ID3D11Device           *pDevice,
  _In_  LPCTSTR                pSrcFile,
  _In_  D3DX11_IMAGE_LOAD_INFO *pLoadInfo,
  _In_  ID3DX11ThreadPump      *pPump,
  _Out_ ID3D11Resource         **ppTexture,
  _Out_ HRESULT                *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="d8d09-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d8d09-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8d09-113">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d8d09-113">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8d09-114">Tipo: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span><span class="sxs-lookup"><span data-stu-id="d8d09-114">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span></span>

<span data-ttu-id="d8d09-115">Un puntero al dispositivo (vea [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) que usará el recurso.</span><span class="sxs-lookup"><span data-stu-id="d8d09-115">A pointer to the device (see [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="d8d09-116">*pSrcFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d8d09-116">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8d09-117">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d8d09-117">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d8d09-118">Nombre del archivo que contiene el recurso.</span><span class="sxs-lookup"><span data-stu-id="d8d09-118">The name of the file containing the resource.</span></span> <span data-ttu-id="d8d09-119">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="d8d09-119">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="d8d09-120">De lo contrario, el tipo de datos se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="d8d09-120">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="d8d09-121">*pLoadInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d8d09-121">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8d09-122">Tipo: **[ **\_ información de \_ carga \_ de imagen de D3DX11**](d3dx11-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="d8d09-122">Type: **[**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)\***</span></span>

<span data-ttu-id="d8d09-123">Opcional.</span><span class="sxs-lookup"><span data-stu-id="d8d09-123">Optional.</span></span> <span data-ttu-id="d8d09-124">Identifica las características de una textura (consulte [**\_ información de \_ carga \_ de imagen de D3DX11**](d3dx11-image-load-info.md)) cuando se crea el procesador de datos; establezca este valor en **null** para leer las características de una textura cuando se carga la textura.</span><span class="sxs-lookup"><span data-stu-id="d8d09-124">Identifies the characteristics of a texture (see [**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="d8d09-125">*pPump* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d8d09-125">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8d09-126">Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="d8d09-126">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="d8d09-127">Un puntero a una interfaz de bombeo de subprocesos (consulte la [**interfaz ID3DX11ThreadPump**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="d8d09-127">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="d8d09-128">Si se especifica **null** , esta función se comportará de forma sincrónica y no volverá hasta que finalice.</span><span class="sxs-lookup"><span data-stu-id="d8d09-128">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="d8d09-129">*ppTexture* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d8d09-129">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8d09-130">Tipo: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\*\***</span><span class="sxs-lookup"><span data-stu-id="d8d09-130">Type: **[**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\*\***</span></span>

<span data-ttu-id="d8d09-131">La dirección de un puntero al recurso de textura (vea [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)).</span><span class="sxs-lookup"><span data-stu-id="d8d09-131">The address of a pointer to the texture resource (see [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)).</span></span>

</dd> <dt>

<span data-ttu-id="d8d09-132">*pHResult* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d8d09-132">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8d09-133">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="d8d09-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="d8d09-134">Puntero al valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="d8d09-134">A pointer to the return value.</span></span> <span data-ttu-id="d8d09-135">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="d8d09-135">May be **NULL**.</span></span> <span data-ttu-id="d8d09-136">Si *pPump* no es **null**, *pHResult* debe ser una ubicación de memoria válida hasta que se complete la ejecución asincrónica.</span><span class="sxs-lookup"><span data-stu-id="d8d09-136">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8d09-137">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d8d09-137">Return value</span></span>

<span data-ttu-id="d8d09-138">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d8d09-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d8d09-139">El valor devuelto es uno de los valores que se muestran en [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="d8d09-139">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d8d09-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8d09-140">Requirements</span></span>



| <span data-ttu-id="d8d09-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8d09-141">Requirement</span></span> | <span data-ttu-id="d8d09-142">Value</span><span class="sxs-lookup"><span data-stu-id="d8d09-142">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d8d09-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d8d09-143">Header</span></span><br/>  | <dl> <span data-ttu-id="d8d09-144"><dt>D3DX11. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8d09-144"><dt>D3DX11.h</dt></span></span> </dl>   |
| <span data-ttu-id="d8d09-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d8d09-145">Library</span></span><br/> | <dl> <span data-ttu-id="d8d09-146"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8d09-146"><dt>D3DX11.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8d09-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="d8d09-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8d09-148">Funciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="d8d09-148">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

