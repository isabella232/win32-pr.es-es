---
description: El monitor debe implementar el método biframes. MCSVC llama a este método cuando el búfer de captura está lleno o se ha superado el tiempo de actualización.
ms.assetid: 243bd35b-2527-463e-b3d2-4bd840fe9c3f
title: 'IMonitor:: biframes (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnFrames
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: c5b6ff3e9d5b97a228e6e1d865fe4d8f1b5bfc9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809464"
---
# <a name="imonitoronframes-method"></a><span data-ttu-id="8506b-104">IMonitor:: alframes (método)</span><span class="sxs-lookup"><span data-stu-id="8506b-104">IMonitor::OnFrames method</span></span>

<span data-ttu-id="8506b-105">El monitor debe implementar el método **Biframes** .</span><span class="sxs-lookup"><span data-stu-id="8506b-105">The **OnFrames** method must be implemented by the monitor.</span></span> <span data-ttu-id="8506b-106">MCSVC llama a este método cuando el búfer de captura está lleno o se ha superado el tiempo de actualización.</span><span class="sxs-lookup"><span data-stu-id="8506b-106">The MCSVC calls this method when either the capture buffer is full or the update time has passed.</span></span>

## <a name="syntax"></a><span data-ttu-id="8506b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8506b-107">Syntax</span></span>


```C++
HRESULT OnFrames(
  [in] UPDATE_EVENT Event
);
```



## <a name="parameters"></a><span data-ttu-id="8506b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8506b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8506b-109">*Evento* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="8506b-109">*Event* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8506b-110">[Actualización \_ de ](update-event.md) Estructura de eventos que contiene la información del marco utilizada para actualizar los eventos.</span><span class="sxs-lookup"><span data-stu-id="8506b-110">[UPDATE\_EVENT](update-event.md) structure that holds frame information used to update events.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8506b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8506b-111">Return value</span></span>

<span data-ttu-id="8506b-112">Si el método se realiza correctamente, el valor devuelto es S \_ OK (que es igual que NoError).</span><span class="sxs-lookup"><span data-stu-id="8506b-112">If the method is successful, the return value is S\_OK (which is the same as NOERROR).</span></span> <span data-ttu-id="8506b-113">El MCSVC devuelve el valor devuelto a NPP para su procesamiento.</span><span class="sxs-lookup"><span data-stu-id="8506b-113">The MCSVC passes the returned value back to the NPP for processing.</span></span>

<span data-ttu-id="8506b-114">Si el método no se realiza correctamente, el valor devuelto es un código de error.</span><span class="sxs-lookup"><span data-stu-id="8506b-114">If the method is unsuccessful, the return value is an error code.</span></span> <span data-ttu-id="8506b-115">El MCSVC devuelve el valor devuelto a NPP para su procesamiento.</span><span class="sxs-lookup"><span data-stu-id="8506b-115">The MCSVC passes the returned value back to the NPP for processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="8506b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8506b-116">Requirements</span></span>



| <span data-ttu-id="8506b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8506b-117">Requirement</span></span> | <span data-ttu-id="8506b-118">Value</span><span class="sxs-lookup"><span data-stu-id="8506b-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8506b-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8506b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8506b-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8506b-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8506b-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8506b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8506b-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8506b-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8506b-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8506b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8506b-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="8506b-124"><dt>Netmon.h</dt></span></span> </dl> |



 

 




