---
title: Método ID3DX11DataLoader Destroy (D3DX11core. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Destruye el cargador una vez finalizado un elemento de trabajo.
ms.assetid: 5d86c4ad-3eb6-421f-bb77-c88e8f5b42bb
keywords:
- Destruir (método) Direct3D 11
- Método destroy Direct3D 11, ID3DX11DataLoader (interfaz)
- Interfaz ID3DX11DataLoader Direct3D 11, método destroy
topic_type:
- apiref
api_name:
- ID3DX11DataLoader.Destroy
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12c3a1c6511a00d66704c104b3b69150a8509e41
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987247"
---
# <a name="id3dx11dataloaderdestroy-method"></a><span data-ttu-id="98e78-107">ID3DX11DataLoader::D método estroy</span><span class="sxs-lookup"><span data-stu-id="98e78-107">ID3DX11DataLoader::Destroy method</span></span>

> [!Note]  
> <span data-ttu-id="98e78-108">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="98e78-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="98e78-109">Destruye el cargador una vez finalizado un elemento de trabajo.</span><span class="sxs-lookup"><span data-stu-id="98e78-109">Destroys the loader after a work item completes.</span></span>

## <a name="syntax"></a><span data-ttu-id="98e78-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="98e78-110">Syntax</span></span>


```C++
HRESULT Destroy();
```



## <a name="parameters"></a><span data-ttu-id="98e78-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="98e78-111">Parameters</span></span>

<span data-ttu-id="98e78-112">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="98e78-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="98e78-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="98e78-113">Return value</span></span>

<span data-ttu-id="98e78-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="98e78-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="98e78-115">El valor devuelto es uno de los valores que se muestran en [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="98e78-115">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="98e78-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="98e78-116">Remarks</span></span>

<span data-ttu-id="98e78-117">Este método lo usa una [**interfaz ID3DX11ThreadPump**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="98e78-117">This method is used by an [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="98e78-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98e78-118">Requirements</span></span>



| <span data-ttu-id="98e78-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="98e78-119">Requirement</span></span> | <span data-ttu-id="98e78-120">Value</span><span class="sxs-lookup"><span data-stu-id="98e78-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="98e78-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="98e78-121">Header</span></span><br/>  | <dl> <span data-ttu-id="98e78-122"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="98e78-122"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="98e78-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="98e78-123">Library</span></span><br/> | <dl> <span data-ttu-id="98e78-124"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="98e78-124"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="98e78-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="98e78-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98e78-126">ID3DX11DataLoader</span><span class="sxs-lookup"><span data-stu-id="98e78-126">ID3DX11DataLoader</span></span>](id3dx11dataloader.md)
</dt> <dt>

[<span data-ttu-id="98e78-127">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="98e78-127">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





