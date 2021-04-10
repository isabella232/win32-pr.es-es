---
description: Solicita que obtenga el contenido de una textura en mosaico como. Archivo DDS (DirectDraw Surface).
MS-HAID: vspixengine.ITileRequest\_RequestTextureTileAsync\_EventID\_DWORD\_UINT\_UINT\_UINT\_UINT\_BSTR\_ITextureCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'ITileRequest:: RequestTextureTileAsync (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E3F4FAC2-E7D9-4FDF-BE64-73D3EA175A8F
api_name:
- ITileRequest.RequestTextureTileAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e22c3b54c1e04242805d698c37a1d4dd2709fa0b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152399"
---
# <a name="span-idvspixengineitilerequest_requesttexturetileasync_eventid_dword_uint_uint_uint_uint_bstr_itexturecallback_ptr_dword_dwordspanitilerequestrequesttexturetileasync-method"></a><span data-ttu-id="88cdd-103"><span id="vspixengine.itilerequest_requesttexturetileasync_eventid_dword_uint_uint_uint_uint_bstr_itexturecallback_ptr_dword_dword"></span>ITileRequest:: RequestTextureTileAsync (método)</span><span class="sxs-lookup"><span data-stu-id="88cdd-103"><span id="vspixengine.itilerequest_requesttexturetileasync_eventid_dword_uint_uint_uint_uint_bstr_itexturecallback_ptr_dword_dword"></span>ITileRequest::RequestTextureTileAsync method</span></span>

<span data-ttu-id="88cdd-104">Solicita que obtenga el contenido de una textura en mosaico como. Archivo DDS (DirectDraw Surface).</span><span class="sxs-lookup"><span data-stu-id="88cdd-104">Requests to get the contents of a tiled texture as a .DDS (DirectDraw Surface) file.</span></span>

## <a name="syntax"></a><span data-ttu-id="88cdd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="88cdd-105">Syntax</span></span>


```C++
HRESULT RequestTextureTileAsync(
   EventID            eventID,
   DWORD              textureFileptr,
   UINT               tileSubresource,
   UINT               tileX,
   UINT               tileY,
   UINT               tileZ,
   BSTR               ddsFilename,
   ITextureCallback * pRequestCallback,
   DWORD              requestCookie,
   DWORD              progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="88cdd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="88cdd-106">Parameters</span></span>

<span data-ttu-id="88cdd-107">*eventID* </span><span class="sxs-lookup"><span data-stu-id="88cdd-107">*eventID* </span></span>  
<span data-ttu-id="88cdd-108">Evento especificado con el que se va a hacer coincidir el contenido del búfer (por ejemplo, un destino de representación podría cambiar con el tiempo).</span><span class="sxs-lookup"><span data-stu-id="88cdd-108">The specified event to match the buffer's content to (for example, a render target could change over time).</span></span>

<span data-ttu-id="88cdd-109">*textureFileptr* </span><span class="sxs-lookup"><span data-stu-id="88cdd-109">*textureFileptr* </span></span>  
<span data-ttu-id="88cdd-110">Dirección del objeto de textura especificado.</span><span class="sxs-lookup"><span data-stu-id="88cdd-110">The address of the specified texture object.</span></span>

<span data-ttu-id="88cdd-111">*tileSubresource* </span><span class="sxs-lookup"><span data-stu-id="88cdd-111">*tileSubresource* </span></span>  
<span data-ttu-id="88cdd-112">Subrecurso especificado del mosaico.</span><span class="sxs-lookup"><span data-stu-id="88cdd-112">The specified subresource of the tile.</span></span>

<span data-ttu-id="88cdd-113">*tileX* </span><span class="sxs-lookup"><span data-stu-id="88cdd-113">*tileX* </span></span>  
<span data-ttu-id="88cdd-114">Posición X del mosaico especificado.</span><span class="sxs-lookup"><span data-stu-id="88cdd-114">The specified tile X position.</span></span>

<span data-ttu-id="88cdd-115">*en mosaico* </span><span class="sxs-lookup"><span data-stu-id="88cdd-115">*tileY* </span></span>  
<span data-ttu-id="88cdd-116">Posición Y de mosaico especificada.</span><span class="sxs-lookup"><span data-stu-id="88cdd-116">The specified tile Y position.</span></span>

<span data-ttu-id="88cdd-117">*tileZ* </span><span class="sxs-lookup"><span data-stu-id="88cdd-117">*tileZ* </span></span>  
<span data-ttu-id="88cdd-118">Posición Z del mosaico especificado.</span><span class="sxs-lookup"><span data-stu-id="88cdd-118">The specified tile Z position.</span></span>

<span data-ttu-id="88cdd-119">*ddsFilename* </span><span class="sxs-lookup"><span data-stu-id="88cdd-119">*ddsFilename* </span></span>  
<span data-ttu-id="88cdd-120">Cadena COM que contiene la ruta de acceso del archivo. DDS donde se escriben los resultados.</span><span class="sxs-lookup"><span data-stu-id="88cdd-120">A COM string that contains the pathname of the .dds file where results are written.</span></span>

<span data-ttu-id="88cdd-121">*pRequestCallback* </span><span class="sxs-lookup"><span data-stu-id="88cdd-121">*pRequestCallback* </span></span>  
<span data-ttu-id="88cdd-122">Dirección de devolución de llamada que se utiliza para notificar al host los resultados.</span><span class="sxs-lookup"><span data-stu-id="88cdd-122">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="88cdd-123">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="88cdd-123">*requestCookie* </span></span>  
<span data-ttu-id="88cdd-124">Cookie que identifica de forma única la solicitud y que se puede usar para indicar que se va a cancelar.</span><span class="sxs-lookup"><span data-stu-id="88cdd-124">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="88cdd-125">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="88cdd-125">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="88cdd-126">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="88cdd-126">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="88cdd-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="88cdd-127">Return value</span></span>

<span data-ttu-id="88cdd-128">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="88cdd-128">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="88cdd-129">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="88cdd-129">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="88cdd-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88cdd-130">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="88cdd-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="88cdd-131">Header</span></span></p></td><td><span data-ttu-id="88cdd-132">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="88cdd-132">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="88cdd-133"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="88cdd-133"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="88cdd-134">**ITileRequest**</span><span class="sxs-lookup"><span data-stu-id="88cdd-134">**ITileRequest**</span></span>](/windows/desktop/direct3dtools/itilerequest)

 

 
