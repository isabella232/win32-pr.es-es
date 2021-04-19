---
description: Proporciona al sistema información sobre un documento antes de que se inicie una operación de almacenamiento escalonado en el Portapapeles.
title: Función DlpNotifyPreStashClipboard (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreStashClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 72ecabb2bbfb7517b52790c0d3b7c1ab8075dbd0
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495823"
---
# <a name="dlpnotifyprestashclipboard-function"></a><span data-ttu-id="e512a-103">Función DlpNotifyPreStashClipboard</span><span class="sxs-lookup"><span data-stu-id="e512a-103">DlpNotifyPreStashClipboard function</span></span>

<span data-ttu-id="e512a-104">Notifica al sistema antes de que se inicie una operación de almacenamiento escalonado en el Portapapeles.</span><span class="sxs-lookup"><span data-stu-id="e512a-104">Notifies the system before a stash clipboard operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="e512a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e512a-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPreStashClipboard();
```



## <a name="parameters"></a><span data-ttu-id="e512a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e512a-106">Parameters</span></span>




## <a name="return-value"></a><span data-ttu-id="e512a-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e512a-107">Return value</span></span>

<span data-ttu-id="e512a-108">Devuelve void.</span><span class="sxs-lookup"><span data-stu-id="e512a-108">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="e512a-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e512a-109">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="e512a-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e512a-110">Requirements</span></span>



| <span data-ttu-id="e512a-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="e512a-111">Requirement</span></span>          |    <span data-ttu-id="e512a-112">Value</span><span class="sxs-lookup"><span data-stu-id="e512a-112">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e512a-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e512a-113">Minimum supported client</span></span><br/> | <span data-ttu-id="e512a-114">Windows 10, versión 1809 (10.0; Compilación 17763)</span><span class="sxs-lookup"><span data-stu-id="e512a-114">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="e512a-115">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e512a-115">DLL</span></span><br/>                      | <span data-ttu-id="e512a-116">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="e512a-116">EndpointDlp.dll</span></span> |