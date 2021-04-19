---
description: Proporciona al sistema información sobre un documento una vez completada una operación de copia en el Portapapeles.
title: Función DlpNotifyPostCopyToClipboard (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostCopyToClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: b4b1a375d68819fc36f82a530a7fe7a8abe881c0
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495898"
---
# <a name="dlpnotifypostcopytoclipboard-function"></a><span data-ttu-id="8e980-103">Función DlpNotifyPostCopyToClipboard</span><span class="sxs-lookup"><span data-stu-id="8e980-103">DlpNotifyPostCopyToClipboard function</span></span>

<span data-ttu-id="8e980-104">Proporciona al sistema información sobre un documento una vez completada una operación de copia en el Portapapeles.</span><span class="sxs-lookup"><span data-stu-id="8e980-104">Provides the system with information about a document after a copy to clipboard operation is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e980-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8e980-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostCopyToClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
```



## <a name="parameters"></a><span data-ttu-id="8e980-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8e980-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e980-107">*DocumentInfo* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="8e980-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e980-108">Puntero a una [estructura PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) que contiene información sobre el documento del que se copió el contenido.</span><span class="sxs-lookup"><span data-stu-id="8e980-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document from which content was copied.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="8e980-109">*OpStatus* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="8e980-109">*OpStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e980-110">Puntero a una estructura [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) que contiene información de estado sobre la operación de copia en el Portapapeles.</span><span class="sxs-lookup"><span data-stu-id="8e980-110">A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the copy to clipboard operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="8e980-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8e980-111">Return value</span></span>

<span data-ttu-id="8e980-112">Devuelve void.</span><span class="sxs-lookup"><span data-stu-id="8e980-112">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e980-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8e980-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="8e980-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e980-114">Requirements</span></span>



| <span data-ttu-id="8e980-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e980-115">Requirement</span></span>          |    <span data-ttu-id="8e980-116">Value</span><span class="sxs-lookup"><span data-stu-id="8e980-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e980-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e980-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8e980-118">Windows 10, versión 1809 (10.0; Compilación 17763)</span><span class="sxs-lookup"><span data-stu-id="8e980-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="8e980-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8e980-119">DLL</span></span><br/>                      | <span data-ttu-id="8e980-120">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="8e980-120">EndpointDlp.dll</span></span> |