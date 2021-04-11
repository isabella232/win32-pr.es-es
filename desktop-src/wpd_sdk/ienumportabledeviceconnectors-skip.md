---
description: Omite el número especificado de dispositivos en la secuencia de enumeración.
ms.assetid: 38b72b80-93f5-433e-977c-e3ee503daae5
title: 'IEnumPortableDeviceConnectors:: Skip (método) (Devpkey. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors.Skip
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: c00daecccd12beee8e9e741c2906e47484fa6da3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083008"
---
# <a name="ienumportabledeviceconnectorsskip-method"></a><span data-ttu-id="98c4d-103">IEnumPortableDeviceConnectors:: Skip (método)</span><span class="sxs-lookup"><span data-stu-id="98c4d-103">IEnumPortableDeviceConnectors::Skip method</span></span>

<span data-ttu-id="98c4d-104">El método **SKIP** omite el número especificado de dispositivos en la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="98c4d-104">The **Skip** method skips the specified number of devices in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="98c4d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="98c4d-105">Syntax</span></span>


```C++
HRESULT Skip(
  [in] UINT32 cConnectors
);
```



## <a name="parameters"></a><span data-ttu-id="98c4d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="98c4d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98c4d-107">*cConnectors* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="98c4d-107">*cConnectors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98c4d-108">El número de dispositivos que se van a omitir.</span><span class="sxs-lookup"><span data-stu-id="98c4d-108">The number of devices to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98c4d-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="98c4d-109">Return value</span></span>

<span data-ttu-id="98c4d-110">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="98c4d-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="98c4d-111">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="98c4d-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="98c4d-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="98c4d-112">Return code</span></span>                                                                             | <span data-ttu-id="98c4d-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="98c4d-113">Description</span></span>                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="98c4d-114"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="98c4d-114"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="98c4d-115">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="98c4d-115">The method succeeded.</span></span><br/>                                                                                                                                                          |
| <dl> <span data-ttu-id="98c4d-116"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="98c4d-116"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="98c4d-117">No se pudo omitir el número especificado de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="98c4d-117">The specified number of devices could not be skipped.</span></span> <span data-ttu-id="98c4d-118">Una posible causa: el parámetro *cConnectors* especifica más dispositivos que los que permanecen realmente en la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="98c4d-118">One possible cause: The *cConnectors* parameter specifies more devices than actually remain in the enumeration sequence.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="98c4d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98c4d-119">Requirements</span></span>



| <span data-ttu-id="98c4d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="98c4d-120">Requirement</span></span> | <span data-ttu-id="98c4d-121">Value</span><span class="sxs-lookup"><span data-stu-id="98c4d-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98c4d-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98c4d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="98c4d-123">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="98c4d-123">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="98c4d-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98c4d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="98c4d-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="98c4d-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                                   |
| <span data-ttu-id="98c4d-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="98c4d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="98c4d-127"><dt>Devpkey. h; </dt> <dt>Portabledeviceconnectapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="98c4d-127"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="98c4d-128">IDL</span><span class="sxs-lookup"><span data-stu-id="98c4d-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="98c4d-129"><dt>Portabledeviceconnectapi. idl</dt></span><span class="sxs-lookup"><span data-stu-id="98c4d-129"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="98c4d-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="98c4d-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="98c4d-131"><dt>PortableDeviceGuids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="98c4d-131"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



## <a name="see-also"></a><span data-ttu-id="98c4d-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="98c4d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98c4d-133">**IEnumPortableDeviceConnectors**</span><span class="sxs-lookup"><span data-stu-id="98c4d-133">**IEnumPortableDeviceConnectors**</span></span>](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




