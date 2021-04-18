---
description: Agregue un elemento de trabajo al bombeo de subprocesos.
ms.assetid: f07789dc-a3d5-4bad-9768-527e701271b8
title: 'ID3DX10ThreadPump:: AddWorkItem (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10ThreadPump.AddWorkItem
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: aaf5286ca6cf7b61b0027b176d9a9261bd0beaa8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708110"
---
# <a name="id3dx10threadpumpaddworkitem-method"></a><span data-ttu-id="b3518-103">ID3DX10ThreadPump:: AddWorkItem (método)</span><span class="sxs-lookup"><span data-stu-id="b3518-103">ID3DX10ThreadPump::AddWorkItem method</span></span>

<span data-ttu-id="b3518-104">Agregue un elemento de trabajo al bombeo de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="b3518-104">Add a work item to the thread pump.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3518-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b3518-105">Syntax</span></span>


```C++
HRESULT AddWorkItem(
  [in]  ID3DX10DataLoader    *pDataLoader,
  [in]  ID3DX10DataProcessor *pDataProcessor,
  [in]  HRESULT              *pHResult,
  [out] void                 **ppDeviceObject
);
```



## <a name="parameters"></a><span data-ttu-id="b3518-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b3518-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3518-107">*pDataLoader* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b3518-107">*pDataLoader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3518-108">Tipo: **[ **ID3DX10DataLoader**](id3dx10dataloader.md)\***</span><span class="sxs-lookup"><span data-stu-id="b3518-108">Type: **[**ID3DX10DataLoader**](id3dx10dataloader.md)\***</span></span>

<span data-ttu-id="b3518-109">Cargador que el bombeo de subprocesos usará cuando un elemento de trabajo requiera que se carguen los datos.</span><span class="sxs-lookup"><span data-stu-id="b3518-109">The loader that the thread pump will use when a work item requires data to be loaded.</span></span>

</dd> <dt>

<span data-ttu-id="b3518-110">*pDataProcessor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b3518-110">*pDataProcessor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3518-111">Tipo: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\***</span><span class="sxs-lookup"><span data-stu-id="b3518-111">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\***</span></span>

<span data-ttu-id="b3518-112">Procesador que utilizará el bombeo de subprocesos cuando un elemento de trabajo requiera que se procesen los datos.</span><span class="sxs-lookup"><span data-stu-id="b3518-112">The processor that the thread pump will use when a work item requires data to be processed.</span></span>

</dd> <dt>

<span data-ttu-id="b3518-113">*pHResult* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b3518-113">*pHResult* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3518-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="b3518-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="b3518-115">Puntero al valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="b3518-115">A pointer to the return value.</span></span> <span data-ttu-id="b3518-116">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="b3518-116">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b3518-117">*ppDeviceObject* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b3518-117">*ppDeviceObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3518-118">Tipo: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="b3518-118">Type: **void\*\***</span></span>

<span data-ttu-id="b3518-119">El dispositivo que usa el objeto.</span><span class="sxs-lookup"><span data-stu-id="b3518-119">The device that uses the object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3518-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b3518-120">Return value</span></span>

<span data-ttu-id="b3518-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b3518-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b3518-122">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="b3518-122">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b3518-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3518-123">Requirements</span></span>



| <span data-ttu-id="b3518-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3518-124">Requirement</span></span> | <span data-ttu-id="b3518-125">Value</span><span class="sxs-lookup"><span data-stu-id="b3518-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b3518-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b3518-126">Header</span></span><br/>  | <dl> <span data-ttu-id="b3518-127"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3518-127"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="b3518-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b3518-128">Library</span></span><br/> | <dl> <span data-ttu-id="b3518-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b3518-129"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3518-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="b3518-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3518-131">ID3DX10ThreadPump</span><span class="sxs-lookup"><span data-stu-id="b3518-131">ID3DX10ThreadPump</span></span>](id3dx10threadpump.md)
</dt> <dt>

[<span data-ttu-id="b3518-132">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="b3518-132">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




