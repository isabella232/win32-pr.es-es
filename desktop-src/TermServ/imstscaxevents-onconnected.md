---
title: IMsTscAxEvents método de conexión
description: Se llama cuando el control de cliente está en proceso de establecer una conexión con Escritorio remoto un servidor host de sesión de escritorio remoto (host de sesión de RD).
ms.assetid: 9c26d112-c070-4870-93d5-2fcc84a1331f
ms.tgt_platform: multiple
keywords:
- Método unconnected Servicios de Escritorio remoto
- Método unconnected Servicios de Escritorio remoto, interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto, método alconnected
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnConnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d83a6a14f58a0704f0a3110532ad8cf8c0d7dc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802143"
---
# <a name="imstscaxeventsonconnected-method"></a><span data-ttu-id="9b28b-106">IMsTscAxEvents:: alconnected (método)</span><span class="sxs-lookup"><span data-stu-id="9b28b-106">IMsTscAxEvents::OnConnected method</span></span>

<span data-ttu-id="9b28b-107">Se llama cuando el control de cliente está en proceso de establecer una conexión con Escritorio remoto un servidor host de sesión de escritorio remoto (host de sesión de RD).</span><span class="sxs-lookup"><span data-stu-id="9b28b-107">Called when the client control is in the process of establishing a connection with a Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b28b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9b28b-108">Syntax</span></span>


```C++
void OnConnected();
```



## <a name="parameters"></a><span data-ttu-id="9b28b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9b28b-109">Parameters</span></span>

<span data-ttu-id="9b28b-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="9b28b-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9b28b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9b28b-111">Return value</span></span>

<span data-ttu-id="9b28b-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="9b28b-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b28b-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9b28b-113">Remarks</span></span>

<span data-ttu-id="9b28b-114">Implemente este método en el receptor de eventos para recibir la notificación de que el control ha establecido una conexión con un servidor host de sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="9b28b-114">Implement this method in your event sink to receive notification that the control has established a connection with an RD Session Host server.</span></span>

<span data-ttu-id="9b28b-115">Consulte el evento [**IMsTscAxEvents:: OnLoginComplete**](imstscaxevents-onlogincomplete.md) para obtener más información sobre cómo llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="9b28b-115">Refer to the [**IMsTscAxEvents::OnLoginComplete**](imstscaxevents-onlogincomplete.md) event for more information on calling this method.</span></span>

<span data-ttu-id="9b28b-116">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="9b28b-116">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9b28b-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b28b-117">Requirements</span></span>



| <span data-ttu-id="9b28b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b28b-118">Requirement</span></span> | <span data-ttu-id="9b28b-119">Value</span><span class="sxs-lookup"><span data-stu-id="9b28b-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b28b-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b28b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9b28b-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9b28b-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9b28b-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b28b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9b28b-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9b28b-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9b28b-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="9b28b-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="9b28b-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b28b-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9b28b-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9b28b-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b28b-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b28b-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9b28b-128">IID</span><span class="sxs-lookup"><span data-stu-id="9b28b-128">IID</span></span><br/>                      | <span data-ttu-id="9b28b-129">IMsTscAxEvents se define como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="9b28b-129">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="9b28b-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="9b28b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b28b-131">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="9b28b-131">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





