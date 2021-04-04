---
title: IMsTscAxEvents OnRequestLeaveFullScreen, método
description: Se llama cuando el cliente solicita dejar el modo de pantalla completa y la propiedad IMsTscAdvancedSettings Put ContainerHandledFullScreen se ha \_ establecido en un valor distinto de cero.
ms.assetid: db6ee012-8288-4360-98b2-12858ea65baa
ms.tgt_platform: multiple
keywords:
- Método OnRequestLeaveFullScreen Servicios de Escritorio remoto
- Método OnRequestLeaveFullScreen Servicios de Escritorio remoto, interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto, método OnRequestLeaveFullScreen
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRequestLeaveFullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e814d6153e32fdf4fa498a6630fc9ca2908510e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802720"
---
# <a name="imstscaxeventsonrequestleavefullscreen-method"></a><span data-ttu-id="9fffd-106">IMsTscAxEvents:: OnRequestLeaveFullScreen (método)</span><span class="sxs-lookup"><span data-stu-id="9fffd-106">IMsTscAxEvents::OnRequestLeaveFullScreen method</span></span>

<span data-ttu-id="9fffd-107">Se llama cuando el cliente solicita dejar el modo de pantalla completa y la propiedad [**IMsTscAdvancedSettings::p UT \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) se ha establecido en un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="9fffd-107">Called when the client requests to leave full-screen mode and the [**IMsTscAdvancedSettings::put\_ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) property has been set to a nonzero value.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fffd-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9fffd-108">Syntax</span></span>


```C++
void OnRequestLeaveFullScreen();
```



## <a name="parameters"></a><span data-ttu-id="9fffd-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9fffd-109">Parameters</span></span>

<span data-ttu-id="9fffd-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="9fffd-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9fffd-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9fffd-111">Return value</span></span>

<span data-ttu-id="9fffd-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="9fffd-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fffd-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9fffd-113">Remarks</span></span>

<span data-ttu-id="9fffd-114">En el modo de pantalla completa controlado por contenedores, el contenedor debe dejar el modo de pantalla completa estándar en respuesta a este evento.</span><span class="sxs-lookup"><span data-stu-id="9fffd-114">In container-handled full-screen mode, the container should leave standard full-screen mode in response to this event.</span></span>

<span data-ttu-id="9fffd-115">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="9fffd-115">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9fffd-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9fffd-116">Requirements</span></span>



| <span data-ttu-id="9fffd-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fffd-117">Requirement</span></span> | <span data-ttu-id="9fffd-118">Value</span><span class="sxs-lookup"><span data-stu-id="9fffd-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9fffd-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9fffd-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9fffd-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9fffd-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9fffd-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9fffd-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9fffd-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9fffd-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9fffd-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="9fffd-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="9fffd-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9fffd-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9fffd-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9fffd-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9fffd-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9fffd-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9fffd-127">IID</span><span class="sxs-lookup"><span data-stu-id="9fffd-127">IID</span></span><br/>                      | <span data-ttu-id="9fffd-128">IMsTscAxEvents se define como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="9fffd-128">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="9fffd-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="9fffd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fffd-130">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="9fffd-130">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





