---
title: IMediaRendererActionInformation IsSetNextSourceAvailable, método
description: Recupera un valor que indica si el DMR está aceptando actualmente el método SetNextSourceFromUriAsync, el método SetNextSourceFromStreamAsync o el método SetNextSourceFromMediaSourceAsync.
ms.assetid: 7588E992-4070-4E0F-8C4B-7DFC097A5076
keywords:
- Método IsSetNextSourceAvailable API de streaming de multimedia
- Método IsSetNextSourceAvailable API de streaming de multimedia, interfaz IMediaRendererActionInformation
- Interfaz IMediaRendererActionInformation API de streaming de multimedia, método IsSetNextSourceAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsSetNextSourceAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 265a9a96d5229e47008c60813fd6c0e3bc567800
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790569"
---
# <a name="imediarendereractioninformationissetnextsourceavailable-method"></a><span data-ttu-id="002ec-106">IMediaRendererActionInformation:: IsSetNextSourceAvailable (método)</span><span class="sxs-lookup"><span data-stu-id="002ec-106">IMediaRendererActionInformation::IsSetNextSourceAvailable method</span></span>

<span data-ttu-id="002ec-107">Recupera un valor que indica si el DMR está aceptando actualmente el método [**SetNextSourceFromUriAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromuriasync) , el método [**SetNextSourceFromStreamAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromstreamasync) o el método [**SetNextSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefrommediasourceasync) .</span><span class="sxs-lookup"><span data-stu-id="002ec-107">Retrieves a value that indicates whether the DMR is currently accepting the [**SetNextSourceFromUriAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromuriasync) method, the [**SetNextSourceFromStreamAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromstreamasync) method or the [**SetNextSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefrommediasourceasync) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="002ec-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="002ec-108">Syntax</span></span>


```C++
HRESULT IsSetNextSourceAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="002ec-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="002ec-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="002ec-110">*valor* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="002ec-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="002ec-111">Valor booleano que es **true** si el DMR está aceptando actualmente el método [**SetNextSourceFromUriAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromuriasync) , el método [**SetNextSourceFromStreamAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromstreamasync) o el método [**SetNextSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefrommediasourceasync) y **false** si no lo está.</span><span class="sxs-lookup"><span data-stu-id="002ec-111">A boolean value that is **True** if the DMR is currently accepting the [**SetNextSourceFromUriAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromuriasync) method, the [**SetNextSourceFromStreamAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromstreamasync) method or the [**SetNextSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefrommediasourceasync) method and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="002ec-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="002ec-112">Return value</span></span>

<span data-ttu-id="002ec-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="002ec-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="002ec-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="002ec-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="002ec-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="002ec-115">Return code</span></span>                                                                          | <span data-ttu-id="002ec-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="002ec-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="002ec-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="002ec-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="002ec-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="002ec-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="002ec-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="002ec-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="002ec-120">**IMediaRendererActionInformation**</span><span class="sxs-lookup"><span data-stu-id="002ec-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

