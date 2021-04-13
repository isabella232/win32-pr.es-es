---
title: IMediaRendererActionInformation IsPlayAvailable, método
description: Recupera un valor que indica si el DMR acepta actualmente la aceptación de los métodos PlayAsync y PlayAtSpeedAsync.
ms.assetid: 969C55FA-872D-4063-B85C-573C8DA5593C
keywords:
- Método IsPlayAvailable API de streaming de multimedia
- Método IsPlayAvailable API de streaming de multimedia, interfaz IMediaRendererActionInformation
- Interfaz IMediaRendererActionInformation API de streaming de multimedia, método IsPlayAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsPlayAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 87fa3a2005772a4d948bafe32d2a0e10cc5a6914
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420655"
---
# <a name="imediarendereractioninformationisplayavailable-method"></a><span data-ttu-id="bce25-106">IMediaRendererActionInformation:: IsPlayAvailable (método)</span><span class="sxs-lookup"><span data-stu-id="bce25-106">IMediaRendererActionInformation::IsPlayAvailable method</span></span>

<span data-ttu-id="bce25-107">Recupera un valor que indica si el DMR acepta actualmente la aceptación de los métodos [**PlayAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playasync) y [**PlayAtSpeedAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playatspeedasync) .</span><span class="sxs-lookup"><span data-stu-id="bce25-107">Retrieves a value that indicates whether the DMR is currently accepting the accepting the [**PlayAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playasync) and [**PlayAtSpeedAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playatspeedasync) methods.</span></span>

## <a name="syntax"></a><span data-ttu-id="bce25-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bce25-108">Syntax</span></span>


```C++
HRESULT IsPlayAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="bce25-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bce25-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bce25-110">*valor* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="bce25-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bce25-111">Valor booleano que es **true** si el DMR acepta actualmente los métodos [**PlayAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playasync) y [**PlayAtSpeedAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playatspeedasync) y **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="bce25-111">A boolean value that is **True** if the DMR is currently accepting the accepting the [**PlayAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playasync) and [**PlayAtSpeedAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playatspeedasync) methods and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bce25-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bce25-112">Return value</span></span>

<span data-ttu-id="bce25-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="bce25-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="bce25-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="bce25-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="bce25-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="bce25-115">Return code</span></span>                                                                          | <span data-ttu-id="bce25-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="bce25-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="bce25-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="bce25-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="bce25-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="bce25-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="bce25-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="bce25-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bce25-120">**IMediaRendererActionInformation**</span><span class="sxs-lookup"><span data-stu-id="bce25-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

