---
title: DeviceController. CachedDevices, método
description: Recupera una colección de punteros de interfaz IBasicDevice que representa la vista almacenada en memoria caché de todos los dispositivos DLNA detectables. | DeviceController. CachedDevices, método
ms.assetid: 89CFA4BB-EDA8-461A-A3A0-A84CBDA99EA4
keywords:
- Método CachedDevices API de streaming de multimedia
- Método CachedDevices API de streaming de multimedia, interfaz DeviceController
- Interfaz DeviceController API de streaming de multimedia, método CachedDevices
topic_type:
- apiref
api_name:
- DeviceController.CachedDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c0bb39e03a9788e0c444f682b61d39fc1c65781b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105717475"
---
# <a name="devicecontrollercacheddevices-method"></a><span data-ttu-id="2827a-107">DeviceController. CachedDevices, método</span><span class="sxs-lookup"><span data-stu-id="2827a-107">DeviceController.CachedDevices method</span></span>

<span data-ttu-id="2827a-108">Recupera una colección de punteros de interfaz [**IBasicDevice**](ibasicdevice.md) que representa la vista almacenada en memoria caché de todos los dispositivos DLNA detectables.</span><span class="sxs-lookup"><span data-stu-id="2827a-108">Retrieves a collection of [**IBasicDevice**](ibasicdevice.md) interface pointers that represents the cached view of all discoverable DLNA devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="2827a-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2827a-109">Syntax</span></span>


```C++
HRESULT CachedDevices(
  [out] IVector< IBasicDevice > **value
);
```



## <a name="parameters"></a><span data-ttu-id="2827a-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2827a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2827a-111">*valor* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2827a-111">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2827a-112">Recibe una colección enumerable de punteros de interfaz [**IBasicDevice**](ibasicdevice.md) .</span><span class="sxs-lookup"><span data-stu-id="2827a-112">Receives an enumerable collection of [**IBasicDevice**](ibasicdevice.md) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2827a-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2827a-113">Return value</span></span>

<span data-ttu-id="2827a-114">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="2827a-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="2827a-115">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="2827a-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="2827a-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="2827a-116">Return code</span></span>                                                                          | <span data-ttu-id="2827a-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="2827a-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="2827a-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="2827a-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="2827a-119">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="2827a-119">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="2827a-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="2827a-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="2827a-121">[**DeviceController**](/previous-versions/windows/desktop/legacy/hh828842(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2827a-121">[**DeviceController**](/previous-versions/windows/desktop/legacy/hh828842(v=vs.85))</span></span>
</dt> </dl>

 

