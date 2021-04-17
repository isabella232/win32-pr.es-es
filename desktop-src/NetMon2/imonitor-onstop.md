---
description: El monitor debe implementar el método OnStop. MSCVC llama a este método para notificar al monitor que se va a detener la captura.
ms.assetid: 5988bfb8-2068-42a1-a774-6f6be9828568
title: 'IMonitor:: OnStop (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnStop
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: a737aa5bede443b63f2074239eec17ea8a205cc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677274"
---
# <a name="imonitoronstop-method"></a><span data-ttu-id="7b78f-104">IMonitor:: OnStop (método)</span><span class="sxs-lookup"><span data-stu-id="7b78f-104">IMonitor::OnStop method</span></span>

<span data-ttu-id="7b78f-105">El monitor debe implementar el método **OnStop** .</span><span class="sxs-lookup"><span data-stu-id="7b78f-105">The **OnStop** method must be implemented by the monitor.</span></span> <span data-ttu-id="7b78f-106">MSCVC llama a este método para notificar al monitor que se va a detener la captura.</span><span class="sxs-lookup"><span data-stu-id="7b78f-106">The MSCVC calls this method to notify the monitor that the capture will be stopped.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b78f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7b78f-107">Syntax</span></span>


```C++
HRESULT OnStop();
```



## <a name="parameters"></a><span data-ttu-id="7b78f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7b78f-108">Parameters</span></span>

<span data-ttu-id="7b78f-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="7b78f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7b78f-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7b78f-110">Return value</span></span>

<span data-ttu-id="7b78f-111">Si el método se realiza correctamente, el valor devuelto es S \_ OK (que es igual que NoError).</span><span class="sxs-lookup"><span data-stu-id="7b78f-111">If the method is successful, the return value is S\_OK (which is the same as NOERROR).</span></span>

<span data-ttu-id="7b78f-112">Si el método no se realiza correctamente, el valor devuelto es un código de error.</span><span class="sxs-lookup"><span data-stu-id="7b78f-112">If the method is unsuccessful, the return value is an error code.</span></span> <span data-ttu-id="7b78f-113">Cuando se devuelve un código de error, el monitor no se puede reiniciar.</span><span class="sxs-lookup"><span data-stu-id="7b78f-113">When an error code is returned, the monitor cannot be restarted.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b78f-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7b78f-114">Remarks</span></span>

<span data-ttu-id="7b78f-115">MCSVC llama a este método después de llamar a [IRTC:: Stop](irtc-stop.md) .</span><span class="sxs-lookup"><span data-stu-id="7b78f-115">The MCSVC calls this method after [IRTC::Stop](irtc-stop.md) is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b78f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b78f-116">Requirements</span></span>



| <span data-ttu-id="7b78f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b78f-117">Requirement</span></span> | <span data-ttu-id="7b78f-118">Value</span><span class="sxs-lookup"><span data-stu-id="7b78f-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7b78f-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7b78f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7b78f-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7b78f-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="7b78f-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7b78f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7b78f-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7b78f-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7b78f-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7b78f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b78f-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b78f-124"><dt>Netmon.h</dt></span></span> </dl> |



 

 




