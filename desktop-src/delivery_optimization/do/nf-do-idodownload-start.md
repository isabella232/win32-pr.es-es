---
title: 'IDODownload:: Start (método)'
description: Inicia o reanuda una descarga.
keywords:
- 'IDODownload:: Start (método)'
topic_type:
- apiref
api_name:
- IDODownload.Start
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 0d05b0660008ae65350c6331428f641bc2126c18
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "105721403"
---
# <a name="idodownloadstart-method"></a><span data-ttu-id="37359-104">IDODownload:: Start (método)</span><span class="sxs-lookup"><span data-stu-id="37359-104">IDODownload::Start method</span></span>

<span data-ttu-id="37359-105">Inicia o reanuda una descarga, pasando los intervalos opcionales como puntero a [**DO_DOWNLOAD_RANGES_INFO**](ns-do-do_download_range_info.md) estructura.</span><span class="sxs-lookup"><span data-stu-id="37359-105">Starts or resumes a download, passing optional ranges as a pointer to [**DO_DOWNLOAD_RANGES_INFO**](ns-do-do_download_range_info.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="37359-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="37359-106">Syntax</span></span>

```cpp
HRESULT Start(
  DO_DOWNLOAD_RANGES_INFO *ranges
);
```

## <a name="parameters"></a><span data-ttu-id="37359-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="37359-107">Parameters</span></span>

`ranges`

<span data-ttu-id="37359-108">Opcional.</span><span class="sxs-lookup"><span data-stu-id="37359-108">Optional.</span></span> <span data-ttu-id="37359-109">Puntero a una estructura de [**DO_DOWNLOAD_RANGES_INFO**](ns-do-do_download_range_info.md) (para descargar solo los intervalos concretos del archivo).</span><span class="sxs-lookup"><span data-stu-id="37359-109">A pointer to a [**DO_DOWNLOAD_RANGES_INFO**](ns-do-do_download_range_info.md) structure (to download only specific ranges of the file).</span></span> <span data-ttu-id="37359-110">Pass `nullptr` para descargar todo el archivo.</span><span class="sxs-lookup"><span data-stu-id="37359-110">Pass `nullptr` to download the entire file.</span></span>

## <a name="return-value"></a><span data-ttu-id="37359-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="37359-111">Return Value</span></span>

<span data-ttu-id="37359-112">Si la función se ejecuta correctamente, devuelve **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="37359-112">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="37359-113">De lo contrario, devuelve un [código de error](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .</span><span class="sxs-lookup"><span data-stu-id="37359-113">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="37359-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37359-114">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="37359-115">**Cliente mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="37359-115">**Minimum supported client**</span></span> | <span data-ttu-id="37359-116">Solo aplicaciones Win32 de Windows 10, versión 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="37359-116">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="37359-117">**Servidor mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="37359-117">**Minimum supported server**</span></span> | <span data-ttu-id="37359-118">Windows Server, versión 1809 \[ Win32 Applications Only\]</span><span class="sxs-lookup"><span data-stu-id="37359-118">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="37359-119">**Header**</span><span class="sxs-lookup"><span data-stu-id="37359-119">**Header**</span></span> | <span data-ttu-id="37359-120">Do. h</span><span class="sxs-lookup"><span data-stu-id="37359-120">Do.h</span></span> |
