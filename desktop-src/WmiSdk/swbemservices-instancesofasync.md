---
description: Recupera las instancias de una clase especificada según los criterios especificados por el usuario.
ms.assetid: 631cd749-9a39-4606-9a38-0b4bb5b4b2cd
ms.tgt_platform: multiple
title: Método SWbemServices. InstancesOfAsync (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.InstancesOfAsync
- ISWbemServices.InstancesOfAsync
- ISWbemServices.InstancesOfAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c518cb38a0ecb221f4fcb0d0e7f9ce6dfc226ba9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908545"
---
# <a name="swbemservicesinstancesofasync-method"></a><span data-ttu-id="746cd-103">SWbemServices. InstancesOfAsync, método</span><span class="sxs-lookup"><span data-stu-id="746cd-103">SWbemServices.InstancesOfAsync method</span></span>

<span data-ttu-id="746cd-104">El método **InstancesOfAsync** del objeto [**SWbemServices**](swbemservices.md) recupera las instancias de una clase especificada según los criterios especificados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="746cd-104">The **InstancesOfAsync** method of the [**SWbemServices**](swbemservices.md) object retrieves instances of a specified class according to user-specified criteria.</span></span>

<span data-ttu-id="746cd-105">Se llama al método en el modo asincrónico.</span><span class="sxs-lookup"><span data-stu-id="746cd-105">The method is called in the asynchronous mode.</span></span> <span data-ttu-id="746cd-106">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="746cd-106">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="746cd-107">Para ver la explicación de la sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="746cd-107">For the syntax explanation, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="746cd-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="746cd-108">Syntax</span></span>


```VB
SWbemServices.InstancesOfAsync( _
  ByVal ObjWbemSink, _
  ByVal strClass, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="746cd-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="746cd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="746cd-110">*ObjWbemSink*</span><span class="sxs-lookup"><span data-stu-id="746cd-110">*ObjWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="746cd-111">Receptor de objeto que recibe las instancias de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="746cd-111">Object sink that receives the instances asynchronously.</span></span> <span data-ttu-id="746cd-112">Cree un objeto [**SWbemSink**](swbemsink.md) para recibir los objetos.</span><span class="sxs-lookup"><span data-stu-id="746cd-112">Create a [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="746cd-113">*strClass*</span><span class="sxs-lookup"><span data-stu-id="746cd-113">*strClass*</span></span> 
</dt> <dd>

<span data-ttu-id="746cd-114">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="746cd-114">Required.</span></span> <span data-ttu-id="746cd-115">Cadena que contiene el nombre de la clase de las instancias de que desea.</span><span class="sxs-lookup"><span data-stu-id="746cd-115">String that contains the name of the class for the instances that you want.</span></span> <span data-ttu-id="746cd-116">Este parámetro no puede estar en blanco.</span><span class="sxs-lookup"><span data-stu-id="746cd-116">This parameter cannot be blank.</span></span>

</dd> <dt>

<span data-ttu-id="746cd-117">*iFlags* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="746cd-117">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="746cd-118">Determina la profundidad de la enumeración de llamadas y si la llamada se devuelve inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="746cd-118">Determines the depth of the call enumeration, and whether or not the call returns immediately.</span></span> <span data-ttu-id="746cd-119">Este parámetro puede aceptar los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="746cd-119">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="746cd-120"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemQueryFlagShallow \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="746cd-120"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="746cd-121">Fuerza a la enumeración a incluir solo las subclases inmediatas de la clase primaria especificada.</span><span class="sxs-lookup"><span data-stu-id="746cd-121">Forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="746cd-122"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemQueryFlagDeep \* \* \* \* (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="746cd-122"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="746cd-123">Valor predeterminado para este parámetro.</span><span class="sxs-lookup"><span data-stu-id="746cd-123">Default for this parameter.</span></span> <span data-ttu-id="746cd-124">Este valor fuerza a la enumeración a incluir todas las clases de la jerarquía.</span><span class="sxs-lookup"><span data-stu-id="746cd-124">This value forces the enumeration to include all classes in the hierarchy.</span></span>

</dd> <dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="746cd-125"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="746cd-125"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="746cd-126">Hace que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**OnProgress**](swbemsink-onprogress.md) para el receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="746cd-126">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="746cd-127"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="746cd-127"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="746cd-128">Impide que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**OnProgress**](swbemsink-onprogress.md) para el receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="746cd-128">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="746cd-129"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="746cd-129"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="746cd-130">Hace que WMI devuelva datos de modificación de clase con la definición de clase base.</span><span class="sxs-lookup"><span data-stu-id="746cd-130">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="746cd-131">Para obtener más información, consulte [localizar información de clase WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="746cd-131">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="746cd-132">*objWbemNamedValueSet* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="746cd-132">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="746cd-133">Normalmente, esto no está definido.</span><span class="sxs-lookup"><span data-stu-id="746cd-133">Typically, this is undefined.</span></span> <span data-ttu-id="746cd-134">De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que atiende la solicitud.</span><span class="sxs-lookup"><span data-stu-id="746cd-134">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="746cd-135">Un proveedor que admite o requiere información de contexto debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.</span><span class="sxs-lookup"><span data-stu-id="746cd-135">A provider that supports or requires context information information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="746cd-136">*objWbemAsyncContext* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="746cd-136">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="746cd-137">Un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que devuelve al receptor del objeto para identificar el origen de la llamada asincrónica original.</span><span class="sxs-lookup"><span data-stu-id="746cd-137">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="746cd-138">Utilice este parámetro si va a realizar varias llamadas asincrónicas mediante el mismo receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="746cd-138">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="746cd-139">Para usar este parámetro, cree un objeto **SWbemNamedValueSet** y use el método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) para agregar un valor que identifique la llamada asincrónica que está realizando.</span><span class="sxs-lookup"><span data-stu-id="746cd-139">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="746cd-140">Este objeto **SWbemNamedValueSet** se devuelve al receptor del objeto y el origen de la llamada se puede extraer mediante el método [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="746cd-140">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="746cd-141">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="746cd-141">Return value</span></span>

<span data-ttu-id="746cd-142">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="746cd-142">This method does not return a value.</span></span> <span data-ttu-id="746cd-143">Si se realiza correctamente, el receptor recibe un evento [**OnObjectReady**](swbemsink-onobjectready.md) por cada instancia.</span><span class="sxs-lookup"><span data-stu-id="746cd-143">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="746cd-144">Después de la última instancia, el receptor del objeto recibe un evento [**alcompleto**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="746cd-144">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="746cd-145">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="746cd-145">Error codes</span></span>

<span data-ttu-id="746cd-146">Una vez finalizado el método **InstancesOfAsync** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="746cd-146">Upon the completion of the **InstancesOfAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="746cd-147">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="746cd-147">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="746cd-148">El usuario actual no tiene permiso para ver las instancias de la clase especificada.</span><span class="sxs-lookup"><span data-stu-id="746cd-148">Current user does not have the permission to view instances of the specified class.</span></span>

</dd> <dt>

<span data-ttu-id="746cd-149">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="746cd-149">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="746cd-150">Se produjo un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="746cd-150">Unspecified error occurred.</span></span>

</dd> <dt>

<span data-ttu-id="746cd-151">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="746cd-151">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="746cd-152">La clase especificada no es válida.</span><span class="sxs-lookup"><span data-stu-id="746cd-152">Specified class is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="746cd-153">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="746cd-153">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="746cd-154">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="746cd-154">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="746cd-155">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="746cd-155">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="746cd-156">Memoria insuficiente para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="746cd-156">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="746cd-157">Observaciones</span><span class="sxs-lookup"><span data-stu-id="746cd-157">Remarks</span></span>

<span data-ttu-id="746cd-158">Esta llamada se devuelve inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="746cd-158">This call returns immediately.</span></span> <span data-ttu-id="746cd-159">Los objetos y el estado solicitados se devuelven al autor de la llamada mediante devoluciones de llamada entregadas al receptor que se especifica en *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="746cd-159">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="746cd-160">Para procesar cada objeto cuando vuelva, cree un *objWbemSink*. Subrutina de evento [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="746cd-160">To process each object when it returns, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="746cd-161">Después de que se devuelvan todos los objetos, puede realizar el procesamiento final en la implementación de *objWbemSink*. Evento [**Alcompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="746cd-161">After all the objects are returned, you can perform the final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="746cd-162">Una devolución de llamada asincrónica permite que un usuario no autenticado proporcione datos al receptor.</span><span class="sxs-lookup"><span data-stu-id="746cd-162">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="746cd-163">Esto supone riesgos de seguridad para los scripts y las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="746cd-163">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="746cd-164">Para eliminar los riesgos, consulte [configuración de la seguridad en una llamada asincrónica](setting-security-on-an-asynchronous-call.md) .</span><span class="sxs-lookup"><span data-stu-id="746cd-164">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md)</span></span>

<span data-ttu-id="746cd-165">El método **InstancesOfAsync** solo funciona con objetos de clase.</span><span class="sxs-lookup"><span data-stu-id="746cd-165">The **InstancesOfAsync** method only works for class objects.</span></span> <span data-ttu-id="746cd-166">No es un error que el enumerador devuelto tenga cero (0) elementos.</span><span class="sxs-lookup"><span data-stu-id="746cd-166">It is not an error for the returned enumerator to have zero (0) elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="746cd-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="746cd-167">Requirements</span></span>



| <span data-ttu-id="746cd-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="746cd-168">Requirement</span></span> | <span data-ttu-id="746cd-169">Value</span><span class="sxs-lookup"><span data-stu-id="746cd-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="746cd-170">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="746cd-170">Minimum supported client</span></span><br/> | <span data-ttu-id="746cd-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="746cd-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="746cd-172">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="746cd-172">Minimum supported server</span></span><br/> | <span data-ttu-id="746cd-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="746cd-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="746cd-174">Encabezado</span><span class="sxs-lookup"><span data-stu-id="746cd-174">Header</span></span><br/>                   | <dl> <span data-ttu-id="746cd-175"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="746cd-175"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="746cd-176">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="746cd-176">Type library</span></span><br/>             | <dl> <span data-ttu-id="746cd-177"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="746cd-177"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="746cd-178">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="746cd-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="746cd-179"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="746cd-179"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="746cd-180">CLSID</span><span class="sxs-lookup"><span data-stu-id="746cd-180">CLSID</span></span><br/>                    | <span data-ttu-id="746cd-181">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="746cd-181">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="746cd-182">IID</span><span class="sxs-lookup"><span data-stu-id="746cd-182">IID</span></span><br/>                      | <span data-ttu-id="746cd-183">\_ISWBEMSERVICES IID</span><span class="sxs-lookup"><span data-stu-id="746cd-183">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="746cd-184">Vea también</span><span class="sxs-lookup"><span data-stu-id="746cd-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="746cd-185">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="746cd-185">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="746cd-186">Llamar a un método</span><span class="sxs-lookup"><span data-stu-id="746cd-186">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

