---
title: IMsTscAxEvents OnLoginComplete, método
description: Se llama cuando el control de cliente ha iniciado sesión correctamente en un servidor de host de sesión de Escritorio remoto (host de sesión de escritorio remoto), siguiendo la presentación del cuadro de diálogo de inicio de sesión de Windows.
ms.assetid: acb345a6-3153-4b8f-ac51-fe0c19fa750a
ms.tgt_platform: multiple
keywords:
- Método OnLoginComplete Servicios de Escritorio remoto
- Método OnLoginComplete Servicios de Escritorio remoto, interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto, método OnLoginComplete
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnLoginComplete
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74d6b63f74ed99c8af939bafdc8a55a41e33b404
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534443"
---
# <a name="imstscaxeventsonlogincomplete-method"></a><span data-ttu-id="6095e-106">IMsTscAxEvents:: OnLoginComplete (método)</span><span class="sxs-lookup"><span data-stu-id="6095e-106">IMsTscAxEvents::OnLoginComplete method</span></span>

<span data-ttu-id="6095e-107">Se llama cuando el control de cliente ha iniciado sesión correctamente en un servidor de host de sesión de Escritorio remoto (host de sesión de escritorio remoto), siguiendo la presentación del cuadro de diálogo de inicio de sesión de Windows.</span><span class="sxs-lookup"><span data-stu-id="6095e-107">Called when the client control has successfully logged on to a Remote Desktop Session Host (RD Session Host) server, following the display of the Windows Logon dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="6095e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6095e-108">Syntax</span></span>


```C++
void OnLoginComplete();
```



## <a name="parameters"></a><span data-ttu-id="6095e-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6095e-109">Parameters</span></span>

<span data-ttu-id="6095e-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="6095e-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6095e-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6095e-111">Return value</span></span>

<span data-ttu-id="6095e-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="6095e-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6095e-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6095e-113">Remarks</span></span>

<span data-ttu-id="6095e-114">Implemente este método en el receptor de eventos para recibir la notificación de que el control ha completado el inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="6095e-114">Implement this method in your event sink to receive notification that the control has completed logon.</span></span>

## <a name="examples"></a><span data-ttu-id="6095e-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="6095e-115">Examples</span></span>

<span data-ttu-id="6095e-116">En el ejemplo siguiente se muestra cómo controlar este evento utilizando Visual Basic código de scripting.</span><span class="sxs-lookup"><span data-stu-id="6095e-116">The following example shows how to handle this event by using Visual Basic Scripting code.</span></span> <span data-ttu-id="6095e-117">La suposición en este ejemplo es que el objeto de control se denomina "MsRdpClient".</span><span class="sxs-lookup"><span data-stu-id="6095e-117">The assumption in this example is that your control object is named "MsRdpClient".</span></span>

<span data-ttu-id="6095e-118">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="6095e-118">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>


```VB
Sub MsRdpClient.OnLoginComplete()
    Msgbox("Login has completed")
End sub
```



## <a name="requirements"></a><span data-ttu-id="6095e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6095e-119">Requirements</span></span>



| <span data-ttu-id="6095e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6095e-120">Requirement</span></span> | <span data-ttu-id="6095e-121">Value</span><span class="sxs-lookup"><span data-stu-id="6095e-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6095e-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6095e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6095e-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6095e-123">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="6095e-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6095e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6095e-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6095e-125">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6095e-126">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6095e-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="6095e-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6095e-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="6095e-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6095e-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6095e-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6095e-129"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="6095e-130">IID</span><span class="sxs-lookup"><span data-stu-id="6095e-130">IID</span></span><br/>                      | <span data-ttu-id="6095e-131">IMsTscAxEvents se define como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="6095e-131">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="6095e-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="6095e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6095e-133">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="6095e-133">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





