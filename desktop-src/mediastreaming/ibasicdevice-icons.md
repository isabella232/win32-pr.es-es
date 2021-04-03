---
title: IBasicDevice Icons (método)
description: Devuelve un vector de interfaces IDeviceIcon.
ms.assetid: 0C083AF3-FE22-4A8E-87B7-0FFA7B65ADBD
keywords:
- Icons (método) API de streaming de multimedia
- Icons (método) API de streaming de multimedia, interfaz IBasicDevice
- IBasicDevice interface media streaming API, Icons (método)
topic_type:
- apiref
api_name:
- IBasicDevice.Icons
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3fb6e4b708b4e38ffb39f152308cec7b885a772f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103789891"
---
# <a name="ibasicdeviceicons-method"></a><span data-ttu-id="49326-106">IBasicDevice:: Icons (método)</span><span class="sxs-lookup"><span data-stu-id="49326-106">IBasicDevice::Icons method</span></span>

<span data-ttu-id="49326-107">Devuelve un vector de interfaces [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) .</span><span class="sxs-lookup"><span data-stu-id="49326-107">Returns a vector of [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) interfaces.</span></span>

## <a name="syntax"></a><span data-ttu-id="49326-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="49326-108">Syntax</span></span>


```C++
HRESULT Icons(
  [out] IVector< IDeviceIcon > **value
);
```



## <a name="parameters"></a><span data-ttu-id="49326-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="49326-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49326-110">*valor* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="49326-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="49326-111">Recibe una colección enumerable de punteros de interfaz [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) .</span><span class="sxs-lookup"><span data-stu-id="49326-111">Receives an enumerable collection of [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49326-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="49326-112">Return value</span></span>

<span data-ttu-id="49326-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="49326-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="49326-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="49326-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="49326-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="49326-115">Return code</span></span>                                                                          | <span data-ttu-id="49326-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="49326-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="49326-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="49326-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="49326-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="49326-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="49326-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="49326-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49326-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="49326-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

