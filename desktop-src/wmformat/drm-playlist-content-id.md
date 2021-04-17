---
title: DRM_PLAYLIST_CONTENT_ID estructura (Drmexternals. h)
description: La \_ estructura de \_ ID. de contenido de la lista de reproducción DRM \_ contiene información sobre el contenido que se va a copiar en el CD como parte de la grabación de una lista de reproducción.
ms.assetid: 124e86ac-b0d4-40b2-868b-fe2fed1898e1
keywords:
- DRM_PLAYLIST_CONTENT_ID estructura de Windows Media Format
- Formato de Windows Media de estructura
topic_type:
- apiref
api_name:
- DRM_PLAYLIST_CONTENT_ID
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f475a8c3620ff1af64cb70914ca1ac591aa55106
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105705160"
---
# <a name="drm_playlist_content_id-structure"></a><span data-ttu-id="220bc-105">\_Estructura de \_ \_ ID. de contenido de lista de reproducción DRM</span><span class="sxs-lookup"><span data-stu-id="220bc-105">DRM\_PLAYLIST\_CONTENT\_ID structure</span></span>

<span data-ttu-id="220bc-106">La estructura de **\_ \_ \_ ID. de contenido de la lista de reproducción DRM** contiene información sobre el contenido que se va a copiar en el CD como parte de la grabación de una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="220bc-106">The **DRM\_PLAYLIST\_CONTENT\_ID** structure contains information about content that is to be copied to CD as part of a playlist burn.</span></span>

## <a name="syntax"></a><span data-ttu-id="220bc-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="220bc-107">Syntax</span></span>


```C++
typedef struct DRM_PLAYLIST_CONTENT_ID {
  LPCWSTR lpcwszV2Header;
  LPCSTR  lpcszV1KID;
  BYTE    *pbOtherData;
  DWORD   cbOtherData;
  DWORD   dwUniqueIDForSession;
  DWORD   dwValidFields;
} ;
```



## <a name="members"></a><span data-ttu-id="220bc-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="220bc-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="220bc-109">**lpcwszV2Header**</span><span class="sxs-lookup"><span data-stu-id="220bc-109">**lpcwszV2Header**</span></span>
</dt> <dd>

<span data-ttu-id="220bc-110">Encabezado DRM.</span><span class="sxs-lookup"><span data-stu-id="220bc-110">DRM header.</span></span> <span data-ttu-id="220bc-111">Utilice este miembro si el contenido está protegido por la versión 2 o posterior de DRM de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="220bc-111">Use this member if the content is protected by Windows Media DRM version 2 or later.</span></span>

</dd> <dt>

<span data-ttu-id="220bc-112">**lpcszV1KID**</span><span class="sxs-lookup"><span data-stu-id="220bc-112">**lpcszV1KID**</span></span>
</dt> <dd>

<span data-ttu-id="220bc-113">El identificador de la clave.</span><span class="sxs-lookup"><span data-stu-id="220bc-113">Key ID.</span></span> <span data-ttu-id="220bc-114">Utilice este miembro si el contenido está protegido por la versión 1 de DRM de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="220bc-114">Use this member if the content is protected by Windows Media DRM version 1.</span></span>

</dd> <dt>

<span data-ttu-id="220bc-115">**pbOtherData**</span><span class="sxs-lookup"><span data-stu-id="220bc-115">**pbOtherData**</span></span>
</dt> <dd>

<span data-ttu-id="220bc-116">Búfer que contiene datos complementarios.</span><span class="sxs-lookup"><span data-stu-id="220bc-116">Buffer containing supplementary data.</span></span>

</dd> <dt>

<span data-ttu-id="220bc-117">**cbOtherData**</span><span class="sxs-lookup"><span data-stu-id="220bc-117">**cbOtherData**</span></span>
</dt> <dd>

<span data-ttu-id="220bc-118">Tamaño del búfer de **pbOtherData** en bytes.</span><span class="sxs-lookup"><span data-stu-id="220bc-118">Size of the **pbOtherData** buffer in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="220bc-119">**dwUniqueIDForSession**</span><span class="sxs-lookup"><span data-stu-id="220bc-119">**dwUniqueIDForSession**</span></span>
</dt> <dd>

<span data-ttu-id="220bc-120">Identificador único para el contenido que se va a usar en la sesión actual.</span><span class="sxs-lookup"><span data-stu-id="220bc-120">Unique identifier for the content to be used in the current session.</span></span>

</dd> <dt>

<span data-ttu-id="220bc-121">**dwValidFields**</span><span class="sxs-lookup"><span data-stu-id="220bc-121">**dwValidFields**</span></span>
</dt> <dd>

<span data-ttu-id="220bc-122">**DWORD** que indica los campos válidos de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="220bc-122">**DWORD** indicating the valid fields of this structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="220bc-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="220bc-123">Requirements</span></span>



| <span data-ttu-id="220bc-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="220bc-124">Requirement</span></span> | <span data-ttu-id="220bc-125">Value</span><span class="sxs-lookup"><span data-stu-id="220bc-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="220bc-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="220bc-126">Minimum supported client</span></span><br/> | <span data-ttu-id="220bc-127">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="220bc-127">Windows XP \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="220bc-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="220bc-128">Minimum supported server</span></span><br/> | <span data-ttu-id="220bc-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="220bc-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="220bc-130">Versión</span><span class="sxs-lookup"><span data-stu-id="220bc-130">Version</span></span><br/>                  | <span data-ttu-id="220bc-131">SDK de Windows Media Format 11</span><span class="sxs-lookup"><span data-stu-id="220bc-131">Windows Media Format 11 SDK</span></span><br/>                                                    |
| <span data-ttu-id="220bc-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="220bc-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="220bc-133"><dt>Drmexternals. h</dt></span><span class="sxs-lookup"><span data-stu-id="220bc-133"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="220bc-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="220bc-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="220bc-135">**Estructuras**</span><span class="sxs-lookup"><span data-stu-id="220bc-135">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





