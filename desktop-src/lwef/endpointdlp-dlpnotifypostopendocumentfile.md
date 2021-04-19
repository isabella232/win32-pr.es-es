---
description: Proporciona al sistema información sobre un archivo de documento una vez completada la operación de apertura.
title: Función DlpNotifyPostOpenDocumentFile (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostOpenDocumentFile
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 0aed30cc0eca066b569ad1299392430c4d1adeff
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495879"
---
# <a name="dlpnotifypostopendocumentfile-function"></a><span data-ttu-id="1a962-103">Función DlpNotifyPostOpenDocumentFile</span><span class="sxs-lookup"><span data-stu-id="1a962-103">DlpNotifyPostOpenDocumentFile function</span></span>

<span data-ttu-id="1a962-104">Proporciona al sistema información sobre un archivo de documento una vez completada una operación de apertura.</span><span class="sxs-lookup"><span data-stu-id="1a962-104">Provides the system with information about a document file after an open operation is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a962-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1a962-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostOpenDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus 
```

## <a name="parameters"></a><span data-ttu-id="1a962-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1a962-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a962-107">*DocumentInfo* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="1a962-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a962-108">Puntero a [un](endpointdlp-dlp_document_info.md) PDLP_DOCUMENT_INFO estructura que contiene información sobre el documento que se abrió.</span><span class="sxs-lookup"><span data-stu-id="1a962-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document that was opened.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="1a962-109">*OpStatus* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="1a962-109">*OpStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a962-110">Puntero a una estructura [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) que contiene información de estado sobre la operación de abrir documento.</span><span class="sxs-lookup"><span data-stu-id="1a962-110">A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the open document operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="1a962-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1a962-111">Return value</span></span>

<span data-ttu-id="1a962-112">Devuelve void.</span><span class="sxs-lookup"><span data-stu-id="1a962-112">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a962-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1a962-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="1a962-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a962-114">Requirements</span></span>



| <span data-ttu-id="1a962-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a962-115">Requirement</span></span>          |    <span data-ttu-id="1a962-116">Value</span><span class="sxs-lookup"><span data-stu-id="1a962-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a962-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a962-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1a962-118">Windows 10, versión 1809 (10.0; Compilación 17763)</span><span class="sxs-lookup"><span data-stu-id="1a962-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="1a962-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1a962-119">DLL</span></span><br/>                      | <span data-ttu-id="1a962-120">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="1a962-120">EndpointDlp.dll</span></span> |