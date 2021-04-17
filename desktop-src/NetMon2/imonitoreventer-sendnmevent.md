---
description: El método SendNMEvent envía eventos a Instrumental de administración de Windows (WMI).
ms.assetid: 85c33a71-72aa-4b0a-8e8b-3a220a080bb2
title: 'IMonitorEventer:: SendNMEvent (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer.SendNMEvent
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 3286fca4d5b852d4562c13446699c1a6b40f3efe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677518"
---
# <a name="imonitoreventersendnmevent-method"></a><span data-ttu-id="10b44-103">IMonitorEventer:: SendNMEvent (método)</span><span class="sxs-lookup"><span data-stu-id="10b44-103">IMonitorEventer::SendNMEvent method</span></span>

<span data-ttu-id="10b44-104">El método **SendNMEvent** envía eventos a instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="10b44-104">The **SendNMEvent** method submits events to Windows Management Instrumentation (WMI).</span></span>

## <a name="syntax"></a><span data-ttu-id="10b44-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="10b44-105">Syntax</span></span>


```C++
HRESULT SendNMEvent(
  [in] PNMEVENTDATA pNMEventData
);
```



## <a name="parameters"></a><span data-ttu-id="10b44-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="10b44-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10b44-107">*pNMEventData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="10b44-107">*pNMEventData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10b44-108">Puntero al evento enviado a WMI.</span><span class="sxs-lookup"><span data-stu-id="10b44-108">Pointer to the event submitted to WMI.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10b44-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="10b44-109">Return value</span></span>

<span data-ttu-id="10b44-110">Si el método se realiza correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="10b44-110">If the method is successful, the return value is S\_OK.</span></span>

<span data-ttu-id="10b44-111">Si el método no se realiza correctamente, el valor devuelto es \_ NMERR \_ de \_ memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="10b44-111">If the method is unsuccessful, the return value is NMERR\_OUT\_OF\_MEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="10b44-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10b44-112">Requirements</span></span>



| <span data-ttu-id="10b44-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="10b44-113">Requirement</span></span> | <span data-ttu-id="10b44-114">Value</span><span class="sxs-lookup"><span data-stu-id="10b44-114">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="10b44-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10b44-115">Minimum supported client</span></span><br/> | <span data-ttu-id="10b44-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="10b44-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="10b44-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10b44-117">Minimum supported server</span></span><br/> | <span data-ttu-id="10b44-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="10b44-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="10b44-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="10b44-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="10b44-120"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="10b44-120"><dt>Netmon.h</dt></span></span> </dl> |



 

 




