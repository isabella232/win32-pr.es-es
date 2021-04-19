---
description: Proporciona al sistema información sobre un documento antes de iniciar una operación de impresión.
title: Función DlpNotifyPrePrint (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPrePrint
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: eef5e3a19a6b93a49ba8b600be77385a99d3153a
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495819"
---
# <a name="dlpnotifypreprint-function"></a><span data-ttu-id="b17dd-103">Función DlpNotifyPrePrint</span><span class="sxs-lookup"><span data-stu-id="b17dd-103">DlpNotifyPrePrint function</span></span>

<span data-ttu-id="b17dd-104">Proporciona al sistema información sobre un documento antes de iniciar una operación de impresión.</span><span class="sxs-lookup"><span data-stu-id="b17dd-104">Provides the system with information about a document before a print operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="b17dd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b17dd-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPrePrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo);
```



## <a name="parameters"></a><span data-ttu-id="b17dd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b17dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b17dd-107">*DocumentInfo* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="b17dd-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b17dd-108">Puntero a una [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) estructura que contiene información sobre el documento que se va a imprimir.</span><span class="sxs-lookup"><span data-stu-id="b17dd-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document to be printed.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="b17dd-109">*PrintInfo* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="b17dd-109">*PrintInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b17dd-110">Puntero a una estructura [DLP_PRINT_INFO](endpointdlp-dlp_print_info.md) que contiene información sobre la operación de impresión.</span><span class="sxs-lookup"><span data-stu-id="b17dd-110">A pointer to a [DLP_PRINT_INFO](endpointdlp-dlp_print_info.md) structure containing information about print operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="b17dd-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b17dd-111">Return value</span></span>

<span data-ttu-id="b17dd-112">Devuelve void.</span><span class="sxs-lookup"><span data-stu-id="b17dd-112">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="b17dd-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b17dd-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="b17dd-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b17dd-114">Requirements</span></span>



| <span data-ttu-id="b17dd-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b17dd-115">Requirement</span></span>          |    <span data-ttu-id="b17dd-116">Value</span><span class="sxs-lookup"><span data-stu-id="b17dd-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b17dd-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b17dd-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b17dd-118">Windows 10, versión 1809 (10.0; Compilación 17763)</span><span class="sxs-lookup"><span data-stu-id="b17dd-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="b17dd-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b17dd-119">DLL</span></span><br/>                      | <span data-ttu-id="b17dd-120">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="b17dd-120">EndpointDlp.dll</span></span> |