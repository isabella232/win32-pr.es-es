---
title: IMediaRendererFactory CreateMediaRendererFromBasicDeviceAsync, método
description: Crea de forma asincrónica una nueva instancia de un objeto que implementa la interfaz IMediaRenderer mediante la interfaz IBasicDevice especificada.
ms.assetid: 14A83789-0F3C-467B-8EFD-3BB421C54217
keywords:
- Método CreateMediaRendererFromBasicDeviceAsync API de streaming de multimedia
- Método CreateMediaRendererFromBasicDeviceAsync API de streaming de multimedia, interfaz IMediaRendererFactory
- Interfaz IMediaRendererFactory API de streaming de multimedia, método CreateMediaRendererFromBasicDeviceAsync
topic_type:
- apiref
api_name:
- IMediaRendererFactory.CreateMediaRendererFromBasicDeviceAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7e4ee614cca9a03ca203ecde9203e019fab38ab4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077653"
---
# <a name="imediarendererfactorycreatemediarendererfrombasicdeviceasync-method"></a><span data-ttu-id="d9765-106">IMediaRendererFactory:: CreateMediaRendererFromBasicDeviceAsync (método)</span><span class="sxs-lookup"><span data-stu-id="d9765-106">IMediaRendererFactory::CreateMediaRendererFromBasicDeviceAsync method</span></span>

<span data-ttu-id="d9765-107">Crea de forma asincrónica una nueva instancia de un objeto que implementa la interfaz [**IMediaRenderer**](imediarenderer.md) mediante la interfaz [**IBasicDevice**](ibasicdevice.md) especificada.</span><span class="sxs-lookup"><span data-stu-id="d9765-107">Asynchronously creates a new instance of an object that implements the [**IMediaRenderer**](imediarenderer.md) interface using the specified [**IBasicDevice**](ibasicdevice.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9765-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d9765-108">Syntax</span></span>


```C++
HRESULT CreateMediaRendererFromBasicDeviceAsync(
  [in]          IBasicDevice                 *basicDevice,
  [out, retval] CreateMediaRendererOperation **value
);
```



## <a name="parameters"></a><span data-ttu-id="d9765-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d9765-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9765-110">*basicDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d9765-110">*basicDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9765-111">Un puntero a una interfaz [**IBasicDevice**](ibasicdevice.md) que representa el dispositivo para el que se creará una instancia de [**IMediaRenderer**](imediarenderer.md) .</span><span class="sxs-lookup"><span data-stu-id="d9765-111">A pointer to an [**IBasicDevice**](ibasicdevice.md) interface representing the device for which an instance of [**IMediaRenderer**](imediarenderer.md) will be created.</span></span>

</dd> <dt>

<span data-ttu-id="d9765-112">*valor* \[ de out, retval\]</span><span class="sxs-lookup"><span data-stu-id="d9765-112">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="d9765-113">Recibe una referencia a un objeto [**CreateMediaRendererOperation**](createmediarendereroperation.md) que se usa para obtener los resultados de la operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="d9765-113">Receives a reference to a [**CreateMediaRendererOperation**](createmediarendereroperation.md) object that is used to get results from the asynchronous operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9765-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d9765-114">Return value</span></span>

<span data-ttu-id="d9765-115">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="d9765-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d9765-116">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="d9765-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d9765-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="d9765-117">Return code</span></span>                                                                          | <span data-ttu-id="d9765-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="d9765-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d9765-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="d9765-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="d9765-120">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="d9765-120">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="d9765-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="d9765-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9765-122">**IMediaRendererFactory**</span><span class="sxs-lookup"><span data-stu-id="d9765-122">**IMediaRendererFactory**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendererfactory)
</dt> </dl>

 

