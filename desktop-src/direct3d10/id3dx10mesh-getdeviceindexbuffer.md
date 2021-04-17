---
description: 'Obtenga acceso al búfer de índice de la malla una vez que se haya confirmado en el dispositivo con ID3DX10Mesh:: CommitToDevice. Esto es diferente de ID3DX10Mesh:: GetIndexBuffer, que devuelve el búfer de índice antes de que se haya confirmado en el dispositivo.'
ms.assetid: 94d21f50-91b5-4f8d-ac73-7a851bba8685
title: 'ID3DX10Mesh:: GetDeviceIndexBuffer (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetDeviceIndexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3ec3e65cfc4acb5a903bcf18d2f707d39127e975
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698328"
---
# <a name="id3dx10meshgetdeviceindexbuffer-method"></a><span data-ttu-id="363b3-104">ID3DX10Mesh:: GetDeviceIndexBuffer (método)</span><span class="sxs-lookup"><span data-stu-id="363b3-104">ID3DX10Mesh::GetDeviceIndexBuffer method</span></span>

<span data-ttu-id="363b3-105">Obtenga acceso al búfer de índice de la malla una vez que se haya confirmado en el dispositivo con [**ID3DX10Mesh:: CommitToDevice**](id3dx10mesh-committodevice.md).</span><span class="sxs-lookup"><span data-stu-id="363b3-105">Access the mesh's index buffer after it has been committed to the device with [**ID3DX10Mesh::CommitToDevice**](id3dx10mesh-committodevice.md).</span></span> <span data-ttu-id="363b3-106">Esto es diferente de [**ID3DX10Mesh:: GetIndexBuffer**](id3dx10mesh-getindexbuffer.md), que devuelve el búfer de índice antes de que se haya confirmado en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="363b3-106">This is different from [**ID3DX10Mesh::GetIndexBuffer**](id3dx10mesh-getindexbuffer.md), which returns the index buffer before it has been committed to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="363b3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="363b3-107">Syntax</span></span>


```C++
HRESULT GetDeviceIndexBuffer(
  [out] ID3D10Buffer **ppIndexBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="363b3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="363b3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="363b3-109">*ppIndexBuffer* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="363b3-109">*ppIndexBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="363b3-110">Tipo: **[ **ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)\*\***</span><span class="sxs-lookup"><span data-stu-id="363b3-110">Type: **[**ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)\*\***</span></span>

<span data-ttu-id="363b3-111">Búfer de índice después de haberse confirmado en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="363b3-111">The index buffer after it has been committed to the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="363b3-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="363b3-112">Return value</span></span>

<span data-ttu-id="363b3-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="363b3-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="363b3-114">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="363b3-114">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="363b3-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="363b3-115">Remarks</span></span>

<span data-ttu-id="363b3-116">Si el búfer de índice de la malla aún no se ha confirmado en el dispositivo, esta API confirmará automáticamente el búfer de índice antes de devolver un puntero al búfer.</span><span class="sxs-lookup"><span data-stu-id="363b3-116">If the mesh's index buffer has not already been committed to the device, this API will automatically commit the index buffer before it returns a pointer to the buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="363b3-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="363b3-117">Requirements</span></span>



| <span data-ttu-id="363b3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="363b3-118">Requirement</span></span> | <span data-ttu-id="363b3-119">Value</span><span class="sxs-lookup"><span data-stu-id="363b3-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="363b3-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="363b3-120">Header</span></span><br/>  | <dl> <span data-ttu-id="363b3-121"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="363b3-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="363b3-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="363b3-122">Library</span></span><br/> | <dl> <span data-ttu-id="363b3-123"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="363b3-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="363b3-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="363b3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="363b3-125">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="363b3-125">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="363b3-126">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="363b3-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




