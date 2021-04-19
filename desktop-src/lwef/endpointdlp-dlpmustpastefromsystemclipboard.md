---
description: Determina si la aplicación debe extraer los datos del Portapapeles del sistema en lugar de tomar los datos de su caché interna.
title: Función DlpMustPasteFromSystemClipboard (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpMustPasteFromSystemClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 5863173b02cb5c63a2de46653c2d268464e82e65
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495916"
---
# <a name="dlpmustpastefromsystemclipboard-function"></a><span data-ttu-id="31272-103">Función DlpMustPasteFromSystemClipboard</span><span class="sxs-lookup"><span data-stu-id="31272-103">DlpMustPasteFromSystemClipboard function</span></span>

<span data-ttu-id="31272-104">Determina si la aplicación debe extraer los datos del Portapapeles del sistema en lugar de tomar los datos de su caché interna.</span><span class="sxs-lookup"><span data-stu-id="31272-104">Determines whether the app must pull the data from the system clipboard rather than taking it from its internal cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="31272-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="31272-105">Syntax</span></span>


```C++
BOOL WINAPI DlpMustPasteFromSystemClipboard();
```


## <a name="return-value"></a><span data-ttu-id="31272-106">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="31272-106">Return value</span></span>

<span data-ttu-id="31272-107">TRUE si es obligatorio llamar al Portapapeles del sistema operativo; de lo contrario, FALSE.</span><span class="sxs-lookup"><span data-stu-id="31272-107">TRUE if calling into the OS clipboard is mandatory; otherwise, FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="31272-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="31272-108">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="31272-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31272-109">Requirements</span></span>



| <span data-ttu-id="31272-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="31272-110">Requirement</span></span>          |    <span data-ttu-id="31272-111">Value</span><span class="sxs-lookup"><span data-stu-id="31272-111">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31272-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31272-112">Minimum supported client</span></span><br/> | <span data-ttu-id="31272-113">Windows 10, versión 1809 (10.0; Compilación 17763)</span><span class="sxs-lookup"><span data-stu-id="31272-113">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="31272-114">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="31272-114">DLL</span></span><br/>                      | <span data-ttu-id="31272-115">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="31272-115">EndpointDlp.dll</span></span> |