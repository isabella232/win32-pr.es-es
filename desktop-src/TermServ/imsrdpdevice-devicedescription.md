---
title: Propiedad DeviceDescription de IMsRdpDevice
description: Recupera la descripción del dispositivo que se va a mostrar al usuario si el nombre para mostrar no está disponible.
ms.assetid: 969f96c6-5655-4cac-9e91-059114dc3815
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad DeviceDescription
- Propiedad DeviceDescription Servicios de Escritorio remoto, interfaz IMsRdpDevice
- Servicios de Escritorio remoto de la interfaz IMsRdpDevice, propiedad DeviceDescription
topic_type:
- apiref
api_name:
- IMsRdpDevice.DeviceDescription
- IMsRdpDevice.get_DeviceDescription
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e352acef945c09c6be592174dd86a46cd8689aca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150597"
---
# <a name="imsrdpdevicedevicedescription-property"></a><span data-ttu-id="f13a8-106">IMsRdpDevice::D propiedad eviceDescription</span><span class="sxs-lookup"><span data-stu-id="f13a8-106">IMsRdpDevice::DeviceDescription property</span></span>

<span data-ttu-id="f13a8-107">Recupera la descripción del dispositivo que se va a mostrar al usuario si el nombre para mostrar no está disponible.</span><span class="sxs-lookup"><span data-stu-id="f13a8-107">Retrieves the device description to be displayed to the user if the display name is not available.</span></span>

<span data-ttu-id="f13a8-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f13a8-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f13a8-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f13a8-109">Syntax</span></span>


```C++
HRESULT get_DeviceDescription(
  [out] BSTR *pDeviceDescription
);
```



## <a name="property-value"></a><span data-ttu-id="f13a8-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="f13a8-110">Property value</span></span>

<span data-ttu-id="f13a8-111">Descripción del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f13a8-111">The device description.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f13a8-112">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="f13a8-112">Error codes</span></span>

<span data-ttu-id="f13a8-113">Si el método se ejecuta correctamente, se devuelve **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="f13a8-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="f13a8-114">Cualquier otro valor **HRESULT** indica que se produjo un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="f13a8-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="f13a8-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f13a8-115">Requirements</span></span>



| <span data-ttu-id="f13a8-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f13a8-116">Requirement</span></span> | <span data-ttu-id="f13a8-117">Value</span><span class="sxs-lookup"><span data-stu-id="f13a8-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f13a8-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f13a8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f13a8-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f13a8-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f13a8-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f13a8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f13a8-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f13a8-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f13a8-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f13a8-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="f13a8-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f13a8-123"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f13a8-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f13a8-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f13a8-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f13a8-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f13a8-126">IID</span><span class="sxs-lookup"><span data-stu-id="f13a8-126">IID</span></span><br/>                      | <span data-ttu-id="f13a8-127">IID \_ IMsRdpDevice se define como 60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span><span class="sxs-lookup"><span data-stu-id="f13a8-127">IID\_IMsRdpDevice is defined as 60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="f13a8-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="f13a8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f13a8-129">**IMsRdpDevice**</span><span class="sxs-lookup"><span data-stu-id="f13a8-129">**IMsRdpDevice**</span></span>](imsrdpdevice.md)
</dt> </dl>

 

 





