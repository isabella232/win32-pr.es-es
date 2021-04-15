---
description: Solicita que obtenga el contenido de una textura como. Archivo DDS (DirectDraw Surface).
MS-HAID: vspixengine.ITextureRequest\_RequestAsync\_EventID\_DWORD\_BSTR\_ITextureCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'ITextureRequest:: RequestAsync (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 89A9F230-D296-43CD-A2A6-747057750EED
api_name:
- ITextureRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e5abfee1b26fd2145aef8e01239cc0b874ee54e2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495677"
---
# <a name="span-idvspixengineitexturerequest_requestasync_eventid_dword_bstr_itexturecallback_ptr_dword_dwordspanitexturerequestrequestasync-method"></a><span data-ttu-id="089e5-103"><span id="vspixengine.itexturerequest_requestasync_eventid_dword_bstr_itexturecallback_ptr_dword_dword"></span>ITextureRequest:: RequestAsync (método)</span><span class="sxs-lookup"><span data-stu-id="089e5-103"><span id="vspixengine.itexturerequest_requestasync_eventid_dword_bstr_itexturecallback_ptr_dword_dword"></span>ITextureRequest::RequestAsync method</span></span>

<span data-ttu-id="089e5-104">Solicita que obtenga el contenido de una textura como. Archivo DDS (DirectDraw Surface).</span><span class="sxs-lookup"><span data-stu-id="089e5-104">Requests to get the contents of a texture as a .DDS (DirectDraw Surface) file.</span></span>

## <a name="syntax"></a><span data-ttu-id="089e5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="089e5-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   EventID            eventID,
   DWORD              textureFileptr,
   BSTR               ddsFilename,
   ITextureCallback * pRequestCallback,
   DWORD              requestCookie,
   DWORD              progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="089e5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="089e5-106">Parameters</span></span>

<span data-ttu-id="089e5-107">*eventID* </span><span class="sxs-lookup"><span data-stu-id="089e5-107">*eventID* </span></span>  
<span data-ttu-id="089e5-108">Evento especificado con el que se va a hacer coincidir el contenido del búfer (por ejemplo, un destino de representación podría cambiar con el tiempo).</span><span class="sxs-lookup"><span data-stu-id="089e5-108">The specified event to match the buffer's content to (for example, a render target could change over time).</span></span>

<span data-ttu-id="089e5-109">*textureFileptr* </span><span class="sxs-lookup"><span data-stu-id="089e5-109">*textureFileptr* </span></span>  
<span data-ttu-id="089e5-110">Dirección del objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="089e5-110">The address of the texture object.</span></span>

<span data-ttu-id="089e5-111">*ddsFilename* </span><span class="sxs-lookup"><span data-stu-id="089e5-111">*ddsFilename* </span></span>  
<span data-ttu-id="089e5-112">Cadena COM que contiene la ruta de acceso del archivo. DDS donde se escriben los resultados.</span><span class="sxs-lookup"><span data-stu-id="089e5-112">A COM string that contains the pathname of the .dds file where results are written.</span></span>

<span data-ttu-id="089e5-113">*pRequestCallback* </span><span class="sxs-lookup"><span data-stu-id="089e5-113">*pRequestCallback* </span></span>  
<span data-ttu-id="089e5-114">Dirección de devolución de llamada que se utiliza para notificar al host los resultados.</span><span class="sxs-lookup"><span data-stu-id="089e5-114">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="089e5-115">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="089e5-115">*requestCookie* </span></span>  
<span data-ttu-id="089e5-116">Cookie que identifica de forma única la solicitud y que se puede usar para indicar que se va a cancelar.</span><span class="sxs-lookup"><span data-stu-id="089e5-116">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="089e5-117">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="089e5-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="089e5-118">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="089e5-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="089e5-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="089e5-119">Return value</span></span>

<span data-ttu-id="089e5-120">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="089e5-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="089e5-121">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="089e5-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="089e5-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="089e5-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="089e5-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="089e5-123">Header</span></span></p></td><td><span data-ttu-id="089e5-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="089e5-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="089e5-125"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="089e5-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="089e5-126">**ITextureRequest**</span><span class="sxs-lookup"><span data-stu-id="089e5-126">**ITextureRequest**</span></span>](/windows/desktop/direct3dtools/itexturerequest)

 

 
