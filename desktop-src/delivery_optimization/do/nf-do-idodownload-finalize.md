---
title: 'IDODownload:: Finalize (método)'
description: Finaliza la descarga.
keywords:
- 'IDODownload:: Finalize (método)'
topic_type:
- apiref
api_name:
- IDODownload.Finalize
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 6befc9a7e64fb0963d45257d68d6bb8d2ba7a2cb
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "105720107"
---
# <a name="idodownloadfinalize-method"></a><span data-ttu-id="fd44d-104">IDODownload:: Finalize (método)</span><span class="sxs-lookup"><span data-stu-id="fd44d-104">IDODownload::Finalize method</span></span>

<span data-ttu-id="fd44d-105">Finaliza la descarga.</span><span class="sxs-lookup"><span data-stu-id="fd44d-105">Finalizes the download.</span></span> <span data-ttu-id="fd44d-106">Una vez finalizada, una descarga no se puede reanudar mediante una llamada a **Start**.</span><span class="sxs-lookup"><span data-stu-id="fd44d-106">Once finalized, a download cannot be resumed by calling **Start**.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd44d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fd44d-107">Syntax</span></span>

```cpp
HRESULT Finalize();
```

## <a name="return-value"></a><span data-ttu-id="fd44d-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fd44d-108">Return Value</span></span>

<span data-ttu-id="fd44d-109">Si la función se ejecuta correctamente, devuelve **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="fd44d-109">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="fd44d-110">De lo contrario, devuelve un [código de error](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .</span><span class="sxs-lookup"><span data-stu-id="fd44d-110">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="fd44d-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd44d-111">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="fd44d-112">**Cliente mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="fd44d-112">**Minimum supported client**</span></span> | <span data-ttu-id="fd44d-113">Solo aplicaciones Win32 de Windows 10, versión 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="fd44d-113">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="fd44d-114">**Servidor mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="fd44d-114">**Minimum supported server**</span></span> | <span data-ttu-id="fd44d-115">Windows Server, versión 1809 \[ Win32 Applications Only\]</span><span class="sxs-lookup"><span data-stu-id="fd44d-115">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="fd44d-116">**Header**</span><span class="sxs-lookup"><span data-stu-id="fd44d-116">**Header**</span></span> | <span data-ttu-id="fd44d-117">Do. h</span><span class="sxs-lookup"><span data-stu-id="fd44d-117">Do.h</span></span> |
