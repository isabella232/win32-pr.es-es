---
description: Una solicitud asincrónica para obtener los fotogramas de lista capturados en el registro de gráficos.
MS-HAID: vspixengine.IFrameListRequest\_RequestAsync\_IFrameListCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IFrameListRequest:: RequestAsync (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 309C28F2-CE01-49E7-9A21-5053E3ED7721
api_name:
- IFrameListRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3627fc5ef3a425ae7607009b4ad382080ea99192
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104079925"
---
# <a name="span-idvspixengineiframelistrequest_requestasync_iframelistcallback_ptr_dword_dwordspaniframelistrequestrequestasync-method"></a><span data-ttu-id="afc6a-103"><span id="vspixengine.iframelistrequest_requestasync_iframelistcallback_ptr_dword_dword"></span>IFrameListRequest:: RequestAsync (método)</span><span class="sxs-lookup"><span data-stu-id="afc6a-103"><span id="vspixengine.iframelistrequest_requestasync_iframelistcallback_ptr_dword_dword"></span>IFrameListRequest::RequestAsync method</span></span>

<span data-ttu-id="afc6a-104">Una solicitud asincrónica para obtener los fotogramas de lista capturados en el registro de gráficos.</span><span class="sxs-lookup"><span data-stu-id="afc6a-104">An asynchronous request to get the list frames captured in the graphics log.</span></span>

## <a name="syntax"></a><span data-ttu-id="afc6a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="afc6a-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   IFrameListCallback * requestCallback,
   DWORD                requestCookie,
   DWORD                progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="afc6a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="afc6a-106">Parameters</span></span>

<span data-ttu-id="afc6a-107">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="afc6a-107">*requestCallback* </span></span>  
<span data-ttu-id="afc6a-108">Dirección de devolución de llamada que se utiliza para notificar al host los resultados.</span><span class="sxs-lookup"><span data-stu-id="afc6a-108">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="afc6a-109">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="afc6a-109">*requestCookie* </span></span>  
<span data-ttu-id="afc6a-110">Cookie que identifica de forma única la solicitud y que se puede usar para indicar que se va a cancelar.</span><span class="sxs-lookup"><span data-stu-id="afc6a-110">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="afc6a-111">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="afc6a-111">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="afc6a-112">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="afc6a-112">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="afc6a-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="afc6a-113">Return value</span></span>

<span data-ttu-id="afc6a-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="afc6a-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="afc6a-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="afc6a-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="afc6a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="afc6a-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="afc6a-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="afc6a-117">Header</span></span></p></td><td><span data-ttu-id="afc6a-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="afc6a-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="afc6a-119"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="afc6a-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="afc6a-120">**IFrameListRequest**</span><span class="sxs-lookup"><span data-stu-id="afc6a-120">**IFrameListRequest**</span></span>](/windows/desktop/direct3dtools/iframelistrequest)

 

 
