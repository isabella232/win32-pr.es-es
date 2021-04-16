---
description: 'El método IWiaDevMgr2:: RegisterEventCallbackCLSID registra una aplicación para recibir eventos incluso si la aplicación no se está ejecutando.'
ms.assetid: e0d421a7-ef49-4e27-9661-c358ac819712
title: 'IWiaDevMgr2:: RegisterEventCallbackCLSID (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.RegisterEventCallbackCLSID
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 63e69d12d47f90ba40f5cc785d8b864c40158774
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542790"
---
# <a name="iwiadevmgr2registereventcallbackclsid-method"></a><span data-ttu-id="610ca-103">IWiaDevMgr2:: RegisterEventCallbackCLSID (método)</span><span class="sxs-lookup"><span data-stu-id="610ca-103">IWiaDevMgr2::RegisterEventCallbackCLSID method</span></span>

<span data-ttu-id="610ca-104">El método **IWiaDevMgr2:: RegisterEventCallbackCLSID** registra una aplicación para recibir eventos incluso si la aplicación no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="610ca-104">The **IWiaDevMgr2::RegisterEventCallbackCLSID** method registers an application to receive events even if the application is not running.</span></span>

## <a name="syntax"></a><span data-ttu-id="610ca-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="610ca-105">Syntax</span></span>


```C++
HRESULT RegisterEventCallbackCLSID(
  [in]               LONG lFlags,
  [in]               BSTR bstrDeviceID,
  [in]         const GUID *pEventGUID,
  [in, unique] const GUID *pClsID,
  [in]               BSTR bstrName,
  [in]               BSTR bstrDescription,
  [in]               BSTR bstrIcon
);
```



## <a name="parameters"></a><span data-ttu-id="610ca-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="610ca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="610ca-107">*lFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="610ca-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="610ca-108">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="610ca-108">Type: **LONG**</span></span>

<span data-ttu-id="610ca-109">Especifica las marcas de registro.</span><span class="sxs-lookup"><span data-stu-id="610ca-109">Specifies registration flags.</span></span> <span data-ttu-id="610ca-110">Se puede establecer en los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="610ca-110">Can be set to the following values:</span></span>



| <span data-ttu-id="610ca-111">Marca de registro</span><span class="sxs-lookup"><span data-stu-id="610ca-111">Registration Flag</span></span>                | <span data-ttu-id="610ca-112">Significado</span><span class="sxs-lookup"><span data-stu-id="610ca-112">Meaning</span></span>                                           |
|----------------------------------|---------------------------------------------------|
| <span data-ttu-id="610ca-113">\_devolución de \_ llamada de evento de registro WIA \_</span><span class="sxs-lookup"><span data-stu-id="610ca-113">WIA\_REGISTER\_EVENT\_CALLBACK</span></span>   | <span data-ttu-id="610ca-114">Regístrese para el evento.</span><span class="sxs-lookup"><span data-stu-id="610ca-114">Register for the event.</span></span>                           |
| <span data-ttu-id="610ca-115">devolución de llamada de evento WIA \_ UNregister \_ \_</span><span class="sxs-lookup"><span data-stu-id="610ca-115">WIA\_UNREGISTER\_EVENT\_CALLBACK</span></span> | <span data-ttu-id="610ca-116">Elimine el registro del evento.</span><span class="sxs-lookup"><span data-stu-id="610ca-116">Delete the registration for the event.</span></span>            |
| <span data-ttu-id="610ca-117">\_ \_ controlador predeterminado de WIA set \_</span><span class="sxs-lookup"><span data-stu-id="610ca-117">WIA\_SET\_DEFAULT\_HANDLER</span></span>       | <span data-ttu-id="610ca-118">Establezca la aplicación como el controlador de eventos predeterminado.</span><span class="sxs-lookup"><span data-stu-id="610ca-118">Set the application as the default event handler.</span></span> |



 

</dd> <dt>

<span data-ttu-id="610ca-119">*bstrDeviceID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="610ca-119">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="610ca-120">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="610ca-120">Type: **BSTR**</span></span>

<span data-ttu-id="610ca-121">Especifica un identificador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="610ca-121">Specifies a device identifier.</span></span> <span data-ttu-id="610ca-122">Pase **null** para registrar el evento en todos los dispositivos WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="610ca-122">Pass **NULL** to register for the event on all WIA 2.0 devices.</span></span>

</dd> <dt>

<span data-ttu-id="610ca-123">*pEventGUID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="610ca-123">*pEventGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="610ca-124">Tipo: \**const GUID \** _</span><span class="sxs-lookup"><span data-stu-id="610ca-124">Type: \**const GUID\** _</span></span>

