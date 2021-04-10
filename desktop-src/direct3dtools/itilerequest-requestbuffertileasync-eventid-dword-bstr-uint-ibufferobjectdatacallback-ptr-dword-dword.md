---
description: Solicita obtener el contenido sin procesar de un icono.
MS-HAID: vspixengine.ITileRequest_RequestBufferTileAsync_EventID_DWORD_BSTR_UINT_IBufferObjectDataCallback_ptr_DWORD_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'ITileRequest:: RequestBufferTileAsync (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2D68766F-1BED-439E-AC51-790471DA4F70
api_name:
- ITileRequest.RequestBufferTileAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 83f013b4bc3235ece2850c75324333e4b59d298f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274801"
---
# <a name="span-idvspixengineitilerequest_requestbuffertileasync_eventid_dword_bstr_uint_ibufferobjectdatacallback_ptr_dword_dwordspanitilerequestrequestbuffertileasync-method"></a><span data-ttu-id="58f6e-103"><span id="vspixengine.itilerequest_requestbuffertileasync_eventid_dword_bstr_uint_ibufferobjectdatacallback_ptr_dword_dword"></span>ITileRequest:: RequestBufferTileAsync (método)</span><span class="sxs-lookup"><span data-stu-id="58f6e-103"><span id="vspixengine.itilerequest_requestbuffertileasync_eventid_dword_bstr_uint_ibufferobjectdatacallback_ptr_dword_dword"></span>ITileRequest::RequestBufferTileAsync method</span></span>

<span data-ttu-id="58f6e-104">Solicita obtener el contenido sin procesar de un icono.</span><span class="sxs-lookup"><span data-stu-id="58f6e-104">Requests to get the raw contents of a tile.</span></span>

## <a name="syntax"></a><span data-ttu-id="58f6e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="58f6e-105">Syntax</span></span>


```C++
HRESULT RequestBufferTileAsync(
   EventID                     eventID,
   DWORD                       RequestedDataUID,
   BSTR                        File,
   UINT                        tileIndex,
   IBufferObjectDataCallback * requestCallback,
   DWORD                       requestCookie,
   DWORD                       progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="58f6e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="58f6e-106">Parameters</span></span>

<span data-ttu-id="58f6e-107">*eventID* </span><span class="sxs-lookup"><span data-stu-id="58f6e-107">*eventID* </span></span>  
<span data-ttu-id="58f6e-108">Evento especificado que debe coincidir con el contenido del icono (por ejemplo, un destino de representación podría cambiar con el tiempo).</span><span class="sxs-lookup"><span data-stu-id="58f6e-108">The specified event to match the tile's content to (for example, a render target could change over time).</span></span>

<span data-ttu-id="58f6e-109">*RequestedDataUID* </span><span class="sxs-lookup"><span data-stu-id="58f6e-109">*RequestedDataUID* </span></span>  
<span data-ttu-id="58f6e-110">Dirección del mosaico especificado.</span><span class="sxs-lookup"><span data-stu-id="58f6e-110">The address of the specified tile.</span></span>

<span data-ttu-id="58f6e-111">*Filesystem* </span><span class="sxs-lookup"><span data-stu-id="58f6e-111">*File* </span></span>  
<span data-ttu-id="58f6e-112">Cadena COM que contiene la ruta de acceso del archivo donde se escriben los resultados.</span><span class="sxs-lookup"><span data-stu-id="58f6e-112">A COM string that contains the pathname of the file where results are written.</span></span>

<span data-ttu-id="58f6e-113">*tileIndex* </span><span class="sxs-lookup"><span data-stu-id="58f6e-113">*tileIndex* </span></span>  
<span data-ttu-id="58f6e-114">Índice del mosaico especificado.</span><span class="sxs-lookup"><span data-stu-id="58f6e-114">The index of the specified tile.</span></span>

<span data-ttu-id="58f6e-115">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="58f6e-115">*requestCallback* </span></span>  
<span data-ttu-id="58f6e-116">Dirección de devolución de llamada que se utiliza para notificar al host los resultados.</span><span class="sxs-lookup"><span data-stu-id="58f6e-116">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="58f6e-117">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="58f6e-117">*requestCookie* </span></span>  
<span data-ttu-id="58f6e-118">Cookie que identifica de forma única la solicitud y que se puede usar para indicar que se va a cancelar.</span><span class="sxs-lookup"><span data-stu-id="58f6e-118">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="58f6e-119">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="58f6e-119">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="58f6e-120">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="58f6e-120">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="58f6e-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="58f6e-121">Return value</span></span>

<span data-ttu-id="58f6e-122">Si este método se ejecuta correctamente, devuelve **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="58f6e-122">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="58f6e-123">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="58f6e-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="58f6e-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58f6e-124">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="58f6e-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="58f6e-125">Header</span></span></p></td><td><span data-ttu-id="58f6e-126">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="58f6e-126">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="58f6e-127"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="58f6e-127"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="58f6e-128">**ITileRequest**</span><span class="sxs-lookup"><span data-stu-id="58f6e-128">**ITileRequest**</span></span>](/windows/desktop/direct3dtools/itilerequest)

 

 
