---
UID: NF:directml.DMLCreateDevice1
title: Función DMLCreateDevice1
description: Crea un dispositivo DirectML para un dispositivo Direct3D 12 determinado.
helpviewer_keywords:
- DMLCreateDevice1
- DMLCreateDevice1 function
- direct3d12.dmlcreatedevice1
- directml/DMLCreateDevice1
ms.topic: reference
tech.root: directml
ms.date: 11/04/2020
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: DirectML.lib
req.dll: DirectML.dll
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DMLCreateDevice1
- directml/DMLCreateDevice1
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- DirectML.dll
api_name:
- DMLCreateDevice1
ms.openlocfilehash: f722b12208bd808f01e177feb907f94c33541496
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803769"
---
# <a name="dmlcreatedevice1-function-directmlh"></a><span data-ttu-id="97c2b-103">Función DMLCreateDevice1 (directml.h)</span><span class="sxs-lookup"><span data-stu-id="97c2b-103">DMLCreateDevice1 function (directml.h)</span></span>

<span data-ttu-id="97c2b-104">Crea un dispositivo DirectML para un dispositivo Direct3D 12 determinado.</span><span class="sxs-lookup"><span data-stu-id="97c2b-104">Creates a DirectML device for a given Direct3D 12 device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="97c2b-105">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="97c2b-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="97c2b-106">Consulte también Historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="97c2b-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="97c2b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="97c2b-107">Syntax</span></span>

```cpp
HRESULT DMLCreateDevice1(
  ID3D12Device            *d3d12Device,
  DML_CREATE_DEVICE_FLAGS flags,
  DML_FEATURE_LEVEL       minimumFeatureLevel,
  REFIID                  riid,
  void                    **ppv
);
```

## <a name="parameters"></a><span data-ttu-id="97c2b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="97c2b-108">Parameters</span></span>

`d3d12Device`

<span data-ttu-id="97c2b-109">Tipo: <b> <a href="/windows/win32/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>\*</b></span><span class="sxs-lookup"><span data-stu-id="97c2b-109">Type: <b><a href="/windows/win32/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>\*</b></span></span>

<span data-ttu-id="97c2b-110">Puntero a un [id3D12Dispositivo](/windows/win32/api/d3d12/nn-d3d12-id3d12device) que representa el dispositivo Direct3D 12 sobre el que se crea el dispositivo DirectML.</span><span class="sxs-lookup"><span data-stu-id="97c2b-110">A pointer to an [ID3D12Device](/windows/win32/api/d3d12/nn-d3d12-id3d12device) representing the Direct3D 12 device to create the DirectML device over.</span></span> <span data-ttu-id="97c2b-111">DirectML admite cualquier nivel de característica D3D y dispositivos Direct3D 12 creados en cualquier adaptador, incluido WARP.</span><span class="sxs-lookup"><span data-stu-id="97c2b-111">DirectML supports any D3D feature level, and Direct3D 12 devices created on any adapter, including WARP.</span></span> <span data-ttu-id="97c2b-112">Sin embargo, no todas las características de DirectML pueden estar disponibles en función de las funcionalidades del dispositivo Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="97c2b-112">However, not all features in DirectML may be available depending on the capabilities of the Direct3D 12 device.</span></span> <span data-ttu-id="97c2b-113">Consulte [IDMLDevice::CheckFeatureSupport para](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport) obtener más información.</span><span class="sxs-lookup"><span data-stu-id="97c2b-113">See [IDMLDevice::CheckFeatureSupport](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport) for more info.</span></span>

<span data-ttu-id="97c2b-114">Si la llamada a **DMLCreateDevice1** es correcta, el dispositivo DirectML mantiene una referencia fuerte al dispositivo Direct3D 12 proporcionado.</span><span class="sxs-lookup"><span data-stu-id="97c2b-114">If the call to **DMLCreateDevice1** is successful, then the DirectML device maintains a strong reference to the supplied Direct3D 12 device.</span></span>

`flags`

<span data-ttu-id="97c2b-115">Tipo: <b>DML_CREATE_DEVICE_FLAGS</b></span><span class="sxs-lookup"><span data-stu-id="97c2b-115">Type: <b>DML_CREATE_DEVICE_FLAGS</b></span></span>

<span data-ttu-id="97c2b-116">Valor [DML_CREATE_DEVICE_FLAGS](/windows/win32/api/directml/ne-directml-dml_create_device_flags) que especifica opciones de creación de dispositivos adicionales.</span><span class="sxs-lookup"><span data-stu-id="97c2b-116">A [DML_CREATE_DEVICE_FLAGS](/windows/win32/api/directml/ne-directml-dml_create_device_flags) value specifying additional device creation options.</span></span>

`minimumFeatureLevel`

<span data-ttu-id="97c2b-117">Tipo: <b>DML_FEATURE_LEVEL</b></span><span class="sxs-lookup"><span data-stu-id="97c2b-117">Type: <b>DML_FEATURE_LEVEL</b></span></span>

