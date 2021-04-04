---
title: IBasicDevice CanWakeDevices, método
description: Recupera un valor que indica si el dispositivo se puede reactivar.
ms.assetid: AAD0597C-AD33-40EE-A5DA-27AC66375D38
keywords:
- Método CanWakeDevices API de streaming de multimedia
- Método CanWakeDevices API de streaming de multimedia, interfaz IBasicDevice
- Interfaz IBasicDevice API de streaming de multimedia, método CanWakeDevices
topic_type:
- apiref
api_name:
- IBasicDevice.CanWakeDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 08a893ac880a426f604f2dc1c73173585e507cc0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076816"
---
# <a name="ibasicdevicecanwakedevices-method"></a><span data-ttu-id="bed17-106">IBasicDevice:: CanWakeDevices (método)</span><span class="sxs-lookup"><span data-stu-id="bed17-106">IBasicDevice::CanWakeDevices method</span></span>

<span data-ttu-id="bed17-107">Recupera un valor que indica si el dispositivo se puede reactivar.</span><span class="sxs-lookup"><span data-stu-id="bed17-107">Retrieves a value that indicates if the device can wake.</span></span>

## <a name="syntax"></a><span data-ttu-id="bed17-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bed17-108">Syntax</span></span>


```C++
HRESULT CanWakeDevices(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="bed17-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bed17-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bed17-110">*valor* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="bed17-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bed17-111">Recibe un puntero a un valor booleano que es **true** si el dispositivo se puede reactivar.</span><span class="sxs-lookup"><span data-stu-id="bed17-111">Receives a pointer to a boolean value that is **True** if the device can wake.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bed17-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bed17-112">Return value</span></span>

<span data-ttu-id="bed17-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="bed17-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="bed17-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="bed17-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="bed17-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="bed17-115">Return code</span></span>                                                                          | <span data-ttu-id="bed17-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="bed17-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="bed17-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="bed17-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="bed17-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="bed17-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="bed17-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="bed17-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bed17-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="bed17-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





