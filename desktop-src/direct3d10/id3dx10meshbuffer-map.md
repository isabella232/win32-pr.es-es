---
description: Obtiene un puntero a la memoria del búfer de malla para modificar su contenido.
ms.assetid: d15ed47a-450e-404a-bcc2-a641abc2d02e
title: 'ID3DX10MeshBuffer:: Map (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10MeshBuffer.Map
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1b8cb03e128a6673963ce2d3cde993babb03da5c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362588"
---
# <a name="id3dx10meshbuffermap-method"></a><span data-ttu-id="6f4cd-103">ID3DX10MeshBuffer:: Map (método)</span><span class="sxs-lookup"><span data-stu-id="6f4cd-103">ID3DX10MeshBuffer::Map method</span></span>

<span data-ttu-id="6f4cd-104">Obtiene un puntero a la memoria del búfer de malla para modificar su contenido.</span><span class="sxs-lookup"><span data-stu-id="6f4cd-104">Get a pointer to the mesh buffer memory to modify its contents.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f4cd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6f4cd-105">Syntax</span></span>


```C++
HRESULT Map(
  [out] void   **ppData,
  [out] SIZE_T *pSize
);
```



## <a name="parameters"></a><span data-ttu-id="6f4cd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6f4cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f4cd-107">*ppData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6f4cd-107">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f4cd-108">Tipo: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="6f4cd-108">Type: **void\*\***</span></span>

<span data-ttu-id="6f4cd-109">Puntero a los datos del búfer.</span><span class="sxs-lookup"><span data-stu-id="6f4cd-109">Pointer to the buffer data.</span></span>

</dd> <dt>

<span data-ttu-id="6f4cd-110">*pSize* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6f4cd-110">*pSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f4cd-111">Tipo: **[ **tamaño \_ T**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6f4cd-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6f4cd-112">Tamaño del búfer en bytes.</span><span class="sxs-lookup"><span data-stu-id="6f4cd-112">Size of the buffer in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f4cd-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6f4cd-113">Return value</span></span>

<span data-ttu-id="6f4cd-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6f4cd-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6f4cd-115">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="6f4cd-115">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6f4cd-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6f4cd-116">Remarks</span></span>



|                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f4cd-117">Diferencias entre Direct3D 9 y Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="6f4cd-117">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="6f4cd-118">Map () en Direct3D 10 es análogo a mapa de recursos () en Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="6f4cd-118">Map() in Direct3D 10 is analogous to resource Map() in Direct3D 9.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6f4cd-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f4cd-119">Requirements</span></span>



| <span data-ttu-id="6f4cd-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f4cd-120">Requirement</span></span> | <span data-ttu-id="6f4cd-121">Value</span><span class="sxs-lookup"><span data-stu-id="6f4cd-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6f4cd-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6f4cd-122">Header</span></span><br/>  | <dl> <span data-ttu-id="6f4cd-123"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f4cd-123"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="6f4cd-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6f4cd-124">Library</span></span><br/> | <dl> <span data-ttu-id="6f4cd-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6f4cd-125"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f4cd-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f4cd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f4cd-127">ID3DX10MeshBuffer</span><span class="sxs-lookup"><span data-stu-id="6f4cd-127">ID3DX10MeshBuffer</span></span>](id3dx10meshbuffer.md)
</dt> <dt>

[<span data-ttu-id="6f4cd-128">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="6f4cd-128">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
