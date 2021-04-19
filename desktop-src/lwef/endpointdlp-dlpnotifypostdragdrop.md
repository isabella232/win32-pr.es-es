---
description: Proporciona al sistema información sobre un documento una vez completada una operación de arrastrar y colocar.
title: Función DlpNotifyPostDragDrop (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreDragDrop
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 468255cee3c3fef44e44dd033b541e317db3d268
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495895"
---
# <a name="dlpnotifypostdragdrop-function"></a><span data-ttu-id="c5eb5-103">Función DlpNotifyPostDragDrop</span><span class="sxs-lookup"><span data-stu-id="c5eb5-103">DlpNotifyPostDragDrop function</span></span>

<span data-ttu-id="c5eb5-104">Proporciona al sistema información sobre un documento una vez completada una operación de arrastrar y colocar.</span><span class="sxs-lookup"><span data-stu-id="c5eb5-104">Provides the system with information about a document after a drag drop operation is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5eb5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c5eb5-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostDragDrop(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
```



## <a name="parameters"></a><span data-ttu-id="c5eb5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c5eb5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5eb5-107">*DocumentInfo* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="c5eb5-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5eb5-108">Puntero a una estructura [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) que contiene información sobre el documento asociado a la operación de arrastrar y colocar.</span><span class="sxs-lookup"><span data-stu-id="c5eb5-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document associated with the drag drop operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="c5eb5-109">*OpStatus* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="c5eb5-109">*OpStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5eb5-110">Puntero a una estructura [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) que contiene información de estado sobre la colocación de arrastre.</span><span class="sxs-lookup"><span data-stu-id="c5eb5-110">A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the drag drop.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="c5eb5-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c5eb5-111">Return value</span></span>

<span data-ttu-id="c5eb5-112">Devuelve void.</span><span class="sxs-lookup"><span data-stu-id="c5eb5-112">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5eb5-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c5eb5-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="c5eb5-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5eb5-114">Requirements</span></span>



| <span data-ttu-id="c5eb5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5eb5-115">Requirement</span></span>          |    <span data-ttu-id="c5eb5-116">Value</span><span class="sxs-lookup"><span data-stu-id="c5eb5-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5eb5-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5eb5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c5eb5-118">Windows 10, versión 1809 (10.0; Compilación 17763)</span><span class="sxs-lookup"><span data-stu-id="c5eb5-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="c5eb5-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c5eb5-119">DLL</span></span><br/>                      | <span data-ttu-id="c5eb5-120">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="c5eb5-120">EndpointDlp.dll</span></span> |