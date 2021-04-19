---
description: Proporciona al sistema información sobre un documento antes de iniciar la operación de cierre del archivo de documento.
title: Función DlpNotifyCloseDocumentFile (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyCloseDocumentFile
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 2438829cde84e9029a86d74e4ed704e1e8d33511
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495907"
---
# <a name="dlpnotifyclosedocumentfile-function"></a><span data-ttu-id="554b2-103">Función DlpNotifyCloseDocumentFile</span><span class="sxs-lookup"><span data-stu-id="554b2-103">DlpNotifyCloseDocumentFile function</span></span>

<span data-ttu-id="554b2-104">Proporciona al sistema información sobre un documento antes de iniciar la operación de cierre del archivo de documento.</span><span class="sxs-lookup"><span data-stu-id="554b2-104">Provides the system with information about a document before the document file close operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="554b2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="554b2-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyCloseDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a><span data-ttu-id="554b2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="554b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="554b2-107">*DocumentInfo* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="554b2-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="554b2-108">Puntero a una [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) estructura que contiene información sobre el documento que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="554b2-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document to be opened.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="554b2-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="554b2-109">Return value</span></span>

<span data-ttu-id="554b2-110">Devuelve void.</span><span class="sxs-lookup"><span data-stu-id="554b2-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="554b2-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="554b2-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="554b2-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="554b2-112">Requirements</span></span>


| <span data-ttu-id="554b2-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="554b2-113">Requirement</span></span>          |    <span data-ttu-id="554b2-114">Value</span><span class="sxs-lookup"><span data-stu-id="554b2-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="554b2-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="554b2-115">Minimum supported client</span></span><br/> | <span data-ttu-id="554b2-116">Windows 10, versión 1809 (10.0; Compilación 17763)</span><span class="sxs-lookup"><span data-stu-id="554b2-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="554b2-117">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="554b2-117">DLL</span></span><br/>                      | <span data-ttu-id="554b2-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="554b2-118">EndpointDlp.dll</span></span> |