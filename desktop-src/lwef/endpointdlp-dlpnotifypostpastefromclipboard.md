---
description: Proporciona al sistema información sobre un documento una vez completada una operación de pegado desde el Portapapeles.
title: Función DlpNotifyPostPasteFromClipboard (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostPasteFromClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 69a5afbc41350092ebd4d433d2f4d7259ece82cf
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495867"
---
# <a name="dlpnotifypostpastefromclipboard-function"></a><span data-ttu-id="cd777-103">Función DlpNotifyPostPasteFromClipboard</span><span class="sxs-lookup"><span data-stu-id="cd777-103">DlpNotifyPostPasteFromClipboard function</span></span>

<span data-ttu-id="cd777-104">Proporciona al sistema información sobre un documento una vez completada una operación de pegado desde el Portapapeles.</span><span class="sxs-lookup"><span data-stu-id="cd777-104">Provides the system with information about a document after a paste from clipboard operation is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd777-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cd777-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostPasteFromClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
```



## <a name="parameters"></a><span data-ttu-id="cd777-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd777-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd777-107">*DocumentInfo* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="cd777-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd777-108">Puntero a una estructura [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) que contiene información sobre el documento en el que se copió el contenido.</span><span class="sxs-lookup"><span data-stu-id="cd777-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document into which content was copied.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="cd777-109">*OpStatus* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="cd777-109">*OpStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd777-110">Puntero a una estructura [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) que contiene información de estado sobre la operación pegar del Portapapeles.</span><span class="sxs-lookup"><span data-stu-id="cd777-110">A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the paste from clipboard operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="cd777-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd777-111">Return value</span></span>

<span data-ttu-id="cd777-112">Devuelve void.</span><span class="sxs-lookup"><span data-stu-id="cd777-112">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd777-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cd777-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="cd777-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd777-114">Requirements</span></span>



| <span data-ttu-id="cd777-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd777-115">Requirement</span></span>          |    <span data-ttu-id="cd777-116">Value</span><span class="sxs-lookup"><span data-stu-id="cd777-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd777-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cd777-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cd777-118">Windows 10, versión 1809 (10.0; Compilación 17763)</span><span class="sxs-lookup"><span data-stu-id="cd777-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="cd777-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cd777-119">DLL</span></span><br/>                      | <span data-ttu-id="cd777-120">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="cd777-120">EndpointDlp.dll</span></span> |