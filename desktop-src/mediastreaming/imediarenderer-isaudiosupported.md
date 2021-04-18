---
title: IMediaRenderer IsAudioSupported, método
description: Recupera un valor que indica si el DMR es capaz de reproducir contenido de audio.
ms.assetid: D5F0C4ED-5778-4388-A7BD-E3923145D663
keywords:
- Método IsAudioSupported API de streaming de multimedia
- Método IsAudioSupported API de streaming de multimedia, interfaz IMediaRenderer
- Interfaz IMediaRenderer API de streaming de multimedia, método IsAudioSupported
topic_type:
- apiref
api_name:
- IMediaRenderer.IsAudioSupported
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4f7670d0a2818cf5518bee0b2586531caeea20fd
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105720091"
---
# <a name="imediarendererisaudiosupported-method"></a><span data-ttu-id="2981f-106">IMediaRenderer:: IsAudioSupported (método)</span><span class="sxs-lookup"><span data-stu-id="2981f-106">IMediaRenderer::IsAudioSupported method</span></span>

<span data-ttu-id="2981f-107">Recupera un valor que indica si el DMR es capaz de reproducir contenido de audio.</span><span class="sxs-lookup"><span data-stu-id="2981f-107">Retrieves a value that indicates whether the DMR is capable of playing audio content.</span></span>

## <a name="syntax"></a><span data-ttu-id="2981f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2981f-108">Syntax</span></span>


```C++
HRESULT IsAudioSupported(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="2981f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2981f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2981f-110">*valor* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2981f-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2981f-111">Valor booleano que es **true** si el DMR es capaz de reproducir contenido de audio y **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="2981f-111">A boolean value that is **True** if the DMR is capable of playing audio content and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2981f-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2981f-112">Return value</span></span>

<span data-ttu-id="2981f-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="2981f-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="2981f-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="2981f-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="2981f-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="2981f-115">Return code</span></span>                                                                          | <span data-ttu-id="2981f-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="2981f-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="2981f-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="2981f-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="2981f-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="2981f-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="2981f-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="2981f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2981f-120">**IMediaRenderer**</span><span class="sxs-lookup"><span data-stu-id="2981f-120">**IMediaRenderer**</span></span>](imediarenderer.md)
</dt> </dl>

 

 





