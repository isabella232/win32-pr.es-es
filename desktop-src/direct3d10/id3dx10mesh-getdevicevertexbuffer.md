---
description: 'Obtenga acceso al búfer de vértices de la malla una vez que se haya confirmado en el dispositivo con ID3DX10Mesh:: CommitToDevice. Esto es diferente de ID3DX10Mesh:: GetVertexBuffer, que devuelve el búfer de vértices antes de que se haya confirmado en el dispositivo.'
ms.assetid: 621d9105-e55d-47b8-8557-8adb7db19d66
title: 'ID3DX10Mesh:: GetDeviceVertexBuffer (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetDeviceVertexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9943050d174acb4e8f8e676f56a95cfdcde88f5a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718369"
---
# <a name="id3dx10meshgetdevicevertexbuffer-method"></a><span data-ttu-id="7c421-104">ID3DX10Mesh:: GetDeviceVertexBuffer (método)</span><span class="sxs-lookup"><span data-stu-id="7c421-104">ID3DX10Mesh::GetDeviceVertexBuffer method</span></span>

<span data-ttu-id="7c421-105">Obtenga acceso al búfer de vértices de la malla una vez que se haya confirmado en el dispositivo con [**ID3DX10Mesh:: CommitToDevice**](id3dx10mesh-committodevice.md).</span><span class="sxs-lookup"><span data-stu-id="7c421-105">Access the mesh's vertex buffer after it has been committed to the device with [**ID3DX10Mesh::CommitToDevice**](id3dx10mesh-committodevice.md).</span></span> <span data-ttu-id="7c421-106">Esto es diferente de [**ID3DX10Mesh:: GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md), que devuelve el búfer de vértices antes de que se haya confirmado en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7c421-106">This is different from [**ID3DX10Mesh::GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md), which returns the vertex buffer before it has been committed to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c421-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7c421-107">Syntax</span></span>


```C++
HRESULT GetDeviceVertexBuffer(
  [in]  UINT         iBuffer,
  [out] ID3D10Buffer **ppVertexBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="7c421-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7c421-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c421-109">*iBuffer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7c421-109">*iBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c421-110">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7c421-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7c421-111">Índice que identifica a qué búfer de vértice se va a tener acceso.</span><span class="sxs-lookup"><span data-stu-id="7c421-111">An index identifying which vertex buffer to access.</span></span>

</dd> <dt>

<span data-ttu-id="7c421-112">*ppVertexBuffer* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7c421-112">*ppVertexBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c421-113">Tipo: **[ **ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)\*\***</span><span class="sxs-lookup"><span data-stu-id="7c421-113">Type: **[**ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)\*\***</span></span>

<span data-ttu-id="7c421-114">Búfer de vértices después de que se haya confirmado en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7c421-114">The vertex buffer after it has been committed to the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c421-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7c421-115">Return value</span></span>

<span data-ttu-id="7c421-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7c421-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7c421-117">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="7c421-117">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7c421-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c421-118">Requirements</span></span>



| <span data-ttu-id="7c421-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c421-119">Requirement</span></span> | <span data-ttu-id="7c421-120">Value</span><span class="sxs-lookup"><span data-stu-id="7c421-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7c421-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7c421-121">Header</span></span><br/>  | <dl> <span data-ttu-id="7c421-122"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c421-122"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="7c421-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7c421-123">Library</span></span><br/> | <dl> <span data-ttu-id="7c421-124"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c421-124"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c421-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="7c421-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c421-126">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="7c421-126">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="7c421-127">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="7c421-127">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
