---
title: Método ID3DX11ThreadPump GetWorkItemCount (D3DX11core. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Obtiene el número de elementos de trabajo en el bombeo de subprocesos.
ms.assetid: 04883b25-64dc-41a3-849f-710a59e9d3da
keywords:
- Método GetWorkItemCount Direct3D 11
- Método GetWorkItemCount Direct3D 11, interfaz ID3DX11ThreadPump
- Interfaz ID3DX11ThreadPump Direct3D 11, método GetWorkItemCount
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.GetWorkItemCount
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29668e66dd3d8c6d29cbfc69a4ef12a2fdfd18b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986904"
---
# <a name="id3dx11threadpumpgetworkitemcount-method"></a><span data-ttu-id="dee9e-107">ID3DX11ThreadPump:: GetWorkItemCount (método)</span><span class="sxs-lookup"><span data-stu-id="dee9e-107">ID3DX11ThreadPump::GetWorkItemCount method</span></span>

> [!Note]  
> <span data-ttu-id="dee9e-108">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="dee9e-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="dee9e-109">Obtiene el número de elementos de trabajo en el bombeo de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="dee9e-109">Gets the number of work items in the thread pump.</span></span>

## <a name="syntax"></a><span data-ttu-id="dee9e-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dee9e-110">Syntax</span></span>


```C++
UINT GetWorkItemCount();
```



## <a name="parameters"></a><span data-ttu-id="dee9e-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dee9e-111">Parameters</span></span>

<span data-ttu-id="dee9e-112">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="dee9e-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dee9e-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dee9e-113">Return value</span></span>

<span data-ttu-id="dee9e-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="dee9e-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="dee9e-115">El número de elementos de trabajo en cola en el bombeo de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="dee9e-115">The number of work items queued in the thread pump.</span></span>

## <a name="requirements"></a><span data-ttu-id="dee9e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dee9e-116">Requirements</span></span>



| <span data-ttu-id="dee9e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="dee9e-117">Requirement</span></span> | <span data-ttu-id="dee9e-118">Value</span><span class="sxs-lookup"><span data-stu-id="dee9e-118">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dee9e-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dee9e-119">Header</span></span><br/>  | <dl> <span data-ttu-id="dee9e-120"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="dee9e-120"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="dee9e-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dee9e-121">Library</span></span><br/> | <dl> <span data-ttu-id="dee9e-122"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dee9e-122"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dee9e-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="dee9e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dee9e-124">ID3DX11ThreadPump</span><span class="sxs-lookup"><span data-stu-id="dee9e-124">ID3DX11ThreadPump</span></span>](id3dx11threadpump.md)
</dt> <dt>

[<span data-ttu-id="dee9e-125">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="dee9e-125">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

