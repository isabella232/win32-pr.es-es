---
title: Propiedad DeviceCount de IMsRdpDeviceCollection
description: Recupera el recuento de objetos de la colección. | Propiedad DeviceCount de IMsRdpDeviceCollection
ms.assetid: dc44f3b8-52c4-4e5f-a633-ea7555fd01dd
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad DeviceCount
- Propiedad DeviceCount Servicios de Escritorio remoto, interfaz IMsRdpDeviceCollection
- Servicios de Escritorio remoto de la interfaz IMsRdpDeviceCollection, propiedad DeviceCount
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection.DeviceCount
- IMsRdpDeviceCollection.get_DeviceCount
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67a389cd89699eb383b9f235858f0cf4a052606a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689783"
---
# <a name="imsrdpdevicecollectiondevicecount-property"></a><span data-ttu-id="59fbc-107">IMsRdpDeviceCollection::D propiedad eviceCount</span><span class="sxs-lookup"><span data-stu-id="59fbc-107">IMsRdpDeviceCollection::DeviceCount property</span></span>

<span data-ttu-id="59fbc-108">Recupera el recuento de objetos de la colección.</span><span class="sxs-lookup"><span data-stu-id="59fbc-108">Retrieves the count of objects in the collection.</span></span>

<span data-ttu-id="59fbc-109">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="59fbc-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="59fbc-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="59fbc-110">Syntax</span></span>


```C++
HRESULT get_DeviceCount(
  [out] ULONG *pDeviceCount
);
```



## <a name="property-value"></a><span data-ttu-id="59fbc-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="59fbc-111">Property value</span></span>

<span data-ttu-id="59fbc-112">Recuento de objetos.</span><span class="sxs-lookup"><span data-stu-id="59fbc-112">The object count.</span></span>

## <a name="error-codes"></a><span data-ttu-id="59fbc-113">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="59fbc-113">Error codes</span></span>

<span data-ttu-id="59fbc-114">Si el método se ejecuta correctamente, se devuelve **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="59fbc-114">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="59fbc-115">Cualquier otro valor **HRESULT** indica que se produjo un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="59fbc-115">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="59fbc-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59fbc-116">Requirements</span></span>



| <span data-ttu-id="59fbc-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="59fbc-117">Requirement</span></span> | <span data-ttu-id="59fbc-118">Value</span><span class="sxs-lookup"><span data-stu-id="59fbc-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="59fbc-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="59fbc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="59fbc-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="59fbc-120">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="59fbc-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="59fbc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="59fbc-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="59fbc-122">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="59fbc-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="59fbc-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="59fbc-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59fbc-124"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="59fbc-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="59fbc-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59fbc-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59fbc-126"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="59fbc-127">IID</span><span class="sxs-lookup"><span data-stu-id="59fbc-127">IID</span></span><br/>                      | <span data-ttu-id="59fbc-128">IID \_ IMsRdpDeviceCollection se define como 56540617-D281-488C-8738-6a8fdf64a118</span><span class="sxs-lookup"><span data-stu-id="59fbc-128">IID\_IMsRdpDeviceCollection is defined as 56540617-d281-488c-8738-6a8fdf64a118</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="59fbc-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="59fbc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59fbc-130">**IMsRdpDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="59fbc-130">**IMsRdpDeviceCollection**</span></span>](imsrdpdevicecollection.md)
</dt> </dl>

 

 





