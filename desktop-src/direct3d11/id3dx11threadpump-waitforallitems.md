---
title: Método ID3DX11ThreadPump WaitForAllItems (D3DX11core. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Espera a que finalicen todos los elementos de trabajo en el bombeo de subprocesos.
ms.assetid: 6dfdaee8-e563-4c37-a2c1-4b115e29c434
keywords:
- Método WaitForAllItems Direct3D 11
- Método WaitForAllItems Direct3D 11, interfaz ID3DX11ThreadPump
- Interfaz ID3DX11ThreadPump Direct3D 11, método WaitForAllItems
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.WaitForAllItems
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40abbab67d6743be2190d5e81c733f63b52b32f5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998449"
---
# <a name="id3dx11threadpumpwaitforallitems-method"></a><span data-ttu-id="506b7-107">ID3DX11ThreadPump:: WaitForAllItems (método)</span><span class="sxs-lookup"><span data-stu-id="506b7-107">ID3DX11ThreadPump::WaitForAllItems method</span></span>

> [!Note]  
> <span data-ttu-id="506b7-108">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="506b7-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="506b7-109">Espera a que finalicen todos los elementos de trabajo en el bombeo de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="506b7-109">Waits for all work items in the thread pump to finish.</span></span>

## <a name="syntax"></a><span data-ttu-id="506b7-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="506b7-110">Syntax</span></span>


```C++
HRESULT WaitForAllItems();
```



## <a name="parameters"></a><span data-ttu-id="506b7-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="506b7-111">Parameters</span></span>

<span data-ttu-id="506b7-112">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="506b7-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="506b7-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="506b7-113">Return value</span></span>

<span data-ttu-id="506b7-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="506b7-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="506b7-115">El valor devuelto es uno de los valores que se muestran en [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="506b7-115">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="506b7-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="506b7-116">Requirements</span></span>



| <span data-ttu-id="506b7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="506b7-117">Requirement</span></span> | <span data-ttu-id="506b7-118">Value</span><span class="sxs-lookup"><span data-stu-id="506b7-118">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="506b7-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="506b7-119">Header</span></span><br/>  | <dl> <span data-ttu-id="506b7-120"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="506b7-120"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="506b7-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="506b7-121">Library</span></span><br/> | <dl> <span data-ttu-id="506b7-122"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="506b7-122"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="506b7-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="506b7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="506b7-124">ID3DX11ThreadPump</span><span class="sxs-lookup"><span data-stu-id="506b7-124">ID3DX11ThreadPump</span></span>](id3dx11threadpump.md)
</dt> <dt>

[<span data-ttu-id="506b7-125">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="506b7-125">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





