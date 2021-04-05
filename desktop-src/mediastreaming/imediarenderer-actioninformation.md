---
title: IMediaRenderer ActionInformation, método
description: Recupera información sobre los métodos que se pueden invocar actualmente en el DMR.
ms.assetid: 7681FF92-DD13-4BBC-B860-E2BDFDA74FB9
keywords:
- Método ActionInformation API de streaming de multimedia
- Método ActionInformation API de streaming de multimedia, interfaz IMediaRenderer
- Interfaz IMediaRenderer API de streaming de multimedia, método ActionInformation
topic_type:
- apiref
api_name:
- IMediaRenderer.ActionInformation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 346e43d6aaf3503c21f6a7586db5a731f0a7c478
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077667"
---
# <a name="imediarendereractioninformation-method"></a><span data-ttu-id="907e9-106">IMediaRenderer:: ActionInformation (método)</span><span class="sxs-lookup"><span data-stu-id="907e9-106">IMediaRenderer::ActionInformation method</span></span>

<span data-ttu-id="907e9-107">Recupera información sobre los métodos que se pueden invocar actualmente en el DMR.</span><span class="sxs-lookup"><span data-stu-id="907e9-107">Retrieves information about which methods can currently be invoked on the DMR.</span></span>

## <a name="syntax"></a><span data-ttu-id="907e9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="907e9-108">Syntax</span></span>


```C++
HRESULT ActionInformation(
  [out] IMediaRendererActionInformation **value
);
```



## <a name="parameters"></a><span data-ttu-id="907e9-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="907e9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="907e9-110">*valor* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="907e9-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="907e9-111">Recibe una referencia a una interfaz [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) .</span><span class="sxs-lookup"><span data-stu-id="907e9-111">Receives a reference to an [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="907e9-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="907e9-112">Return value</span></span>

<span data-ttu-id="907e9-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="907e9-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="907e9-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="907e9-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="907e9-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="907e9-115">Return code</span></span>                                                                          | <span data-ttu-id="907e9-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="907e9-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="907e9-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="907e9-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="907e9-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="907e9-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="907e9-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="907e9-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="907e9-120">**IMediaRenderer**</span><span class="sxs-lookup"><span data-stu-id="907e9-120">**IMediaRenderer**</span></span>](imediarenderer.md)
</dt> </dl>

 

