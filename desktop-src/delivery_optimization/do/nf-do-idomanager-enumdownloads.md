---
title: 'IDOManager:: EnumDownloads (método)'
description: Recupera un puntero de interfaz a un objeto de enumerador que se usa para enumerar las descargas existentes.
keywords:
- 'IDOManager:: EnumDownloads (método)'
topic_type:
- apiref
api_name:
- IDOManager.EnumDownloads
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: a1e7fed2955fdc1b5ac0c11cfebc34aa95517603
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "105720105"
---
# <a name="idomanagerenumdownloads-method"></a><span data-ttu-id="0a7bd-104">IDOManager:: EnumDownloads (método)</span><span class="sxs-lookup"><span data-stu-id="0a7bd-104">IDOManager::EnumDownloads method</span></span>

<span data-ttu-id="0a7bd-105">Recupera un puntero de interfaz a un objeto de enumerador que se usa para enumerar las descargas existentes.</span><span class="sxs-lookup"><span data-stu-id="0a7bd-105">Retrieves an interface pointer to an enumerator object that is used to enumerate existing downloads.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a7bd-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0a7bd-106">Syntax</span></span>

```cpp
HRESULT EnumDownloads(
  DO_DOWNLOAD_ENUM_CATEGORY *category, 
  IEnumUnknown **ppEnum
);
```

## <a name="parameters"></a><span data-ttu-id="0a7bd-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0a7bd-107">Parameters</span></span>

`category`

<span data-ttu-id="0a7bd-108">Opcional.</span><span class="sxs-lookup"><span data-stu-id="0a7bd-108">Optional.</span></span> <span data-ttu-id="0a7bd-109">Nombre de la propiedad que se va a utilizar como categoría que se va a enumerar.</span><span class="sxs-lookup"><span data-stu-id="0a7bd-109">The property name to be used as a category to enumerate.</span></span> <span data-ttu-id="0a7bd-110">Al pasar `nullptr` , se recuperarán todas las descargas existentes.</span><span class="sxs-lookup"><span data-stu-id="0a7bd-110">Passing `nullptr` will retrieve all existing downloads.</span></span> <span data-ttu-id="0a7bd-111">Las siguientes propiedades se admiten como una categoría.</span><span class="sxs-lookup"><span data-stu-id="0a7bd-111">The following properties are supported as a category.</span></span>

- <span data-ttu-id="0a7bd-112">**DODownloadProperty_Id**</span><span class="sxs-lookup"><span data-stu-id="0a7bd-112">**DODownloadProperty_Id**</span></span>
- <span data-ttu-id="0a7bd-113">**DODownloadProperty_Uri**</span><span class="sxs-lookup"><span data-stu-id="0a7bd-113">**DODownloadProperty_Uri**</span></span>
- <span data-ttu-id="0a7bd-114">**DODownloadProperty_ContentId**</span><span class="sxs-lookup"><span data-stu-id="0a7bd-114">**DODownloadProperty_ContentId**</span></span>
- <span data-ttu-id="0a7bd-115">**DODownloadProperty_DisplayName**</span><span class="sxs-lookup"><span data-stu-id="0a7bd-115">**DODownloadProperty_DisplayName**</span></span>
- <span data-ttu-id="0a7bd-116">**DODownloadProperty_LocalPath**</span><span class="sxs-lookup"><span data-stu-id="0a7bd-116">**DODownloadProperty_LocalPath**</span></span>

`ppEnum`

<span data-ttu-id="0a7bd-117">La dirección de un puntero de interfaz a **IEnumUnknown**, que se usa para enumerar las descargas existentes.</span><span class="sxs-lookup"><span data-stu-id="0a7bd-117">The address of an interface pointer to **IEnumUnknown**, which is used to enumerate existing downloads.</span></span> <span data-ttu-id="0a7bd-118">El contenido del enumerador depende del valor de *Category*.</span><span class="sxs-lookup"><span data-stu-id="0a7bd-118">The contents of the enumerator depend on the value of *category*.</span></span> <span data-ttu-id="0a7bd-119">Las descargas incluidas en la interfaz de enumeración son las que crearon previamente el mismo llamador en esta función.</span><span class="sxs-lookup"><span data-stu-id="0a7bd-119">The downloads included in the enumeration interface are the ones that were previously created by the same caller to this function.</span></span> 

## <a name="return-value"></a><span data-ttu-id="0a7bd-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0a7bd-120">Return Value</span></span>

<span data-ttu-id="0a7bd-121">Si la función se ejecuta correctamente, devuelve **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="0a7bd-121">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="0a7bd-122">De lo contrario, devuelve un [código de error](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .</span><span class="sxs-lookup"><span data-stu-id="0a7bd-122">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="0a7bd-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a7bd-123">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="0a7bd-124">**Cliente mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="0a7bd-124">**Minimum supported client**</span></span> | <span data-ttu-id="0a7bd-125">Solo aplicaciones Win32 de Windows 10, versión 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="0a7bd-125">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="0a7bd-126">**Servidor mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="0a7bd-126">**Minimum supported server**</span></span> | <span data-ttu-id="0a7bd-127">Windows Server, versión 1809 \[ Win32 Applications Only\]</span><span class="sxs-lookup"><span data-stu-id="0a7bd-127">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="0a7bd-128">**Header**</span><span class="sxs-lookup"><span data-stu-id="0a7bd-128">**Header**</span></span> | <span data-ttu-id="0a7bd-129">Do. h</span><span class="sxs-lookup"><span data-stu-id="0a7bd-129">Do.h</span></span> |
