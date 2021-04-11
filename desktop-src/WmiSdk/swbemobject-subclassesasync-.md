---
description: El \_ método SubclassesAsync de SWbemObject proporciona de forma asincrónica las subclases del objeto actual, que debe ser una clase.
ms.assetid: 14d4a609-3aa4-49bd-bea4-6a71bc24d9dd
ms.tgt_platform: multiple
title: Método SWbemObject.SubclassesAsync_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.SubclassesAsync_
- ISWbemObject.SubclassesAsync_
- ISWbemObject.SubclassesAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6e922953e9f25aae2e47ea572678790b1228a581
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279105"
---
# <a name="swbemobjectsubclassesasync_-method"></a><span data-ttu-id="8ef87-103">SWbemObject. SubclassesAsync, \_ método</span><span class="sxs-lookup"><span data-stu-id="8ef87-103">SWbemObject.SubclassesAsync\_ method</span></span>

<span data-ttu-id="8ef87-104">El **método \_ SubclassesAsync** de [**SWbemObject**](swbemobject.md) proporciona de forma asincrónica las subclases del objeto actual, que debe ser una clase.</span><span class="sxs-lookup"><span data-stu-id="8ef87-104">The **SubclassesAsync\_** method of [**SWbemObject**](swbemobject.md) asynchronously supplies the subclasses of the current object, which must be a class.</span></span>

<span data-ttu-id="8ef87-105">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="8ef87-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8ef87-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8ef87-106">Syntax</span></span>


