---
description: Registra una aplicación en ejecución para la notificación de eventos de adquisición de imágenes de Windows (WIA) 2,0.
ms.assetid: 978dcd41-d63b-421d-b7e1-8e9368b36180
title: 'IWiaDevMgr2:: RegisterEventCallbackInterface (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.RegisterEventCallbackInterface
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 7cd3a7e00cff56bc5d91bfc843ab79fe71aa1123
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276855"
---
# <a name="iwiadevmgr2registereventcallbackinterface-method"></a><span data-ttu-id="71446-103">IWiaDevMgr2:: RegisterEventCallbackInterface (método)</span><span class="sxs-lookup"><span data-stu-id="71446-103">IWiaDevMgr2::RegisterEventCallbackInterface method</span></span>

<span data-ttu-id="71446-104">Registra una aplicación en ejecución para la notificación de eventos de adquisición de imágenes de Windows (WIA) 2,0.</span><span class="sxs-lookup"><span data-stu-id="71446-104">Registers a running application for Windows Image Acquisition (WIA) 2.0 event notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="71446-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="71446-105">Syntax</span></span>


```C++
HRESULT RegisterEventCallbackInterface(
  [in]        LONG              lFlags,
  [in]        BSTR              bstrDeviceID,
  [in]  const GUID              *pEventGUID,
  [in]        IWiaEventCallback *pIWiaEventCallback,
  [out]       IUnknown          **pEventObject
);
```



## <a name="parameters"></a><span data-ttu-id="71446-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="71446-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71446-107">*lFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="71446-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71446-108">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="71446-108">Type: **LONG**</span></span>

<span data-ttu-id="71446-109">Actualmente no se usa.</span><span class="sxs-lookup"><span data-stu-id="71446-109">Currently unused.</span></span> <span data-ttu-id="71446-110">Debe establecerse como cero.</span><span class="sxs-lookup"><span data-stu-id="71446-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="71446-111">*bstrDeviceID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="71446-111">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71446-112">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="71446-112">Type: **BSTR**</span></span>

<span data-ttu-id="71446-113">Especifica el identificador único de un dispositivo WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="71446-113">Specifies the unique identifier of a WIA 2.0 device.</span></span> <span data-ttu-id="71446-114">Establezca este parámetro en **null** para registrarse en el evento en todos los dispositivos WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="71446-114">Set this parameter to **NULL** to register for the event on all WIA 2.0 devices.</span></span>

</dd> <dt>

<span data-ttu-id="71446-115">*pEventGUID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="71446-115">*pEventGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71446-116">Tipo: \**const GUID \** _</span><span class="sxs-lookup"><span data-stu-id="71446-116">Type: \**const GUID\** _</span></span>

<span data-ttu-id="71446-117">Especifica un puntero al identificador de eventos para el que se registra la aplicación.</span><span class="sxs-lookup"><span data-stu-id="71446-117">Specifies a pointer to the event identifier that the application is registering for.</span></span> <span data-ttu-id="71446-118">Vea [identificadores de eventos de WIA](-wia-wia-event-identifiers.md) para los identificadores de eventos estándar.</span><span class="sxs-lookup"><span data-stu-id="71446-118">See [WIA Event Identifiers](-wia-wia-event-identifiers.md) for standard event identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="71446-119">_pIWiaEventCallback \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="71446-119">_pIWiaEventCallback\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71446-120">Tipo: \**[**IWiaEventCallback**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback) \** _</span><span class="sxs-lookup"><span data-stu-id="71446-120">Type: \**[**IWiaEventCallback**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback)\** _</span></span>

<span data-ttu-id="71446-121">Especifica un puntero a la interfaz [_ *IWiaEventCallback* \*](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback) que WIA 2,0 usa para enviar la notificación de eventos.</span><span class="sxs-lookup"><span data-stu-id="71446-121">Specifies a pointer to the [_ *IWiaEventCallback*\*](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback) interface that the WIA 2.0 uses to send event notification.</span></span>

</dd> <dt>

<span data-ttu-id="71446-122">*pEventObject* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="71446-122">*pEventObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71446-123">Tipo: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***</span><span class="sxs-lookup"><span data-stu-id="71446-123">Type: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***</span></span>

