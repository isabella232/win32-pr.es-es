---
title: Propiedad DeviceInstanceId de IMsRdpDevice
description: Recupera el identificador de instancia del dispositivo.
ms.assetid: 54bdda17-39da-4821-9ac3-2ce80f5015f4
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad DeviceInstanceId
- Propiedad DeviceInstanceId Servicios de Escritorio remoto, interfaz IMsRdpDevice
- Servicios de Escritorio remoto de la interfaz IMsRdpDevice, propiedad DeviceInstanceId
topic_type:
- apiref
api_name:
- IMsRdpDevice.DeviceInstanceId
- IMsRdpDevice.get_DeviceInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86a159911e4294e2207ad4ae989d4ef9e390384c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997147"
---
# <a name="imsrdpdevicedeviceinstanceid-property"></a><span data-ttu-id="2081d-106">IMsRdpDevice::D propiedad eviceInstanceId</span><span class="sxs-lookup"><span data-stu-id="2081d-106">IMsRdpDevice::DeviceInstanceId property</span></span>

<span data-ttu-id="2081d-107">Recupera el identificador de instancia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2081d-107">Retrieves the device instance identifier of the device.</span></span>

<span data-ttu-id="2081d-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2081d-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2081d-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2081d-109">Syntax</span></span>


```C++
HRESULT get_DeviceInstanceId(
  [out] BSTR *pDevInstanceId
);
```



## <a name="property-value"></a><span data-ttu-id="2081d-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="2081d-110">Property value</span></span>

<span data-ttu-id="2081d-111">Identificador de instancia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2081d-111">The device instance identifier.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2081d-112">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="2081d-112">Error codes</span></span>

<span data-ttu-id="2081d-113">Si el método se ejecuta correctamente, se devuelve **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="2081d-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="2081d-114">Cualquier otro valor **HRESULT** indica que se produjo un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="2081d-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="2081d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2081d-115">Requirements</span></span>



| <span data-ttu-id="2081d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2081d-116">Requirement</span></span> | <span data-ttu-id="2081d-117">Value</span><span class="sxs-lookup"><span data-stu-id="2081d-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2081d-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2081d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2081d-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2081d-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="2081d-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2081d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2081d-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2081d-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="2081d-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="2081d-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="2081d-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2081d-123"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="2081d-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2081d-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2081d-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2081d-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="2081d-126">IID</span><span class="sxs-lookup"><span data-stu-id="2081d-126">IID</span></span><br/>                      | <span data-ttu-id="2081d-127">IID \_ IMsRdpDevice se define como 60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span><span class="sxs-lookup"><span data-stu-id="2081d-127">IID\_IMsRdpDevice is defined as 60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="2081d-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="2081d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2081d-129">**IMsRdpDevice**</span><span class="sxs-lookup"><span data-stu-id="2081d-129">**IMsRdpDevice**</span></span>](imsrdpdevice.md)
</dt> </dl>

 

 





