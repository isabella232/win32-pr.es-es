---
description: Proporciona al sistema información sobre un documento antes de iniciar una operación de copia en el Portapapeles.
title: Función DlpNotifyPreCopyToClipboard (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreCopyToClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: b8e835e58d19570b9459d91ad131bbc0f38f378a
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495856"
---
# <a name="dlpnotifyprecopytoclipboard-function"></a><span data-ttu-id="1818b-103">Función DlpNotifyPreCopyToClipboard</span><span class="sxs-lookup"><span data-stu-id="1818b-103">DlpNotifyPreCopyToClipboard function</span></span>

<span data-ttu-id="1818b-104">Proporciona al sistema información sobre un documento antes de iniciar una operación de copia en el Portapapeles.</span><span class="sxs-lookup"><span data-stu-id="1818b-104">Provides the system with information about a document before a copy to clipboard operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="1818b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1818b-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPreCopyToClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a><span data-ttu-id="1818b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1818b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1818b-107">*DocumentInfo* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="1818b-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1818b-108">Puntero a una [estructura PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) que contiene información sobre el documento del que se copia el contenido.</span><span class="sxs-lookup"><span data-stu-id="1818b-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document from which content is being copied.</span></span>

</dd> </dl>




## <a name="return-value"></a><span data-ttu-id="1818b-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1818b-109">Return value</span></span>

<span data-ttu-id="1818b-110">Devuelve void.</span><span class="sxs-lookup"><span data-stu-id="1818b-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="1818b-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1818b-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="1818b-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1818b-112">Requirements</span></span>



| <span data-ttu-id="1818b-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="1818b-113">Requirement</span></span>          |    <span data-ttu-id="1818b-114">Value</span><span class="sxs-lookup"><span data-stu-id="1818b-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1818b-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1818b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1818b-116">Windows 10, versión 1809 (10.0; Compilación 17763)</span><span class="sxs-lookup"><span data-stu-id="1818b-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="1818b-117">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1818b-117">DLL</span></span><br/>                      | <span data-ttu-id="1818b-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="1818b-118">EndpointDlp.dll</span></span> |