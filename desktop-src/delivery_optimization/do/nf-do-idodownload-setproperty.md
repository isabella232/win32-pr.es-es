---
title: 'IDODownload:: SetProperty (método)'
description: Establece una propiedad de descarga.
keywords:
- 'IDODownload:: SetProperty (método)'
topic_type:
- apiref
api_name:
- IDODownload.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 0d496f49851aab665e49f3aaeb51e4b941d6c183
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "103785099"
---
# <a name="idodownloadsetproperty-method"></a><span data-ttu-id="98023-104">IDODownload:: SetProperty (método)</span><span class="sxs-lookup"><span data-stu-id="98023-104">IDODownload::SetProperty method</span></span>

<span data-ttu-id="98023-105">Establece una propiedad de descarga.</span><span class="sxs-lookup"><span data-stu-id="98023-105">Sets a download property.</span></span> <span data-ttu-id="98023-106">El método acepta un puntero a una **variante** que contiene una propiedad específica que se va a aplicar a la descarga.</span><span class="sxs-lookup"><span data-stu-id="98023-106">The method accepts a pointer to a **VARIANT** that contains a specific property to apply to the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="98023-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="98023-107">Syntax</span></span>

```cpp
HRESULT SetProperty(
  DODownloadProperty propId,
  VARIANT* propVal
);
```

## <a name="parameters"></a><span data-ttu-id="98023-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="98023-108">Parameters</span></span>

`propId`

<span data-ttu-id="98023-109">IDENTIFICADOR de propiedad necesario que se va a establecer (de tipo **DODownloadProperty**).</span><span class="sxs-lookup"><span data-stu-id="98023-109">The required property ID to set (of type **DODownloadProperty**).</span></span>

`propVal`

<span data-ttu-id="98023-110">Valor de propiedad que se va a establecer, almacenado en una **variante**.</span><span class="sxs-lookup"><span data-stu-id="98023-110">The property value to set, stored in a **VARIANT**.</span></span>

## <a name="return-value"></a><span data-ttu-id="98023-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="98023-111">Return Value</span></span>

<span data-ttu-id="98023-112">Si la función se ejecuta correctamente, devuelve **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="98023-112">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="98023-113">De lo contrario, devuelve un [código de error](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .</span><span class="sxs-lookup"><span data-stu-id="98023-113">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

|<span data-ttu-id="98023-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="98023-114">Return value</span></span>|<span data-ttu-id="98023-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="98023-115">Description</span></span>|
|-|-|
|<span data-ttu-id="98023-116">DO_E_UNKNOWN_PROPERTY_ID</span><span class="sxs-lookup"><span data-stu-id="98023-116">DO_E_UNKNOWN_PROPERTY_ID</span></span>|<span data-ttu-id="98023-117">se desconoce el *propId* .</span><span class="sxs-lookup"><span data-stu-id="98023-117">*propId* is unknown.</span></span>|
|<span data-ttu-id="98023-118">DO_E_INVALID_STATE</span><span class="sxs-lookup"><span data-stu-id="98023-118">DO_E_INVALID_STATE</span></span>|<span data-ttu-id="98023-119">La descarga no está actualmente en un estado que permita establecer propiedades.</span><span class="sxs-lookup"><span data-stu-id="98023-119">The download is not currently in a state that allows setting properties.</span></span>|

## <a name="requirements"></a><span data-ttu-id="98023-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98023-120">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="98023-121">**Cliente mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="98023-121">**Minimum supported client**</span></span> | <span data-ttu-id="98023-122">Solo aplicaciones Win32 de Windows 10, versión 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="98023-122">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="98023-123">**Servidor mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="98023-123">**Minimum supported server**</span></span> | <span data-ttu-id="98023-124">Windows Server, versión 1809 \[ Win32 Applications Only\]</span><span class="sxs-lookup"><span data-stu-id="98023-124">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="98023-125">**Header**</span><span class="sxs-lookup"><span data-stu-id="98023-125">**Header**</span></span> | <span data-ttu-id="98023-126">Do. h</span><span class="sxs-lookup"><span data-stu-id="98023-126">Do.h</span></span> |
