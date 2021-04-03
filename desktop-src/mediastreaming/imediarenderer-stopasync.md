---
title: IMediaRenderer StopAsync, método
description: Indica al DMR de forma asincrónica que detenga la reproducción del contenido actual. | IMediaRenderer StopAsync, método
ms.assetid: B6B0F3F2-E95E-4A58-9CBD-CF4CB24FDAD0
keywords:
- Método StopAsync API de streaming de multimedia
- Método StopAsync API de streaming de multimedia, interfaz IMediaRenderer
- Interfaz IMediaRenderer API de streaming de multimedia, método StopAsync
topic_type:
- apiref
api_name:
- IMediaRenderer.StopAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a5f73d534fdd786038a242614a981f4915d92c13
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914629"
---
# <a name="imediarendererstopasync-method"></a><span data-ttu-id="c36c6-107">IMediaRenderer:: StopAsync (método)</span><span class="sxs-lookup"><span data-stu-id="c36c6-107">IMediaRenderer::StopAsync method</span></span>

<span data-ttu-id="c36c6-108">Indica al DMR de forma asincrónica que detenga la reproducción del contenido actual.</span><span class="sxs-lookup"><span data-stu-id="c36c6-108">Instructs the DMR asynchronously to stop playing the current content.</span></span>

## <a name="syntax"></a><span data-ttu-id="c36c6-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c36c6-109">Syntax</span></span>


```C++
HRESULT StopAsync(
  [out] PlaybackOperation **value
);
```



## <a name="parameters"></a><span data-ttu-id="c36c6-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c36c6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c36c6-111">*valor* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c36c6-111">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c36c6-112">Recibe una referencia a un objeto [**PlaybackOperation**](playbackoperation.md) que se usa para obtener los resultados de la operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="c36c6-112">Receives a reference to a [**PlaybackOperation**](playbackoperation.md) object that is used to get results from the asynchronous operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c36c6-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c36c6-113">Return value</span></span>

<span data-ttu-id="c36c6-114">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="c36c6-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c36c6-115">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="c36c6-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c36c6-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c36c6-116">Return code</span></span>                                                                          | <span data-ttu-id="c36c6-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="c36c6-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="c36c6-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="c36c6-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="c36c6-119">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="c36c6-119">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="c36c6-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="c36c6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c36c6-121">**IMediaRenderer**</span><span class="sxs-lookup"><span data-stu-id="c36c6-121">**IMediaRenderer**</span></span>](imediarenderer.md)
</dt> </dl>

 

 





