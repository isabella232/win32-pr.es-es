---
description: Elimina la clase o instancia especificada en la ruta de acceso del objeto.
ms.assetid: f5ed170e-d002-4dd9-b8b6-b764a7a41a27
ms.tgt_platform: multiple
title: Método SWbemServices. DeleteAsync (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.DeleteAsync
- ISWbemServices.DeleteAsync
- ISWbemServices.DeleteAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: adc8811c11f67b9fc92628740bd15df2086948d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715720"
---
# <a name="swbemservicesdeleteasync-method"></a><span data-ttu-id="42a55-103">SWbemServices. DeleteAsync, método</span><span class="sxs-lookup"><span data-stu-id="42a55-103">SWbemServices.DeleteAsync method</span></span>

<span data-ttu-id="42a55-104">El método **DeleteAsync** del objeto [**SWbemServices**](swbemservices.md) elimina la clase o instancia especificada en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="42a55-104">The **DeleteAsync** method of the [**SWbemServices**](swbemservices.md) object deletes the class or instance specified in the object path.</span></span> <span data-ttu-id="42a55-105">La llamada a **DeleteAsync** vuelve inmediatamente y los resultados y el estado se devuelven al autor de la llamada a través de los eventos entregados al receptor especificado en *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="42a55-105">The call to **DeleteAsync** returns immediately and the results and status are returned to the caller through events delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="42a55-106">Para obtener más información acerca de la creación de un receptor, consulte [recibir un evento WMI](receiving-a-wmi-event.md).</span><span class="sxs-lookup"><span data-stu-id="42a55-106">For more information about creating a sink, see [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span> <span data-ttu-id="42a55-107">Solo puede eliminar objetos en el espacio de nombres al que está conectado.</span><span class="sxs-lookup"><span data-stu-id="42a55-107">You can only delete objects in the namespace to which you are connected.</span></span>

<span data-ttu-id="42a55-108">Si un proveedor dinámico proporciona la clase o la instancia, a veces no es posible eliminar este objeto a menos que el proveedor admita la eliminación de la clase o la instancia.</span><span class="sxs-lookup"><span data-stu-id="42a55-108">If a dynamic provider supplies the class or instance, sometimes it is not possible to delete this object unless the provider supports class or instance deletion.</span></span>

<span data-ttu-id="42a55-109">Se llama al método en el modo asincrónico.</span><span class="sxs-lookup"><span data-stu-id="42a55-109">The method is called in the asynchronous mode.</span></span> <span data-ttu-id="42a55-110">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="42a55-110">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="42a55-111">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="42a55-111">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="42a55-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="42a55-112">Syntax</span></span>


```VB
SWbemServices.DeleteAsync( _
  [ ByVal ObjWbemSink ], _
  ByVal strObjectPath, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="42a55-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="42a55-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42a55-114">*ObjWbemSink* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="42a55-114">*ObjWbemSink* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="42a55-115">Receptor de objeto que recibe los resultados de la eliminación.</span><span class="sxs-lookup"><span data-stu-id="42a55-115">Object sink that receives the results of the deletion.</span></span> <span data-ttu-id="42a55-116">Cree un objeto [**SWbemSink**](swbemsink.md) para recibir los objetos.</span><span class="sxs-lookup"><span data-stu-id="42a55-116">Create an [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="42a55-117">*strObjectPath*</span><span class="sxs-lookup"><span data-stu-id="42a55-117">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="42a55-118">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="42a55-118">Required.</span></span> <span data-ttu-id="42a55-119">Cadena que contiene la ruta de acceso al objeto que desea eliminar.</span><span class="sxs-lookup"><span data-stu-id="42a55-119">String that contains the object path to the object that you want to delete.</span></span> <span data-ttu-id="42a55-120">Para obtener más información, vea [Descripción de la ubicación de un objeto WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="42a55-120">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="42a55-121">*iFlags* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="42a55-121">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="42a55-122">Determina si se devuelven actualizaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="42a55-122">Determines if status updates are returned.</span></span> <span data-ttu-id="42a55-123">Este parámetro puede aceptar los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="42a55-123">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="42a55-124"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="42a55-124"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="42a55-125">Hace que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**OnProgress**](swbemsink-onprogress.md) para el receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="42a55-125">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="42a55-126"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="42a55-126"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="42a55-127">Impide que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**OnProgress**](swbemsink-onprogress.md) para el receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="42a55-127">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="42a55-128">*objWbemNamedValueSet* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="42a55-128">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="42a55-129">Normalmente, esto no está definido.</span><span class="sxs-lookup"><span data-stu-id="42a55-129">Typically, this is undefined.</span></span> <span data-ttu-id="42a55-130">De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que atiende la solicitud.</span><span class="sxs-lookup"><span data-stu-id="42a55-130">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="42a55-131">Un proveedor que admite o requiere tal información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.</span><span class="sxs-lookup"><span data-stu-id="42a55-131">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="42a55-132">*objWbemAsyncContext* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="42a55-132">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="42a55-133">Un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que devuelve al receptor del objeto para identificar el origen de la llamada asincrónica original.</span><span class="sxs-lookup"><span data-stu-id="42a55-133">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="42a55-134">Utilice este parámetro si va a realizar varias llamadas asincrónicas mediante el mismo receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="42a55-134">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="42a55-135">Para usar este parámetro, cree un objeto **SWbemNamedValueSet** y use el método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) para agregar un valor que identifique la llamada asincrónica que está realizando.</span><span class="sxs-lookup"><span data-stu-id="42a55-135">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="42a55-136">Este objeto **SWbemNamedValueSet** se devuelve al receptor del objeto y el origen de la llamada se puede extraer mediante el método [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="42a55-136">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="42a55-137">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="42a55-137">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42a55-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="42a55-138">Return value</span></span>

<span data-ttu-id="42a55-139">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="42a55-139">This method does not return a value.</span></span> <span data-ttu-id="42a55-140">Si la llamada se realiza correctamente, el receptor del objeto recibe la notificación de la eliminación.</span><span class="sxs-lookup"><span data-stu-id="42a55-140">If the call is successful, the object sink receives notification of the deletion.</span></span>

## <a name="error-codes"></a><span data-ttu-id="42a55-141">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="42a55-141">Error codes</span></span>

<span data-ttu-id="42a55-142">Después de completar el método **DeleteAsync** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="42a55-142">After the completion of the **DeleteAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="42a55-143">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="42a55-143">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="42a55-144">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="42a55-144">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="42a55-145">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="42a55-145">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="42a55-146">Se especificó un parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="42a55-146">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="42a55-147">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="42a55-147">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="42a55-148">Memoria insuficiente para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="42a55-148">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="42a55-149">**wbemErrTransportFailure** -2147749909 (0x80041015)</span><span class="sxs-lookup"><span data-stu-id="42a55-149">**wbemErrTransportFailure** - 2147749909 (0x80041015)</span></span>
</dt> <dd>

<span data-ttu-id="42a55-150">Se produjo un error de red, evitando el funcionamiento normal.</span><span class="sxs-lookup"><span data-stu-id="42a55-150">Networking error occurred, preventing normal operation.</span></span>

</dd> <dt>

<span data-ttu-id="42a55-151">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="42a55-151">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="42a55-152">El nombre de usuario y la contraseña actuales o especificados no son válidos o están autorizados para establecer la conexión.</span><span class="sxs-lookup"><span data-stu-id="42a55-152">Current or specified user name and password are not valid or authorized to make the connection.</span></span>

</dd> <dt>

<span data-ttu-id="42a55-153">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="42a55-153">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="42a55-154">No se encontró el elemento solicitado.</span><span class="sxs-lookup"><span data-stu-id="42a55-154">Requested item was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="42a55-155">Observaciones</span><span class="sxs-lookup"><span data-stu-id="42a55-155">Remarks</span></span>

<span data-ttu-id="42a55-156">Esta llamada se devuelve inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="42a55-156">This call returns immediately.</span></span> <span data-ttu-id="42a55-157">El estado de la operación de eliminación se devuelve al autor de la llamada a través de una devolución de llamada que se entrega al receptor que se especifica en *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="42a55-157">The status of the delete operation is returned to the caller through a callback delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="42a55-158">Puede realizar el procesamiento final en su implementación de *objWbemSink*. Evento [**Alcompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="42a55-158">You can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="42a55-159">Una devolución de llamada asincrónica permite que un usuario no autenticado proporcione datos al receptor.</span><span class="sxs-lookup"><span data-stu-id="42a55-159">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="42a55-160">Esto supone riesgos de seguridad para los scripts y las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="42a55-160">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="42a55-161">Para eliminar los riesgos, consulte [configuración de la seguridad en una llamada asincrónica](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="42a55-161">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="42a55-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42a55-162">Requirements</span></span>



| <span data-ttu-id="42a55-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="42a55-163">Requirement</span></span> | <span data-ttu-id="42a55-164">Value</span><span class="sxs-lookup"><span data-stu-id="42a55-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="42a55-165">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42a55-165">Minimum supported client</span></span><br/> | <span data-ttu-id="42a55-166">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="42a55-166">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="42a55-167">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42a55-167">Minimum supported server</span></span><br/> | <span data-ttu-id="42a55-168">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="42a55-168">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="42a55-169">Encabezado</span><span class="sxs-lookup"><span data-stu-id="42a55-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="42a55-170"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="42a55-170"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="42a55-171">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="42a55-171">Type library</span></span><br/>             | <dl> <span data-ttu-id="42a55-172"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="42a55-172"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="42a55-173">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="42a55-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42a55-174"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42a55-174"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="42a55-175">CLSID</span><span class="sxs-lookup"><span data-stu-id="42a55-175">CLSID</span></span><br/>                    | <span data-ttu-id="42a55-176">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="42a55-176">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="42a55-177">IID</span><span class="sxs-lookup"><span data-stu-id="42a55-177">IID</span></span><br/>                      | <span data-ttu-id="42a55-178">\_ISWBEMSERVICES IID</span><span class="sxs-lookup"><span data-stu-id="42a55-178">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="42a55-179">Vea también</span><span class="sxs-lookup"><span data-stu-id="42a55-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42a55-180">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="42a55-180">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="42a55-181">**SWbemObjectPath**</span><span class="sxs-lookup"><span data-stu-id="42a55-181">**SWbemObjectPath**</span></span>](swbemobjectpath.md)
</dt> </dl>

 

