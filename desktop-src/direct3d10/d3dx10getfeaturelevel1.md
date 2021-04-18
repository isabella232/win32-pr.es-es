---
description: Obtiene un puntero de interfaz de dispositivo de Direct3D 10,1 de un puntero de interfaz de Direct3D 10,0.
ms.assetid: cf31a67f-0493-4e79-8e73-0297ab93bbae
title: Función D3DX10GetFeatureLevel1 (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10GetFeatureLevel1
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 817eb4dd68ce797da76c0609e2ead01a21b5b270
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707749"
---
# <a name="d3dx10getfeaturelevel1-function"></a><span data-ttu-id="151d5-103">D3DX10GetFeatureLevel1 función)</span><span class="sxs-lookup"><span data-stu-id="151d5-103">D3DX10GetFeatureLevel1 function</span></span>

<span data-ttu-id="151d5-104">Obtiene un puntero de interfaz de dispositivo de Direct3D 10,1 de un puntero de interfaz de Direct3D 10,0.</span><span class="sxs-lookup"><span data-stu-id="151d5-104">Get a Direct3D 10.1 device interface pointer from a Direct3D 10.0 interface pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="151d5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="151d5-105">Syntax</span></span>


```C++
HRESULT D3DX10GetFeatureLevel1(
  _In_  ID3D10Device  *pDevice,
  _Out_ ID3D10Device1 **ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="151d5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="151d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="151d5-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="151d5-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="151d5-108">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="151d5-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="151d5-109">Puntero al dispositivo Direct3D 10,0 (vea la interfaz [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) ).</span><span class="sxs-lookup"><span data-stu-id="151d5-109">Pointer to the Direct3D 10.0 device (see the [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) interface).</span></span>

</dd> <dt>

<span data-ttu-id="151d5-110">*ppDevice* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="151d5-110">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="151d5-111">Tipo: **[ **ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1)\*\***</span><span class="sxs-lookup"><span data-stu-id="151d5-111">Type: **[**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1)\*\***</span></span>

<span data-ttu-id="151d5-112">Puntero al dispositivo Direct3D 10,1 (vea la interfaz [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) ).</span><span class="sxs-lookup"><span data-stu-id="151d5-112">Pointer to the Direct3D 10.1 device (see the [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) interface).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="151d5-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="151d5-113">Return value</span></span>

<span data-ttu-id="151d5-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="151d5-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="151d5-115">Esta función devuelve uno de los siguientes [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="151d5-115">This function returns one of the following [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span> <span data-ttu-id="151d5-116">Si se puede adquirir una interfaz de dispositivo de Direct3D 10,1, esta función se ejecuta correctamente y pasa un puntero a la interfaz 10,1 mediante el parámetro *ppDevice* .</span><span class="sxs-lookup"><span data-stu-id="151d5-116">If a Direct3D 10.1 device interface can be acquired, this function succeeds and passes a pointer to the 10.1 interface using the *ppDevice* parameter.</span></span> <span data-ttu-id="151d5-117">Si no se puede adquirir una interfaz de dispositivo de Direct3D 10,1, esta función devuelve E \_ FAIL, y no devolverá nada para el parámetro *ppDevice* .</span><span class="sxs-lookup"><span data-stu-id="151d5-117">If a Direct3D 10.1 device interface cannot be acquired, this function returns E\_FAIL, and will not return anything for the *ppDevice* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="151d5-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="151d5-118">Remarks</span></span>

<span data-ttu-id="151d5-119">Para que esta función se realice correctamente, debe haber adquirido el puntero [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) proporcionado mediante una llamada a la función [**D3DX10CreateDevice**](d3dx10createdevice.md) , la función [**D3DX10CreateDeviceAndSwapChain**](d3dx10createdeviceandswapchain.md) , la función [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1) o la función [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1) .</span><span class="sxs-lookup"><span data-stu-id="151d5-119">For this function to succeed, you must have acquired the supplied [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) pointer using a call to the [**D3DX10CreateDevice**](d3dx10createdevice.md) function, the [**D3DX10CreateDeviceAndSwapChain**](d3dx10createdeviceandswapchain.md) function, the [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1) function, or the [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1) function.</span></span>

<span data-ttu-id="151d5-120">Solo puede crear un dispositivo Direct3D 10,1 en equipos que ejecuten Windows Vista Service Pack 1 o posterior y con el hardware compatible con Direct3D 10,1 instalado.</span><span class="sxs-lookup"><span data-stu-id="151d5-120">You can only create a Direct3D 10.1 device on computers running Windows Vista Service Pack 1 or later, and with Direct3D 10.1-compatible hardware installed.</span></span> <span data-ttu-id="151d5-121">Esta función devolverá E \_ producirá un error en cualquier equipo que no cumpla estos requisitos.</span><span class="sxs-lookup"><span data-stu-id="151d5-121">This function will return E\_FAIL on any computer not meeting these requirements.</span></span> <span data-ttu-id="151d5-122">Sin embargo, puede llamar a esta función en cualquier versión de Windows que tenga instalado el archivo DLL D3DX10.</span><span class="sxs-lookup"><span data-stu-id="151d5-122">However, you can call this function on any version of Windows that has the D3DX10 DLL installed.</span></span>

## <a name="requirements"></a><span data-ttu-id="151d5-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="151d5-123">Requirements</span></span>



| <span data-ttu-id="151d5-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="151d5-124">Requirement</span></span> | <span data-ttu-id="151d5-125">Value</span><span class="sxs-lookup"><span data-stu-id="151d5-125">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="151d5-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="151d5-126">Header</span></span><br/> | <dl> <span data-ttu-id="151d5-127"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="151d5-127"><dt>D3DX10Core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="151d5-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="151d5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="151d5-129">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="151d5-129">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 




