---
description: Proporciona al sistema información sobre un documento antes de iniciar una operación de guardar como.
title: Función DlpNotifyPreSaveAsDocument (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreSaveAsDocument
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 5226ed63227e2d9dd01155066e2e6e19f77e063f
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495820"
---
# <a name="dlpnotifypresaveasdocument-function"></a><span data-ttu-id="7352a-103">Función DlpNotifyPreSaveAsDocument</span><span class="sxs-lookup"><span data-stu-id="7352a-103">DlpNotifyPreSaveAsDocument function</span></span>

<span data-ttu-id="7352a-104">Proporciona al sistema información sobre un documento antes de iniciar una operación de guardar como.</span><span class="sxs-lookup"><span data-stu-id="7352a-104">Provides the system with information about a document before a save as operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="7352a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7352a-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPreSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination);
```



## <a name="parameters"></a><span data-ttu-id="7352a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7352a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7352a-107">*DocumentInfo* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="7352a-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7352a-108">Puntero a una estructura [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) que contiene información sobre el documento que se va a guardar.</span><span class="sxs-lookup"><span data-stu-id="7352a-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document to be saved.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="7352a-109">*Destino* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="7352a-109">*Destination* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7352a-110">**LPCWSTR que** contiene la ruta de acceso de destino del documento que se va a guardar.</span><span class="sxs-lookup"><span data-stu-id="7352a-110">A **LPCWSTR** containing the destination path of the document to be saved.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="7352a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7352a-111">Return value</span></span>

<span data-ttu-id="7352a-112">Devuelve void.</span><span class="sxs-lookup"><span data-stu-id="7352a-112">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="7352a-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7352a-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="7352a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7352a-114">Requirements</span></span>



| <span data-ttu-id="7352a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7352a-115">Requirement</span></span>          |    <span data-ttu-id="7352a-116">Value</span><span class="sxs-lookup"><span data-stu-id="7352a-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7352a-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7352a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7352a-118">Windows 10, versión 1809 (10.0; Compilación 17763)</span><span class="sxs-lookup"><span data-stu-id="7352a-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="7352a-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7352a-119">DLL</span></span><br/>                      | <span data-ttu-id="7352a-120">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="7352a-120">EndpointDlp.dll</span></span> |