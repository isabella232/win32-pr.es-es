---
title: 'IDODownloadInternal:: GetPropertyEx (método)'
description: Recupera un puntero a una **variante** que contiene un valor de propiedad de descarga extendida específico.
keywords:
- 'IDODownloadInternal:: GetPropertyEx (método)'
topic_type:
- apiref
api_name:
- IDODownloadInternal.GetPropertyEx
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: 908f9b15df5c0c4a2769149419ff12d545201e5c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420974"
---
# <a name="idodownloadinternalgetpropertyex-method"></a><span data-ttu-id="3c4cf-104">IDODownloadInternal:: GetPropertyEx (método)</span><span class="sxs-lookup"><span data-stu-id="3c4cf-104">IDODownloadInternal::GetPropertyEx method</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3c4cf-105">La interfaz **IDODownloadInternal** está en desuso.</span><span class="sxs-lookup"><span data-stu-id="3c4cf-105">The **IDODownloadInternal** interface is deprecated.</span></span> <span data-ttu-id="3c4cf-106">En su lugar, use la interfaz [IDODownload](../do/nn-do-idodownload.md) .</span><span class="sxs-lookup"><span data-stu-id="3c4cf-106">Instead, use the [IDODownload](../do/nn-do-idodownload.md) interface.</span></span>

<span data-ttu-id="3c4cf-107">Recupera un puntero a una **variante** que contiene un valor de propiedad de descarga extendida específico.</span><span class="sxs-lookup"><span data-stu-id="3c4cf-107">Retrieves a pointer to a **VARIANT** that contains a specific extended download property value.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c4cf-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3c4cf-108">Syntax</span></span>

```cpp
HRESULT GetPropertyEx(
  DODownloadPropertyEx propId, 
  VARIANT* propVal
);
```

## <a name="parameters"></a><span data-ttu-id="3c4cf-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3c4cf-109">Parameters</span></span>

`propId`

<span data-ttu-id="3c4cf-110">IDENTIFICADOR de propiedad necesario que se va a obtener (de tipo **DODownloadPropertyEx**).</span><span class="sxs-lookup"><span data-stu-id="3c4cf-110">The required property ID to get (of type **DODownloadPropertyEx**).</span></span>

`propVal`

<span data-ttu-id="3c4cf-111">Valor de propiedad resultante, almacenado en una **variante**.</span><span class="sxs-lookup"><span data-stu-id="3c4cf-111">The resulting property value, stored in a **VARIANT**.</span></span>

## <a name="return-value"></a><span data-ttu-id="3c4cf-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3c4cf-112">Return Value</span></span>

<span data-ttu-id="3c4cf-113">Si la función se ejecuta correctamente, devuelve **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="3c4cf-113">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="3c4cf-114">De lo contrario, devuelve un [código de error](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .</span><span class="sxs-lookup"><span data-stu-id="3c4cf-114">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

|<span data-ttu-id="3c4cf-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3c4cf-115">Return value</span></span>|<span data-ttu-id="3c4cf-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="3c4cf-116">Description</span></span>|
|-|-|
|<span data-ttu-id="3c4cf-117">DO_E_UNKNOWN_PROPERTY_ID</span><span class="sxs-lookup"><span data-stu-id="3c4cf-117">DO_E_UNKNOWN_PROPERTY_ID</span></span>|<span data-ttu-id="3c4cf-118">se desconoce el *propId* .</span><span class="sxs-lookup"><span data-stu-id="3c4cf-118">*propId* is unknown.</span></span>|
|<span data-ttu-id="3c4cf-119">DO_E_WRITE_ONLY_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="3c4cf-119">DO_E_WRITE_ONLY_PROPERTY</span></span>|<span data-ttu-id="3c4cf-120">La propiedad es de solo escritura y no se puede leer.</span><span class="sxs-lookup"><span data-stu-id="3c4cf-120">The property is write-only, and cannot be read.</span></span>|
|<span data-ttu-id="3c4cf-121">E_NOT_SET</span><span class="sxs-lookup"><span data-stu-id="3c4cf-121">E_NOT_SET</span></span>|<span data-ttu-id="3c4cf-122">No se estableció esta propiedad a través de **SetPropertyEx**.</span><span class="sxs-lookup"><span data-stu-id="3c4cf-122">No such property was set via **SetPropertyEx**.</span></span>|

## <a name="requirements"></a><span data-ttu-id="3c4cf-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c4cf-123">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="3c4cf-124">**Cliente mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="3c4cf-124">**Minimum supported client**</span></span> | <span data-ttu-id="3c4cf-125">Solo aplicaciones Win32 de Windows 10, versión 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="3c4cf-125">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="3c4cf-126">**Servidor mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="3c4cf-126">**Minimum supported server**</span></span> | <span data-ttu-id="3c4cf-127">Windows Server, versión 1809 \[ Win32 Applications Only\]</span><span class="sxs-lookup"><span data-stu-id="3c4cf-127">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="3c4cf-128">**Header**</span><span class="sxs-lookup"><span data-stu-id="3c4cf-128">**Header**</span></span> | <span data-ttu-id="3c4cf-129">DODownloadInternal. h</span><span class="sxs-lookup"><span data-stu-id="3c4cf-129">DODownloadInternal.h</span></span> |