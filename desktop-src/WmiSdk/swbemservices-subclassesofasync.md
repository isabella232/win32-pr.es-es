---
description: Devuelve una colección de subclases para una clase especificada.
ms.assetid: a9d16ee9-992e-4ce5-9c03-0a2c9958588c
ms.tgt_platform: multiple
title: Método SWbemServices. SubclassesOfAsync (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.SubclassesOfAsync
- ISWbemServices.SubclassesOfAsync
- ISWbemServices.SubclassesOfAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d8d325c96ea1a292d8ac3afc76bfea619fe5a143
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002311"
---
# <a name="swbemservicessubclassesofasync-method"></a><span data-ttu-id="8b5a3-103">SWbemServices. SubclassesOfAsync, método</span><span class="sxs-lookup"><span data-stu-id="8b5a3-103">SWbemServices.SubclassesOfAsync method</span></span>

<span data-ttu-id="8b5a3-104">El método **SubclassesOfAsync** del objeto [**SWbemServices**](swbemservices.md) devuelve una colección de subclases para una clase especificada.</span><span class="sxs-lookup"><span data-stu-id="8b5a3-104">The **SubclassesOfAsync** method of the [**SWbemServices**](swbemservices.md) object returns a collection of subclasses for a specified class.</span></span> <span data-ttu-id="8b5a3-105">Utilice este método solo para los objetos de clase.</span><span class="sxs-lookup"><span data-stu-id="8b5a3-105">Only use this method for class objects.</span></span>

<span data-ttu-id="8b5a3-106">Se llama a este método en el modo asincrónico.</span><span class="sxs-lookup"><span data-stu-id="8b5a3-106">This method is called in the asynchronous mode.</span></span> <span data-ttu-id="8b5a3-107">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="8b5a3-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="8b5a3-108">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="8b5a3-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8b5a3-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8b5a3-109">Syntax</span></span>


```VB
SWbemServices.SubclassesOfAsync( _
  ByVal ObjWbemSink, _
  [ ByVal strSuperclass ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="8b5a3-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8b5a3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b5a3-111">*ObjWbemSink*</span><span class="sxs-lookup"><span data-stu-id="8b5a3-111">*ObjWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="8b5a3-112">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8b5a3-112">Required.</span></span> <span data-ttu-id="8b5a3-113">Receptor de objeto que recibe las subclases de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="8b5a3-113">Object sink that receives the subclasses asynchronously.</span></span> <span data-ttu-id="8b5a3-114">Cree un objeto [**SWbemSink**](swbemsink.md) para recibir los objetos.</span><span class="sxs-lookup"><span data-stu-id="8b5a3-114">Create a [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="8b5a3-115">*strSuperclass* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="8b5a3-115">*strSuperclass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8b5a3-116">Especifica un nombre de clase principal.</span><span class="sxs-lookup"><span data-stu-id="8b5a3-116">Specifies a parent class name.</span></span> <span data-ttu-id="8b5a3-117">Solo las clases que son subclases de esta clase se devuelven en el enumerador.</span><span class="sxs-lookup"><span data-stu-id="8b5a3-117">Only the classes that are subclasses of this class are returned in the enumerator.</span></span> <span data-ttu-id="8b5a3-118">Si este parámetro está en blanco y el valor de *iFlags* es **wbemQueryFlagShallow**, solo se devuelven las clases de nivel superior (es decir, las clases que no tienen clase primaria).</span><span class="sxs-lookup"><span data-stu-id="8b5a3-118">If this parameter is blank, and if *iFlags* is **wbemQueryFlagShallow**, only the top-level classes are returned (that is, classes that have no parent class).</span></span> <span data-ttu-id="8b5a3-119">Si este parámetro está en blanco y si *iFlags* es **wbemQueryFlagDeep**, se devuelven todas las clases del espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="8b5a3-119">If this parameter is blank, and if *iFlags* is **wbemQueryFlagDeep**, all classes within the namespace are returned.</span></span>

</dd> <dt>

<span data-ttu-id="8b5a3-120">*iFlags* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="8b5a3-120">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8b5a3-121">Determina la profundidad de la enumeración de llamadas.</span><span class="sxs-lookup"><span data-stu-id="8b5a3-121">Determines the depth of the call enumeration.</span></span> <span data-ttu-id="8b5a3-122">El valor predeterminado de este parámetro es **wbemQueryFlagDeep**.</span><span class="sxs-lookup"><span data-stu-id="8b5a3-122">The default value for this parameter is **wbemQueryFlagDeep**.</span></span> <span data-ttu-id="8b5a3-123">Este parámetro puede aceptar los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="8b5a3-123">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="8b5a3-124"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemQueryFlagShallow \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="8b5a3-124"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="8b5a3-125">Fuerza a la enumeración a incluir solo las subclases inmediatas de la clase primaria especificada.</span><span class="sxs-lookup"><span data-stu-id="8b5a3-125">Forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="8b5a3-126"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemQueryFlagDeep \* \* \* \* (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="8b5a3-126"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="8b5a3-127">Valor predeterminado para este parámetro.</span><span class="sxs-lookup"><span data-stu-id="8b5a3-127">Default for this parameter.</span></span> <span data-ttu-id="8b5a3-128">Este valor fuerza la enumeración recursiva en todas las subclases que se derivan de la clase primaria especificada.</span><span class="sxs-lookup"><span data-stu-id="8b5a3-128">This value forces recursive enumeration into all subclasses that are derived from the specified parent class.</span></span> <span data-ttu-id="8b5a3-129">La clase primaria no se devuelve en la enumeración.</span><span class="sxs-lookup"><span data-stu-id="8b5a3-129">The parent class is not returned in the enumeration.</span></span>

</dd> <dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="8b5a3-130"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="8b5a3-130"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="8b5a3-131">Hace que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**OnProgress**](swbemsink-onprogress.md) para el receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="8b5a3-131">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="8b5a3-132"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="8b5a3-132"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="8b5a3-133">Impide que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**OnProgress**](swbemsink-onprogress.md) para el receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="8b5a3-133">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="8b5a3-134"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="8b5a3-134"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="8b5a3-135">Hace que WMI devuelva datos de modificación de clase con la definición de clase base.</span><span class="sxs-lookup"><span data-stu-id="8b5a3-135">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="8b5a3-136">Para obtener más información, consulte [localizar información de clase WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="8b5a3-136">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="8b5a3-137">*objwbemNamedValueSet* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="8b5a3-137">*objwbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8b5a3-138">Normalmente, este parámetro es indefinido.</span><span class="sxs-lookup"><span data-stu-id="8b5a3-138">Typically, this parameter is undefined.</span></span> <span data-ttu-id="8b5a3-139">De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que atiende la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8b5a3-139">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="8b5a3-140">Un proveedor que admite o requiere tal información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.</span><span class="sxs-lookup"><span data-stu-id="8b5a3-140">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="8b5a3-141">*objWbemAsyncContext* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="8b5a3-141">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8b5a3-142">Un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que devuelve al receptor del objeto para identificar el origen de la llamada asincrónica original.</span><span class="sxs-lookup"><span data-stu-id="8b5a3-142">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="8b5a3-143">Use este parámetro para realizar varias llamadas asincrónicas mediante el mismo receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="8b5a3-143">Use this parameter to make multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="8b5a3-144">Para usar este parámetro, cree un objeto **SWbemNamedValueSet** y use el método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) para agregar un valor que identifique la llamada asincrónica que está realizando.</span><span class="sxs-lookup"><span data-stu-id="8b5a3-144">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="8b5a3-145">Este objeto **SWbemNamedValueSet** se devuelve al receptor del objeto y el origen de la llamada se puede extraer mediante el método [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="8b5a3-145">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="8b5a3-146">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="8b5a3-146">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b5a3-147">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8b5a3-147">Return value</span></span>

<span data-ttu-id="8b5a3-148">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="8b5a3-148">This method does not return a value.</span></span> <span data-ttu-id="8b5a3-149">Si se realiza correctamente, el receptor recibe un evento [**OnObjectReady**](swbemsink-onobjectready.md) por cada instancia.</span><span class="sxs-lookup"><span data-stu-id="8b5a3-149">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="8b5a3-150">Después de la última instancia, el receptor del objeto recibe un evento [**alcompleto**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="8b5a3-150">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8b5a3-151">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="8b5a3-151">Error codes</span></span>

<span data-ttu-id="8b5a3-152">Después de completar el método **SubclassesOfAsync** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="8b5a3-152">After the completion of the **SubclassesOfAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

> [!Note]  
> <span data-ttu-id="8b5a3-153">Una colección devuelta con cero elementos no es un error.</span><span class="sxs-lookup"><span data-stu-id="8b5a3-153">A returned collection with zero elements is not an error.</span></span>

 

<dl> <dt>

<span data-ttu-id="8b5a3-154">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="8b5a3-154">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="8b5a3-155">El usuario actual no tiene permiso para ver una o varias de las clases devueltas por la llamada.</span><span class="sxs-lookup"><span data-stu-id="8b5a3-155">Current user does not have the permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="8b5a3-156">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="8b5a3-156">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="8b5a3-157">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="8b5a3-157">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="8b5a3-158">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="8b5a3-158">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="8b5a3-159">La clase especificada no existe.</span><span class="sxs-lookup"><span data-stu-id="8b5a3-159">Specified class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="8b5a3-160">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="8b5a3-160">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="8b5a3-161">Se especificó un parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="8b5a3-161">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="8b5a3-162">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="8b5a3-162">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="8b5a3-163">Memoria insuficiente para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="8b5a3-163">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8b5a3-164">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8b5a3-164">Remarks</span></span>

<span data-ttu-id="8b5a3-165">Esta llamada se devuelve inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="8b5a3-165">This call returns immediately.</span></span> <span data-ttu-id="8b5a3-166">Los objetos y el estado solicitados se devuelven al autor de la llamada mediante devoluciones de llamada entregadas al receptor que se especifica en *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="8b5a3-166">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="8b5a3-167">Para procesar cada objeto cuando llegue, cree un *objWbemSink*. Subrutina de evento [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="8b5a3-167">To process each object when it arrives, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="8b5a3-168">Después de que se devuelvan todos los objetos, puede realizar el procesamiento final en la implementación de *objWbemSink*. Evento [**Alcompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="8b5a3-168">After all the objects are returned, you can perform the final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="8b5a3-169">Una devolución de llamada asincrónica permite que un usuario no autenticado proporcione datos al receptor.</span><span class="sxs-lookup"><span data-stu-id="8b5a3-169">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="8b5a3-170">Esto supone riesgos de seguridad para los scripts y las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="8b5a3-170">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="8b5a3-171">Para eliminar los riesgos, consulte [configuración de la seguridad en una llamada asincrónica](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="8b5a3-171">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8b5a3-172">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b5a3-172">Requirements</span></span>



| <span data-ttu-id="8b5a3-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b5a3-173">Requirement</span></span> | <span data-ttu-id="8b5a3-174">Value</span><span class="sxs-lookup"><span data-stu-id="8b5a3-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b5a3-175">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b5a3-175">Minimum supported client</span></span><br/> | <span data-ttu-id="8b5a3-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8b5a3-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8b5a3-177">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b5a3-177">Minimum supported server</span></span><br/> | <span data-ttu-id="8b5a3-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8b5a3-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8b5a3-179">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8b5a3-179">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b5a3-180"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b5a3-180"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8b5a3-181">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="8b5a3-181">Type library</span></span><br/>             | <dl> <span data-ttu-id="8b5a3-182"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8b5a3-182"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8b5a3-183">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8b5a3-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b5a3-184"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b5a3-184"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="8b5a3-185">CLSID</span><span class="sxs-lookup"><span data-stu-id="8b5a3-185">CLSID</span></span><br/>                    | <span data-ttu-id="8b5a3-186">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="8b5a3-186">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="8b5a3-187">IID</span><span class="sxs-lookup"><span data-stu-id="8b5a3-187">IID</span></span><br/>                      | <span data-ttu-id="8b5a3-188">\_ISWBEMSERVICES IID</span><span class="sxs-lookup"><span data-stu-id="8b5a3-188">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="8b5a3-189">Vea también</span><span class="sxs-lookup"><span data-stu-id="8b5a3-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b5a3-190">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="8b5a3-190">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="8b5a3-191">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="8b5a3-191">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> </dl>

 

