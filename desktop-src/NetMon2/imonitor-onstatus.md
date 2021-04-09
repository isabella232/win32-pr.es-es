---
description: El método MCSVC llama al método de estado para notificar al monitor que existe un evento de estado NPP. Este método debe ser implementado por el monitor.
ms.assetid: 771852b1-77d8-4d7d-b3fb-03eb3ea593b8
title: 'IMonitor:: alstatus (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnStatus
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: fc2716a10673cc1178591b14a335b1d8559aa35a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155108"
---
# <a name="imonitoronstatus-method"></a><span data-ttu-id="71f50-104">IMonitor:: alstatus (método)</span><span class="sxs-lookup"><span data-stu-id="71f50-104">IMonitor::OnStatus method</span></span>

<span data-ttu-id="71f50-105">El método MCSVC llama al método de **Estado** para notificar al monitor que existe un evento de estado NPP.</span><span class="sxs-lookup"><span data-stu-id="71f50-105">The MCSVC method calls the **OnStatus** method to notify the monitor that an NPP status event exists.</span></span> <span data-ttu-id="71f50-106">Este método debe ser implementado por el monitor.</span><span class="sxs-lookup"><span data-stu-id="71f50-106">This method must be implemented by the monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="71f50-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="71f50-107">Syntax</span></span>


```C++
HRESULT OnStatus(
  [in] UPDATE_EVENT Event
);
```



## <a name="parameters"></a><span data-ttu-id="71f50-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="71f50-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71f50-109">*Evento* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="71f50-109">*Event* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71f50-110">Una estructura de [ \_ eventos de actualización](update-event.md) .</span><span class="sxs-lookup"><span data-stu-id="71f50-110">An [UPDATE\_EVENT](update-event.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71f50-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="71f50-111">Return value</span></span>

<span data-ttu-id="71f50-112">Si el método se realiza correctamente, el valor devuelto es S \_ OK (que es igual que NoError) y MCSVC devuelve el valor devuelto a NPP para su procesamiento.</span><span class="sxs-lookup"><span data-stu-id="71f50-112">If the method is successful, the return value is S\_OK (which is the same as NOERROR), and the MCSVC passes the returned value back to the NPP for processing.</span></span>

<span data-ttu-id="71f50-113">Si el método no se realiza correctamente, devuelve un código de error.</span><span class="sxs-lookup"><span data-stu-id="71f50-113">If the method is unsuccessful, return an error code.</span></span> <span data-ttu-id="71f50-114">En caso de error, MCSVC devuelve el valor devuelto a NPP para su procesamiento.</span><span class="sxs-lookup"><span data-stu-id="71f50-114">On error, the MCSVC passes the returned value back to the NPP for processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="71f50-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71f50-115">Requirements</span></span>



| <span data-ttu-id="71f50-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="71f50-116">Requirement</span></span> | <span data-ttu-id="71f50-117">Value</span><span class="sxs-lookup"><span data-stu-id="71f50-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="71f50-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71f50-118">Minimum supported client</span></span><br/> | <span data-ttu-id="71f50-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="71f50-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="71f50-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71f50-120">Minimum supported server</span></span><br/> | <span data-ttu-id="71f50-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="71f50-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="71f50-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="71f50-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="71f50-123"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="71f50-123"><dt>Netmon.h</dt></span></span> </dl> |



 

 




