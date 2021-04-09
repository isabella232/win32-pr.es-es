---
title: IDODownload::P método ause
description: Pausa la descarga.
keywords:
- IDODownload::P método ause
topic_type:
- apiref
api_name:
- IDODownload.Pause
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: a7239253238b0d9b7e606329b10f05b3645b7e16
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "104149019"
---
# <a name="idodownloadpause-method"></a><span data-ttu-id="cd106-104">IDODownload::P método ause</span><span class="sxs-lookup"><span data-stu-id="cd106-104">IDODownload::Pause method</span></span>

<span data-ttu-id="cd106-105">Pausa la descarga.</span><span class="sxs-lookup"><span data-stu-id="cd106-105">Pauses the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd106-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cd106-106">Syntax</span></span>

```cpp
HRESULT Pause();
```

## <a name="return-value"></a><span data-ttu-id="cd106-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd106-107">Return Value</span></span>

<span data-ttu-id="cd106-108">Si la función se ejecuta correctamente, devuelve **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="cd106-108">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="cd106-109">De lo contrario, devuelve un [código de error](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .</span><span class="sxs-lookup"><span data-stu-id="cd106-109">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="cd106-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd106-110">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="cd106-111">**Cliente mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="cd106-111">**Minimum supported client**</span></span> | <span data-ttu-id="cd106-112">Solo aplicaciones Win32 de Windows 10, versión 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="cd106-112">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="cd106-113">**Servidor mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="cd106-113">**Minimum supported server**</span></span> | <span data-ttu-id="cd106-114">Windows Server, versión 1809 \[ Win32 Applications Only\]</span><span class="sxs-lookup"><span data-stu-id="cd106-114">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="cd106-115">**Header**</span><span class="sxs-lookup"><span data-stu-id="cd106-115">**Header**</span></span> | <span data-ttu-id="cd106-116">Do. h</span><span class="sxs-lookup"><span data-stu-id="cd106-116">Do.h</span></span> |
