---
title: Propiedad DeviceById de IMsRdpDeviceCollection
description: Recupera el dispositivo con el identificador especificado.
ms.assetid: b64e83fa-5a94-4080-8efa-45cbfe5ceb88
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad DeviceById
- Propiedad DeviceById Servicios de Escritorio remoto, interfaz IMsRdpDeviceCollection
- Servicios de Escritorio remoto de la interfaz IMsRdpDeviceCollection, propiedad DeviceById
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection.DeviceById
- IMsRdpDeviceCollection.get_DeviceById
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 228e3c7cf03457ca740d4a415257008988215077
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490342"
---
# <a name="imsrdpdevicecollectiondevicebyid-property"></a><span data-ttu-id="c56a8-106">IMsRdpDeviceCollection::D propiedad eviceById</span><span class="sxs-lookup"><span data-stu-id="c56a8-106">IMsRdpDeviceCollection::DeviceById property</span></span>

<span data-ttu-id="c56a8-107">Recupera el dispositivo con el identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="c56a8-107">Retrieves the device with the specified identifier.</span></span>

<span data-ttu-id="c56a8-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c56a8-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c56a8-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c56a8-109">Syntax</span></span>


```C++
HRESULT get_DeviceById(
  [in]          BSTR devInstanceId,
  [out, retval] IMsRdpDevice **ppDevice
);
```



## <a name="property-value"></a><span data-ttu-id="c56a8-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="c56a8-110">Property value</span></span>

<span data-ttu-id="c56a8-111">Puntero a la interfaz [**IMsRdpDevice**](imsrdpdevice.md) .</span><span class="sxs-lookup"><span data-stu-id="c56a8-111">An [**IMsRdpDevice**](imsrdpdevice.md) interface pointer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c56a8-112">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="c56a8-112">Error codes</span></span>

<span data-ttu-id="c56a8-113">Si el método se ejecuta correctamente, se devuelve **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="c56a8-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="c56a8-114">Cualquier otro valor **HRESULT** indica que se produjo un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="c56a8-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="c56a8-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c56a8-115">Requirements</span></span>



| <span data-ttu-id="c56a8-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c56a8-116">Requirement</span></span> | <span data-ttu-id="c56a8-117">Value</span><span class="sxs-lookup"><span data-stu-id="c56a8-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="c56a8-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c56a8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c56a8-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c56a8-119">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="c56a8-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c56a8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c56a8-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c56a8-121">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="c56a8-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="c56a8-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="c56a8-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c56a8-123"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="c56a8-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c56a8-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c56a8-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c56a8-125"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="c56a8-126">IID</span><span class="sxs-lookup"><span data-stu-id="c56a8-126">IID</span></span><br/>                      | <span data-ttu-id="c56a8-127">IID \_ IMsRdpDeviceCollection se define como 56540617-D281-488C-8738-6a8fdf64a118</span><span class="sxs-lookup"><span data-stu-id="c56a8-127">IID\_IMsRdpDeviceCollection is defined as 56540617-d281-488c-8738-6a8fdf64a118</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c56a8-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="c56a8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c56a8-129">**IMsRdpDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="c56a8-129">**IMsRdpDeviceCollection**</span></span>](imsrdpdevicecollection.md)
</dt> </dl>

 

 