<span data-ttu-id="610ca-125">Especifica el evento para el que se registra la aplicación.</span><span class="sxs-lookup"><span data-stu-id="610ca-125">Specifies the event that the application is registering for.</span></span> <span data-ttu-id="610ca-126">Para obtener una lista de eventos estándar, vea [identificadores de eventos de WIA](-wia-wia-event-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="610ca-126">For a list of standard events, see [WIA Event Identifiers](-wia-wia-event-identifiers.md).</span></span>

</dd> <dt>

<span data-ttu-id="610ca-127">_pClsID \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="610ca-127">_pClsID\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="610ca-128">Tipo: \**const GUID \** _</span><span class="sxs-lookup"><span data-stu-id="610ca-128">Type: \**const GUID\** _</span></span>

<span data-ttu-id="610ca-129">Puntero al identificador de clase de la aplicación (_ \* CLSID \* \*).</span><span class="sxs-lookup"><span data-stu-id="610ca-129">Pointer to the application class ID (_\*CLSID\*\*).</span></span> <span data-ttu-id="610ca-130">El sistema en tiempo de ejecución de WIA 2,0 usa el **CLSID** de la aplicación para iniciar la aplicación cuando se produce un evento para el que se ha registrado.</span><span class="sxs-lookup"><span data-stu-id="610ca-130">The WIA 2.0 run-time system uses the application **CLSID** to start the application when an event occurs that it is registered for.</span></span>

</dd> <dt>

<span data-ttu-id="610ca-131">*bstrName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="610ca-131">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="610ca-132">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="610ca-132">Type: **BSTR**</span></span>

<span data-ttu-id="610ca-133">Especifica el nombre de la aplicación que se registra para el evento.</span><span class="sxs-lookup"><span data-stu-id="610ca-133">Specifies the name of the application that registers for the event.</span></span>

</dd> <dt>

<span data-ttu-id="610ca-134">*bstrDescription* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="610ca-134">*bstrDescription* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="610ca-135">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="610ca-135">Type: **BSTR**</span></span>

<span data-ttu-id="610ca-136">Especifica una descripción de texto de la aplicación que se registra para el evento.</span><span class="sxs-lookup"><span data-stu-id="610ca-136">Specifies a text description of the application that registers for the event.</span></span>

</dd> <dt>

<span data-ttu-id="610ca-137">*bstrIcon* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="610ca-137">*bstrIcon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="610ca-138">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="610ca-138">Type: **BSTR**</span></span>

<span data-ttu-id="610ca-139">Especifica el nombre de un archivo de imagen que se va a utilizar para el icono de la aplicación que se registra para el evento.</span><span class="sxs-lookup"><span data-stu-id="610ca-139">Specifies the name of an image file to use for the icon for the application that registers for the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="610ca-140">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="610ca-140">Return value</span></span>

<span data-ttu-id="610ca-141">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="610ca-141">Type: **HRESULT**</span></span>

<span data-ttu-id="610ca-142">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="610ca-142">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="610ca-143">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="610ca-143">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="610ca-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="610ca-144">Remarks</span></span>

<span data-ttu-id="610ca-145">Las aplicaciones WIA 2,0 usan este método para registrarse y recibir eventos de dispositivo de hardware.</span><span class="sxs-lookup"><span data-stu-id="610ca-145">WIA 2.0 applications use this method to register to receive hardware device events.</span></span> <span data-ttu-id="610ca-146">Después de llamar a **IWiaDevMgr2:: RegisterEventCallbackCLSID** , la aplicación se registra para recibir eventos de dispositivo WIA 2,0, incluso si no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="610ca-146">After **IWiaDevMgr2::RegisterEventCallbackCLSID** is called, the application is registered to receive WIA 2.0 device events even if it is not running.</span></span>

<span data-ttu-id="610ca-147">Cuando se produce el evento, el sistema WIA 2,0 determina qué aplicación se registra para recibir el evento.</span><span class="sxs-lookup"><span data-stu-id="610ca-147">When the event occurs, the WIA 2.0 system determines which application is registered to receive the event.</span></span> <span data-ttu-id="610ca-148">Usa la función [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) y el CLSID especificado en el parámetro *pClsID* para crear una instancia de la aplicación y, a continuación, llama al método [**ImageEventCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) para transmitir la información del evento a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="610ca-148">It uses the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function and the CLSID specified in the *pClsID* parameter to create an instance of the application, and then calls the [**ImageEventCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) method to transmit the event information to the application.</span></span>

<span data-ttu-id="610ca-149">Una aplicación puede invocar el método [**EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) para enumerar la información de registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="610ca-149">An application can invoke the [**EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) method to enumerate event registration information.</span></span>

<span data-ttu-id="610ca-150">Si la aplicación no es un componente del modelo de objetos componentes (COM) registrado y no es compatible con la arquitectura WIA 2,0, use el método [**IWiaDevMgr2:: RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) para registrar una aplicación para eventos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="610ca-150">If the application is not a registered Component Object Model (COM) component and is not compatible with the WIA 2.0 architecture, use the [**IWiaDevMgr2::RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) method to register an application for device events.</span></span>

> [!Note]  
> <span data-ttu-id="610ca-151">En una aplicación multiproceso, no hay ninguna garantía de que la devolución de llamada de notificación de eventos se devuelva en el mismo subproceso que registró la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="610ca-151">In a multi-threaded application, there is no guarantee that the event notification callback is returned on the same thread that registered the callback.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="610ca-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="610ca-152">Requirements</span></span>



| <span data-ttu-id="610ca-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="610ca-153">Requirement</span></span> | <span data-ttu-id="610ca-154">Value</span><span class="sxs-lookup"><span data-stu-id="610ca-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="610ca-155">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="610ca-155">Minimum supported client</span></span><br/> | <span data-ttu-id="610ca-156">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="610ca-156">Windows Vista \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="610ca-157">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="610ca-157">Minimum supported server</span></span><br/> | <span data-ttu-id="610ca-158">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="610ca-158">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="610ca-159">Encabezado</span><span class="sxs-lookup"><span data-stu-id="610ca-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="610ca-160"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="610ca-160"><dt>Wia.h</dt></span></span> </dl> |



 

 
