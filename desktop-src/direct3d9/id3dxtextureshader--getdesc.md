---
description: Obtiene una descripción de la tabla de constantes.
ms.assetid: 91b537bb-5f7a-448b-a21f-c0ddf66d7238
title: 'ID3DXTextureShader:: GetDesc (método) (D3DX9Shader. h)'
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
ms.openlocfilehash: 97302b7e0f8c9f05e6229e20c2c9c158173ed944
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280346"
---
# <a name="id3dxtextureshadergetdesc-method"></a><span data-ttu-id="ad57d-103">ID3DXTextureShader:: GetDesc (método)</span><span class="sxs-lookup"><span data-stu-id="ad57d-103">ID3DXTextureShader::GetDesc method</span></span>

<span data-ttu-id="ad57d-104">Obtiene una descripción de la tabla de constantes.</span><span class="sxs-lookup"><span data-stu-id="ad57d-104">Gets a description of the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad57d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ad57d-105">Syntax</span></span>


```C++
HRESULT GetDesc(
  [in] D3DXCONSTANTTABLE_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="ad57d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ad57d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad57d-107">*pDesc* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ad57d-107">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad57d-108">Tipo: **[ **D3DXCONSTANTTABLE \_ DESC**](d3dxconstanttable-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="ad57d-108">Type: **[**D3DXCONSTANTTABLE\_DESC**](d3dxconstanttable-desc.md)\***</span></span>

<span data-ttu-id="ad57d-109">Atributos de la tabla Constant.</span><span class="sxs-lookup"><span data-stu-id="ad57d-109">The attributes of the constant table.</span></span> <span data-ttu-id="ad57d-110">Vea [**D3DXCONSTANTTABLE \_ DESC**](d3dxconstanttable-desc.md).</span><span class="sxs-lookup"><span data-stu-id="ad57d-110">See [**D3DXCONSTANTTABLE\_DESC**](d3dxconstanttable-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad57d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ad57d-111">Return value</span></span>

<span data-ttu-id="ad57d-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ad57d-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ad57d-113">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ad57d-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ad57d-114">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="ad57d-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad57d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad57d-115">Requirements</span></span>



| <span data-ttu-id="ad57d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad57d-116">Requirement</span></span> | <span data-ttu-id="ad57d-117">Value</span><span class="sxs-lookup"><span data-stu-id="ad57d-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad57d-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ad57d-118">Header</span></span><br/>  | <dl> <span data-ttu-id="ad57d-119"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad57d-119"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="ad57d-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ad57d-120">Library</span></span><br/> | <dl> <span data-ttu-id="ad57d-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ad57d-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ad57d-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="ad57d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad57d-123">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="ad57d-123">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 




