---
description: Proporciona al sistema información sobre un documento una vez completada la operación guardar como.
title: Función DlpNotifyPostSaveAsDocument (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostSaveAsDocument
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 564e7173cbfe72a020f1c7e12a60ceda25fd845c
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495863"
---
# <a name="dlpnotifypostsaveasdocument-function"></a><span data-ttu-id="b3190-103">Función DlpNotifyPostSaveAsDocument</span><span class="sxs-lookup"><span data-stu-id="b3190-103">DlpNotifyPostSaveAsDocument function</span></span>

<span data-ttu-id="b3190-104">Proporciona al sistema información sobre un documento una vez completada la operación guardar como.</span><span class="sxs-lookup"><span data-stu-id="b3190-104">Provides the system with information about a document after the save as operation is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3190-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b3190-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination, _In_ const PDLP_POSTOP_STATUS OpStatus); 
```

## <a name="parameters"></a><span data-ttu-id="b3190-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b3190-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3190-107">*DocumentInfo* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="b3190-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3190-108">Puntero a una [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) estructura que contiene información sobre el documento que se guardó.</span><span class="sxs-lookup"><span data-stu-id="b3190-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document that was saved.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="b3190-109">*Destino* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="b3190-109">*Destination* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3190-110">**LPCWSTR que** contiene la ruta de acceso de destino del documento que se guardó.</span><span class="sxs-lookup"><span data-stu-id="b3190-110">A **LPCWSTR** containing the destination path the document that was saved.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="b3190-111">*OpStatus* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="b3190-111">*OpStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3190-112">Puntero a una estructura [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) que contiene información de estado sobre la operación guardar como.</span><span class="sxs-lookup"><span data-stu-id="b3190-112">A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the save as operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="b3190-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b3190-113">Return value</span></span>

<span data-ttu-id="b3190-114">Devuelve void.</span><span class="sxs-lookup"><span data-stu-id="b3190-114">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3190-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b3190-115">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="b3190-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3190-116">Requirements</span></span>



| <span data-ttu-id="b3190-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3190-117">Requirement</span></span>          |    <span data-ttu-id="b3190-118">Value</span><span class="sxs-lookup"><span data-stu-id="b3190-118">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3190-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b3190-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b3190-120">Windows 10, versión 1809 (10.0; Compilación 17763)</span><span class="sxs-lookup"><span data-stu-id="b3190-120">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="b3190-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b3190-121">DLL</span></span><br/>                      | <span data-ttu-id="b3190-122">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="b3190-122">EndpointDlp.dll</span></span> |