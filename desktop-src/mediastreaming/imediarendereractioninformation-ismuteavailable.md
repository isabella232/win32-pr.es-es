---
title: IMediaRendererActionInformation IsMuteAvailable, método
description: Recupera un valor que indica si el DMR es capaz de silenciar el audio.
ms.assetid: F744C2D7-5518-4A9F-A71E-60CF0B312177
keywords:
- Método IsMuteAvailable API de streaming de multimedia
- Método IsMuteAvailable API de streaming de multimedia, interfaz IMediaRendererActionInformation
- Interfaz IMediaRendererActionInformation API de streaming de multimedia, método IsMuteAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsMuteAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 96751a7f2f1aedcd9e29be981ffadf6c43bf4008
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077639"
---
# <a name="imediarendereractioninformationismuteavailable-method"></a><span data-ttu-id="f529e-106">IMediaRendererActionInformation:: IsMuteAvailable (método)</span><span class="sxs-lookup"><span data-stu-id="f529e-106">IMediaRendererActionInformation::IsMuteAvailable method</span></span>

<span data-ttu-id="f529e-107">Recupera un valor que indica si el DMR es capaz de silenciar el audio.</span><span class="sxs-lookup"><span data-stu-id="f529e-107">Retrieves a value that indicates whether the DMR is capable of muting the audio.</span></span>

## <a name="syntax"></a><span data-ttu-id="f529e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f529e-108">Syntax</span></span>


```C++
HRESULT IsMuteAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="f529e-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f529e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f529e-110">*valor* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f529e-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f529e-111">Valor booleano que es **true** si el DMR es capaz de silenciar el audio y **false** si no lo es.</span><span class="sxs-lookup"><span data-stu-id="f529e-111">A boolean value that is **True** if the DMR is capable of muting the audio and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f529e-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f529e-112">Return value</span></span>

<span data-ttu-id="f529e-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f529e-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f529e-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="f529e-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f529e-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="f529e-115">Return code</span></span>                                                                          | <span data-ttu-id="f529e-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="f529e-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="f529e-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="f529e-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f529e-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="f529e-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="f529e-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="f529e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f529e-120">**IMediaRendererActionInformation**</span><span class="sxs-lookup"><span data-stu-id="f529e-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

