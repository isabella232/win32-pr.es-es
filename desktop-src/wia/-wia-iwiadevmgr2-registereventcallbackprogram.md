---
description: 'El método IWiaDevMgr2:: RegisterEventCallbackProgram registra una aplicación para recibir eventos de dispositivo. Se proporciona principalmente para la compatibilidad con versiones anteriores de aplicaciones que no se escribieron para la adquisición de imágenes de Windows (WIA) 2,0.'
ms.assetid: 6b427f19-719b-44ce-8e2c-3c44672345c8
title: 'IWiaDevMgr2:: RegisterEventCallbackProgram (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.RegisterEventCallbackProgram
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 9b18b5833b7616493c24f0128caa7c910b685e37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720390"
---
# <a name="iwiadevmgr2registereventcallbackprogram-method"></a><span data-ttu-id="cb59f-104">IWiaDevMgr2:: RegisterEventCallbackProgram (método)</span><span class="sxs-lookup"><span data-stu-id="cb59f-104">IWiaDevMgr2::RegisterEventCallbackProgram method</span></span>

<span data-ttu-id="cb59f-105">El método **IWiaDevMgr2:: RegisterEventCallbackProgram** registra una aplicación para recibir eventos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cb59f-105">The **IWiaDevMgr2::RegisterEventCallbackProgram** method registers an application to receive device events.</span></span> <span data-ttu-id="cb59f-106">Se proporciona principalmente para la compatibilidad con versiones anteriores de aplicaciones que no se escribieron para la adquisición de imágenes de Windows (WIA) 2,0.</span><span class="sxs-lookup"><span data-stu-id="cb59f-106">It is primarily provided for backward compatibility with applications that were not written for Windows Image Acquisition (WIA) 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb59f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cb59f-107">Syntax</span></span>


```C++
HRESULT RegisterEventCallbackProgram(
  [in]       LONG lFlags,
  [in]       BSTR bstrDeviceID,
  [in] const GUID *pEventGUID,
  [in]       BSTR bstrFullAppName,
  [in]       BSTR bstrCommandlineArg,
  [in]       BSTR bstrName,
  [in]       BSTR bstrDescription,
  [in]       BSTR bstrIcon
);
```



## <a name="parameters"></a><span data-ttu-id="cb59f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cb59f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb59f-109">*lFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cb59f-109">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb59f-110">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="cb59f-110">Type: **LONG**</span></span>

<span data-ttu-id="cb59f-111">Marcas de registro.</span><span class="sxs-lookup"><span data-stu-id="cb59f-111">The registration flags.</span></span> <span data-ttu-id="cb59f-112">Se puede establecer en los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="cb59f-112">Can be set to the following values.</span></span>



| <span data-ttu-id="cb59f-113">Value</span><span class="sxs-lookup"><span data-stu-id="cb59f-113">Value</span></span>                                                                                                                                                                                                           | <span data-ttu-id="cb59f-114">Significado</span><span class="sxs-lookup"><span data-stu-id="cb59f-114">Meaning</span></span>                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="WIA_REGISTER_EVENT_CALLBACK"></span><span id="wia_register_event_callback"></span><dl> <span data-ttu-id="cb59f-115"><dt>**\_devolución de \_ llamada de evento de registro WIA \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cb59f-115"><dt>**WIA\_REGISTER\_EVENT\_CALLBACK**</dt></span></span> </dl>       | <span data-ttu-id="cb59f-116">Regístrese para el evento.</span><span class="sxs-lookup"><span data-stu-id="cb59f-116">Register for the event.</span></span><br/>                           |
| <span id="WIA_UNREGISTER_EVENT_CALLBACK"></span><span id="wia_unregister_event_callback"></span><dl> <span data-ttu-id="cb59f-117"><dt>**devolución de llamada de evento WIA \_ UNregister \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cb59f-117"><dt>**WIA\_UNREGISTER\_EVENT\_CALLBACK**</dt></span></span> </dl> | <span data-ttu-id="cb59f-118">Elimine el registro del evento.</span><span class="sxs-lookup"><span data-stu-id="cb59f-118">Delete the registration for the event.</span></span><br/>            |
| <span id="WIA_SET_DEFAULT_HANDLER"></span><span id="wia_set_default_handler"></span><dl> <span data-ttu-id="cb59f-119"><dt>**\_ \_ controlador predeterminado de WIA set \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cb59f-119"><dt>**WIA\_SET\_DEFAULT\_HANDLER**</dt></span></span> </dl>                   | <span data-ttu-id="cb59f-120">Establezca la aplicación como el controlador de eventos predeterminado.</span><span class="sxs-lookup"><span data-stu-id="cb59f-120">Set the application as the default event handler.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="cb59f-121">*bstrDeviceID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cb59f-121">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb59f-122">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="cb59f-122">Type: **BSTR**</span></span>