<span data-ttu-id="71446-124">Recibe la dirección de un puntero a la interfaz [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="71446-124">Receives the address of a pointer to the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71446-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="71446-125">Return value</span></span>

<span data-ttu-id="71446-126">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="71446-126">Type: **HRESULT**</span></span>

<span data-ttu-id="71446-127">Devuelve los códigos de error COM estándar o los siguientes.</span><span class="sxs-lookup"><span data-stu-id="71446-127">Returns the standard COM error codes or the following.</span></span>



| <span data-ttu-id="71446-128">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="71446-128">Return code</span></span>                                                                               | <span data-ttu-id="71446-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="71446-129">Description</span></span>                                                            |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="71446-130"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="71446-130"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="71446-131">No se puede devolver la interfaz [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="71446-131">The [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface cannot be returned.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="71446-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="71446-132">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="71446-133">El uso de los métodos [**IWiaDevMgr:: RegisterEventCallbackInterface**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface), **IWiaDevMgr2:: RegisterEventCallbackInterface** y [**DeviceManager. RegisterEvent**](/previous-versions/windows/desktop/wiaaut/-wiaaut-idevicemanager-registerevent) del mismo proceso después de que se reinicie el servicio de imágenes fijas puede producir una infracción de acceso, si se usaron las funciones antes de que se detuviera el servicio.</span><span class="sxs-lookup"><span data-stu-id="71446-133">Using the [**IWiaDevMgr::RegisterEventCallbackInterface**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface), **IWiaDevMgr2::RegisterEventCallbackInterface**, and [**DeviceManager.RegisterEvent**](/previous-versions/windows/desktop/wiaaut/-wiaaut-idevicemanager-registerevent) methods from the same process after the Still Image Service is restarted may cause an access violation, if the functions were used before the service was stopped.</span></span>

 

<span data-ttu-id="71446-134">Cuando las aplicaciones de WIA 2,0 empiezan a ejecutarse, utilizan este método para registrarse y recibir eventos de dispositivo de hardware.</span><span class="sxs-lookup"><span data-stu-id="71446-134">When WIA 2.0 applications begin executing, they use this method to register to receive hardware device events.</span></span> <span data-ttu-id="71446-135">Esto evita que la aplicación se reinicie cuando se produce otro evento para el que se ha registrado.</span><span class="sxs-lookup"><span data-stu-id="71446-135">This prevents the application from being restarted when another event for which it is registered occurs.</span></span> <span data-ttu-id="71446-136">Una vez que una aplicación llama a **IWiaDevMgr2:: RegisterEventCallbackInterface** para registrarse a fin de recibir eventos de WIA 2,0 desde un dispositivo, WIA 2,0 envía los eventos registrados al programa.</span><span class="sxs-lookup"><span data-stu-id="71446-136">Once an application calls **IWiaDevMgr2::RegisterEventCallbackInterface** to register itself to receive WIA 2.0 events from a device, the registered events are routed to the program by WIA 2.0.</span></span>

<span data-ttu-id="71446-137">Las aplicaciones deben llamar al método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en los punteros de interfaz que reciben a través del parámetro *pEventObject* .</span><span class="sxs-lookup"><span data-stu-id="71446-137">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *pEventObject* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="71446-138">En una aplicación multiproceso, la devolución de llamada de notificación de eventos puede entrar en un subproceso diferente del que registró la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="71446-138">In a multithreaded application, the event notification callback may come in on a different thread from the one that registered the callback.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="71446-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71446-139">Requirements</span></span>



| <span data-ttu-id="71446-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="71446-140">Requirement</span></span> | <span data-ttu-id="71446-141">Value</span><span class="sxs-lookup"><span data-stu-id="71446-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="71446-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71446-142">Minimum supported client</span></span><br/> | <span data-ttu-id="71446-143">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="71446-143">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="71446-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71446-144">Minimum supported server</span></span><br/> | <span data-ttu-id="71446-145">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="71446-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="71446-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="71446-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="71446-147"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="71446-147"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="71446-148">IDL</span><span class="sxs-lookup"><span data-stu-id="71446-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="71446-149"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="71446-149"><dt>Wia.idl</dt></span></span> </dl> |



 

 
