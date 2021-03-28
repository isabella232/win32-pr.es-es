---
title: Método ID3DX11DataProcessor CreateDeviceObject (D3DX11core. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Crea un objeto de dispositivo.
ms.assetid: 797d216b-2f54-4d24-aa97-04be0c71f909
keywords:
- Método CreateDeviceObject Direct3D 11
- Método CreateDeviceObject Direct3D 11, interfaz ID3DX11DataProcessor
- Interfaz ID3DX11DataProcessor Direct3D 11, método CreateDeviceObject
topic_type:
- apiref
api_name:
- ID3DX11DataProcessor.CreateDeviceObject
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6ff178cec1830d1b0213af23a2a70654416d35e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362806"
---
# <a name="id3dx11dataprocessorcreatedeviceobject-method"></a><span data-ttu-id="03c8d-107">ID3DX11DataProcessor:: CreateDeviceObject (método)</span><span class="sxs-lookup"><span data-stu-id="03c8d-107">ID3DX11DataProcessor::CreateDeviceObject method</span></span>

> [!Note]  
> <span data-ttu-id="03c8d-108">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="03c8d-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="03c8d-109">Crea un objeto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="03c8d-109">Creates a device object.</span></span>

## <a name="syntax"></a><span data-ttu-id="03c8d-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="03c8d-110">Syntax</span></span>


```C++
HRESULT CreateDeviceObject(
  [out] void **ppDataObject
);
```



## <a name="parameters"></a><span data-ttu-id="03c8d-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="03c8d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03c8d-112">*ppDataObject* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="03c8d-112">*ppDataObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="03c8d-113">Tipo: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="03c8d-113">Type: **void\*\***</span></span>

<span data-ttu-id="03c8d-114">Dirección de un puntero al objeto de dispositivo creado.</span><span class="sxs-lookup"><span data-stu-id="03c8d-114">Address of a pointer to the created device object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03c8d-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="03c8d-115">Return value</span></span>

<span data-ttu-id="03c8d-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="03c8d-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="03c8d-117">El valor devuelto es uno de los valores que se muestran en [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="03c8d-117">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="03c8d-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="03c8d-118">Remarks</span></span>

<span data-ttu-id="03c8d-119">Este método lo usa una [**interfaz ID3DX11ThreadPump**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="03c8d-119">This method is used by an [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="03c8d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03c8d-120">Requirements</span></span>



| <span data-ttu-id="03c8d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="03c8d-121">Requirement</span></span> | <span data-ttu-id="03c8d-122">Value</span><span class="sxs-lookup"><span data-stu-id="03c8d-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="03c8d-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="03c8d-123">Header</span></span><br/>  | <dl> <span data-ttu-id="03c8d-124"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="03c8d-124"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="03c8d-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="03c8d-125">Library</span></span><br/> | <dl> <span data-ttu-id="03c8d-126"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="03c8d-126"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="03c8d-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="03c8d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03c8d-128">ID3DX11DataProcessor</span><span class="sxs-lookup"><span data-stu-id="03c8d-128">ID3DX11DataProcessor</span></span>](id3dx11dataprocessor.md)
</dt> <dt>

[<span data-ttu-id="03c8d-129">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="03c8d-129">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





