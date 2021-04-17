---
title: MediaRenderer. PauseAsync, método
description: Indica al DMR de forma asincrónica que PAUSE la reproducción del contenido actual. | MediaRenderer. PauseAsync, método
ms.assetid: 1bd36349-0551-44e8-9550-3fd80900de9a
keywords:
- Método PauseAsync API de streaming de multimedia
- Método PauseAsync API de streaming de multimedia, interfaz MediaRenderer
- Interfaz MediaRenderer API de streaming de multimedia, método PauseAsync
topic_type:
- apiref
api_name:
- MediaRenderer.PauseAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2bbbc55931c7cc7fc5e2e5ec39ba63fe7a064478
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105717523"
---
# <a name="mediarendererpauseasync-method"></a><span data-ttu-id="d61ab-107">MediaRenderer. PauseAsync, método</span><span class="sxs-lookup"><span data-stu-id="d61ab-107">MediaRenderer.PauseAsync method</span></span>

<span data-ttu-id="d61ab-108">Indica al DMR de forma asincrónica que PAUSE la reproducción del contenido actual.</span><span class="sxs-lookup"><span data-stu-id="d61ab-108">Instructs the DMR asynchronously to pause playing the current content.</span></span>

## <a name="syntax"></a><span data-ttu-id="d61ab-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d61ab-109">Syntax</span></span>


```C++
HRESULT PauseAsync(
  [out] PlaybackOperation **value
);
```



## <a name="parameters"></a><span data-ttu-id="d61ab-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d61ab-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d61ab-111">*valor* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d61ab-111">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d61ab-112">Recibe una referencia a un objeto [**PlaybackOperation**](playbackoperation.md) que se usa para obtener los resultados de la operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="d61ab-112">Receives a reference to a [**PlaybackOperation**](playbackoperation.md) object that is used to get results from the asynchronous operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d61ab-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d61ab-113">Return value</span></span>

<span data-ttu-id="d61ab-114">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="d61ab-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d61ab-115">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="d61ab-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d61ab-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="d61ab-116">Return code</span></span>                                                                          | <span data-ttu-id="d61ab-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="d61ab-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d61ab-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="d61ab-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="d61ab-119">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="d61ab-119">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="d61ab-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="d61ab-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d61ab-121">**MediaRenderer**</span><span class="sxs-lookup"><span data-stu-id="d61ab-121">**MediaRenderer**</span></span>](mediarenderer.md)
</dt> </dl>

 

 