<span data-ttu-id="cb59f-123">Un identificador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cb59f-123">A device identifier.</span></span> <span data-ttu-id="cb59f-124">Pase **null** para registrar el evento en todos los dispositivos WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="cb59f-124">Pass **NULL** to register for the event on all WIA 2.0 devices.</span></span>

</dd> <dt>

<span data-ttu-id="cb59f-125">*pEventGUID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cb59f-125">*pEventGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb59f-126">Tipo: \**const GUID \** _</span><span class="sxs-lookup"><span data-stu-id="cb59f-126">Type: \**const GUID\** _</span></span>

<span data-ttu-id="cb59f-127">Evento para el que se registra la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cb59f-127">The event that the application is registering for.</span></span> <span data-ttu-id="cb59f-128">Para obtener una lista de GUID de eventos válidos, vea [identificadores de eventos de WIA](-wia-wia-event-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="cb59f-128">For a list of valid event GUIDs, see [WIA Event Identifiers](-wia-wia-event-identifiers.md).</span></span>

</dd> <dt>

<span data-ttu-id="cb59f-129">_bstrFullAppName \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="cb59f-129">_bstrFullAppName\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb59f-130">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="cb59f-130">Type: **BSTR**</span></span>

<span data-ttu-id="cb59f-131">Nombre completo de la ruta de acceso de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cb59f-131">The full path name of the application.</span></span>

</dd> <dt>

<span data-ttu-id="cb59f-132">*bstrCommandlineArg* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cb59f-132">*bstrCommandlineArg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb59f-133">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="cb59f-133">Type: **BSTR**</span></span>

<span data-ttu-id="cb59f-134">Argumentos de línea de comandos adecuados para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cb59f-134">The appropriate command-line arguments for the application.</span></span>

</dd> <dt>

<span data-ttu-id="cb59f-135">*bstrName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cb59f-135">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb59f-136">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="cb59f-136">Type: **BSTR**</span></span>

<span data-ttu-id="cb59f-137">Nombre de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cb59f-137">The name of the application.</span></span> <span data-ttu-id="cb59f-138">El nombre se muestra al usuario cuando se registran varias aplicaciones para el mismo evento.</span><span class="sxs-lookup"><span data-stu-id="cb59f-138">The name is displayed to the user when multiple applications register for the same event.</span></span>

</dd> <dt>

<span data-ttu-id="cb59f-139">*bstrDescription* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cb59f-139">*bstrDescription* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb59f-140">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="cb59f-140">Type: **BSTR**</span></span>

<span data-ttu-id="cb59f-141">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cb59f-141">The description of the application.</span></span> <span data-ttu-id="cb59f-142">La descripción se muestra al usuario cuando se registran varias aplicaciones para el mismo evento.</span><span class="sxs-lookup"><span data-stu-id="cb59f-142">The description is displayed to the user when multiple applications register for the same event.</span></span>

</dd> <dt>

<span data-ttu-id="cb59f-143">*bstrIcon* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cb59f-143">*bstrIcon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb59f-144">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="cb59f-144">Type: **BSTR**</span></span>

