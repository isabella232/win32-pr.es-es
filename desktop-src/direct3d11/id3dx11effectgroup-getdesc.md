---
title: Método ID3DX11EffectGroup GetDesc (D3dx11effect. h)
description: Obtiene una descripción del grupo.
ms.assetid: 04bb707a-be21-43d1-8d9d-5a84d29fda74
keywords:
- Método GetDesc Direct3D 11
- Método GetDesc Direct3D 11, interfaz ID3DX11EffectGroup
- Interfaz ID3DX11EffectGroup Direct3D 11, método GetDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c32d44e215a6c89a7d71e899d9839509cbe39417
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003904"
---
# <a name="id3dx11effectgroupgetdesc-method"></a><span data-ttu-id="79796-106">ID3DX11EffectGroup:: GetDesc (método)</span><span class="sxs-lookup"><span data-stu-id="79796-106">ID3DX11EffectGroup::GetDesc method</span></span>

<span data-ttu-id="79796-107">Obtiene una descripción del grupo.</span><span class="sxs-lookup"><span data-stu-id="79796-107">Gets a group description.</span></span>

## <a name="syntax"></a><span data-ttu-id="79796-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="79796-108">Syntax</span></span>


```C++
HRESULT GetDesc(
   D3DX11_GROUP_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="79796-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="79796-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79796-110">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="79796-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="79796-111">Tipo: **[ **\_ \_ DESC de grupo de D3DX11**](d3dx11-group-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="79796-111">Type: **[**D3DX11\_GROUP\_DESC**](d3dx11-group-desc.md)\***</span></span>

<span data-ttu-id="79796-112">Puntero a una estructura [**de \_ \_ DESC de grupo de D3DX11**](d3dx11-group-desc.md) .</span><span class="sxs-lookup"><span data-stu-id="79796-112">A pointer to a [**D3DX11\_GROUP\_DESC**](d3dx11-group-desc.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79796-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="79796-113">Return value</span></span>

<span data-ttu-id="79796-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="79796-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="79796-115">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="79796-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="79796-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="79796-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="79796-117">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="79796-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="79796-118">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="79796-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="79796-119">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="79796-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="79796-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79796-120">Requirements</span></span>



| <span data-ttu-id="79796-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="79796-121">Requirement</span></span> | <span data-ttu-id="79796-122">Value</span><span class="sxs-lookup"><span data-stu-id="79796-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79796-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="79796-123">Header</span></span><br/>  | <dl> <span data-ttu-id="79796-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="79796-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="79796-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="79796-125">Library</span></span><br/> | <dl> <span data-ttu-id="79796-126"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="79796-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79796-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="79796-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79796-128">ID3DX11EffectGroup</span><span class="sxs-lookup"><span data-stu-id="79796-128">ID3DX11EffectGroup</span></span>](id3dx11effectgroup.md)
</dt> </dl>

 

 