<span data-ttu-id="97c2b-118">Valor [DML_FEATURE_LEVEL](/windows/win32/api/directml/ne-directml-dml_feature_level) especifica la compatibilidad mínima de nivel de característica necesaria.</span><span class="sxs-lookup"><span data-stu-id="97c2b-118">A [DML_FEATURE_LEVEL](/windows/win32/api/directml/ne-directml-dml_feature_level) value specifying the minimum feature level support required.</span></span>

<span data-ttu-id="97c2b-119">Este parámetro puede ser útil para los autores de llamadas que requieren una versión específica de DirectML, pero que pueden encontrarse llamando a una versión anterior de DirectML.</span><span class="sxs-lookup"><span data-stu-id="97c2b-119">This parameter can be useful for callers that require a specific version of DirectML, but who may find themselves calling into an older version of DirectML.</span></span> <span data-ttu-id="97c2b-120">Esto puede ocurrir, por ejemplo, cuando el usuario ejecuta la aplicación en una versión anterior de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="97c2b-120">This can happen, for example, when the user runs your application on an older version of Windows 10.</span></span>

<span data-ttu-id="97c2b-121">Las aplicaciones que dependen explícitamente de la funcionalidad introducida en un nivel de característica determinado pueden especificarla como *minimumFeatureLevel*.</span><span class="sxs-lookup"><span data-stu-id="97c2b-121">Applications that explicitly depend on functionality introduced in a particular feature level can specify it as a *minimumFeatureLevel*.</span></span> <span data-ttu-id="97c2b-122">Esto garantizará que **DMLCreateDevice1** no se realizará  correctamente a menos que la implementación subyacente sea al menos tan capaz como este nivel mínimo de características solicitado.</span><span class="sxs-lookup"><span data-stu-id="97c2b-122">This will guarantee that **DMLCreateDevice1** won't succeed unless the underlying implementation is *at least* as capable as this requested minimum feature level.</span></span>

<span data-ttu-id="97c2b-123">Tenga en cuenta que,  como este parámetro especifica un nivel mínimo de características, el dispositivo DirectML subyacente puede admitir de hecho un nivel de característica superior al mínimo solicitado.</span><span class="sxs-lookup"><span data-stu-id="97c2b-123">Note that as this parameter specifies a *minimum* feature level, the underlying DirectML device may in fact support a higher feature level than the requested minimum.</span></span> <span data-ttu-id="97c2b-124">Una vez que la creación del dispositivo se realiza correctamente, puede consultar todos los niveles de características compatibles con este dispositivo mediante [IDMLDevice::CheckFeatureSupport](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport).</span><span class="sxs-lookup"><span data-stu-id="97c2b-124">Once device creation succeeds, you can query all of the feature levels supported by this device using [IDMLDevice::CheckFeatureSupport](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport).</span></span>

`riid`

<span data-ttu-id="97c2b-125">Tipo: <b>REFIID</b></span><span class="sxs-lookup"><span data-stu-id="97c2b-125">Type: <b>REFIID</b></span></span>

<span data-ttu-id="97c2b-126">Referencia al identificador único global (GUID) de la interfaz que desea que se devuelva en el <i>dispositivo</i>.</span><span class="sxs-lookup"><span data-stu-id="97c2b-126">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in <i>device</i>.</span></span> <span data-ttu-id="97c2b-127">Se espera que sea el GUID de [IDMLDevice.](/windows/win32/api/directml/nn-directml-idmldevice)</span><span class="sxs-lookup"><span data-stu-id="97c2b-127">This is expected to be the GUID of [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice).</span></span>

`ppv`

<span data-ttu-id="97c2b-128">Tipo: \_ COM \_ Outptr opt \_ \_ <b>void\*\*</b></span><span class="sxs-lookup"><span data-stu-id="97c2b-128">Type: \_COM\_Outptr\_opt\_ <b>void\*\*</b></span></span>

<span data-ttu-id="97c2b-129">Puntero a un bloque de memoria que recibe un puntero al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="97c2b-129">A pointer to a memory block that receives a pointer to the device.</span></span> <span data-ttu-id="97c2b-130">Esta es la dirección de un puntero a [un IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice), que representa el dispositivo DirectML creado.</span><span class="sxs-lookup"><span data-stu-id="97c2b-130">This is the address of a pointer to an [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice), representing  the DirectML device created.</span></span>


## <a name="return-value"></a><span data-ttu-id="97c2b-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="97c2b-131">Return value</span></span>

