---
title: IMsRdpDeviceCollection RescanDevices, método
description: Actualiza la lista de objetos de la colección. | IMsRdpDeviceCollection RescanDevices, método
ms.assetid: 2e2a959d-0a1d-4aca-9daf-3c24fb9b3b08
ms.tgt_platform: multiple
keywords:
- Método RescanDevices Servicios de Escritorio remoto
- Método RescanDevices Servicios de Escritorio remoto, interfaz IMsRdpDeviceCollection
- Interfaz IMsRdpDeviceCollection Servicios de Escritorio remoto, método RescanDevices
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection.RescanDevices
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 773231ffd89a0998f6073f844a3f974920625987
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105678735"
---
# <a name="imsrdpdevicecollectionrescandevices-method"></a><span data-ttu-id="ffdfa-107">IMsRdpDeviceCollection:: RescanDevices (método)</span><span class="sxs-lookup"><span data-stu-id="ffdfa-107">IMsRdpDeviceCollection::RescanDevices method</span></span>

<span data-ttu-id="ffdfa-108">Actualiza la lista de objetos de la colección.</span><span class="sxs-lookup"><span data-stu-id="ffdfa-108">Refreshes the list of objects in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffdfa-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ffdfa-109">Syntax</span></span>


```C++
HRESULT RescanDevices(
  [in] VARIANT_BOOL vboolDynRedir
);
```



## <a name="parameters"></a><span data-ttu-id="ffdfa-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ffdfa-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffdfa-111">*vboolDynRedir* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ffdfa-111">*vboolDynRedir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffdfa-112">El estado de redirección predeterminada que se aplicará a los dispositivos o unidades recién detectados.</span><span class="sxs-lookup"><span data-stu-id="ffdfa-112">The default redirection state that will be applied to any newly discovered devices or drives.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffdfa-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ffdfa-113">Return value</span></span>

<span data-ttu-id="ffdfa-114">Si el método se ejecuta correctamente, se devuelve **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="ffdfa-114">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="ffdfa-115">Cualquier otro valor **HRESULT** indica que se produjo un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="ffdfa-115">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffdfa-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ffdfa-116">Requirements</span></span>



| <span data-ttu-id="ffdfa-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ffdfa-117">Requirement</span></span> | <span data-ttu-id="ffdfa-118">Value</span><span class="sxs-lookup"><span data-stu-id="ffdfa-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffdfa-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ffdfa-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ffdfa-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ffdfa-120">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="ffdfa-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ffdfa-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ffdfa-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ffdfa-122">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="ffdfa-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ffdfa-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="ffdfa-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ffdfa-124"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="ffdfa-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ffdfa-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ffdfa-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ffdfa-126"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="ffdfa-127">IID</span><span class="sxs-lookup"><span data-stu-id="ffdfa-127">IID</span></span><br/>                      | <span data-ttu-id="ffdfa-128">IID \_ IMsRdpDeviceCollection se define como 56540617-D281-488C-8738-6a8fdf64a118</span><span class="sxs-lookup"><span data-stu-id="ffdfa-128">IID\_IMsRdpDeviceCollection is defined as 56540617-d281-488c-8738-6a8fdf64a118</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ffdfa-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="ffdfa-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffdfa-130">**IMsRdpDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="ffdfa-130">**IMsRdpDeviceCollection**</span></span>](imsrdpdevicecollection.md)
</dt> </dl>

 

 





