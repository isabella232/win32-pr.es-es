---
description: Define códigos de error de clave de medios para el motor multimedia.
ms.assetid: F6E13260-74A2-40D0-A704-4E1CDB16B8D8
title: Enumeración MF_MEDIA_ENGINE_KEYERR
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MEDIA_ENGINE_KEYERR
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: 22dd22a7771f5d1e9466709f0b0da9ee936ef2b9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104361868"
---
# <a name="mf_media_engine_keyerr-enumeration"></a><span data-ttu-id="6f446-103">\_ \_ Enumeración de KEYERR del motor multimedia MF \_</span><span class="sxs-lookup"><span data-stu-id="6f446-103">MF\_MEDIA\_ENGINE\_KEYERR enumeration</span></span>

<span data-ttu-id="6f446-104">Define códigos de error de clave de medios para el motor multimedia.</span><span class="sxs-lookup"><span data-stu-id="6f446-104">Defines media key error codes for the media engine.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f446-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6f446-105">Syntax</span></span>


```C++
typedef enum _MF_MEDIA_ENGINE_KEYERR { 
  MF_MEDIAENGINE_KEYERR_UNKNOWN          = 1,
  MF_MEDIAENGINE_KEYERR_CLIENT           = 2,
  MF_MEDIAENGINE_KEYERR_SERVICE          = 3,
  MF_MEDIAENGINE_KEYERR_OUTPUT           = 4,
  MF_MEDIAENGINE_KEYERR_HARDWARECHANGE   = 5,
  MF_MEDIAENGINE_KEYERR_DOMAIN           = 6
} MF_MEDIA_ENGINE_KEYERR;
```



## <a name="constants"></a><span data-ttu-id="6f446-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="6f446-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6f446-107"><span id="MF_MEDIAENGINE_KEYERR_UNKNOWN"></span><span id="mf_mediaengine_keyerr_unknown"></span>**MF \_ MEDIAENGINE \_ KEYERR \_ desconocido**</span><span class="sxs-lookup"><span data-stu-id="6f446-107"><span id="MF_MEDIAENGINE_KEYERR_UNKNOWN"></span><span id="mf_mediaengine_keyerr_unknown"></span>**MF\_MEDIAENGINE\_KEYERR\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="6f446-108">Error desconocido.</span><span class="sxs-lookup"><span data-stu-id="6f446-108">Unknown error occurred.</span></span>

</dd> <dt>

<span data-ttu-id="6f446-109"><span id="MF_MEDIAENGINE_KEYERR_CLIENT"></span><span id="mf_mediaengine_keyerr_client"></span>**\_ \_ cliente KEYERR de MF MEDIAENGINE \_**</span><span class="sxs-lookup"><span data-stu-id="6f446-109"><span id="MF_MEDIAENGINE_KEYERR_CLIENT"></span><span id="mf_mediaengine_keyerr_client"></span>**MF\_MEDIAENGINE\_KEYERR\_CLIENT**</span></span>
</dt> <dd>

<span data-ttu-id="6f446-110">Se produjo un error con el cliente.</span><span class="sxs-lookup"><span data-stu-id="6f446-110">An error with the client occurred.</span></span>

</dd> <dt>

<span data-ttu-id="6f446-111"><span id="MF_MEDIAENGINE_KEYERR_SERVICE"></span><span id="mf_mediaengine_keyerr_service"></span>**\_ \_ servicio KEYERR de MF MEDIAENGINE \_**</span><span class="sxs-lookup"><span data-stu-id="6f446-111"><span id="MF_MEDIAENGINE_KEYERR_SERVICE"></span><span id="mf_mediaengine_keyerr_service"></span>**MF\_MEDIAENGINE\_KEYERR\_SERVICE**</span></span>
</dt> <dd>

<span data-ttu-id="6f446-112">Se produjo un error con el servicio.</span><span class="sxs-lookup"><span data-stu-id="6f446-112">An error with the service occurred.</span></span>

