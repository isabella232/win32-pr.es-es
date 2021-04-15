---
description: Obtiene el número de elementos de cada una de las tres colas dentro del bombeo de subprocesos.
ms.assetid: b5b829a5-5ef7-4ef5-afb4-efe1bb22ae70
title: 'ID3DX10ThreadPump:: GetQueueStatus (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10ThreadPump.GetQueueStatus
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4cf3b5879da0346cefbb5b8835d6922dd736cfd3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708108"
---
# <a name="id3dx10threadpumpgetqueuestatus-method"></a><span data-ttu-id="186a6-103">ID3DX10ThreadPump:: GetQueueStatus (método)</span><span class="sxs-lookup"><span data-stu-id="186a6-103">ID3DX10ThreadPump::GetQueueStatus method</span></span>

<span data-ttu-id="186a6-104">Obtiene el número de elementos de cada una de las tres colas dentro del bombeo de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="186a6-104">Get the number of items in each of the three queues inside the thread pump.</span></span>

## <a name="syntax"></a><span data-ttu-id="186a6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="186a6-105">Syntax</span></span>


```C++
HRESULT GetQueueStatus(
  [in] UINT *pIoQueue,
  [in] UINT *pProcessQueue,
  [in] UINT *pDeviceQueue
);
```



## <a name="parameters"></a><span data-ttu-id="186a6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="186a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="186a6-107">*pIoQueue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="186a6-107">*pIoQueue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="186a6-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="186a6-108">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="186a6-109">Número de elementos de la cola de e/s.</span><span class="sxs-lookup"><span data-stu-id="186a6-109">Number of items in the I/O queue.</span></span>

</dd> <dt>

<span data-ttu-id="186a6-110">*pProcessQueue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="186a6-110">*pProcessQueue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="186a6-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="186a6-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="186a6-112">Número de elementos de la cola de procesos.</span><span class="sxs-lookup"><span data-stu-id="186a6-112">Number of items in the process queue.</span></span>

</dd> <dt>

<span data-ttu-id="186a6-113">*pDeviceQueue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="186a6-113">*pDeviceQueue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="186a6-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="186a6-114">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="186a6-115">Número de elementos en la cola del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="186a6-115">Number of items in the device queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="186a6-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="186a6-116">Return value</span></span>

<span data-ttu-id="186a6-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="186a6-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="186a6-118">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="186a6-118">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="186a6-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="186a6-119">Requirements</span></span>



| <span data-ttu-id="186a6-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="186a6-120">Requirement</span></span> | <span data-ttu-id="186a6-121">Value</span><span class="sxs-lookup"><span data-stu-id="186a6-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="186a6-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="186a6-122">Header</span></span><br/>  | <dl> <span data-ttu-id="186a6-123"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="186a6-123"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="186a6-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="186a6-124">Library</span></span><br/> | <dl> <span data-ttu-id="186a6-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="186a6-125"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="186a6-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="186a6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="186a6-127">ID3DX10ThreadPump</span><span class="sxs-lookup"><span data-stu-id="186a6-127">ID3DX10ThreadPump</span></span>](id3dx10threadpump.md)
</dt> <dt>

[<span data-ttu-id="186a6-128">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="186a6-128">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
