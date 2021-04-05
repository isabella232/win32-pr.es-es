---
title: IBasicDevice DiscoveredOnCurrentNetwork, método
description: Recupera un valor que indica si el dispositivo está en la red actual.
ms.assetid: E64D4E49-9790-4647-9A01-2C28C407F238
keywords:
- Método DiscoveredOnCurrentNetwork API de streaming de multimedia
- Método DiscoveredOnCurrentNetwork API de streaming de multimedia, interfaz IBasicDevice
- Interfaz IBasicDevice API de streaming de multimedia, método DiscoveredOnCurrentNetwork
topic_type:
- apiref
api_name:
- IBasicDevice.DiscoveredOnCurrentNetwork
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e79a012413b3b3d78a9c4617f01ca6cc01cf7e1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419440"
---
# <a name="ibasicdevicediscoveredoncurrentnetwork-method"></a><span data-ttu-id="da73a-106">IBasicDevice::D método iscoveredOnCurrentNetwork</span><span class="sxs-lookup"><span data-stu-id="da73a-106">IBasicDevice::DiscoveredOnCurrentNetwork method</span></span>

<span data-ttu-id="da73a-107">Recupera un valor que indica si el dispositivo está en la red actual.</span><span class="sxs-lookup"><span data-stu-id="da73a-107">Retrieves a value that indicates if the device is on the current network.</span></span>

## <a name="syntax"></a><span data-ttu-id="da73a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="da73a-108">Syntax</span></span>


```C++
HRESULT DiscoveredOnCurrentNetwork(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="da73a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="da73a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da73a-110">*valor* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="da73a-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="da73a-111">Recibe un puntero a un valor booleano que es **true** si el dispositivo está en la red actual.</span><span class="sxs-lookup"><span data-stu-id="da73a-111">Receives a pointer to a boolean value that is **True** if the device is on the current network.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da73a-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="da73a-112">Return value</span></span>

<span data-ttu-id="da73a-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="da73a-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="da73a-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="da73a-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="da73a-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="da73a-115">Return code</span></span>                                                                          | <span data-ttu-id="da73a-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="da73a-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="da73a-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="da73a-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="da73a-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="da73a-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="da73a-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="da73a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da73a-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="da73a-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





