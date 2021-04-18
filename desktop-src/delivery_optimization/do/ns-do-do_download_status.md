---
title: Estructura de DO_DOWNLOAD_STATUS
description: Se usa para obtener el estado de una descarga específica.
keywords:
- Estructura de DO_DOWNLOAD_STATUS
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_STATUS
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 5e113bb4866ef1033886dbb1579d21aa296d0e5e
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "105720101"
---
# <a name="do_download_status-structure"></a><span data-ttu-id="82600-104">Estructura de DO_DOWNLOAD_STATUS</span><span class="sxs-lookup"><span data-stu-id="82600-104">DO_DOWNLOAD_STATUS structure</span></span>

<span data-ttu-id="82600-105">La estructura de **DO_DOWNLOAD_STATUS** se utiliza para obtener el estado de una descarga específica.</span><span class="sxs-lookup"><span data-stu-id="82600-105">The **DO_DOWNLOAD_STATUS** structure is used to obtain the status of a specific download.</span></span> <span data-ttu-id="82600-106">Se obtiene mediante una llamada a la función **IDODownload:: getStatus** .</span><span class="sxs-lookup"><span data-stu-id="82600-106">It is obtained by calling the **IDODownload::GetStatus** function.</span></span>

## <a name="syntax"></a><span data-ttu-id="82600-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="82600-107">Syntax</span></span>
```cpp
typedef struct _DO_DOWNLOAD_STATUS
{
  UINT64 BytesTotal;
  UINT64 BytesTransferred;
  DODownloadState State;
  HRESULT Error;
  HRESULT ExtendedError;
} DO_DOWNLOAD_STATUS;
```

## <a name="members"></a><span data-ttu-id="82600-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="82600-108">Members</span></span>

`BytesTotal`

<span data-ttu-id="82600-109">Número total de bytes que se van a descargar.</span><span class="sxs-lookup"><span data-stu-id="82600-109">The total number of bytes to download.</span></span>

`BytesTransferred`

<span data-ttu-id="82600-110">Número de bytes que ya se han descargado.</span><span class="sxs-lookup"><span data-stu-id="82600-110">The number of bytes that have already been downloaded.</span></span>

`State`

<span data-ttu-id="82600-111">Estado de descarga actual tal y como se define en la enumeración **DODownloadState** .</span><span class="sxs-lookup"><span data-stu-id="82600-111">The current download state as defined by the **DODownloadState** enumeration.</span></span>

`Error`

<span data-ttu-id="82600-112">La información de error (si existe) que está asociada a la descarga actual.</span><span class="sxs-lookup"><span data-stu-id="82600-112">The error information (if it exists) that is associated with the current download.</span></span>

`ExtendedError`

<span data-ttu-id="82600-113">La información de error extendida (si existe) que está asociada a la descarga actual.</span><span class="sxs-lookup"><span data-stu-id="82600-113">The extended error information (if it exists) that is associated with the current download.</span></span>

## <a name="requirements"></a><span data-ttu-id="82600-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82600-114">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="82600-115">**Cliente mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="82600-115">**Minimum supported client**</span></span> | <span data-ttu-id="82600-116">Solo aplicaciones Win32 de Windows 10, versión 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="82600-116">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="82600-117">**Servidor mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="82600-117">**Minimum supported server**</span></span> | <span data-ttu-id="82600-118">Windows Server, versión 1809 \[ Win32 Applications Only\]</span><span class="sxs-lookup"><span data-stu-id="82600-118">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="82600-119">**Header**</span><span class="sxs-lookup"><span data-stu-id="82600-119">**Header**</span></span> | <span data-ttu-id="82600-120">Do. h</span><span class="sxs-lookup"><span data-stu-id="82600-120">Do.h</span></span> |
