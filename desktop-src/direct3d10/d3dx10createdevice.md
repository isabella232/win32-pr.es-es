---
description: Cree el mejor dispositivo Direct3D 10 que representa el adaptador de pantalla. Si se puede crear un dispositivo compatible con Direct3D 10,1, será posible adquirir un puntero de interfaz ID3D10Device1 desde el puntero de interfaz de dispositivo devuelto.
ms.assetid: 1af8f4e5-a59e-403a-95d2-069b91bad93e
title: Función D3DX10CreateDevice (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateDevice
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 38236a48cdd5197f7f19ef9be3f6fc0f1faca72c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718426"
---
# <a name="d3dx10createdevice-function"></a><span data-ttu-id="92fea-104">D3DX10CreateDevice función)</span><span class="sxs-lookup"><span data-stu-id="92fea-104">D3DX10CreateDevice function</span></span>

<span data-ttu-id="92fea-105">Cree el mejor dispositivo Direct3D 10 que representa el adaptador de pantalla.</span><span class="sxs-lookup"><span data-stu-id="92fea-105">Create the best Direct3D 10 device that represents the display adapter.</span></span> <span data-ttu-id="92fea-106">Si se puede crear un dispositivo compatible con Direct3D 10,1, será posible adquirir un puntero de [**interfaz ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) desde el puntero de interfaz de dispositivo devuelto.</span><span class="sxs-lookup"><span data-stu-id="92fea-106">If a Direct3D 10.1-compatible device can be created, it will be possible to acquire an [**ID3D10Device1 Interface**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) pointer from the returned device interface pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="92fea-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92fea-107">Syntax</span></span>


```C++
HRESULT D3DX10CreateDevice(
  _In_  IDXGIAdapter      *pAdapter,
  _In_  D3D10_DRIVER_TYPE DriverType,
  _In_  HMODULE           Software,
  _In_  UINT              Flags,
  _Out_ ID3D10Device      **ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="92fea-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="92fea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92fea-109">*pAdapter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="92fea-109">*pAdapter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92fea-110">Tipo: **[ **IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)\***</span><span class="sxs-lookup"><span data-stu-id="92fea-110">Type: **[**IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)\***</span></span>

<span data-ttu-id="92fea-111">Puntero al adaptador de pantalla (consulte la interfaz [**IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter) ) al crear un dispositivo de hardware; de lo contrario, establezca este parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="92fea-111">Pointer to the display adapter (see the [**IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter) interface) when creating a hardware device; otherwise set this parameter to **NULL**.</span></span> <span data-ttu-id="92fea-112">Si se especifica **null** al crear un dispositivo de hardware, Direct3D usará el primer adaptador enumerado por la interfaz [**IDXGIFactory**](/windows/win32/api/dxgi/nn-dxgi-idxgifactory) .</span><span class="sxs-lookup"><span data-stu-id="92fea-112">If **NULL** is specified when creating a hardware device, Direct3D will use the first adapter enumerated by the [**IDXGIFactory**](/windows/win32/api/dxgi/nn-dxgi-idxgifactory) interface.</span></span>

</dd> <dt>

<span data-ttu-id="92fea-113">*DriverType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="92fea-113">*DriverType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92fea-114">Tipo: **[ **\_ \_ tipo de controlador D3D10**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)**</span><span class="sxs-lookup"><span data-stu-id="92fea-114">Type: **[**D3D10\_DRIVER\_TYPE**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)**</span></span>

<span data-ttu-id="92fea-115">El tipo de controlador de dispositivo (vea la enumeración del [**\_ \_ tipo de controlador D3D10**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type) ).</span><span class="sxs-lookup"><span data-stu-id="92fea-115">The device-driver type (see the [**D3D10\_DRIVER\_TYPE**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type) enumeration).</span></span> <span data-ttu-id="92fea-116">El tipo de controlador determina el tipo de dispositivo que va a crear.</span><span class="sxs-lookup"><span data-stu-id="92fea-116">The driver type determines the type of device you will create.</span></span>

</dd> <dt>

<span data-ttu-id="92fea-117">*Software* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="92fea-117">*Software* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92fea-118">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="92fea-118">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="92fea-119">Identificador de un módulo cargado que implementa un controlador de software (como D3D10Ref.dll).</span><span class="sxs-lookup"><span data-stu-id="92fea-119">A handle to a loaded module that implements a software driver (such as D3D10Ref.dll).</span></span> <span data-ttu-id="92fea-120">Para obtener un identificador, llame a la función [GetModuleHandle](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea) .</span><span class="sxs-lookup"><span data-stu-id="92fea-120">To get a handle, call the [GetModuleHandle](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea) function.</span></span>

</dd> <dt>

<span data-ttu-id="92fea-121">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="92fea-121">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92fea-122">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="92fea-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="92fea-123">Marcas de creación de dispositivos (consulte [**D3D10 \_ Create \_ Device \_ Flag**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag) Enumeration) que habilitan las [capas de API](d3d10-graphics-programming-guide-api-features-layers.md).</span><span class="sxs-lookup"><span data-stu-id="92fea-123">Device creation flags (see the [**D3D10\_CREATE\_DEVICE\_FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag) enumeration) that enable [API layers](d3d10-graphics-programming-guide-api-features-layers.md).</span></span> <span data-ttu-id="92fea-124">Estas marcas pueden ser OR bit a bit.</span><span class="sxs-lookup"><span data-stu-id="92fea-124">These flags can be bitwise OR'd together.</span></span>

</dd> <dt>

<span data-ttu-id="92fea-125">*ppDevice* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="92fea-125">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="92fea-126">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span><span class="sxs-lookup"><span data-stu-id="92fea-126">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span></span>

<span data-ttu-id="92fea-127">Dirección de un puntero al dispositivo creado (vea la interfaz [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) ).</span><span class="sxs-lookup"><span data-stu-id="92fea-127">Address of a pointer to the device created (see the [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) interface).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92fea-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="92fea-128">Return value</span></span>

<span data-ttu-id="92fea-129">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="92fea-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="92fea-130">Esta función devuelve uno de los siguientes [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="92fea-130">This function returns one of the following [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="92fea-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="92fea-131">Remarks</span></span>

<span data-ttu-id="92fea-132">Esta función intenta crear el mejor dispositivo para el hardware.</span><span class="sxs-lookup"><span data-stu-id="92fea-132">This function attempts to create the best device for the hardware.</span></span> <span data-ttu-id="92fea-133">En primer lugar, la función intenta crear un dispositivo 10,1.</span><span class="sxs-lookup"><span data-stu-id="92fea-133">First, the function attempts to create a 10.1 device.</span></span> <span data-ttu-id="92fea-134">Si no se puede crear un dispositivo 10,1, la función intenta crear un dispositivo 10,0.</span><span class="sxs-lookup"><span data-stu-id="92fea-134">If a 10.1 device cannot be created, the function attempts to create a 10.0 device.</span></span> <span data-ttu-id="92fea-135">Si ninguno de los dispositivos se crea correctamente, la función devuelve E \_ Fail.</span><span class="sxs-lookup"><span data-stu-id="92fea-135">If neither device is successfully created, the function returns E\_FAIL.</span></span>

<span data-ttu-id="92fea-136">Si su aplicación solo necesita crear un dispositivo 10,1 o un dispositivo 10,0, use las siguientes funciones en su lugar:</span><span class="sxs-lookup"><span data-stu-id="92fea-136">If your application needs to create only a 10.1 device, or a 10.0 device only, use the following functions instead:</span></span>

-   <span data-ttu-id="92fea-137">Use la función [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice) para crear solo un dispositivo Direct3D 10,0.</span><span class="sxs-lookup"><span data-stu-id="92fea-137">Use the [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice) function to create a Direct3D 10.0 device only.</span></span>
-   <span data-ttu-id="92fea-138">Use la función [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1) para crear solo un dispositivo Direct3D 10,1.</span><span class="sxs-lookup"><span data-stu-id="92fea-138">Use the [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1) function to create a Direct3D 10.1 device only.</span></span>
-   <span data-ttu-id="92fea-139">Use la función [**D3DX10GetFeatureLevel1**](d3dx10getfeaturelevel1.md) para obtener un puntero de interfaz [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) de un puntero de interfaz [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) .</span><span class="sxs-lookup"><span data-stu-id="92fea-139">Use the [**D3DX10GetFeatureLevel1**](d3dx10getfeaturelevel1.md) function to get an [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) interface pointer from an [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) interface pointer.</span></span>

<span data-ttu-id="92fea-140">Un dispositivo Direct3D 10,1 solo se puede crear en equipos que ejecutan Windows Vista Service Pack 1 o posterior y con hardware compatible con Direct3D 10,1 instalado.</span><span class="sxs-lookup"><span data-stu-id="92fea-140">A Direct3D 10.1 device can only be created on computers running Windows Vista Service Pack 1 or later, and with Direct3D 10.1-compatible hardware installed.</span></span> <span data-ttu-id="92fea-141">Sin embargo, es válido llamar a esta función en equipos que ejecutan cualquier versión de Windows que tenga instalado el archivo DLL D3DX10.</span><span class="sxs-lookup"><span data-stu-id="92fea-141">However, it is legal to call this function on computers running any version of Windows that has the D3DX10 DLL installed.</span></span>

## <a name="requirements"></a><span data-ttu-id="92fea-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92fea-142">Requirements</span></span>



| <span data-ttu-id="92fea-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="92fea-143">Requirement</span></span> | <span data-ttu-id="92fea-144">Value</span><span class="sxs-lookup"><span data-stu-id="92fea-144">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="92fea-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="92fea-145">Header</span></span><br/> | <dl> <span data-ttu-id="92fea-146"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="92fea-146"><dt>D3DX10Core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92fea-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="92fea-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92fea-148">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="92fea-148">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
