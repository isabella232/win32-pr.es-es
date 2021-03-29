---
title: IRemoteDesktopClientEvents OnAutoReconnecting, método
description: Se llama cuando el control de cliente intenta restablecer automáticamente una conexión a una sesión remota.
ms.assetid: 299408A9-ED14-42F4-B324-AF4C86FEDABE
ms.tgt_platform: multiple
keywords:
- Método OnAutoReconnecting Servicios de Escritorio remoto
- Método OnAutoReconnecting Servicios de Escritorio remoto, interfaz IRemoteDesktopClientEvents
- Interfaz IRemoteDesktopClientEvents Servicios de Escritorio remoto, método OnAutoReconnecting
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnAutoReconnecting
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d74c37919384727fdf51aad004349478798a3ffd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535392"
---
# <a name="iremotedesktopclienteventsonautoreconnecting-method"></a><span data-ttu-id="59b28-106">IRemoteDesktopClientEvents:: OnAutoReconnecting (método)</span><span class="sxs-lookup"><span data-stu-id="59b28-106">IRemoteDesktopClientEvents::OnAutoReconnecting method</span></span>

<span data-ttu-id="59b28-107">Se llama cuando el control de cliente intenta restablecer automáticamente una conexión a una sesión remota.</span><span class="sxs-lookup"><span data-stu-id="59b28-107">Called when the client control attempts to automatically reestablish a connection to a remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="59b28-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="59b28-108">Syntax</span></span>


```C++
void OnAutoReconnecting(
  [in] long         disconnectReason,
  [in] long         ExtendedDisconnectReason,
  [in] BSTR         disconnectErrorMessage,
  [in] VARIANT_BOOL networkAvailable,
  [in] long         attemptCount,
  [in] long         maxAttemptCount
);
```



## <a name="parameters"></a><span data-ttu-id="59b28-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="59b28-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59b28-110">*disconnectReason* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="59b28-110">*disconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59b28-111">Motivo del evento de desconexión.</span><span class="sxs-lookup"><span data-stu-id="59b28-111">The reason for the disconnect event.</span></span>

</dd> <dt>

<span data-ttu-id="59b28-112">*ExtendedDisconnectReason* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="59b28-112">*ExtendedDisconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59b28-113">Información extendida para el evento de desconexión.</span><span class="sxs-lookup"><span data-stu-id="59b28-113">Extended information for the disconnect event.</span></span>

</dd> <dt>

<span data-ttu-id="59b28-114">*disconnectErrorMessage* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="59b28-114">*disconnectErrorMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59b28-115">Mensaje de error para el evento de desconexión.</span><span class="sxs-lookup"><span data-stu-id="59b28-115">The error message for the disconnect event.</span></span>

</dd> <dt>

<span data-ttu-id="59b28-116">*networkAvailable* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="59b28-116">*networkAvailable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59b28-117">Si la red está disponible.</span><span class="sxs-lookup"><span data-stu-id="59b28-117">Whether the network is available.</span></span>

</dd> <dt>

<span data-ttu-id="59b28-118">*attemptCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="59b28-118">*attemptCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59b28-119">Qué intento es.</span><span class="sxs-lookup"><span data-stu-id="59b28-119">Which attempt this is.</span></span>

</dd> <dt>

<span data-ttu-id="59b28-120">*maxAttemptCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="59b28-120">*maxAttemptCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59b28-121">Se realizará el número máximo de intentos de reconexión.</span><span class="sxs-lookup"><span data-stu-id="59b28-121">The maximum number of reconnect attempts will be performed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59b28-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="59b28-122">Return value</span></span>

<span data-ttu-id="59b28-123">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="59b28-123">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="59b28-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59b28-124">Requirements</span></span>



| <span data-ttu-id="59b28-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="59b28-125">Requirement</span></span> | <span data-ttu-id="59b28-126">Value</span><span class="sxs-lookup"><span data-stu-id="59b28-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59b28-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="59b28-127">Minimum supported client</span></span><br/> | <span data-ttu-id="59b28-128">Windows 8</span><span class="sxs-lookup"><span data-stu-id="59b28-128">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="59b28-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="59b28-129">Minimum supported server</span></span><br/> | <span data-ttu-id="59b28-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="59b28-130">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="59b28-131">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="59b28-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="59b28-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59b28-132"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="59b28-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="59b28-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59b28-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59b28-134"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="59b28-135">IID</span><span class="sxs-lookup"><span data-stu-id="59b28-135">IID</span></span><br/>                      | <span data-ttu-id="59b28-136">DIID \_ IRemoteDesktopClientEvents se define como 079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="59b28-136">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="59b28-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="59b28-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59b28-138">**IRemoteDesktopClientEvents**</span><span class="sxs-lookup"><span data-stu-id="59b28-138">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





