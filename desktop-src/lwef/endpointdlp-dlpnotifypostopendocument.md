---
description: Proporciona al sistema información sobre un documento una vez completada la operación de apertura.
title: Función DlpNotifyPostOpenDocument (endpointdlp.h)
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
ms.openlocfilehash: 10121e69ddbdc41516e56ec07e87a2f6dd8148cd
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495892"
---
# <a name="dlpnotifypostopendocument-function"></a><span data-ttu-id="2fdd8-103">Función DlpNotifyPostOpenDocument</span><span class="sxs-lookup"><span data-stu-id="2fdd8-103">DlpNotifyPostOpenDocument function</span></span>

<span data-ttu-id="2fdd8-104">Proporciona al sistema información sobre un documento una vez completada una operación de documento abierto.</span><span class="sxs-lookup"><span data-stu-id="2fdd8-104">Provides the system with information about a document after an open document operation is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fdd8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2fdd8-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostOpenDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus); 
```

## <a name="parameters"></a><span data-ttu-id="2fdd8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2fdd8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fdd8-107">*DocumentInfo* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="2fdd8-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fdd8-108">Puntero a una [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) estructura que contiene información sobre el documento que se abrió.</span><span class="sxs-lookup"><span data-stu-id="2fdd8-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document that was opened.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="2fdd8-109">*OpStatus* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="2fdd8-109">*OpStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fdd8-110">Puntero a una estructura [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) que contiene información de estado sobre la operación de documento abierto.</span><span class="sxs-lookup"><span data-stu-id="2fdd8-110">A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the open document operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="2fdd8-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2fdd8-111">Return value</span></span>

<span data-ttu-id="2fdd8-112">Devuelve void.</span><span class="sxs-lookup"><span data-stu-id="2fdd8-112">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fdd8-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2fdd8-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="2fdd8-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2fdd8-114">Requirements</span></span>



| <span data-ttu-id="2fdd8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fdd8-115">Requirement</span></span>          |    <span data-ttu-id="2fdd8-116">Value</span><span class="sxs-lookup"><span data-stu-id="2fdd8-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2fdd8-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2fdd8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2fdd8-118">Windows 10, versión 1809 (10.0; Compilación 17763)</span><span class="sxs-lookup"><span data-stu-id="2fdd8-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="2fdd8-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2fdd8-119">DLL</span></span><br/>                      | <span data-ttu-id="2fdd8-120">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="2fdd8-120">EndpointDlp.dll</span></span> |