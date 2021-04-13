---
title: 'IDODownload:: GetStatus (método)'
description: Recupera un puntero a una estructura de **DO_DOWNLOAD_STATUS** que refleja el estado actual de la descarga.
keywords:
- 'IDODownload:: GetStatus (método)'
topic_type:
- apiref
api_name:
- IDODownload.GetStatus
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 8b9b2603354bbb5345cf866ee0c94785a254952d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "104420045"
---
# <a name="idodownloadgetstatus-method"></a><span data-ttu-id="031b4-104">IDODownload:: GetStatus (método)</span><span class="sxs-lookup"><span data-stu-id="031b4-104">IDODownload::GetStatus method</span></span>

<span data-ttu-id="031b4-105">Recupera un puntero a una estructura de **DO_DOWNLOAD_STATUS** que refleja el estado actual de la descarga.</span><span class="sxs-lookup"><span data-stu-id="031b4-105">Retrieves a pointer to a **DO_DOWNLOAD_STATUS** structure that reflects the current status of the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="031b4-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="031b4-106">Syntax</span></span>

```cpp
HRESULT GetStatus(
  DO_DOWNLOAD_STATUS *status
);
```

## <a name="parameters"></a><span data-ttu-id="031b4-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="031b4-107">Parameters</span></span>

`status`

<span data-ttu-id="031b4-108">Puntero a una estructura de **DO_DOWNLOAD_STATUS** .</span><span class="sxs-lookup"><span data-stu-id="031b4-108">A pointer to a **DO_DOWNLOAD_STATUS** structure.</span></span>

## <a name="return-value"></a><span data-ttu-id="031b4-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="031b4-109">Return Value</span></span>

<span data-ttu-id="031b4-110">Si la función se ejecuta correctamente, devuelve **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="031b4-110">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="031b4-111">De lo contrario, devuelve un [código de error](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .</span><span class="sxs-lookup"><span data-stu-id="031b4-111">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="031b4-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="031b4-112">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="031b4-113">**Cliente mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="031b4-113">**Minimum supported client**</span></span> | <span data-ttu-id="031b4-114">Solo aplicaciones Win32 de Windows 10, versión 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="031b4-114">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="031b4-115">**Servidor mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="031b4-115">**Minimum supported server**</span></span> | <span data-ttu-id="031b4-116">Windows Server, versión 1809 \[ Win32 Applications Only\]</span><span class="sxs-lookup"><span data-stu-id="031b4-116">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="031b4-117">**Header**</span><span class="sxs-lookup"><span data-stu-id="031b4-117">**Header**</span></span> | <span data-ttu-id="031b4-118">Do. h</span><span class="sxs-lookup"><span data-stu-id="031b4-118">Do.h</span></span> |
