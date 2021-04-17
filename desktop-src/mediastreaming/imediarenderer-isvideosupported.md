---
title: IMediaRenderer IsVideoSupported, método
description: Recupera un valor que indica si el DMR es capaz de reproducir contenido de vídeo.
ms.assetid: AE9A14D0-A7A2-4A71-9454-06A05C7D85F9
keywords:
- Método IsVideoSupported API de streaming de multimedia
- Método IsVideoSupported API de streaming de multimedia, interfaz IMediaRenderer
- Interfaz IMediaRenderer API de streaming de multimedia, método IsVideoSupported
topic_type:
- apiref
api_name:
- IMediaRenderer.IsVideoSupported
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9808841bf60a384d6a4566e75f53248b0f86338c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104358260"
---
# <a name="imediarendererisvideosupported-method"></a><span data-ttu-id="9a010-106">IMediaRenderer:: IsVideoSupported (método)</span><span class="sxs-lookup"><span data-stu-id="9a010-106">IMediaRenderer::IsVideoSupported method</span></span>

<span data-ttu-id="9a010-107">Recupera un valor que indica si el DMR es capaz de reproducir contenido de vídeo.</span><span class="sxs-lookup"><span data-stu-id="9a010-107">Retrieves a value that indicates whether the DMR is capable of playing video content.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a010-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9a010-108">Syntax</span></span>


```C++
HRESULT IsVideoSupported(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="9a010-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9a010-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a010-110">*valor* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9a010-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9a010-111">Valor booleano que es **true** si el DMR es capaz de reproducir contenido de vídeo y **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="9a010-111">A boolean value that is **True** if the DMR is capable of playing video content and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a010-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9a010-112">Return value</span></span>

<span data-ttu-id="9a010-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="9a010-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="9a010-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="9a010-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="9a010-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="9a010-115">Return code</span></span>                                                                          | <span data-ttu-id="9a010-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="9a010-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="9a010-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="9a010-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="9a010-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="9a010-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="9a010-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="9a010-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a010-120">**IMediaRenderer**</span><span class="sxs-lookup"><span data-stu-id="9a010-120">**IMediaRenderer**</span></span>](imediarenderer.md)
</dt> </dl>

 

 





