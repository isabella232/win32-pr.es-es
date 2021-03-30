---
title: 'IDODownload:: GetProperty (método)'
description: Recupera un puntero a un **valor de tipo Variant** que contiene una propiedad de descarga específica.
keywords:
- 'IDODownload:: GetProperty (método)'
topic_type:
- apiref
api_name:
- IDODownload.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: e734f109e596663ee699c764ca85f1ee45ad7947
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "103904324"
---
# <a name="idodownloadgetproperty-method"></a><span data-ttu-id="b9cc7-104">IDODownload:: GetProperty (método)</span><span class="sxs-lookup"><span data-stu-id="b9cc7-104">IDODownload::GetProperty method</span></span>

<span data-ttu-id="b9cc7-105">Recupera un puntero a un **valor de tipo Variant** que contiene una propiedad de descarga específica.</span><span class="sxs-lookup"><span data-stu-id="b9cc7-105">Retrieves a pointer to a **VARIANT** that contains a specific download property.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9cc7-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b9cc7-106">Syntax</span></span>

```cpp
HRESULT GetProperty(
  DODownloadProperty propId, 
  VARIANT* propVal
);
```

## <a name="parameters"></a><span data-ttu-id="b9cc7-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b9cc7-107">Parameters</span></span>

`propId`

<span data-ttu-id="b9cc7-108">IDENTIFICADOR de propiedad necesario que se va a obtener (de tipo **DODownloadProperty**).</span><span class="sxs-lookup"><span data-stu-id="b9cc7-108">The required property ID to get (of type **DODownloadProperty**).</span></span>

`propVal`

<span data-ttu-id="b9cc7-109">Valor de propiedad resultante, almacenado en una **variante**.</span><span class="sxs-lookup"><span data-stu-id="b9cc7-109">The resulting property value, stored in a **VARIANT**.</span></span>

## <a name="return-value"></a><span data-ttu-id="b9cc7-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b9cc7-110">Return Value</span></span>

<span data-ttu-id="b9cc7-111">Si la función se ejecuta correctamente, devuelve **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="b9cc7-111">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="b9cc7-112">De lo contrario, devuelve un [código de error](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .</span><span class="sxs-lookup"><span data-stu-id="b9cc7-112">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

|<span data-ttu-id="b9cc7-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b9cc7-113">Return value</span></span>|<span data-ttu-id="b9cc7-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="b9cc7-114">Description</span></span>|
|-|-|
|<span data-ttu-id="b9cc7-115">DO_E_UNKNOWN_PROPERTY_ID</span><span class="sxs-lookup"><span data-stu-id="b9cc7-115">DO_E_UNKNOWN_PROPERTY_ID</span></span>|<span data-ttu-id="b9cc7-116">se desconoce el *propId* .</span><span class="sxs-lookup"><span data-stu-id="b9cc7-116">*propId* is unknown.</span></span>|
|<span data-ttu-id="b9cc7-117">DO_E_WRITE_ONLY_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="b9cc7-117">DO_E_WRITE_ONLY_PROPERTY</span></span>|<span data-ttu-id="b9cc7-118">La propiedad es de solo escritura y no se puede leer.</span><span class="sxs-lookup"><span data-stu-id="b9cc7-118">The property is write-only, and cannot be read.</span></span>|
|<span data-ttu-id="b9cc7-119">E_NOT_SET</span><span class="sxs-lookup"><span data-stu-id="b9cc7-119">E_NOT_SET</span></span>|<span data-ttu-id="b9cc7-120">No se ha establecido esta propiedad mediante **SetProperty**.</span><span class="sxs-lookup"><span data-stu-id="b9cc7-120">No such property was set via **SetProperty**.</span></span>|

## <a name="requirements"></a><span data-ttu-id="b9cc7-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9cc7-121">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="b9cc7-122">**Cliente mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="b9cc7-122">**Minimum supported client**</span></span> | <span data-ttu-id="b9cc7-123">Solo aplicaciones Win32 de Windows 10, versión 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="b9cc7-123">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="b9cc7-124">**Servidor mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="b9cc7-124">**Minimum supported server**</span></span> | <span data-ttu-id="b9cc7-125">Windows Server, versión 1809 \[ Win32 Applications Only\]</span><span class="sxs-lookup"><span data-stu-id="b9cc7-125">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="b9cc7-126">**Header**</span><span class="sxs-lookup"><span data-stu-id="b9cc7-126">**Header**</span></span> | <span data-ttu-id="b9cc7-127">Do. h</span><span class="sxs-lookup"><span data-stu-id="b9cc7-127">Do.h</span></span> |
