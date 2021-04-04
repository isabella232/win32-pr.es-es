---
title: 'IDODownloadStatusCallback:: OnStatusChange (método)'
description: Llama a la implementación de este método cada vez que cambia el estado de la descarga.
keywords:
- 'IDODownloadStatusCallback:: OnStatusChange (método)'
topic_type:
- apiref
api_name:
- IDODownloadStatusCallback.OnStatusChange
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 9abf13969a6183f98102792b9bcf7a3329ca243d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "104077154"
---
# <a name="idodownloadstatuscallbackonstatuschange-method"></a><span data-ttu-id="a4f34-104">IDODownloadStatusCallback:: OnStatusChange (método)</span><span class="sxs-lookup"><span data-stu-id="a4f34-104">IDODownloadStatusCallback::OnStatusChange method</span></span>

<span data-ttu-id="a4f34-105">Llama a la implementación de este método cada vez que cambia el estado de la descarga.</span><span class="sxs-lookup"><span data-stu-id="a4f34-105">DO calls your implementation of this method any time a download status has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4f34-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a4f34-106">Syntax</span></span>

```cpp
HRESULT OnStatusChange(
  IDODownload *download,
  DO_DOWNLOAD_STATUS *status
);
```

## <a name="parameters"></a><span data-ttu-id="a4f34-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a4f34-107">Parameters</span></span>

`download`

<span data-ttu-id="a4f34-108">Puntero a la interfaz **IDODownload** cuyo estado ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="a4f34-108">An pointer to the **IDODownload** interface whose status changed.</span></span>

`status`

<span data-ttu-id="a4f34-109">Puntero a una estructura de **DO_DOWNLOAD_STATUS** que contiene el estado de la descarga.</span><span class="sxs-lookup"><span data-stu-id="a4f34-109">A pointer to a **DO_DOWNLOAD_STATUS** structure containing the download's status.</span></span>

## <a name="return-value"></a><span data-ttu-id="a4f34-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a4f34-110">Return Value</span></span>

<span data-ttu-id="a4f34-111">Si la función se ejecuta correctamente, devuelve **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="a4f34-111">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="a4f34-112">De lo contrario, devuelve un [código de error](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .</span><span class="sxs-lookup"><span data-stu-id="a4f34-112">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="a4f34-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4f34-113">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="a4f34-114">**Cliente mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="a4f34-114">**Minimum supported client**</span></span> | <span data-ttu-id="a4f34-115">Solo aplicaciones Win32 de Windows 10, versión 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="a4f34-115">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="a4f34-116">**Servidor mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="a4f34-116">**Minimum supported server**</span></span> | <span data-ttu-id="a4f34-117">Windows Server, versión 1809 \[ Win32 Applications Only\]</span><span class="sxs-lookup"><span data-stu-id="a4f34-117">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="a4f34-118">**Header**</span><span class="sxs-lookup"><span data-stu-id="a4f34-118">**Header**</span></span> | <span data-ttu-id="a4f34-119">Do. h</span><span class="sxs-lookup"><span data-stu-id="a4f34-119">Do.h</span></span> |
