---
description: Proporciona al sistema información sobre un documento antes de iniciar una operación de pegar desde el Portapapeles.
title: Función DlpNotifyPrePasteFromClipboard (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPrePasteFromClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: cfec6e7abbf2b94ce8bf78e0b1a10082ec54419d
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495815"
---
# <a name="dlpnotifyprepastefromclipboard-function"></a><span data-ttu-id="58517-103">Función DlpNotifyPrePasteFromClipboard</span><span class="sxs-lookup"><span data-stu-id="58517-103">DlpNotifyPrePasteFromClipboard function</span></span>

<span data-ttu-id="58517-104">Proporciona al sistema información sobre un documento antes de iniciar una operación de pegar desde el Portapapeles.</span><span class="sxs-lookup"><span data-stu-id="58517-104">Provides the system with information about a document before a paste from clipboard operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="58517-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="58517-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPrePasteFromClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a><span data-ttu-id="58517-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="58517-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58517-107">*DocumentInfo* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="58517-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58517-108">Puntero a una [estructura PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) que contiene información sobre el documento en el que se pega el contenido.</span><span class="sxs-lookup"><span data-stu-id="58517-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document into which content is being pasted.</span></span>

</dd> </dl>




## <a name="return-value"></a><span data-ttu-id="58517-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="58517-109">Return value</span></span>

<span data-ttu-id="58517-110">Devuelve void.</span><span class="sxs-lookup"><span data-stu-id="58517-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="58517-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="58517-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="58517-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58517-112">Requirements</span></span>



| <span data-ttu-id="58517-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="58517-113">Requirement</span></span>          |    <span data-ttu-id="58517-114">Value</span><span class="sxs-lookup"><span data-stu-id="58517-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="58517-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="58517-115">Minimum supported client</span></span><br/> | <span data-ttu-id="58517-116">Windows 10, versión 1809 (10.0; Compilación 17763)</span><span class="sxs-lookup"><span data-stu-id="58517-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="58517-117">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="58517-117">DLL</span></span><br/>                      | <span data-ttu-id="58517-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="58517-118">EndpointDlp.dll</span></span> |