</dd> <dt>

<span data-ttu-id="6f446-113"><span id="MF_MEDIAENGINE_KEYERR_OUTPUT"></span><span id="mf_mediaengine_keyerr_output"></span>**\_ \_ salida KEYERR MEDIAENGINE \_ MF**</span><span class="sxs-lookup"><span data-stu-id="6f446-113"><span id="MF_MEDIAENGINE_KEYERR_OUTPUT"></span><span id="mf_mediaengine_keyerr_output"></span>**MF\_MEDIAENGINE\_KEYERR\_OUTPUT**</span></span>
</dt> <dd>

<span data-ttu-id="6f446-114">Se produjo un error con la salida.</span><span class="sxs-lookup"><span data-stu-id="6f446-114">An error with the output occurred.</span></span>

</dd> <dt>

<span data-ttu-id="6f446-115"><span id="MF_MEDIAENGINE_KEYERR_HARDWARECHANGE_"></span><span id="mf_mediaengine_keyerr_hardwarechange_"></span>**MF \_ MEDIAENGINE \_ KEYERR \_ HARDWARECHANGE**</span><span class="sxs-lookup"><span data-stu-id="6f446-115"><span id="MF_MEDIAENGINE_KEYERR_HARDWARECHANGE_"></span><span id="mf_mediaengine_keyerr_hardwarechange_"></span>**MF\_MEDIAENGINE\_KEYERR\_HARDWARECHANGE**</span></span> 
</dt> <dd>

<span data-ttu-id="6f446-116">Se produjo un error relacionado con un cambio de hardware.</span><span class="sxs-lookup"><span data-stu-id="6f446-116">An error occurred related to a hardware change.</span></span>

</dd> <dt>

<span data-ttu-id="6f446-117"><span id="MF_MEDIAENGINE_KEYERR_DOMAIN"></span><span id="mf_mediaengine_keyerr_domain"></span>**\_ \_ dominio KEYERR de MF MEDIAENGINE \_**</span><span class="sxs-lookup"><span data-stu-id="6f446-117"><span id="MF_MEDIAENGINE_KEYERR_DOMAIN"></span><span id="mf_mediaengine_keyerr_domain"></span>**MF\_MEDIAENGINE\_KEYERR\_DOMAIN**</span></span>
</dt> <dd>

<span data-ttu-id="6f446-118">Se produjo un error con el dominio.</span><span class="sxs-lookup"><span data-stu-id="6f446-118">An error with the domain occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6f446-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6f446-119">Remarks</span></span>

<span data-ttu-id="6f446-120">**MF \_ El \_ motor de \_ KEYERR** se usa con el parámetro de *código* de [**IMFMediaKeySessionNotify:: KeyError**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediakeysessionnotify-keyerror) y el valor de *código* devuelto desde [**IMFMediaKeySession:: GetError**](imfmediakeysession-geterror.md).</span><span class="sxs-lookup"><span data-stu-id="6f446-120">**MF\_MEDIA\_ENGINE\_KEYERR** is used with the *code* parameter of [**IMFMediaKeySessionNotify::KeyError**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediakeysessionnotify-keyerror) and the *code* value returned from [**IMFMediaKeySession::GetError**](imfmediakeysession-geterror.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6f446-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f446-121">Requirements</span></span>



| <span data-ttu-id="6f446-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f446-122">Requirement</span></span> | <span data-ttu-id="6f446-123">Value</span><span class="sxs-lookup"><span data-stu-id="6f446-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f446-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f446-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6f446-125">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="6f446-125">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6f446-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f446-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6f446-127">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="6f446-127">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="6f446-128">IDL</span><span class="sxs-lookup"><span data-stu-id="6f446-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6f446-129"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6f446-129"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f446-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f446-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f446-131">Enumeraciones de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6f446-131">Media Foundation Enumerations</span></span>](media-foundation-enumerations.md)
</dt> </dl>

 

 




