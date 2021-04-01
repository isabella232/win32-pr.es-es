---
title: Enumeración ControlCloseStatus
description: Indica si la aplicación que contiene el control puede cerrar el control inmediatamente.
ms.assetid: ac2e1c68-81b1-4b51-aa7e-0ff703e619a2
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto enumeración ControlCloseStatus
topic_type:
- apiref
api_name:
- ControlCloseStatus
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6b94e0ce5cd040a2ade970f566897d2eac339dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996025"
---
# <a name="controlclosestatus-enumeration"></a><span data-ttu-id="6ecee-104">Enumeración ControlCloseStatus</span><span class="sxs-lookup"><span data-stu-id="6ecee-104">ControlCloseStatus enumeration</span></span>

<span data-ttu-id="6ecee-105">Indica si la aplicación que contiene el control puede cerrar el control inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="6ecee-105">Indicates whether the application containing the control can close the control immediately.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ecee-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6ecee-106">Syntax</span></span>


```C++
enum ControlCloseStatus {
  controlCloseCanProceed     = 0x0000, 
  controlCloseWaitForEvents  = 0x0001 

};
```



## <a name="constants"></a><span data-ttu-id="6ecee-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="6ecee-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6ecee-108"><span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>**controlCloseCanProceed**</span><span class="sxs-lookup"><span data-stu-id="6ecee-108"><span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>**controlCloseCanProceed**</span></span>
</dt> <dd>

<span data-ttu-id="6ecee-109">El contenedor puede continuar con el cierre inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="6ecee-109">Container can go ahead with close immediately.</span></span> <span data-ttu-id="6ecee-110">Esto puede ocurrir si el control no está conectado.</span><span class="sxs-lookup"><span data-stu-id="6ecee-110">This can happen if the control is not connected.</span></span>

</dd> <dt>

<span data-ttu-id="6ecee-111"><span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>**controlCloseWaitForEvents**</span><span class="sxs-lookup"><span data-stu-id="6ecee-111"><span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>**controlCloseWaitForEvents**</span></span>
</dt> <dd>

<span data-ttu-id="6ecee-112">El contenedor debe esperar los eventos [**IMsTscAxEvents:: OnDisconnect**](imstscaxevents-ondisconnected.md) o [**IMsTscAxEvents:: OnConfirmClose**](imstscaxevents-onconfirmclose.md).</span><span class="sxs-lookup"><span data-stu-id="6ecee-112">Container should wait for events [**IMsTscAxEvents::OnDisconnected**](imstscaxevents-ondisconnected.md) or [**IMsTscAxEvents::OnConfirmClose**](imstscaxevents-onconfirmclose.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6ecee-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ecee-113">Requirements</span></span>



| <span data-ttu-id="6ecee-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ecee-114">Requirement</span></span> | <span data-ttu-id="6ecee-115">Value</span><span class="sxs-lookup"><span data-stu-id="6ecee-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ecee-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ecee-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6ecee-117">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="6ecee-117">Windows 8.1</span></span><br/>                                                                 |
| <span data-ttu-id="6ecee-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ecee-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6ecee-119">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="6ecee-119">Windows Server 2012 R2</span></span><br/>                                                      |
| <span data-ttu-id="6ecee-120">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6ecee-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="6ecee-121"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ecee-121"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ecee-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ecee-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ecee-123">**IMsRdpClient::RequestClose**</span><span class="sxs-lookup"><span data-stu-id="6ecee-123">**IMsRdpClient::RequestClose**</span></span>](imsrdpclient-requestclose.md)
</dt> <dt>

[<span data-ttu-id="6ecee-124">**IMsTscAxEvents::OnConfirmClose**</span><span class="sxs-lookup"><span data-stu-id="6ecee-124">**IMsTscAxEvents::OnConfirmClose**</span></span>](imstscaxevents-onconfirmclose.md)
</dt> <dt>

[<span data-ttu-id="6ecee-125">**IMsTscAxEvents:: OnDisconnection**</span><span class="sxs-lookup"><span data-stu-id="6ecee-125">**IMsTscAxEvents::OnDisconnected**</span></span>](imstscaxevents-ondisconnected.md)
</dt> </dl>

 

 





