---
description: Detiene el modo de receptor de Miracast, desactiva la detectabilidad y anula el registro de la devolución de llamada.
ms.assetid: 38AE60CB-F601-4C03-A725-9B802341B84B
title: Función WFDDisplaySinkStop (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDStopDisplaySink
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: d1ebaa9920ca7d38cff22cef6383b37065faa2ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677585"
---
# <a name="wfddisplaysinkstop-function"></a><span data-ttu-id="afc22-103">WFDDisplaySinkStop función)</span><span class="sxs-lookup"><span data-stu-id="afc22-103">WFDDisplaySinkStop function</span></span>

<span data-ttu-id="afc22-104">Detiene el modo de receptor de Miracast, desactiva la detectabilidad y anula el registro de la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="afc22-104">Stops the Miracast sink mode, turns off discoverability, and un-registers the callback.</span></span> <span data-ttu-id="afc22-105">La aplicación debe llamarla una vez al apagar.</span><span class="sxs-lookup"><span data-stu-id="afc22-105">Your app should call this once on shutdown.</span></span>

## <a name="syntax"></a><span data-ttu-id="afc22-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="afc22-106">Syntax</span></span>


```C++
DWORD WINAPI WFDStopDisplaySink(void);
```



## <a name="parameters"></a><span data-ttu-id="afc22-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="afc22-107">Parameters</span></span>

<span data-ttu-id="afc22-108">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="afc22-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="afc22-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="afc22-109">Return value</span></span>

<span data-ttu-id="afc22-110">Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="afc22-110">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

## <a name="remarks"></a><span data-ttu-id="afc22-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="afc22-111">Remarks</span></span>

<span data-ttu-id="afc22-112">Se espera que la aplicación haya desbloqueado las devoluciones de llamada en curso antes de llamar a **WFDStopDisplaySink**.</span><span class="sxs-lookup"><span data-stu-id="afc22-112">It is expected that your app has unblocked any callbacks in progress before calling **WFDStopDisplaySink**.</span></span>

## <a name="requirements"></a><span data-ttu-id="afc22-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="afc22-113">Requirements</span></span>



| <span data-ttu-id="afc22-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="afc22-114">Requirement</span></span> | <span data-ttu-id="afc22-115">Value</span><span class="sxs-lookup"><span data-stu-id="afc22-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="afc22-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="afc22-116">Minimum supported client</span></span><br/> | <span data-ttu-id="afc22-117">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="afc22-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="afc22-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="afc22-118">Minimum supported server</span></span><br/> | <span data-ttu-id="afc22-119">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="afc22-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="afc22-120">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="afc22-120">End of client support</span></span><br/>    | <span data-ttu-id="afc22-121">Windows 10</span><span class="sxs-lookup"><span data-stu-id="afc22-121">Windows 10</span></span><br/>                                                                      |
| <span data-ttu-id="afc22-122">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="afc22-122">End of server support</span></span><br/>    | <span data-ttu-id="afc22-123">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="afc22-123">Windows Server 2016</span></span><br/>                                                             |
| <span data-ttu-id="afc22-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="afc22-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="afc22-125"><dt>Wfdsink. h</dt></span><span class="sxs-lookup"><span data-stu-id="afc22-125"><dt>Wfdsink.h</dt></span></span> </dl>       |
| <span data-ttu-id="afc22-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="afc22-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="afc22-127"><dt>Wifidisplay. lib</dt></span><span class="sxs-lookup"><span data-stu-id="afc22-127"><dt>Wifidisplay.lib</dt></span></span> </dl> |
| <span data-ttu-id="afc22-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="afc22-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="afc22-129"><dt>Wifidisplay.dll</dt></span><span class="sxs-lookup"><span data-stu-id="afc22-129"><dt>Wifidisplay.dll</dt></span></span> </dl> |



 

 




