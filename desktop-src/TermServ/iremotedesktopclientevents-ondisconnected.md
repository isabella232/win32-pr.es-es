---
title: IRemoteDesktopClientEvents método OnDisconnect
description: Se llama cuando el control de cliente se ha desconectado de una sesión remota.
ms.assetid: EA26B530-0AA8-49D6-8E3C-E53179FC5104
ms.tgt_platform: multiple
keywords:
- Método OnDisconnection Servicios de Escritorio remoto
- Método OnDisconnection Servicios de Escritorio remoto, interfaz IRemoteDesktopClientEvents
- Interfaz IRemoteDesktopClientEvents Servicios de Escritorio remoto, método OnDisconnect
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnDisconnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bd59b03fe9cb23309d53773289291c8a791935a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802936"
---
# <a name="iremotedesktopclienteventsondisconnected-method"></a><span data-ttu-id="5a118-106">IRemoteDesktopClientEvents:: OnDisconnection (método)</span><span class="sxs-lookup"><span data-stu-id="5a118-106">IRemoteDesktopClientEvents::OnDisconnected method</span></span>

<span data-ttu-id="5a118-107">Se llama cuando el control de cliente se ha desconectado de una sesión remota.</span><span class="sxs-lookup"><span data-stu-id="5a118-107">Called when the client control has been disconnected from a remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a118-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5a118-108">Syntax</span></span>


```C++
void OnDisconnected(
  [in] long disconnectReason,
  [in] long ExtendedDisconnectReason,
  [in] BSTR disconnectErrorMessage
);
```



## <a name="parameters"></a><span data-ttu-id="5a118-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5a118-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a118-110">*disconnectReason* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5a118-110">*disconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a118-111">Motivo del evento de desconexión.</span><span class="sxs-lookup"><span data-stu-id="5a118-111">The reason for the disconnect event.</span></span>

</dd> <dt>

<span data-ttu-id="5a118-112">*ExtendedDisconnectReason* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5a118-112">*ExtendedDisconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a118-113">Información extendida para el evento de desconexión.</span><span class="sxs-lookup"><span data-stu-id="5a118-113">Extended information for the disconnect event.</span></span>

</dd> <dt>

<span data-ttu-id="5a118-114">*disconnectErrorMessage* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5a118-114">*disconnectErrorMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a118-115">Mensaje de error para el evento de desconexión.</span><span class="sxs-lookup"><span data-stu-id="5a118-115">The error message for the disconnect event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a118-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5a118-116">Return value</span></span>

<span data-ttu-id="5a118-117">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="5a118-117">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a118-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a118-118">Requirements</span></span>



| <span data-ttu-id="5a118-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a118-119">Requirement</span></span> | <span data-ttu-id="5a118-120">Value</span><span class="sxs-lookup"><span data-stu-id="5a118-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a118-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a118-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5a118-122">Windows 8</span><span class="sxs-lookup"><span data-stu-id="5a118-122">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="5a118-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a118-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5a118-124">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5a118-124">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="5a118-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="5a118-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="5a118-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a118-126"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="5a118-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5a118-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a118-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a118-128"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="5a118-129">IID</span><span class="sxs-lookup"><span data-stu-id="5a118-129">IID</span></span><br/>                      | <span data-ttu-id="5a118-130">DIID \_ IRemoteDesktopClientEvents se define como 079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="5a118-130">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5a118-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="5a118-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a118-132">**IRemoteDesktopClientEvents**</span><span class="sxs-lookup"><span data-stu-id="5a118-132">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





