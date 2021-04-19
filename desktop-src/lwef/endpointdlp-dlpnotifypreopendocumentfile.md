---
description: Proporciona al sistema información sobre un archivo de documento antes de iniciar una operación de apertura.
title: Función DlpNotifyPreOpenDocumentFile (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreOpenDocumentFile
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 12caf5230d8affce195a63da155ed6b6ca409b72
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495851"
---
# <a name="dlpnotifypreopendocumentfile-function"></a><span data-ttu-id="baefe-103">Función DlpNotifyPreOpenDocumentFile</span><span class="sxs-lookup"><span data-stu-id="baefe-103">DlpNotifyPreOpenDocumentFile function</span></span>

<span data-ttu-id="baefe-104">Proporciona al sistema información sobre un archivo de documento antes de iniciar una operación de apertura.</span><span class="sxs-lookup"><span data-stu-id="baefe-104">Provides the system with information about a document file before an open operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="baefe-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="baefe-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPreOpenDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a><span data-ttu-id="baefe-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="baefe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="baefe-107">*DocumentInfo* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="baefe-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="baefe-108">Puntero a [un](endpointdlp-dlp_document_info.md) PDLP_DOCUMENT_INFO estructura que contiene información sobre el documento que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="baefe-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document to be opened.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="baefe-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="baefe-109">Return value</span></span>

<span data-ttu-id="baefe-110">Devuelve void.</span><span class="sxs-lookup"><span data-stu-id="baefe-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="baefe-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="baefe-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="baefe-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="baefe-112">Requirements</span></span>



| <span data-ttu-id="baefe-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="baefe-113">Requirement</span></span>          |    <span data-ttu-id="baefe-114">Value</span><span class="sxs-lookup"><span data-stu-id="baefe-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="baefe-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="baefe-115">Minimum supported client</span></span><br/> | <span data-ttu-id="baefe-116">Windows 10, versión 1809 (10.0; Compilación 17763)</span><span class="sxs-lookup"><span data-stu-id="baefe-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="baefe-117">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="baefe-117">DLL</span></span><br/>                      | <span data-ttu-id="baefe-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="baefe-118">EndpointDlp.dll</span></span> |