<span data-ttu-id="97c2b-132">Tipo: [ **HRESULT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="97c2b-132">Type: [**HRESULT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="97c2b-133">Si la función se realiza correctamente, devuelve <b>S_OK</b>.</span><span class="sxs-lookup"><span data-stu-id="97c2b-133">If the function succeeds, it returns <b>S_OK</b>.</span></span> <span data-ttu-id="97c2b-134">De lo contrario, devuelve un código de error [HRESULT.](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="97c2b-134">Otherwise, it returns an [HRESULT](/windows/desktop/winprog/windows-data-types) error code.</span></span>

<span data-ttu-id="97c2b-135">Si esta versión de DirectML no admite el *valor minimumFeatureLevel* solicitado, esta función devolverá **DXGI_ERROR_UNSUPPORTED**.</span><span class="sxs-lookup"><span data-stu-id="97c2b-135">If this version of DirectML doesn't support the *minimumFeatureLevel* requested, then this function will return **DXGI_ERROR_UNSUPPORTED**.</span></span>

<span data-ttu-id="97c2b-136">La característica Herramientas de gráficos a petición (FOD) debe estar instalada para poder usar las capas de depuración de DirectML.</span><span class="sxs-lookup"><span data-stu-id="97c2b-136">The Graphics Tools Feature on Demand (FOD) must be installed in order to use the DirectML debug layers.</span></span> <span data-ttu-id="97c2b-137">Si la [DML_CREATE_DEVICE_FLAG_DEBUG](/windows/win32/api/directml/ne-directml-dml_create_device_flags) se especifica en  las marcas y las capas de depuración no están instaladas, **DMLCreateDevice1** **devuelve DXGI_ERROR_SDK_COMPONENT_MISSING**.</span><span class="sxs-lookup"><span data-stu-id="97c2b-137">If the [DML_CREATE_DEVICE_FLAG_DEBUG](/windows/win32/api/directml/ne-directml-dml_create_device_flags) flag is specified in *flags* and the debug layers are not installed, then **DMLCreateDevice1** returns **DXGI_ERROR_SDK_COMPONENT_MISSING**.</span></span>

## <a name="remarks"></a><span data-ttu-id="97c2b-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="97c2b-138">Remarks</span></span>

<span data-ttu-id="97c2b-139">Se introdujo una versión más reciente de esta función, [DMLCreateDevice1,]()en la versión 1.1.0 de DirectML.</span><span class="sxs-lookup"><span data-stu-id="97c2b-139">A newer version of this function, [DMLCreateDevice1](), was introduced in DirectML version 1.1.0.</span></span> <span data-ttu-id="97c2b-140">**DMLCreateDevice1 equivale** a llamar a **DMLCreateDevice1** y proporcionar *un minimumFeatureLevel* [de DML_FEATURE_LEVEL_1_0](/windows/win32/api/directml/ne-directml-dml_feature_level).</span><span class="sxs-lookup"><span data-stu-id="97c2b-140">**DMLCreateDevice1** is equivalent to calling **DMLCreateDevice1** and supplying a *minimumFeatureLevel* of [DML_FEATURE_LEVEL_1_0](/windows/win32/api/directml/ne-directml-dml_feature_level).</span></span>

## <a name="availability"></a><span data-ttu-id="97c2b-141">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="97c2b-141">Availability</span></span>

<span data-ttu-id="97c2b-142">Esta API se introdujo en la versión de `1.1.0` DirectML.</span><span class="sxs-lookup"><span data-stu-id="97c2b-142">This API was introduced in DirectML version `1.1.0`.</span></span>

## <a name="requirements"></a><span data-ttu-id="97c2b-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97c2b-143">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="97c2b-144">**Plataforma de destino**</span><span class="sxs-lookup"><span data-stu-id="97c2b-144">**Target Platform**</span></span> | <span data-ttu-id="97c2b-145">Windows</span><span class="sxs-lookup"><span data-stu-id="97c2b-145">Windows</span></span> |
| <span data-ttu-id="97c2b-146">**Header**</span><span class="sxs-lookup"><span data-stu-id="97c2b-146">**Header**</span></span> | <span data-ttu-id="97c2b-147">directml.h</span><span class="sxs-lookup"><span data-stu-id="97c2b-147">directml.h</span></span> |
| <span data-ttu-id="97c2b-148">**Library**</span><span class="sxs-lookup"><span data-stu-id="97c2b-148">**Library**</span></span> | <span data-ttu-id="97c2b-149">DirectML.lib</span><span class="sxs-lookup"><span data-stu-id="97c2b-149">DirectML.lib</span></span> |
| <span data-ttu-id="97c2b-150">**Dll**</span><span class="sxs-lookup"><span data-stu-id="97c2b-150">**DLL**</span></span> | <span data-ttu-id="97c2b-151">DirectML.dll</span><span class="sxs-lookup"><span data-stu-id="97c2b-151">DirectML.dll</span></span> |

## <a name="see-also"></a><span data-ttu-id="97c2b-152">Consulta también</span><span class="sxs-lookup"><span data-stu-id="97c2b-152">See also</span></span>

* [<span data-ttu-id="97c2b-153">DML_FEATURE_LEVEL enumeración</span><span class="sxs-lookup"><span data-stu-id="97c2b-153">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* [<span data-ttu-id="97c2b-154">Historial de versiones de DirectML</span><span class="sxs-lookup"><span data-stu-id="97c2b-154">DirectML version history</span></span>](../dml-version-history.md)
* [<span data-ttu-id="97c2b-155">Historial de nivel de característica de DirectML</span><span class="sxs-lookup"><span data-stu-id="97c2b-155">DirectML feature level history</span></span>](/windows/win32/direct3d12/dml-feature_level-history)    
* [<span data-ttu-id="97c2b-156">Uso de la capa de depuración de DirectML</span><span class="sxs-lookup"><span data-stu-id="97c2b-156">Using the DirectML debug layer</span></span>](../dml-debug-layer.md)