<span data-ttu-id="cb59f-145">Icono que representa la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cb59f-145">The icon that represents the application.</span></span> <span data-ttu-id="cb59f-146">El icono se muestra al usuario cuando se registran varias aplicaciones para el mismo evento.</span><span class="sxs-lookup"><span data-stu-id="cb59f-146">The icon is displayed to the user when multiple applications register for the same event.</span></span> <span data-ttu-id="cb59f-147">La cadena contiene el nombre de la aplicación y el índice de base cero del icono separado por una coma, por ejemplo, "MyApp, 0".</span><span class="sxs-lookup"><span data-stu-id="cb59f-147">The string contains the name of the application and the zero-based index of the icon separated by a comma, for example, "MyApp, 0".</span></span> <span data-ttu-id="cb59f-148">Puede haber más de un icono que represente una aplicación.</span><span class="sxs-lookup"><span data-stu-id="cb59f-148">There might be more than one icon that represents an application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb59f-149">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cb59f-149">Return value</span></span>

<span data-ttu-id="cb59f-150">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="cb59f-150">Type: **HRESULT**</span></span>

<span data-ttu-id="cb59f-151">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="cb59f-151">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cb59f-152">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cb59f-152">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb59f-153">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cb59f-153">Remarks</span></span>

<span data-ttu-id="cb59f-154">Use **IWiaDevMgr2:: RegisterEventCallbackProgram** para registrar eventos de dispositivo de hardware.</span><span class="sxs-lookup"><span data-stu-id="cb59f-154">Use **IWiaDevMgr2::RegisterEventCallbackProgram** to register for hardware device events.</span></span> <span data-ttu-id="cb59f-155">Cuando se produce un evento en el que se registra una aplicación para, se inicia la aplicación y la información del evento se transmite a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cb59f-155">When an event occurs that an application is registered for, the application is launched, and the event information is transmitted to the application.</span></span>

<span data-ttu-id="cb59f-156">Use el método [**EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) para recuperar un puntero a un objeto de enumerador para las propiedades de registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="cb59f-156">Use the [**EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) method to retrieve a pointer to an enumerator object for event registration properties.</span></span>

<span data-ttu-id="cb59f-157">Use el método **IWiaDevMgr2:: RegisterEventCallbackProgram** para mantener la compatibilidad con las aplicaciones no escritas para la arquitectura WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="cb59f-157">Only use the **IWiaDevMgr2::RegisterEventCallbackProgram** method for backward compatibility with applications not written for the WIA 2.0 architecture.</span></span> <span data-ttu-id="cb59f-158">Use las interfaces del modelo de objetos componentes (COM) proporcionadas por la arquitectura WIA 2,0 para las nuevas aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="cb59f-158">Use the Component Object Model (COM) interfaces provided by the WIA 2.0 architecture for new applications.</span></span> <span data-ttu-id="cb59f-159">En concreto, llame a [**IWiaDevMgr2:: RegisterEventCallbackInterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md) o [**IWiaDevMgr2:: RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md) para registrar una nueva aplicación para eventos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cb59f-159">Specifically, call [**IWiaDevMgr2::RegisterEventCallbackInterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md) or [**IWiaDevMgr2::RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md) to register a new application for device events.</span></span>

<span data-ttu-id="cb59f-160">Normalmente, se llama a este método con un programa de instalación o un script.</span><span class="sxs-lookup"><span data-stu-id="cb59f-160">Typically, this method is called by an install program or a script.</span></span> <span data-ttu-id="cb59f-161">El programa de instalación o el script registra la aplicación para recibir eventos de dispositivo WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="cb59f-161">The install program or script registers the application to receive WIA 2.0 device events.</span></span> <span data-ttu-id="cb59f-162">Cuando se produce el evento, el sistema en tiempo de ejecución de WIA 2,0 inicia la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cb59f-162">When the event occurs, the application is started by the WIA 2.0 run-time system.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb59f-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb59f-163">Requirements</span></span>



| <span data-ttu-id="cb59f-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb59f-164">Requirement</span></span> | <span data-ttu-id="cb59f-165">Value</span><span class="sxs-lookup"><span data-stu-id="cb59f-165">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="cb59f-166">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb59f-166">Minimum supported client</span></span><br/> | <span data-ttu-id="cb59f-167">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cb59f-167">Windows Vista \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="cb59f-168">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb59f-168">Minimum supported server</span></span><br/> | <span data-ttu-id="cb59f-169">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="cb59f-169">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="cb59f-170">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cb59f-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb59f-171"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb59f-171"><dt>Wia.h</dt></span></span> </dl> |



 

 




