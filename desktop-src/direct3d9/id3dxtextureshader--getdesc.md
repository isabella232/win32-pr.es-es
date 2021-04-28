---
description: 'Método ID3DXTextureShader::GetDesc: obtiene una descripción de la tabla constante.'
ms.assetid: 91b537bb-5f7a-448b-a21f-c0ddf66d7238
title: Método ID3DXTextureShader::GetDesc (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6ea94f0e22d838f09dae9b423f85aa1d55d2365b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117643"
---
# <a name="id3dxtextureshadergetdesc-method"></a><span data-ttu-id="df86f-103">Método ID3DXTextureShader::GetDesc</span><span class="sxs-lookup"><span data-stu-id="df86f-103">ID3DXTextureShader::GetDesc method</span></span>

<span data-ttu-id="df86f-104">Obtiene una descripción de la tabla constante.</span><span class="sxs-lookup"><span data-stu-id="df86f-104">Gets a description of the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="df86f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="df86f-105">Syntax</span></span>


```C++
HRESULT GetDesc(
  [in] D3DXCONSTANTTABLE_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="df86f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="df86f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df86f-107">*pDesc* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="df86f-107">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df86f-108">Tipo: **[ **D3DXCONSTANTTABLE \_ DESC**](d3dxconstanttable-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="df86f-108">Type: **[**D3DXCONSTANTTABLE\_DESC**](d3dxconstanttable-desc.md)\***</span></span>

<span data-ttu-id="df86f-109">Atributos de la tabla constante.</span><span class="sxs-lookup"><span data-stu-id="df86f-109">The attributes of the constant table.</span></span> <span data-ttu-id="df86f-110">Vea [**D3DXCONSTANTTABLE \_ DESC**](d3dxconstanttable-desc.md).</span><span class="sxs-lookup"><span data-stu-id="df86f-110">See [**D3DXCONSTANTTABLE\_DESC**](d3dxconstanttable-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df86f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="df86f-111">Return value</span></span>

<span data-ttu-id="df86f-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="df86f-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="df86f-113">Si el método se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="df86f-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="df86f-114">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="df86f-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="df86f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df86f-115">Requirements</span></span>



| <span data-ttu-id="df86f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="df86f-116">Requirement</span></span> | <span data-ttu-id="df86f-117">Value</span><span class="sxs-lookup"><span data-stu-id="df86f-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="df86f-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="df86f-118">Header</span></span><br/>  | <dl> <span data-ttu-id="df86f-119"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="df86f-119"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="df86f-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="df86f-120">Library</span></span><br/> | <dl> <span data-ttu-id="df86f-121"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="df86f-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="df86f-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="df86f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df86f-123">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="df86f-123">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 




