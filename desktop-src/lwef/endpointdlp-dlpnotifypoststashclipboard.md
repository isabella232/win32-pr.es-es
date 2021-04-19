---
description: Proporciona al sistema información de estado una vez completada una operación de almacenamiento escalonado del Portapapeles.
title: Función DlpNotifyPostStashClipboard (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostStashClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: e549593acab6d74edf838a0f82952d8f3034bfcc
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495859"
---
# <a name="dlpnotifypoststashclipboard-function"></a><span data-ttu-id="6fa2e-103">Función DlpNotifyPostStashClipboard</span><span class="sxs-lookup"><span data-stu-id="6fa2e-103">DlpNotifyPostStashClipboard function</span></span>

<span data-ttu-id="6fa2e-104">Proporciona al sistema información de estado una vez completada una operación de almacenamiento escalonado del Portapapeles.</span><span class="sxs-lookup"><span data-stu-id="6fa2e-104">Provides the system with status information after a stash clipboard operation is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fa2e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6fa2e-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostStashClipboard(_In_ const PDLP_POSTOP_STATUS OpStatus);
```



## <a name="parameters"></a><span data-ttu-id="6fa2e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6fa2e-106">Parameters</span></span>


<dl> <dt>

<span data-ttu-id="6fa2e-107">*OpStatus* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="6fa2e-107">*OpStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fa2e-108">Puntero a una estructura [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) que contiene información de estado sobre la operación de stash del Portapapeles.</span><span class="sxs-lookup"><span data-stu-id="6fa2e-108">A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the stash clipboard operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="6fa2e-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6fa2e-109">Return value</span></span>

<span data-ttu-id="6fa2e-110">Devuelve void.</span><span class="sxs-lookup"><span data-stu-id="6fa2e-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fa2e-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6fa2e-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="6fa2e-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fa2e-112">Requirements</span></span>



| <span data-ttu-id="6fa2e-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fa2e-113">Requirement</span></span>          |    <span data-ttu-id="6fa2e-114">Value</span><span class="sxs-lookup"><span data-stu-id="6fa2e-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6fa2e-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6fa2e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="6fa2e-116">Windows 10, versión 1809 (10.0; Compilación 17763)</span><span class="sxs-lookup"><span data-stu-id="6fa2e-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="6fa2e-117">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6fa2e-117">DLL</span></span><br/>                      | <span data-ttu-id="6fa2e-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="6fa2e-118">EndpointDlp.dll</span></span> |