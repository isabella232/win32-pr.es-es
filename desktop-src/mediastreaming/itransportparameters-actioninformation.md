---
title: ITransportParameters ActionInformation, método
description: Obtiene una interfaz IMediaRendererActionInformation que proporciona información sobre los métodos que se pueden invocar actualmente en el DMR.
ms.assetid: 3EEB94E1-B6BC-4111-AEF1-D5724BD0A2E7
keywords:
- Método ActionInformation API de streaming de multimedia
- Método ActionInformation API de streaming de multimedia, interfaz ITransportParameters
- Interfaz ITransportParameters API de streaming de multimedia, método ActionInformation
topic_type:
- apiref
api_name:
- ITransportParameters.ActionInformation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b194da50e71402b6af69eb4cc9d67902e8ae89a0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077652"
---
# <a name="itransportparametersactioninformation-method"></a><span data-ttu-id="e3e13-106">ITransportParameters:: ActionInformation (método)</span><span class="sxs-lookup"><span data-stu-id="e3e13-106">ITransportParameters::ActionInformation method</span></span>

<span data-ttu-id="e3e13-107">Obtiene una interfaz [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) que proporciona información sobre los métodos que se pueden invocar actualmente en el DMR.</span><span class="sxs-lookup"><span data-stu-id="e3e13-107">Obtains an [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) interface that provides information about which methods can currently be invoked on the DMR.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3e13-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e3e13-108">Syntax</span></span>


```C++
HRESULT ActionInformation(
  [out, retval] IMediaRendererActionInformation **value
);
```



## <a name="parameters"></a><span data-ttu-id="e3e13-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e3e13-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3e13-110">*valor* \[ de out, retval\]</span><span class="sxs-lookup"><span data-stu-id="e3e13-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="e3e13-111">Recibe una referencia a una interfaz [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) .</span><span class="sxs-lookup"><span data-stu-id="e3e13-111">Receives a reference to an [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3e13-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e3e13-112">Return value</span></span>

<span data-ttu-id="e3e13-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="e3e13-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="e3e13-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="e3e13-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="e3e13-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e3e13-115">Return code</span></span>                                                                          | <span data-ttu-id="e3e13-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3e13-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="e3e13-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="e3e13-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="e3e13-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="e3e13-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="e3e13-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="e3e13-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3e13-120">**ITransportParameters**</span><span class="sxs-lookup"><span data-stu-id="e3e13-120">**ITransportParameters**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-itransportparameters)
</dt> </dl>

 

