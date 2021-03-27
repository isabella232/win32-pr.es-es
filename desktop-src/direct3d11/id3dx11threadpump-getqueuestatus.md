---
title: Método ID3DX11ThreadPump GetQueueStatus (D3DX11core. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Obtiene el número de elementos de cada una de las tres colas dentro del bombeo de subprocesos.
ms.assetid: 69e1c786-6c7d-4432-bf34-3bf7606a07f6
keywords:
- Método GetQueueStatus Direct3D 11
- Método GetQueueStatus Direct3D 11, interfaz ID3DX11ThreadPump
- Interfaz ID3DX11ThreadPump Direct3D 11, método GetQueueStatus
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.GetQueueStatus
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3c945cb2978af15263d3f72d34a47c5e8ca8a69
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986905"
---
# <a name="id3dx11threadpumpgetqueuestatus-method"></a><span data-ttu-id="96ec7-107">ID3DX11ThreadPump:: GetQueueStatus (método)</span><span class="sxs-lookup"><span data-stu-id="96ec7-107">ID3DX11ThreadPump::GetQueueStatus method</span></span>

> [!Note]  
> <span data-ttu-id="96ec7-108">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="96ec7-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="96ec7-109">Obtiene el número de elementos de cada una de las tres colas dentro del bombeo de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="96ec7-109">Gets the number of items in each of the three queues inside the thread pump.</span></span>

## <a name="syntax"></a><span data-ttu-id="96ec7-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="96ec7-110">Syntax</span></span>


```C++
HRESULT GetQueueStatus(
  [in] UINT *pIoQueue,
  [in] UINT *pProcessQueue,
  [in] UINT *pDeviceQueue
);
```



## <a name="parameters"></a><span data-ttu-id="96ec7-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="96ec7-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96ec7-112">*pIoQueue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="96ec7-112">*pIoQueue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96ec7-113">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="96ec7-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="96ec7-114">Número de elementos de la cola de e/s.</span><span class="sxs-lookup"><span data-stu-id="96ec7-114">Number of items in the I/O queue.</span></span>

</dd> <dt>

<span data-ttu-id="96ec7-115">*pProcessQueue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="96ec7-115">*pProcessQueue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96ec7-116">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="96ec7-116">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="96ec7-117">Número de elementos de la cola de procesos.</span><span class="sxs-lookup"><span data-stu-id="96ec7-117">Number of items in the process queue.</span></span>

</dd> <dt>

<span data-ttu-id="96ec7-118">*pDeviceQueue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="96ec7-118">*pDeviceQueue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96ec7-119">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="96ec7-119">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="96ec7-120">Número de elementos en la cola del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="96ec7-120">Number of items in the device queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96ec7-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="96ec7-121">Return value</span></span>

<span data-ttu-id="96ec7-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="96ec7-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="96ec7-123">El valor devuelto es uno de los valores que se muestran en [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="96ec7-123">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="96ec7-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96ec7-124">Requirements</span></span>



| <span data-ttu-id="96ec7-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="96ec7-125">Requirement</span></span> | <span data-ttu-id="96ec7-126">Value</span><span class="sxs-lookup"><span data-stu-id="96ec7-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="96ec7-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="96ec7-127">Header</span></span><br/>  | <dl> <span data-ttu-id="96ec7-128"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="96ec7-128"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="96ec7-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="96ec7-129">Library</span></span><br/> | <dl> <span data-ttu-id="96ec7-130"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="96ec7-130"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="96ec7-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="96ec7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96ec7-132">ID3DX11ThreadPump</span><span class="sxs-lookup"><span data-stu-id="96ec7-132">ID3DX11ThreadPump</span></span>](id3dx11threadpump.md)
</dt> <dt>

[<span data-ttu-id="96ec7-133">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="96ec7-133">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

