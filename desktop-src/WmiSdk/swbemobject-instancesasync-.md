---
description: El \_ método InstancesAsync de SWbemObject proporciona de forma asincrónica las instancias del objeto de clase actual. Este método implementa una consulta simple. Las consultas más complejas pueden requerir el uso de SWbemServices.ExecQuery.
ms.assetid: d10fcbbf-6110-4152-8201-db43dc7a3c14
ms.tgt_platform: multiple
title: Método SWbemObject.InstancesAsync_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.InstancesAsync_
- ISWbemObject.InstancesAsync_
- ISWbemObject.InstancesAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 800e28184593e339f739fb52d488803666f552c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908556"
---
# <a name="swbemobjectinstancesasync_-method"></a><span data-ttu-id="93437-105">SWbemObject. InstancesAsync, \_ método</span><span class="sxs-lookup"><span data-stu-id="93437-105">SWbemObject.InstancesAsync\_ method</span></span>

<span data-ttu-id="93437-106">El **método \_ InstancesAsync** de [**SWbemObject**](swbemobject.md) proporciona de forma asincrónica las instancias del objeto de clase actual.</span><span class="sxs-lookup"><span data-stu-id="93437-106">The **InstancesAsync\_** method of [**SWbemObject**](swbemobject.md) asynchronously supplies the instances of the current class object.</span></span> <span data-ttu-id="93437-107">Este método implementa una consulta simple.</span><span class="sxs-lookup"><span data-stu-id="93437-107">This method implements a simple query.</span></span> <span data-ttu-id="93437-108">Las consultas más complejas pueden requerir el uso de [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span><span class="sxs-lookup"><span data-stu-id="93437-108">More complex queries may require the use of [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span></span>

<span data-ttu-id="93437-109">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="93437-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="93437-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="93437-110">Syntax</span></span>


```VB
SWbemObject.InstancesAsync_( _
  ByVal objWbemSink, _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="93437-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="93437-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93437-112">*objWbemSink* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="93437-112">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93437-113">Receptor de objeto que devuelve las instancias de.</span><span class="sxs-lookup"><span data-stu-id="93437-113">Object sink that returns the instances.</span></span>

</dd> <dt>

<span data-ttu-id="93437-114">*iFlags* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="93437-114">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="93437-115">Entero que determina el comportamiento de la llamada.</span><span class="sxs-lookup"><span data-stu-id="93437-115">Integer that determines the behavior of the call.</span></span> <span data-ttu-id="93437-116">Este parámetro puede aceptar los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="93437-116">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="93437-117"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="93437-117"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="93437-118">Hace que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**SWbemSink. OnProgress**](swbemsink-onprogress.md) para el receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="93437-118">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="93437-119"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="93437-119"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="93437-120">Impide que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**OnProgress**](swbemsink-onprogress.md) para el receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="93437-120">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="93437-121"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="93437-121"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="93437-122">Hace que WMI devuelva las descripciones de clase y propiedad localizadas.</span><span class="sxs-lookup"><span data-stu-id="93437-122">Causes WMI to return the localized class and property descriptions.</span></span> <span data-ttu-id="93437-123">Para obtener más información, consulte [localizar información de clase WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="93437-123">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="93437-124">*objwbemNamedValueSet* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="93437-124">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="93437-125">Normalmente, esto no está definido.</span><span class="sxs-lookup"><span data-stu-id="93437-125">Typically, this is undefined.</span></span> <span data-ttu-id="93437-126">De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que atiende la solicitud.</span><span class="sxs-lookup"><span data-stu-id="93437-126">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="93437-127">Un proveedor que admite o requiere tal información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.</span><span class="sxs-lookup"><span data-stu-id="93437-127">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="93437-128">*objWbemAsyncContext* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="93437-128">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="93437-129">Se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que devuelve al receptor del objeto para identificar el origen de la llamada asincrónica original.</span><span class="sxs-lookup"><span data-stu-id="93437-129">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="93437-130">Utilice este parámetro si va a realizar varias llamadas asincrónicas mediante el mismo receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="93437-130">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="93437-131">Para usar este parámetro, cree un objeto **SWbemNamedValueSet** y use el método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) para agregar un valor que identifique la llamada asincrónica que está realizando.</span><span class="sxs-lookup"><span data-stu-id="93437-131">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="93437-132">Este objeto **SWbemNamedValueSet** se devuelve al receptor del objeto y el origen de la llamada se puede extraer mediante el método [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="93437-132">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="93437-133">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="93437-133">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93437-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="93437-134">Return value</span></span>

<span data-ttu-id="93437-135">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="93437-135">This method does not return a value.</span></span> <span data-ttu-id="93437-136">Si se realiza correctamente, el receptor recibe un evento [**OnObjectReady**](swbemsink-onobjectready.md) por cada instancia.</span><span class="sxs-lookup"><span data-stu-id="93437-136">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="93437-137">Después de la última instancia, el receptor de objeto recibirá un evento [**alcompleto**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="93437-137">After the last instance, the object sink will receive an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="93437-138">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="93437-138">Error codes</span></span>

<span data-ttu-id="93437-139">Después de completar el método **InstancesAsync \_** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="93437-139">After the completion of the **InstancesAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="93437-140">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="93437-140">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="93437-141">El usuario actual no tiene permiso para ver las instancias de la clase especificada.</span><span class="sxs-lookup"><span data-stu-id="93437-141">Current user does not have permission to view instances of the specified class.</span></span>

</dd> <dt>

<span data-ttu-id="93437-142">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="93437-142">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="93437-143">Se produjo un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="93437-143">Unspecified error occurred.</span></span>

</dd> <dt>

<span data-ttu-id="93437-144">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="93437-144">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="93437-145">La clase especificada no es válida.</span><span class="sxs-lookup"><span data-stu-id="93437-145">Specified class is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="93437-146">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="93437-146">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="93437-147">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="93437-147">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="93437-148">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="93437-148">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="93437-149">Memoria insuficiente para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="93437-149">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="93437-150">Observaciones</span><span class="sxs-lookup"><span data-stu-id="93437-150">Remarks</span></span>

<span data-ttu-id="93437-151">Esta llamada se devuelve inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="93437-151">This call returns immediately.</span></span> <span data-ttu-id="93437-152">Los objetos y el estado solicitados se devuelven al autor de la llamada mediante devoluciones de llamada entregadas al receptor que se especifica en *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="93437-152">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="93437-153">Para procesar cada objeto cuando llegue, cree un *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="93437-153">To process each object when it arrives, create an *objWbemSink*.</span></span> <span data-ttu-id="93437-154">Subrutina de evento [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="93437-154">[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="93437-155">Después de que se devuelvan todos los objetos, puede realizar el procesamiento final en la implementación de *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="93437-155">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.</span></span> <span data-ttu-id="93437-156">Evento [**Alcompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="93437-156">[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="93437-157">Una devolución de llamada asincrónica permite que un usuario no autenticado proporcione datos al receptor.</span><span class="sxs-lookup"><span data-stu-id="93437-157">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="93437-158">Esto supone riesgos de seguridad para los scripts y las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="93437-158">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="93437-159">Para eliminar los riesgos, utilice la comunicación semisincrónica o la comunicación sincrónica.</span><span class="sxs-lookup"><span data-stu-id="93437-159">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="93437-160">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="93437-160">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="93437-161">El **método \_ InstancesAsync** solo funciona con objetos de clase.</span><span class="sxs-lookup"><span data-stu-id="93437-161">The **InstancesAsync\_** method only works for class objects.</span></span> <span data-ttu-id="93437-162">No es un error que la colección devuelta tenga cero (0) elementos.</span><span class="sxs-lookup"><span data-stu-id="93437-162">It is not an error for the returned collection to have zero (0) elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="93437-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93437-163">Requirements</span></span>



| <span data-ttu-id="93437-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="93437-164">Requirement</span></span> | <span data-ttu-id="93437-165">Value</span><span class="sxs-lookup"><span data-stu-id="93437-165">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="93437-166">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="93437-166">Minimum supported client</span></span><br/> | <span data-ttu-id="93437-167">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="93437-167">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="93437-168">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="93437-168">Minimum supported server</span></span><br/> | <span data-ttu-id="93437-169">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="93437-169">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="93437-170">Encabezado</span><span class="sxs-lookup"><span data-stu-id="93437-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="93437-171"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="93437-171"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="93437-172">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="93437-172">Type library</span></span><br/>             | <dl> <span data-ttu-id="93437-173"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="93437-173"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="93437-174">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="93437-174">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93437-175"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93437-175"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="93437-176">CLSID</span><span class="sxs-lookup"><span data-stu-id="93437-176">CLSID</span></span><br/>                    | <span data-ttu-id="93437-177">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="93437-177">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="93437-178">IID</span><span class="sxs-lookup"><span data-stu-id="93437-178">IID</span></span><br/>                      | <span data-ttu-id="93437-179">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="93437-179">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="93437-180">Vea también</span><span class="sxs-lookup"><span data-stu-id="93437-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93437-181">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="93437-181">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="93437-182">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="93437-182">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> </dl>

 

