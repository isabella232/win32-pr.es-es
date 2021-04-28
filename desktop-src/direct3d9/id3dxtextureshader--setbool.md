---
description: 'Método ID3DXTextureShader::SetBool: establece un valor BOOL.'
ms.assetid: 0d3c1f3a-f497-4e92-81e9-8647006910e1
title: Método ID3DXTextureShader::SetBool (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetBool
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 512daf7e770c72fe038622877d1756a5fd3532bf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117633"
---
# <a name="id3dxtextureshadersetbool-method"></a><span data-ttu-id="8a655-103">Método ID3DXTextureShader::SetBool</span><span class="sxs-lookup"><span data-stu-id="8a655-103">ID3DXTextureShader::SetBool method</span></span>

<span data-ttu-id="8a655-104">Establece un valor BOOL.</span><span class="sxs-lookup"><span data-stu-id="8a655-104">Sets a BOOL value.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a655-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8a655-105">Syntax</span></span>


```C++
HRESULT SetBool(
  [in] D3DXHANDLE hConstant,
  [in] BOOL       b
);
```



## <a name="parameters"></a><span data-ttu-id="8a655-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8a655-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a655-107">*hConstant* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="8a655-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a655-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="8a655-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="8a655-109">Identificador único de la constante.</span><span class="sxs-lookup"><span data-stu-id="8a655-109">Unique identifier to the constant.</span></span> <span data-ttu-id="8a655-110">Vea [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="8a655-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="8a655-111">*b* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="8a655-111">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a655-112">Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8a655-112">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8a655-113">Valor BOOL.</span><span class="sxs-lookup"><span data-stu-id="8a655-113">BOOL value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a655-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8a655-114">Return value</span></span>

<span data-ttu-id="8a655-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8a655-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8a655-116">Si el método se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8a655-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8a655-117">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="8a655-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a655-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a655-118">Requirements</span></span>



| <span data-ttu-id="8a655-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a655-119">Requirement</span></span> | <span data-ttu-id="8a655-120">Value</span><span class="sxs-lookup"><span data-stu-id="8a655-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a655-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8a655-121">Header</span></span><br/>  | <dl> <span data-ttu-id="8a655-122"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="8a655-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="8a655-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8a655-123">Library</span></span><br/> | <dl> <span data-ttu-id="8a655-124"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="8a655-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="8a655-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8a655-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a655-126">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="8a655-126">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
