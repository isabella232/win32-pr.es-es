---
title: IMediaRendererActionInformation IsSeekAvailable, método
description: Recupera un valor que indica si el DMR está aceptando actualmente el método SeekAsync.
ms.assetid: F0817184-70F2-43AC-A2BE-A15F4B195085
keywords:
- Método IsSeekAvailable API de streaming de multimedia
- Método IsSeekAvailable API de streaming de multimedia, interfaz IMediaRendererActionInformation
- Interfaz IMediaRendererActionInformation API de streaming de multimedia, método IsSeekAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsSeekAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 700afb72efbab01bbd3a8f5e15fa444eb6b06272
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904576"
---
# <a name="imediarendereractioninformationisseekavailable-method"></a><span data-ttu-id="2604c-106">IMediaRendererActionInformation:: IsSeekAvailable (método)</span><span class="sxs-lookup"><span data-stu-id="2604c-106">IMediaRendererActionInformation::IsSeekAvailable method</span></span>

<span data-ttu-id="2604c-107">Recupera un valor que indica si el DMR está aceptando actualmente el método [**SeekAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-seekasync) .</span><span class="sxs-lookup"><span data-stu-id="2604c-107">Retrieves a value that indicates whether the DMR is currently accepting the [**SeekAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-seekasync) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2604c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2604c-108">Syntax</span></span>


```C++
HRESULT IsSeekAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="2604c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2604c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2604c-110">*valor* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2604c-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2604c-111">Valor booleano que es **true** si el DMR está aceptando actualmente el método [**SeekAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-seekasync) y **false** si no lo está.</span><span class="sxs-lookup"><span data-stu-id="2604c-111">A boolean value that is **True** if the DMR is currently accepting the [**SeekAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-seekasync) method and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2604c-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2604c-112">Return value</span></span>

<span data-ttu-id="2604c-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="2604c-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="2604c-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="2604c-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="2604c-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="2604c-115">Return code</span></span>                                                                          | <span data-ttu-id="2604c-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="2604c-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="2604c-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="2604c-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="2604c-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="2604c-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="2604c-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="2604c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2604c-120">**IMediaRendererActionInformation**</span><span class="sxs-lookup"><span data-stu-id="2604c-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

