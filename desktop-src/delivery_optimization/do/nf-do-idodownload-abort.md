---
title: 'IDODownload:: ABORT (método)'
description: Anula la descarga.
keywords:
- 'IDODownload:: ABORT (método)'
topic_type:
- apiref
api_name:
- IDODownload.Abort
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: babcd5ee00689ac103288074467980777f644668
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "105720108"
---
# <a name="idodownloadabort-method"></a><span data-ttu-id="70782-104">IDODownload:: ABORT (método)</span><span class="sxs-lookup"><span data-stu-id="70782-104">IDODownload::Abort method</span></span>

<span data-ttu-id="70782-105">Anula la descarga.</span><span class="sxs-lookup"><span data-stu-id="70782-105">Aborts the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="70782-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="70782-106">Syntax</span></span>

```cpp
HRESULT Abort();
```

## <a name="return-value"></a><span data-ttu-id="70782-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="70782-107">Return Value</span></span>

<span data-ttu-id="70782-108">Si la función se ejecuta correctamente, devuelve **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="70782-108">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="70782-109">De lo contrario, devuelve un [código de error](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .</span><span class="sxs-lookup"><span data-stu-id="70782-109">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="70782-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70782-110">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="70782-111">**Cliente mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="70782-111">**Minimum supported client**</span></span> | <span data-ttu-id="70782-112">Solo aplicaciones Win32 de Windows 10, versión 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="70782-112">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="70782-113">**Servidor mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="70782-113">**Minimum supported server**</span></span> | <span data-ttu-id="70782-114">Windows Server, versión 1809 \[ Win32 Applications Only\]</span><span class="sxs-lookup"><span data-stu-id="70782-114">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="70782-115">**Header**</span><span class="sxs-lookup"><span data-stu-id="70782-115">**Header**</span></span> | <span data-ttu-id="70782-116">Do. h</span><span class="sxs-lookup"><span data-stu-id="70782-116">Do.h</span></span> |
