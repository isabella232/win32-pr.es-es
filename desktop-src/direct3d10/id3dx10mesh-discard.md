---
description: 'Quita los datos de malla del dispositivo que se ha confirmado en el dispositivo (con ID3DX10Mesh:: CommitToDevice).'
ms.assetid: 60eee1f8-f04b-4f33-8f86-0564d0334f97
title: ID3DX10Mesh::D método iscard (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.Discard
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f861de8eefff603954e896a1b6684afc8806764f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105678794"
---
# <a name="id3dx10meshdiscard-method"></a><span data-ttu-id="f3c1f-103">ID3DX10Mesh::D método iscard</span><span class="sxs-lookup"><span data-stu-id="f3c1f-103">ID3DX10Mesh::Discard method</span></span>

<span data-ttu-id="f3c1f-104">Quita los datos de malla del dispositivo que se ha confirmado en el dispositivo (con [**ID3DX10Mesh:: CommitToDevice**](id3dx10mesh-committodevice.md)).</span><span class="sxs-lookup"><span data-stu-id="f3c1f-104">Removes mesh data from the device that has been committed to the device (with [**ID3DX10Mesh::CommitToDevice**](id3dx10mesh-committodevice.md)).</span></span>

## <a name="syntax"></a><span data-ttu-id="f3c1f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f3c1f-105">Syntax</span></span>


```C++
HRESULT Discard(
  [in] D3DX10_MESH_DISCARD_FLAGS dwDiscard
);
```



## <a name="parameters"></a><span data-ttu-id="f3c1f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f3c1f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3c1f-107">*dwDiscard* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f3c1f-107">*dwDiscard* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3c1f-108">Tipo: **[ **\_ \_ \_ marcas de descartado de malla D3DX10**](d3dx10-mesh-discard-flags.md)**</span><span class="sxs-lookup"><span data-stu-id="f3c1f-108">Type: **[**D3DX10\_MESH\_DISCARD\_FLAGS**](d3dx10-mesh-discard-flags.md)**</span></span>

<span data-ttu-id="f3c1f-109">Especifica qué partes de los datos de la malla se van a descartar del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3c1f-109">Specifies which pieces of mesh data to discard from the device.</span></span> <span data-ttu-id="f3c1f-110">Consulte [**D3DX10 \_ mesh \_ discard \_ Flags**](d3dx10-mesh-discard-flags.md).</span><span class="sxs-lookup"><span data-stu-id="f3c1f-110">See [**D3DX10\_MESH\_DISCARD\_FLAGS**](d3dx10-mesh-discard-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3c1f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f3c1f-111">Return value</span></span>

<span data-ttu-id="f3c1f-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f3c1f-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f3c1f-113">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="f3c1f-113">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f3c1f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3c1f-114">Requirements</span></span>



| <span data-ttu-id="f3c1f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3c1f-115">Requirement</span></span> | <span data-ttu-id="f3c1f-116">Value</span><span class="sxs-lookup"><span data-stu-id="f3c1f-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f3c1f-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f3c1f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="f3c1f-118"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3c1f-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="f3c1f-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f3c1f-119">Library</span></span><br/> | <dl> <span data-ttu-id="f3c1f-120"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f3c1f-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3c1f-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="f3c1f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3c1f-122">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="f3c1f-122">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="f3c1f-123">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="f3c1f-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