```VB
SWbemObject.SubclassesAsync_( _
  ByVal objWbemSink, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="8ef87-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8ef87-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ef87-108">*objWbemSink* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8ef87-108">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ef87-109">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8ef87-109">Required.</span></span> <span data-ttu-id="8ef87-110">Receptor de objeto que recibe los objetos de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="8ef87-110">Object sink that receives the objects asynchronously.</span></span>

</dd> <dt>

<span data-ttu-id="8ef87-111">*iFlags* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8ef87-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8ef87-112">Determina la información detallada que enumera la llamada.</span><span class="sxs-lookup"><span data-stu-id="8ef87-112">Determines how detailed the call enumerates.</span></span> <span data-ttu-id="8ef87-113">Este parámetro puede aceptar los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="8ef87-113">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="8ef87-114"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemQueryFlagDeep \* \* \* \* (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="8ef87-114"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="8ef87-115">Fuerza la enumeración recursiva en todas las subclases derivadas de la clase primaria especificada.</span><span class="sxs-lookup"><span data-stu-id="8ef87-115">Forces recursive enumeration into all subclasses derived from the specified parent class.</span></span> <span data-ttu-id="8ef87-116">La propia clase primaria no se devuelve en la enumeración.</span><span class="sxs-lookup"><span data-stu-id="8ef87-116">The parent class itself is not returned in the enumeration.</span></span>

</dd> <dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="8ef87-117"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemQueryFlagShallow \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="8ef87-117"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="8ef87-118">Valor predeterminado para este parámetro.</span><span class="sxs-lookup"><span data-stu-id="8ef87-118">Default for this parameter.</span></span> <span data-ttu-id="8ef87-119">Obliga a la enumeración a incluir solo las subclases inmediatas de la clase primaria especificada.</span><span class="sxs-lookup"><span data-stu-id="8ef87-119">It forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="8ef87-120"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="8ef87-120"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="8ef87-121">Hace que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**SWbemSink. OnProgress**](swbemsink-onprogress.md) para el receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="8ef87-121">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="8ef87-122"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="8ef87-122"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="8ef87-123">Impide que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**OnProgress**](swbemsink-onprogress.md) para el receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="8ef87-123">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="8ef87-124"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="8ef87-124"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="8ef87-125">Hace que WMI devuelva datos de modificación de clase con la definición de clase base.</span><span class="sxs-lookup"><span data-stu-id="8ef87-125">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="8ef87-126">Para obtener más información acerca de los calificadores modificados, consulte [localizar información de clase WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="8ef87-126">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="8ef87-127">*objWbemNamedValueSet* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8ef87-127">*objWbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8ef87-128">Normalmente, esto no está definido.</span><span class="sxs-lookup"><span data-stu-id="8ef87-128">Typically, this is undefined.</span></span> <span data-ttu-id="8ef87-129">De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que atiende la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8ef87-129">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="8ef87-130">Un proveedor que admite o requiere tal información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.</span><span class="sxs-lookup"><span data-stu-id="8ef87-130">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="8ef87-131">*objWbemAsyncContext* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8ef87-131">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8ef87-132">Se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que devuelve al receptor del objeto para identificar el origen de la llamada asincrónica original.</span><span class="sxs-lookup"><span data-stu-id="8ef87-132">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="8ef87-133">Utilice este parámetro cuando realice varias llamadas asincrónicas mediante el mismo receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="8ef87-133">Use this parameter when you make multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="8ef87-134">Para usar este parámetro, cree un objeto **SWbemNamedValueSet** y use el método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) para agregar un valor que identifique la llamada asincrónica que está realizando.</span><span class="sxs-lookup"><span data-stu-id="8ef87-134">To use this parameter, create an **SWbemNamedValueSet** object, and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="8ef87-135">Este objeto **SWbemNamedValueSet** se devuelve al receptor del objeto y el origen de la llamada se puede extraer mediante el método [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="8ef87-135">This **SWbemNamedValueSet** object is returned to the object sink, and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="8ef87-136">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="8ef87-136">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ef87-137">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8ef87-137">Return value</span></span>

<span data-ttu-id="8ef87-138">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="8ef87-138">This method does not return a value.</span></span> <span data-ttu-id="8ef87-139">Si se realiza correctamente, el receptor recibe un evento [**OnObjectReady**](swbemsink-onobjectready.md) para cada instancia.</span><span class="sxs-lookup"><span data-stu-id="8ef87-139">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event for each instance.</span></span> <span data-ttu-id="8ef87-140">Después de la última instancia, el receptor del objeto recibe un evento [**alcompleto**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="8ef87-140">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8ef87-141">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="8ef87-141">Error codes</span></span>

<span data-ttu-id="8ef87-142">Después de completar el método **SubclassesAsync \_** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="8ef87-142">After the completion of the **SubclassesAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="8ef87-143">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="8ef87-143">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="8ef87-144">El usuario actual no tiene permiso para ver una o varias de las clases devueltas por la llamada.</span><span class="sxs-lookup"><span data-stu-id="8ef87-144">Current user does not have permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="8ef87-145">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="8ef87-145">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="8ef87-146">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="8ef87-146">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="8ef87-147">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="8ef87-147">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="8ef87-148">La clase especificada no existe.</span><span class="sxs-lookup"><span data-stu-id="8ef87-148">Specified class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="8ef87-149">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="8ef87-149">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="8ef87-150">Se especificó un parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="8ef87-150">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="8ef87-151">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="8ef87-151">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="8ef87-152">Memoria insuficiente para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="8ef87-152">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8ef87-153">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8ef87-153">Remarks</span></span>

<span data-ttu-id="8ef87-154">Esta llamada se devuelve inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="8ef87-154">This call returns immediately.</span></span> <span data-ttu-id="8ef87-155">Los objetos y el estado solicitados se devuelven al autor de la llamada mediante devoluciones de llamada entregadas al receptor que se especifica en *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="8ef87-155">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="8ef87-156">Para procesar cada objeto cuando llegue, cree un *objWbemSink*. Subrutina de evento [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="8ef87-156">To process each object when it arrives, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="8ef87-157">Después de que se devuelvan todos los objetos, puede realizar el procesamiento final en la implementación de *objWbemSink*. Evento [**Alcompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="8ef87-157">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="8ef87-158">Una devolución de llamada asincrónica permite que un usuario no autenticado proporcione datos al receptor.</span><span class="sxs-lookup"><span data-stu-id="8ef87-158">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="8ef87-159">Esto supone riesgos de seguridad para los scripts y las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="8ef87-159">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="8ef87-160">Para eliminar los riesgos, utilice la comunicación semisincrónica o la comunicación sincrónica.</span><span class="sxs-lookup"><span data-stu-id="8ef87-160">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="8ef87-161">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="8ef87-161">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="8ef87-162">Se recomienda que los scripts comprueben el origen de la llamada mediante un parámetro *objWbemAsyncContext* .</span><span class="sxs-lookup"><span data-stu-id="8ef87-162">It is recommended that scripts verify the source of the call by using an *objWbemAsyncContext* parameter.</span></span>

<span data-ttu-id="8ef87-163">No es un error que la colección devuelta tenga cero elementos si no hay ninguna subclase del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="8ef87-163">It is not an error for the returned collection to have zero elements if there are no subclasses of the current object.</span></span> <span data-ttu-id="8ef87-164">El **método \_ SubclassesAsync** solo funciona con objetos de clase.</span><span class="sxs-lookup"><span data-stu-id="8ef87-164">The **SubclassesAsync\_** method only works for class objects.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ef87-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ef87-165">Requirements</span></span>



| <span data-ttu-id="8ef87-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ef87-166">Requirement</span></span> | <span data-ttu-id="8ef87-167">Value</span><span class="sxs-lookup"><span data-stu-id="8ef87-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ef87-168">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ef87-168">Minimum supported client</span></span><br/> | <span data-ttu-id="8ef87-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8ef87-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8ef87-170">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ef87-170">Minimum supported server</span></span><br/> | <span data-ttu-id="8ef87-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8ef87-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8ef87-172">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8ef87-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ef87-173"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ef87-173"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8ef87-174">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="8ef87-174">Type library</span></span><br/>             | <dl> <span data-ttu-id="8ef87-175"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8ef87-175"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8ef87-176">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8ef87-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ef87-177"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ef87-177"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="8ef87-178">CLSID</span><span class="sxs-lookup"><span data-stu-id="8ef87-178">CLSID</span></span><br/>                    | <span data-ttu-id="8ef87-179">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="8ef87-179">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="8ef87-180">IID</span><span class="sxs-lookup"><span data-stu-id="8ef87-180">IID</span></span><br/>                      | <span data-ttu-id="8ef87-181">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="8ef87-181">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="8ef87-182">Vea también</span><span class="sxs-lookup"><span data-stu-id="8ef87-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ef87-183">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="8ef87-183">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="8ef87-184">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="8ef87-184">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> <dt>

[<span data-ttu-id="8ef87-185">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="8ef87-185">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md)
</dt> </dl>

 

