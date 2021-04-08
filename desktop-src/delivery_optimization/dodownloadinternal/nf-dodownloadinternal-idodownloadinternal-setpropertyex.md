---
title: 'IDODownloadInternal:: SetPropertyEx (método)'
description: Establece una propiedad de descarga extendida. El método acepta un puntero a una **variante** que contiene un valor de propiedad específico que se va a aplicar a la descarga.
keywords:
- 'IDODownloadInternal:: SetPropertyEx (método)'
topic_type:
- apiref
api_name:
- IDODownloadInternal.SetPropertyEx
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: e6630cc3e767531dd94da39fe73d88284c9ca0d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995304"
---
# <a name="idodownloadinternalsetpropertyex-method"></a><span data-ttu-id="90b49-105">IDODownloadInternal:: SetPropertyEx (método)</span><span class="sxs-lookup"><span data-stu-id="90b49-105">IDODownloadInternal::SetPropertyEx method</span></span>

> [!IMPORTANT]
> <span data-ttu-id="90b49-106">La interfaz **IDODownloadInternal** está en desuso.</span><span class="sxs-lookup"><span data-stu-id="90b49-106">The **IDODownloadInternal** interface is deprecated.</span></span> <span data-ttu-id="90b49-107">En su lugar, use la interfaz [IDODownload](../do/nn-do-idodownload.md) .</span><span class="sxs-lookup"><span data-stu-id="90b49-107">Instead, use the [IDODownload](../do/nn-do-idodownload.md) interface.</span></span>

<span data-ttu-id="90b49-108">Establece una propiedad de descarga extendida.</span><span class="sxs-lookup"><span data-stu-id="90b49-108">Sets an extended download property.</span></span> <span data-ttu-id="90b49-109">El método acepta un puntero a una **variante** que contiene un valor de propiedad específico que se va a aplicar a la descarga.</span><span class="sxs-lookup"><span data-stu-id="90b49-109">The method accepts a pointer to a **VARIANT** that contains a specific property value to apply to the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="90b49-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="90b49-110">Syntax</span></span>

```cpp
HRESULT SetPropertyEx(
  DODownloadPropertyEx propId, 
  VARIANT* propVal
);
```

## <a name="parameters"></a><span data-ttu-id="90b49-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="90b49-111">Parameters</span></span>

`propId`

<span data-ttu-id="90b49-112">IDENTIFICADOR de propiedad necesario que se va a establecer (de tipo **DODownloadPropertyEx**).</span><span class="sxs-lookup"><span data-stu-id="90b49-112">The required property ID to set (of type **DODownloadPropertyEx**).</span></span>

`propVal`

<span data-ttu-id="90b49-113">Valor de propiedad que se va a establecer, almacenado en una **variante**.</span><span class="sxs-lookup"><span data-stu-id="90b49-113">The property value to set, stored in a **VARIANT**.</span></span>

## <a name="return-value"></a><span data-ttu-id="90b49-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="90b49-114">Return Value</span></span>

<span data-ttu-id="90b49-115">Si la función se ejecuta correctamente, devuelve **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="90b49-115">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="90b49-116">De lo contrario, devuelve un [código de error](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .</span><span class="sxs-lookup"><span data-stu-id="90b49-116">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

|<span data-ttu-id="90b49-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="90b49-117">Return value</span></span>|<span data-ttu-id="90b49-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="90b49-118">Description</span></span>|
|-|-|
|<span data-ttu-id="90b49-119">DO_E_UNKNOWN_PROPERTY_ID</span><span class="sxs-lookup"><span data-stu-id="90b49-119">DO_E_UNKNOWN_PROPERTY_ID</span></span>|<span data-ttu-id="90b49-120">se desconoce el *propId* .</span><span class="sxs-lookup"><span data-stu-id="90b49-120">*propId* is unknown.</span></span>|
|<span data-ttu-id="90b49-121">DO_E_INVALID_STATE</span><span class="sxs-lookup"><span data-stu-id="90b49-121">DO_E_INVALID_STATE</span></span>|<span data-ttu-id="90b49-122">La descarga no está actualmente en un estado que permita establecer propiedades.</span><span class="sxs-lookup"><span data-stu-id="90b49-122">The download is not currently in a state that allows setting properties.</span></span>|

## <a name="requirements"></a><span data-ttu-id="90b49-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90b49-123">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="90b49-124">**Cliente mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="90b49-124">**Minimum supported client**</span></span> | <span data-ttu-id="90b49-125">Solo aplicaciones Win32 de Windows 10, versión 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="90b49-125">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="90b49-126">**Servidor mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="90b49-126">**Minimum supported server**</span></span> | <span data-ttu-id="90b49-127">Windows Server, versión 1809 \[ Win32 Applications Only\]</span><span class="sxs-lookup"><span data-stu-id="90b49-127">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="90b49-128">**Header**</span><span class="sxs-lookup"><span data-stu-id="90b49-128">**Header**</span></span> | <span data-ttu-id="90b49-129">DODownloadInternal. h</span><span class="sxs-lookup"><span data-stu-id="90b49-129">DODownloadInternal.h</span></span> |