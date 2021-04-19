---
description: Proporciona al sistema información sobre un documento una vez completada una operación de impresión.
title: Función DlpNotifyPostPrint (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostPrint
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: b1206aa4e358e0763c10a0d9b5028acae25f5683
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495864"
---
# <a name="dlpnotifypostprint-function"></a><span data-ttu-id="2b073-103">Función DlpNotifyPostPrint</span><span class="sxs-lookup"><span data-stu-id="2b073-103">DlpNotifyPostPrint function</span></span>

<span data-ttu-id="2b073-104">Proporciona al sistema información sobre un documento una vez completada una operación de impresión.</span><span class="sxs-lookup"><span data-stu-id="2b073-104">Provides the system with information about a document after a print operation has completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b073-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2b073-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostPrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
```

## <a name="parameters"></a><span data-ttu-id="2b073-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2b073-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b073-107">*DocumentInfo* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="2b073-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b073-108">Puntero a una estructura [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) que contiene información sobre el documento asociado a la operación de impresión.</span><span class="sxs-lookup"><span data-stu-id="2b073-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document associated with the print operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="2b073-109">*PrintInfo* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="2b073-109">*PrintInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b073-110">Puntero a una estructura [DLP_PRINT_INFO](endpointdlp-dlp_print_info.md) que contiene información sobre la operación de impresión.</span><span class="sxs-lookup"><span data-stu-id="2b073-110">A pointer to a [DLP_PRINT_INFO](endpointdlp-dlp_print_info.md) structure containing information about the print operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="2b073-111">*OpStatus* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="2b073-111">*OpStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b073-112">Puntero a una estructura [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) que contiene información de estado sobre la operación de impresión.</span><span class="sxs-lookup"><span data-stu-id="2b073-112">A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the print operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="2b073-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2b073-113">Return value</span></span>

<span data-ttu-id="2b073-114">Devuelve void.</span><span class="sxs-lookup"><span data-stu-id="2b073-114">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b073-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2b073-115">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="2b073-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b073-116">Requirements</span></span>



| <span data-ttu-id="2b073-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b073-117">Requirement</span></span>          |    <span data-ttu-id="2b073-118">Value</span><span class="sxs-lookup"><span data-stu-id="2b073-118">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b073-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b073-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2b073-120">Windows 10, versión 1809 (10.0; Compilación 17763)</span><span class="sxs-lookup"><span data-stu-id="2b073-120">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="2b073-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2b073-121">DLL</span></span><br/>                      | <span data-ttu-id="2b073-122">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="2b073-122">EndpointDlp.dll</span></span> |