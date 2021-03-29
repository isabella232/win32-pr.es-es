---
title: IMediaRendererActionInformation IsPauseAvailable, método
description: Recupera un valor que indica si el DMR está aceptando actualmente el método PauseAsync.
ms.assetid: 095A664F-D974-410D-8741-87A171EDD071
keywords:
- Método IsPauseAvailable API de streaming de multimedia
- Método IsPauseAvailable API de streaming de multimedia, interfaz IMediaRendererActionInformation
- Interfaz IMediaRendererActionInformation API de streaming de multimedia, método IsPauseAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsPauseAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9eb0b750f5a04528aef830d87376c276bdaf6674
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904577"
---
# <a name="imediarendereractioninformationispauseavailable-method"></a><span data-ttu-id="69778-106">IMediaRendererActionInformation:: IsPauseAvailable (método)</span><span class="sxs-lookup"><span data-stu-id="69778-106">IMediaRendererActionInformation::IsPauseAvailable method</span></span>

<span data-ttu-id="69778-107">Recupera un valor que indica si el DMR está aceptando actualmente el método [**PauseAsync**](imediarenderer-pauseasync.md) .</span><span class="sxs-lookup"><span data-stu-id="69778-107">Retrieves a value that indicates whether the DMR is currently accepting the [**PauseAsync**](imediarenderer-pauseasync.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="69778-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="69778-108">Syntax</span></span>


```C++
HRESULT IsPauseAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="69778-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="69778-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69778-110">*valor* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="69778-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="69778-111">Valor booleano que es **true** si el DMR está aceptando actualmente el método [**PauseAsync**](imediarenderer-pauseasync.md) y **false** si no lo está.</span><span class="sxs-lookup"><span data-stu-id="69778-111">A boolean value that is **True** if the DMR is currently accepting the [**PauseAsync**](imediarenderer-pauseasync.md) method and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69778-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="69778-112">Return value</span></span>

<span data-ttu-id="69778-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="69778-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="69778-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="69778-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="69778-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="69778-115">Return code</span></span>                                                                          | <span data-ttu-id="69778-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="69778-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="69778-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="69778-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="69778-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="69778-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="69778-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="69778-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69778-120">**IMediaRendererActionInformation**</span><span class="sxs-lookup"><span data-stu-id="69778-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

