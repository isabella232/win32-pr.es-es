---
title: Estructura de DO_DOWNLOAD_ENUM_CATEGORY
description: 'Lo usa **IDOManager:: EnumDownloads** para filtrar la enumeración downloads por el valor de la propiedad específica.'
keywords:
- Estructura de DO_DOWNLOAD_ENUM_CATEGORY
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_ENUM_CATEGORY
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: a78c94cd9d8854453517976300e12a031f65b8cb
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "105720103"
---
# <a name="do_download_enum_category-structure"></a><span data-ttu-id="c16ef-104">Estructura de DO_DOWNLOAD_ENUM_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="c16ef-104">DO_DOWNLOAD_ENUM_CATEGORY structure</span></span>

<span data-ttu-id="c16ef-105">**IDOManager:: EnumDownloads** usa la estructura **DO_DOWNLOAD_ENUM_CATEGORY** para filtrar la enumeración downloads por el valor de la propiedad específica.</span><span class="sxs-lookup"><span data-stu-id="c16ef-105">The **DO_DOWNLOAD_ENUM_CATEGORY** structure is used by **IDOManager::EnumDownloads** to filter the downloads enumeration by the specific property's value.</span></span>

## <a name="syntax"></a><span data-ttu-id="c16ef-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c16ef-106">Syntax</span></span>
```cpp
typedef struct _DO_DOWNLOAD_ENUM_CATEGORY
{
  DODownloadProperty Property;
  LPCWSTR Value;
} DO_DOWNLOAD_ENUM_CATEGORY;
```

## <a name="members"></a><span data-ttu-id="c16ef-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="c16ef-107">Members</span></span>

`Property`

<span data-ttu-id="c16ef-108">Nombre de propiedad que se va a utilizar para la enumeración de descarga.</span><span class="sxs-lookup"><span data-stu-id="c16ef-108">The property name to be used for the download enumeration.</span></span> <span data-ttu-id="c16ef-109">Estas propiedades se admiten para la enumeración.</span><span class="sxs-lookup"><span data-stu-id="c16ef-109">These properties are supported for enumeration purposes.</span></span>
- <span data-ttu-id="c16ef-110">**DODownloadProperty_Id**</span><span class="sxs-lookup"><span data-stu-id="c16ef-110">**DODownloadProperty_Id**</span></span>
- <span data-ttu-id="c16ef-111">**DODownloadProperty_Uri**</span><span class="sxs-lookup"><span data-stu-id="c16ef-111">**DODownloadProperty_Uri**</span></span>
- <span data-ttu-id="c16ef-112">**DODownloadProperty_ContentId**</span><span class="sxs-lookup"><span data-stu-id="c16ef-112">**DODownloadProperty_ContentId**</span></span>
- <span data-ttu-id="c16ef-113">**DODownloadProperty_DisplayName**</span><span class="sxs-lookup"><span data-stu-id="c16ef-113">**DODownloadProperty_DisplayName**</span></span>
- <span data-ttu-id="c16ef-114">**DODownloadProperty_LocalPath**</span><span class="sxs-lookup"><span data-stu-id="c16ef-114">**DODownloadProperty_LocalPath**</span></span>

`Value`

<span data-ttu-id="c16ef-115">Valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="c16ef-115">The property's value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c16ef-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c16ef-116">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="c16ef-117">**Cliente mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="c16ef-117">**Minimum supported client**</span></span> | <span data-ttu-id="c16ef-118">Solo aplicaciones Win32 de Windows 10, versión 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="c16ef-118">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="c16ef-119">**Servidor mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="c16ef-119">**Minimum supported server**</span></span> | <span data-ttu-id="c16ef-120">Windows Server, versión 1809 \[ Win32 Applications Only\]</span><span class="sxs-lookup"><span data-stu-id="c16ef-120">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="c16ef-121">**Header**</span><span class="sxs-lookup"><span data-stu-id="c16ef-121">**Header**</span></span> | <span data-ttu-id="c16ef-122">Do. h</span><span class="sxs-lookup"><span data-stu-id="c16ef-122">Do.h</span></span> |
