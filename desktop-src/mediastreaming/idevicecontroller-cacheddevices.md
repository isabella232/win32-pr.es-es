---
title: IDeviceController CachedDevices, método
description: Recupera una colección de punteros de interfaz IBasicDevice que representa la vista almacenada en memoria caché de todos los dispositivos DLNA detectables. | IDeviceController CachedDevices, método
ms.assetid: 94C2A7FF-5AF8-4F13-BBA5-54ED78C3BBF6
keywords:
- Método CachedDevices API de streaming de multimedia
- Método CachedDevices API de streaming de multimedia, interfaz IDeviceController
- Interfaz IDeviceController API de streaming de multimedia, método CachedDevices
topic_type:
- apiref
api_name:
- IDeviceController.CachedDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 69be1faea277fa8999ae5ddf3658aaa61a1116b9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003734"
---
# <a name="idevicecontrollercacheddevices-method"></a><span data-ttu-id="00651-107">IDeviceController:: CachedDevices (método)</span><span class="sxs-lookup"><span data-stu-id="00651-107">IDeviceController::CachedDevices method</span></span>

<span data-ttu-id="00651-108">Recupera una colección de punteros de interfaz [**IBasicDevice**](ibasicdevice.md) que representa la vista almacenada en memoria caché de todos los dispositivos DLNA detectables.</span><span class="sxs-lookup"><span data-stu-id="00651-108">Retrieves a collection of [**IBasicDevice**](ibasicdevice.md) interface pointers that represents the cached view of all discoverable DLNA devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="00651-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="00651-109">Syntax</span></span>


```C++
HRESULT CachedDevices(
  [out] IVector< IBasicDevice > **value
);
```



## <a name="parameters"></a><span data-ttu-id="00651-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="00651-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00651-111">*valor* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="00651-111">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="00651-112">Recibe una colección enumerable de punteros de interfaz [**IBasicDevice**](ibasicdevice.md) .</span><span class="sxs-lookup"><span data-stu-id="00651-112">Receives an enumerable collection of [**IBasicDevice**](ibasicdevice.md) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00651-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="00651-113">Return value</span></span>

<span data-ttu-id="00651-114">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="00651-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="00651-115">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="00651-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="00651-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="00651-116">Return code</span></span>                                                                          | <span data-ttu-id="00651-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="00651-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="00651-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="00651-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="00651-119">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="00651-119">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="00651-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="00651-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00651-121">**IDeviceController**</span><span class="sxs-lookup"><span data-stu-id="00651-121">**IDeviceController**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-idevicecontroller)
</dt> </dl>

 

