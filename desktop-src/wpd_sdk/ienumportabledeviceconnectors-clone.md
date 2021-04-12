---
description: Crea una copia de la interfaz IEnumPortableDeviceConnectors actual.
ms.assetid: 64274cb0-1f57-481d-914f-41238cbe2f1b
title: 'IEnumPortableDeviceConnectors:: Clone (método) (Devpkey. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors.Clone
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 0e5273f1c400732c94c7c63918787f5e130a854d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361312"
---
# <a name="ienumportabledeviceconnectorsclone-method"></a><span data-ttu-id="5de37-103">IEnumPortableDeviceConnectors:: Clone (método)</span><span class="sxs-lookup"><span data-stu-id="5de37-103">IEnumPortableDeviceConnectors::Clone method</span></span>

<span data-ttu-id="5de37-104">El método **Clone** crea una copia de la interfaz [**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md) actual.</span><span class="sxs-lookup"><span data-stu-id="5de37-104">The **Clone** method creates a copy of the current [**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="5de37-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5de37-105">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumPortableDeviceConnectors **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="5de37-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5de37-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5de37-107">*ppEnum* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5de37-107">*ppEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5de37-108">Dirección de un puntero a una interfaz [**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md) .</span><span class="sxs-lookup"><span data-stu-id="5de37-108">The address of a pointer to an [**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md) interface.</span></span> <span data-ttu-id="5de37-109">La aplicación que realiza la llamada debe liberar esta interfaz cuando se hace con ella.</span><span class="sxs-lookup"><span data-stu-id="5de37-109">The calling application must release this interface when it is done with it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5de37-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5de37-110">Return value</span></span>

<span data-ttu-id="5de37-111">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="5de37-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="5de37-112">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="5de37-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="5de37-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="5de37-113">Return code</span></span>                                                                          | <span data-ttu-id="5de37-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="5de37-114">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="5de37-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="5de37-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="5de37-116">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="5de37-116">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5de37-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5de37-117">Requirements</span></span>



| <span data-ttu-id="5de37-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5de37-118">Requirement</span></span> | <span data-ttu-id="5de37-119">Value</span><span class="sxs-lookup"><span data-stu-id="5de37-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5de37-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5de37-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5de37-121">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="5de37-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="5de37-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5de37-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5de37-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5de37-123">None supported</span></span><br/>                                                                                                                                              |
| <span data-ttu-id="5de37-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5de37-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5de37-125"><dt>Devpkey. h; </dt> <dt>Portabledeviceconnectapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5de37-125"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="5de37-126">IDL</span><span class="sxs-lookup"><span data-stu-id="5de37-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5de37-127"><dt>Portabledeviceconnectapi. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5de37-127"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="5de37-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5de37-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="5de37-129"><dt>PortableDeviceGuids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5de37-129"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



## <a name="see-also"></a><span data-ttu-id="5de37-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="5de37-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5de37-131">**IEnumPortableDeviceConnectors**</span><span class="sxs-lookup"><span data-stu-id="5de37-131">**IEnumPortableDeviceConnectors**</span></span>](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




