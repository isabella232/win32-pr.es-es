---
description: Proporciona al sistema información sobre un documento cuando se introduce un destino de colocación.
title: Función DlpNotifyEnterDropTarget (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyEnterDropTarget
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: ec1eee1cee7bbcc38ce3094e3e2f8b650cf3b2a9
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495901"
---
# <a name="dlpnotifyenterdroptarget-function"></a><span data-ttu-id="865a6-103">Función DlpNotifyEnterDropTarget</span><span class="sxs-lookup"><span data-stu-id="865a6-103">DlpNotifyEnterDropTarget function</span></span>

<span data-ttu-id="865a6-104">Proporciona al sistema información sobre un documento cuando se introduce un destino de colocación.</span><span class="sxs-lookup"><span data-stu-id="865a6-104">Provides the system with information about a document when a drop target is entered.</span></span>

## <a name="syntax"></a><span data-ttu-id="865a6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="865a6-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyEnterDropTarget(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a><span data-ttu-id="865a6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="865a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="865a6-107">*DocumentInfo* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="865a6-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="865a6-108">Puntero a una estructura [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) que contiene información sobre el documento asociado a la operación de colocación.</span><span class="sxs-lookup"><span data-stu-id="865a6-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document associated with the drop operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="865a6-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="865a6-109">Return value</span></span>

<span data-ttu-id="865a6-110">Devuelve void.</span><span class="sxs-lookup"><span data-stu-id="865a6-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="865a6-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="865a6-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="865a6-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="865a6-112">Requirements</span></span>



| <span data-ttu-id="865a6-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="865a6-113">Requirement</span></span>          |    <span data-ttu-id="865a6-114">Value</span><span class="sxs-lookup"><span data-stu-id="865a6-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="865a6-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="865a6-115">Minimum supported client</span></span><br/> | <span data-ttu-id="865a6-116">Windows 10, versión 1809 (10.0; Compilación 17763)</span><span class="sxs-lookup"><span data-stu-id="865a6-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="865a6-117">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="865a6-117">DLL</span></span><br/>                      | <span data-ttu-id="865a6-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="865a6-118">EndpointDlp.dll</span></span> |