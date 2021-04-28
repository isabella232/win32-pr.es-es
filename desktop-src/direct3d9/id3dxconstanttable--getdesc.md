---
description: 'Método ID3DXConstantTable::GetDesc: obtiene una descripción de la tabla constante.'
ms.assetid: 3a7396c6-3a3e-44c2-96b7-60339015b376
title: Método ID3DXConstantTable::GetDesc (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 81b64f1a01af8909aa820e772214a1f11c6099b8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115243"
---
# <a name="id3dxconstanttablegetdesc-method"></a><span data-ttu-id="7893c-103">Método ID3DXConstantTable::GetDesc</span><span class="sxs-lookup"><span data-stu-id="7893c-103">ID3DXConstantTable::GetDesc method</span></span>

<span data-ttu-id="7893c-104">Obtiene una descripción de la tabla constante.</span><span class="sxs-lookup"><span data-stu-id="7893c-104">Gets a description of the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="7893c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7893c-105">Syntax</span></span>


```C++
HRESULT GetDesc(
  [in] D3DXCONSTANTTABLE_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="7893c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7893c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7893c-107">*pDesc* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="7893c-107">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7893c-108">Tipo: **[ **D3DXCONSTANTTABLE \_ DESC**](d3dxconstanttable-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="7893c-108">Type: **[**D3DXCONSTANTTABLE\_DESC**](d3dxconstanttable-desc.md)\***</span></span>

<span data-ttu-id="7893c-109">Descripción de la tabla constante.</span><span class="sxs-lookup"><span data-stu-id="7893c-109">Description of the constant table.</span></span> <span data-ttu-id="7893c-110">Vea [**D3DXCONSTANTTABLE \_ DESC**](d3dxconstanttable-desc.md).</span><span class="sxs-lookup"><span data-stu-id="7893c-110">See [**D3DXCONSTANTTABLE\_DESC**](d3dxconstanttable-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7893c-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7893c-111">Return value</span></span>

<span data-ttu-id="7893c-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7893c-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7893c-113">Si el método se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7893c-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7893c-114">Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="7893c-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="7893c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7893c-115">Requirements</span></span>



| <span data-ttu-id="7893c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7893c-116">Requirement</span></span> | <span data-ttu-id="7893c-117">Value</span><span class="sxs-lookup"><span data-stu-id="7893c-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7893c-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7893c-118">Header</span></span><br/>  | <dl> <span data-ttu-id="7893c-119"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="7893c-119"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="7893c-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7893c-120">Library</span></span><br/> | <dl> <span data-ttu-id="7893c-121"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="7893c-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="7893c-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7893c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7893c-123">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="7893c-123">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> <dt>

[<span data-ttu-id="7893c-124">**ID3DXConstantTable::GetConstantDesc**</span><span class="sxs-lookup"><span data-stu-id="7893c-124">**ID3DXConstantTable::GetConstantDesc**</span></span>](id3dxconstanttable--getconstantdesc.md)
</dt> </dl>

 

 




