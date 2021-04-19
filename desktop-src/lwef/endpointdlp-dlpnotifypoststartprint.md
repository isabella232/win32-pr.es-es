---
description: Proporciona al sistema información sobre un documento después de que se haya iniciado una operación de impresión.
title: Función DlpNotifyPostStartPrint (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostOpenDocument
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 7bc2505b44797edc836ed8ae89e5d9caf3f93f05
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495860"
---
# <a name="dlpnotifypoststartprint-function"></a><span data-ttu-id="7fd25-103">Función DlpNotifyPostStartPrint</span><span class="sxs-lookup"><span data-stu-id="7fd25-103">DlpNotifyPostStartPrint function</span></span>

<span data-ttu-id="7fd25-104">Proporciona al sistema información sobre un documento después de que se haya iniciado una operación de impresión.</span><span class="sxs-lookup"><span data-stu-id="7fd25-104">Provides the system with information about a document after a print operation has started.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fd25-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7fd25-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostStartPrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo);
```

## <a name="parameters"></a><span data-ttu-id="7fd25-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7fd25-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fd25-107">*DocumentInfo* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="7fd25-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fd25-108">Puntero a una estructura [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) que contiene información sobre el documento asociado a la operación de impresión.</span><span class="sxs-lookup"><span data-stu-id="7fd25-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document associated with the print operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="7fd25-109">*PrintInfo* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="7fd25-109">*PrintInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fd25-110">Puntero a una estructura [DLP_PRINT_INFO](endpointdlp-dlp_print_info.md) que contiene información sobre la operación de impresión.</span><span class="sxs-lookup"><span data-stu-id="7fd25-110">A pointer to a [DLP_PRINT_INFO](endpointdlp-dlp_print_info.md) structure containing information about the print operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="7fd25-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7fd25-111">Return value</span></span>

<span data-ttu-id="7fd25-112">Devuelve void.</span><span class="sxs-lookup"><span data-stu-id="7fd25-112">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="7fd25-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7fd25-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="7fd25-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7fd25-114">Requirements</span></span>



| <span data-ttu-id="7fd25-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fd25-115">Requirement</span></span>          |    <span data-ttu-id="7fd25-116">Value</span><span class="sxs-lookup"><span data-stu-id="7fd25-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7fd25-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7fd25-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7fd25-118">Windows 10, versión 1809 (10.0; Compilación 17763)</span><span class="sxs-lookup"><span data-stu-id="7fd25-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="7fd25-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7fd25-119">DLL</span></span><br/>                      | <span data-ttu-id="7fd25-120">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="7fd25-120">EndpointDlp.dll</span></span> |