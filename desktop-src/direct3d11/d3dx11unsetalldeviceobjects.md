---
title: Función D3DX11UnsetAllDeviceObjects (D3DX11core. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Tenga en cuenta que, en lugar de usar esta función, se recomienda usar el método ID3D11DeviceContext ClearState.
ms.assetid: 0e52bbca-f171-477f-89b0-ba56a2cfa096
keywords:
- Función D3DX11UnsetAllDeviceObjects Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11UnsetAllDeviceObjects
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8ac7e33bfef7f8470f616ac07b3aa90463f3f3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362667"
---
# <a name="d3dx11unsetalldeviceobjects-function"></a><span data-ttu-id="003c3-105">D3DX11UnsetAllDeviceObjects función)</span><span class="sxs-lookup"><span data-stu-id="003c3-105">D3DX11UnsetAllDeviceObjects function</span></span>

> [!Note]  
> <span data-ttu-id="003c3-106">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="003c3-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="003c3-107">En lugar de usar esta función, se recomienda usar el método [**ID3D11DeviceContext:: ClearState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-clearstate) .</span><span class="sxs-lookup"><span data-stu-id="003c3-107">Instead of using this function, we recommend that you use the [**ID3D11DeviceContext::ClearState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-clearstate) method.</span></span>

 

<span data-ttu-id="003c3-108">Quita todos los recursos del dispositivo estableciendo sus punteros en **null**.</span><span class="sxs-lookup"><span data-stu-id="003c3-108">Removes all resources from the device by setting their pointers to **NULL**.</span></span> <span data-ttu-id="003c3-109">Se debe llamar a este método durante el cierre de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="003c3-109">This should be called during shutdown of your application.</span></span> <span data-ttu-id="003c3-110">Ayuda a garantizar que cuando se liberan todos los recursos que no están enlazados al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="003c3-110">It helps ensure that when one is releasing all of their resources that none of them are bound to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="003c3-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="003c3-111">Syntax</span></span>


```C++
HRESULT D3DX11UnsetAllDeviceObjects(
  _In_ ID3D11DeviceContext *pContext
);
```



## <a name="parameters"></a><span data-ttu-id="003c3-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="003c3-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="003c3-113">*pContext* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="003c3-113">*pContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="003c3-114">Tipo: **[ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="003c3-114">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="003c3-115">Puntero a un objeto [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="003c3-115">Pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="003c3-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="003c3-116">Return value</span></span>

<span data-ttu-id="003c3-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="003c3-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="003c3-118">El valor devuelto es uno de los valores que se muestran en [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="003c3-118">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="003c3-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="003c3-119">Requirements</span></span>



| <span data-ttu-id="003c3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="003c3-120">Requirement</span></span> | <span data-ttu-id="003c3-121">Value</span><span class="sxs-lookup"><span data-stu-id="003c3-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="003c3-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="003c3-122">Header</span></span><br/>  | <dl> <span data-ttu-id="003c3-123"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="003c3-123"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="003c3-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="003c3-124">Library</span></span><br/> | <dl> <span data-ttu-id="003c3-125"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="003c3-125"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="003c3-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="003c3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="003c3-127">Funciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="003c3-127">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

 





