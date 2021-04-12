---
title: 'IDOManager:: CreateDownload (método)'
description: Crea una nueva descarga.
keywords:
- 'IDOManager:: CreateDownload (método)'
topic_type:
- apiref
api_name:
- IDOManager.CreateDownload
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: b79bf0a1c5602fafea113585dfe6e8ca5b01057c
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "104420043"
---
# <a name="idomanagercreatedownload-method"></a><span data-ttu-id="c6c0a-104">IDOManager:: CreateDownload (método)</span><span class="sxs-lookup"><span data-stu-id="c6c0a-104">IDOManager::CreateDownload method</span></span>

<span data-ttu-id="c6c0a-105">Crea una nueva descarga.</span><span class="sxs-lookup"><span data-stu-id="c6c0a-105">Creates a new download.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6c0a-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c6c0a-106">Syntax</span></span>

```cpp
HRESULT CreateDownload(
  IDODownload **download
);
```

## <a name="parameters"></a><span data-ttu-id="c6c0a-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c6c0a-107">Parameters</span></span>

`download`

<span data-ttu-id="c6c0a-108">Dirección de un puntero de interfaz **IDODownload** .</span><span class="sxs-lookup"><span data-stu-id="c6c0a-108">The address of an **IDODownload** interface pointer.</span></span>

## <a name="return-value"></a><span data-ttu-id="c6c0a-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c6c0a-109">Return Value</span></span>

<span data-ttu-id="c6c0a-110">Si la función se ejecuta correctamente, devuelve **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="c6c0a-110">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="c6c0a-111">De lo contrario, devuelve un [código de error](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .</span><span class="sxs-lookup"><span data-stu-id="c6c0a-111">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="c6c0a-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6c0a-112">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="c6c0a-113">**Cliente mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="c6c0a-113">**Minimum supported client**</span></span> | <span data-ttu-id="c6c0a-114">Solo aplicaciones Win32 de Windows 10, versión 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="c6c0a-114">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="c6c0a-115">**Servidor mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="c6c0a-115">**Minimum supported server**</span></span> | <span data-ttu-id="c6c0a-116">Windows Server, versión 1809 \[ Win32 Applications Only\]</span><span class="sxs-lookup"><span data-stu-id="c6c0a-116">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="c6c0a-117">**Header**</span><span class="sxs-lookup"><span data-stu-id="c6c0a-117">**Header**</span></span> | <span data-ttu-id="c6c0a-118">Do. h</span><span class="sxs-lookup"><span data-stu-id="c6c0a-118">Do.h</span></span> |
