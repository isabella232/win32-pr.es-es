---
title: IMsTscAxEvents método de conexión
description: Se llama cuando el control de cliente comienza a conectarse a un servidor en respuesta a una llamada a IMsTscAx Connect.
ms.assetid: c5e367a8-126a-48bb-bc94-1063f77e8239
ms.tgt_platform: multiple
keywords:
- Método biconnect Servicios de Escritorio remoto
- Método biconnect Servicios de Escritorio remoto, interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto, método biconnect
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnConnecting
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2004fde83b79aff7b7c5082562de94f943eacb25
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421921"
---
# <a name="imstscaxeventsonconnecting-method"></a><span data-ttu-id="da1f1-106">IMsTscAxEvents:: alconnect (método)</span><span class="sxs-lookup"><span data-stu-id="da1f1-106">IMsTscAxEvents::OnConnecting method</span></span>

<span data-ttu-id="da1f1-107">Se llama cuando el control de cliente comienza a conectarse a un servidor en respuesta a una llamada a [**IMsTscAx:: Connect**](imstscax-connect.md).</span><span class="sxs-lookup"><span data-stu-id="da1f1-107">Called when the client control begins connecting to a server in response to a call to [**IMsTscAx::Connect**](imstscax-connect.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="da1f1-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="da1f1-108">Syntax</span></span>


```C++
void OnConnecting();
```



## <a name="parameters"></a><span data-ttu-id="da1f1-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="da1f1-109">Parameters</span></span>

<span data-ttu-id="da1f1-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="da1f1-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="da1f1-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="da1f1-111">Return value</span></span>

<span data-ttu-id="da1f1-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="da1f1-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="da1f1-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="da1f1-113">Remarks</span></span>

<span data-ttu-id="da1f1-114">Implemente este método en el receptor de eventos para recibir la notificación de que el control ha empezado a conectarse.</span><span class="sxs-lookup"><span data-stu-id="da1f1-114">Implement this method in your event sink to receive notification that the control has begun connecting.</span></span>

## <a name="examples"></a><span data-ttu-id="da1f1-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="da1f1-115">Examples</span></span>

<span data-ttu-id="da1f1-116">En el ejemplo siguiente se muestra cómo controlar este evento con código de scripting de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="da1f1-116">The following example shows how to handle this event with Visual Basic Scripting code.</span></span> <span data-ttu-id="da1f1-117">La suposición en este ejemplo es que el objeto de control se denomina "MsRdpClient".</span><span class="sxs-lookup"><span data-stu-id="da1f1-117">The assumption in this example is that your control object is named "MsRdpClient".</span></span>

<span data-ttu-id="da1f1-118">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="da1f1-118">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>


```VB
Sub MsRdpClient.OnConnecting()
    Msgbox("Connecting")
End sub
```



## <a name="requirements"></a><span data-ttu-id="da1f1-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da1f1-119">Requirements</span></span>



| <span data-ttu-id="da1f1-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="da1f1-120">Requirement</span></span> | <span data-ttu-id="da1f1-121">Value</span><span class="sxs-lookup"><span data-stu-id="da1f1-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="da1f1-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="da1f1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="da1f1-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="da1f1-123">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="da1f1-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="da1f1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="da1f1-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="da1f1-125">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="da1f1-126">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="da1f1-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="da1f1-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da1f1-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="da1f1-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="da1f1-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da1f1-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da1f1-129"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="da1f1-130">IID</span><span class="sxs-lookup"><span data-stu-id="da1f1-130">IID</span></span><br/>                      | <span data-ttu-id="da1f1-131">IMsTscAxEvents se define como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="da1f1-131">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="da1f1-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="da1f1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da1f1-133">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="da1f1-133">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





