---
description: Recupera un objeto, que es una definición de clase o una instancia de, en función de la ruta de acceso del objeto.
ms.assetid: 8da46851-52b8-4b5a-8c9d-1d492f57f4b6
ms.tgt_platform: multiple
title: Método SWbemServices. GetAsync (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.GetAsync
- ISWbemServices.GetAsync
- ISWbemServices.GetAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 451f13bde9458e7d57ec393f42b92a4092c99924
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908546"
---
# <a name="swbemservicesgetasync-method"></a><span data-ttu-id="158f5-103">SWbemServices. GetAsync (método)</span><span class="sxs-lookup"><span data-stu-id="158f5-103">SWbemServices.GetAsync method</span></span>

<span data-ttu-id="158f5-104">El método **GetAsync** del objeto [**SWbemServices**](swbemservices.md) recupera un objeto, que es una definición de clase o una instancia, basándose en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="158f5-104">The **GetAsync** method of the [**SWbemServices**](swbemservices.md) object retrieves an object, that is a class definition or an instance, based on the object path.</span></span>

<span data-ttu-id="158f5-105">Este método solo recupera los objetos del espacio de nombres que está asociado al objeto [**SWbemServices**](swbemservices.md) actual.</span><span class="sxs-lookup"><span data-stu-id="158f5-105">This method retrieves only objects from the namespace that is associated with the current [**SWbemServices**](swbemservices.md) object.</span></span>

<span data-ttu-id="158f5-106">Se llama a este método en el modo asincrónico.</span><span class="sxs-lookup"><span data-stu-id="158f5-106">This method is called in the asynchronous mode.</span></span> <span data-ttu-id="158f5-107">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="158f5-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="158f5-108">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="158f5-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="158f5-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="158f5-109">Syntax</span></span>


```VB
SWbemServices.GetAsync( _
  ByVal objWbemSink, _
  [ ByVal strObjectPath ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="158f5-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="158f5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="158f5-111">*objWbemSink*</span><span class="sxs-lookup"><span data-stu-id="158f5-111">*objWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="158f5-112">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="158f5-112">Required.</span></span> <span data-ttu-id="158f5-113">Receptor de objeto que obtiene objetos de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="158f5-113">Object sink that gets objects asynchronously.</span></span> <span data-ttu-id="158f5-114">Cree un objeto [**SWbemSink**](swbemsink.md) para recibir los objetos.</span><span class="sxs-lookup"><span data-stu-id="158f5-114">Create a [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="158f5-115">*strObjectPath* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="158f5-115">*strObjectPath* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="158f5-116">Ruta de acceso del objeto que se desea recuperar.</span><span class="sxs-lookup"><span data-stu-id="158f5-116">Path of the object that you want to retrieve.</span></span> <span data-ttu-id="158f5-117">Si este valor está vacío, el objeto vacío que se devuelve puede convertirse en una nueva clase.</span><span class="sxs-lookup"><span data-stu-id="158f5-117">If this value is empty, the empty object that is returned can become a new class.</span></span> <span data-ttu-id="158f5-118">Para obtener más información, vea [Descripción de la ubicación de un objeto WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="158f5-118">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="158f5-119">*iFlags* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="158f5-119">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="158f5-120">Entero que determina el comportamiento de la llamada.</span><span class="sxs-lookup"><span data-stu-id="158f5-120">Integer that determines the behavior of the call.</span></span> <span data-ttu-id="158f5-121">Este parámetro puede aceptar los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="158f5-121">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="158f5-122"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="158f5-122"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="158f5-123">Hace que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**OnProgress**](swbemsink-onprogress.md) para el receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="158f5-123">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="158f5-124"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="158f5-124"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="158f5-125">Impide que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**OnProgress**](swbemsink-onprogress.md) para el receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="158f5-125">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="158f5-126"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="158f5-126"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="158f5-127">Hace que WMI devuelva datos de modificación de clase con la definición de clase base.</span><span class="sxs-lookup"><span data-stu-id="158f5-127">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="158f5-128">Para obtener más información, consulte [localizar información de clase WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="158f5-128">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="158f5-129">*objwbemNamedValueSet* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="158f5-129">*objwbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="158f5-130">Normalmente, este valor es indefinido.</span><span class="sxs-lookup"><span data-stu-id="158f5-130">Typically, this value is undefined.</span></span> <span data-ttu-id="158f5-131">De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que atiende la solicitud.</span><span class="sxs-lookup"><span data-stu-id="158f5-131">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="158f5-132">Un proveedor que admite o requiere tal información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.</span><span class="sxs-lookup"><span data-stu-id="158f5-132">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="158f5-133">*objWbemAsyncContext* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="158f5-133">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="158f5-134">Un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que devuelve al receptor del objeto para identificar el origen de la llamada asincrónica original.</span><span class="sxs-lookup"><span data-stu-id="158f5-134">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="158f5-135">Utilice este parámetro si va a realizar varias llamadas asincrónicas mediante el mismo receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="158f5-135">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="158f5-136">Para usar este parámetro, cree un objeto **SWbemNamedValueSet** y use el método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) para agregar un valor que identifique la llamada asincrónica que está realizando.</span><span class="sxs-lookup"><span data-stu-id="158f5-136">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="158f5-137">Este objeto **SWbemNamedValueSet** se devuelve al receptor del objeto y el origen de la llamada se puede extraer mediante el método [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="158f5-137">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="158f5-138">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="158f5-138">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="158f5-139">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="158f5-139">Return value</span></span>

<span data-ttu-id="158f5-140">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="158f5-140">This method does not return a value.</span></span> <span data-ttu-id="158f5-141">Si se realiza correctamente, el receptor recibe un evento [**OnObjectReady**](swbemsink-onobjectready.md) cuando el objeto está disponible.</span><span class="sxs-lookup"><span data-stu-id="158f5-141">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event when the object is available.</span></span>

## <a name="error-codes"></a><span data-ttu-id="158f5-142">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="158f5-142">Error codes</span></span>

<span data-ttu-id="158f5-143">Después de completar el método **GetAsync** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="158f5-143">After the completion of the **GetAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="158f5-144">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="158f5-144">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="158f5-145">El usuario actual no tiene permiso para obtener acceso al objeto.</span><span class="sxs-lookup"><span data-stu-id="158f5-145">Current user does not have the permission to access the object.</span></span>

</dd> <dt>

<span data-ttu-id="158f5-146">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="158f5-146">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="158f5-147">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="158f5-147">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="158f5-148">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="158f5-148">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="158f5-149">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="158f5-149">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="158f5-150">**wbemErrInvalidObjectPath** -2147749946 (0x8004103A)</span><span class="sxs-lookup"><span data-stu-id="158f5-150">**wbemErrInvalidObjectPath** - 2147749946 (0x8004103A)</span></span>
</dt> <dd>

<span data-ttu-id="158f5-151">La ruta de acceso especificada no era válida.</span><span class="sxs-lookup"><span data-stu-id="158f5-151">Specified path was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="158f5-152">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="158f5-152">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="158f5-153">No se encontró el objeto solicitado.</span><span class="sxs-lookup"><span data-stu-id="158f5-153">Requested object could not be found.</span></span>

</dd> <dt>

<span data-ttu-id="158f5-154">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="158f5-154">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="158f5-155">Memoria insuficiente para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="158f5-155">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="158f5-156">Observaciones</span><span class="sxs-lookup"><span data-stu-id="158f5-156">Remarks</span></span>

<span data-ttu-id="158f5-157">Esta llamada se devuelve inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="158f5-157">This call returns immediately.</span></span> <span data-ttu-id="158f5-158">El objeto y el estado solicitados se devuelven al autor de la llamada a través de una devolución de llamada que se entrega al receptor que se especifica en *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="158f5-158">The requested object and status are returned to the caller through a callback delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="158f5-159">Para procesar el objeto cuando vuelve, cree un *objWbemSink*. [**OnObjectReady**](swbemsink-onobjectready.md)o *objWbemSink*. Subrutina de eventos [**Alcompletada**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="158f5-159">To process the object when it returns, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md), or an *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event subroutine.</span></span>

<span data-ttu-id="158f5-160">Una devolución de llamada asincrónica permite que un usuario no autenticado proporcione datos al receptor.</span><span class="sxs-lookup"><span data-stu-id="158f5-160">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="158f5-161">Esto supone riesgos de seguridad para los scripts y las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="158f5-161">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="158f5-162">Para eliminar los riesgos, utilice la comunicación sincrónica o semisincrónica.</span><span class="sxs-lookup"><span data-stu-id="158f5-162">To eliminate the risks, use semisynchronous or synchronous communication.</span></span> <span data-ttu-id="158f5-163">Para obtener más información, vea [establecer la seguridad en una llamada asincrónica](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="158f5-163">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="158f5-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="158f5-164">Requirements</span></span>



| <span data-ttu-id="158f5-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="158f5-165">Requirement</span></span> | <span data-ttu-id="158f5-166">Value</span><span class="sxs-lookup"><span data-stu-id="158f5-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="158f5-167">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="158f5-167">Minimum supported client</span></span><br/> | <span data-ttu-id="158f5-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="158f5-168">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="158f5-169">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="158f5-169">Minimum supported server</span></span><br/> | <span data-ttu-id="158f5-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="158f5-170">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="158f5-171">Encabezado</span><span class="sxs-lookup"><span data-stu-id="158f5-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="158f5-172"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="158f5-172"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="158f5-173">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="158f5-173">Type library</span></span><br/>             | <dl> <span data-ttu-id="158f5-174"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="158f5-174"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="158f5-175">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="158f5-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="158f5-176"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="158f5-176"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="158f5-177">CLSID</span><span class="sxs-lookup"><span data-stu-id="158f5-177">CLSID</span></span><br/>                    | <span data-ttu-id="158f5-178">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="158f5-178">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="158f5-179">IID</span><span class="sxs-lookup"><span data-stu-id="158f5-179">IID</span></span><br/>                      | <span data-ttu-id="158f5-180">\_ISWBEMSERVICES IID</span><span class="sxs-lookup"><span data-stu-id="158f5-180">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="158f5-181">Vea también</span><span class="sxs-lookup"><span data-stu-id="158f5-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="158f5-182">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="158f5-182">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="158f5-183">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="158f5-183">**SWbemObject**</span></span>](swbemobject.md)
</dt> </dl>

 

