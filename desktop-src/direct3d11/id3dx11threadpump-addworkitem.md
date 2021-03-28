---
title: Método ID3DX11ThreadPump AddWorkItem (D3DX11core. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Agrega un elemento de trabajo al bombeo de subprocesos.
ms.assetid: 2578506c-6175-457a-bf10-94929bb3c0c4
keywords:
- Método AddWorkItem Direct3D 11
- Método AddWorkItem Direct3D 11, interfaz ID3DX11ThreadPump
- Interfaz ID3DX11ThreadPump Direct3D 11, método AddWorkItem
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.AddWorkItem
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebf249405bd71287f93444ae8d23dab694027360
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362454"
---
# <a name="id3dx11threadpumpaddworkitem-method"></a><span data-ttu-id="bc843-107">ID3DX11ThreadPump:: AddWorkItem (método)</span><span class="sxs-lookup"><span data-stu-id="bc843-107">ID3DX11ThreadPump::AddWorkItem method</span></span>

> [!Note]  
> <span data-ttu-id="bc843-108">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="bc843-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="bc843-109">Agrega un elemento de trabajo al bombeo de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="bc843-109">Adds a work item to the thread pump.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc843-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bc843-110">Syntax</span></span>


```C++
HRESULT AddWorkItem(
  [in]  ID3DX11DataLoader    *pDataLoader,
  [in]  ID3DX11DataProcessor *pDataProcessor,
  [in]  HRESULT              *pHResult,
  [out] void                 **ppDeviceObject
);
```



## <a name="parameters"></a><span data-ttu-id="bc843-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bc843-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc843-112">*pDataLoader* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bc843-112">*pDataLoader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc843-113">Tipo: **[ **ID3DX11DataLoader**](id3dx11dataloader.md)\***</span><span class="sxs-lookup"><span data-stu-id="bc843-113">Type: **[**ID3DX11DataLoader**](id3dx11dataloader.md)\***</span></span>

<span data-ttu-id="bc843-114">Cargador que el bombeo de subprocesos usará cuando un elemento de trabajo requiera que se carguen los datos.</span><span class="sxs-lookup"><span data-stu-id="bc843-114">The loader that the thread pump will use when a work item requires data to be loaded.</span></span>

</dd> <dt>

<span data-ttu-id="bc843-115">*pDataProcessor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bc843-115">*pDataProcessor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc843-116">Tipo: **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\***</span><span class="sxs-lookup"><span data-stu-id="bc843-116">Type: **[**ID3DX11DataProcessor**](id3dx11dataprocessor.md)\***</span></span>

<span data-ttu-id="bc843-117">Procesador que utilizará el bombeo de subprocesos cuando un elemento de trabajo requiera que se procesen los datos.</span><span class="sxs-lookup"><span data-stu-id="bc843-117">The processor that the thread pump will use when a work item requires data to be processed.</span></span>

</dd> <dt>

<span data-ttu-id="bc843-118">*pHResult* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bc843-118">*pHResult* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc843-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="bc843-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="bc843-120">Puntero al valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="bc843-120">A pointer to the return value.</span></span> <span data-ttu-id="bc843-121">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="bc843-121">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bc843-122">*ppDeviceObject* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="bc843-122">*ppDeviceObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc843-123">Tipo: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="bc843-123">Type: **void\*\***</span></span>

<span data-ttu-id="bc843-124">El dispositivo que usa el objeto.</span><span class="sxs-lookup"><span data-stu-id="bc843-124">The device that uses the object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc843-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bc843-125">Return value</span></span>

<span data-ttu-id="bc843-126">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bc843-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bc843-127">El valor devuelto es uno de los valores que se muestran en [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="bc843-127">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bc843-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc843-128">Requirements</span></span>



| <span data-ttu-id="bc843-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc843-129">Requirement</span></span> | <span data-ttu-id="bc843-130">Value</span><span class="sxs-lookup"><span data-stu-id="bc843-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc843-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bc843-131">Header</span></span><br/>  | <dl> <span data-ttu-id="bc843-132"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc843-132"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="bc843-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bc843-133">Library</span></span><br/> | <dl> <span data-ttu-id="bc843-134"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc843-134"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bc843-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="bc843-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc843-136">ID3DX11ThreadPump</span><span class="sxs-lookup"><span data-stu-id="bc843-136">ID3DX11ThreadPump</span></span>](id3dx11threadpump.md)
</dt> <dt>

[<span data-ttu-id="bc843-137">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="bc843-137">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





