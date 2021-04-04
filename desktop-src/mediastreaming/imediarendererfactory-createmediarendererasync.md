---
title: IMediaRendererFactory CreateMediaRendererAsync, método
description: Crea de forma asincrónica una nueva instancia de un objeto que implementa la interfaz IMediaRenderer con el nombre de dispositivo único especificado (UDN).
ms.assetid: FD1242F8-4C2E-4027-B1DE-5FD69557684C
keywords:
- Método CreateMediaRendererAsync API de streaming de multimedia
- Método CreateMediaRendererAsync API de streaming de multimedia, interfaz IMediaRendererFactory
- Interfaz IMediaRendererFactory API de streaming de multimedia, método CreateMediaRendererAsync
topic_type:
- apiref
api_name:
- IMediaRendererFactory.CreateMediaRendererAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b152e5889ad83440a48e178be0b89a97d2a9f664
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790563"
---
# <a name="imediarendererfactorycreatemediarendererasync-method"></a><span data-ttu-id="c92bf-106">IMediaRendererFactory:: CreateMediaRendererAsync (método)</span><span class="sxs-lookup"><span data-stu-id="c92bf-106">IMediaRendererFactory::CreateMediaRendererAsync method</span></span>

<span data-ttu-id="c92bf-107">Crea de forma asincrónica una nueva instancia de un objeto que implementa la interfaz [**IMediaRenderer**](imediarenderer.md) con el nombre de dispositivo único especificado (UDN).</span><span class="sxs-lookup"><span data-stu-id="c92bf-107">Asynchronously creates a new instance of an object that implements the [**IMediaRenderer**](imediarenderer.md) interface using the specified Unique Device Name (UDN).</span></span>

## <a name="syntax"></a><span data-ttu-id="c92bf-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c92bf-108">Syntax</span></span>


```C++
HRESULT CreateMediaRendererAsync(
  [in]          HSTRING                      deviceIdentifier,
  [out, retval] CreateMediaRendererOperation **value
);
```



## <a name="parameters"></a><span data-ttu-id="c92bf-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c92bf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c92bf-110">*deviceIdentifier* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c92bf-110">*deviceIdentifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c92bf-111">Un HSTRING que contiene un UDN que identifica el dispositivo DMR de DLNA para el que se creará una instancia de [**IMediaRenderer**](imediarenderer.md) .</span><span class="sxs-lookup"><span data-stu-id="c92bf-111">An HSTRING containing a UDN that identifies the DLNA DMR device for which an instance of [**IMediaRenderer**](imediarenderer.md) will be created.</span></span>

</dd> <dt>

<span data-ttu-id="c92bf-112">*valor* \[ de out, retval\]</span><span class="sxs-lookup"><span data-stu-id="c92bf-112">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="c92bf-113">Recibe una referencia a un objeto [**CreateMediaRendererOperation**](createmediarendereroperation.md) que se usa para obtener los resultados de la operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="c92bf-113">Receives a reference to a [**CreateMediaRendererOperation**](createmediarendereroperation.md) object that is used to get results from the asynchronous operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c92bf-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c92bf-114">Return value</span></span>

<span data-ttu-id="c92bf-115">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="c92bf-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c92bf-116">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="c92bf-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c92bf-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c92bf-117">Return code</span></span>                                                                          | <span data-ttu-id="c92bf-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="c92bf-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="c92bf-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="c92bf-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="c92bf-120">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="c92bf-120">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="c92bf-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="c92bf-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c92bf-122">**IMediaRendererFactory**</span><span class="sxs-lookup"><span data-stu-id="c92bf-122">**IMediaRendererFactory**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendererfactory)
</dt> </dl>

 

