---
description: El \_ método ExecMethodAsync de SWbemObject ejecuta de forma asincrónica un método que exporta un proveedor de métodos.
ms.assetid: b848b38b-c0c3-49cd-b1e2-b0a440b82d61
ms.tgt_platform: multiple
title: Método de cMethodAsync_ de SWbemObject.Exe(Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.ExecMethodAsync_
- ISWbemObject.ExecMethodAsync_
- ISWbemObject.ExecMethodAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8af1b7c10eed427423afea8b40a1df5bc237f99e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278975"
---
# <a name="swbemobjectexecmethodasync_-method"></a><span data-ttu-id="e2157-103">SWbemObject.Exe\_ método cMethodAsync</span><span class="sxs-lookup"><span data-stu-id="e2157-103">SWbemObject.ExecMethodAsync\_ method</span></span>

<span data-ttu-id="e2157-104">El **método \_ ExecMethodAsync** de [**SWbemObject**](swbemobject.md) ejecuta de forma asincrónica un método que exporta un proveedor de métodos.</span><span class="sxs-lookup"><span data-stu-id="e2157-104">The **ExecMethodAsync\_** method of [**SWbemObject**](swbemobject.md) asynchronously executes a method that a method provider exports.</span></span> <span data-ttu-id="e2157-105">Este método es similar a [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md), pero funciona directamente en el objeto del método que se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="e2157-105">This method is similar to [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md), but operates directly on the object of the method to be executed.</span></span> <span data-ttu-id="e2157-106">Instrumental de administración de Windows (WMI) no implementa este método.</span><span class="sxs-lookup"><span data-stu-id="e2157-106">Windows Management Instrumentation (WMI) does not implement this method.</span></span> <span data-ttu-id="e2157-107">El proveedor implementa este método.</span><span class="sxs-lookup"><span data-stu-id="e2157-107">The provider implements this method.</span></span>

<span data-ttu-id="e2157-108">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="e2157-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e2157-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e2157-109">Syntax</span></span>


```VB
objOutParams = .ExecMethodAsync_( _
  ByVal objWbemSink, _
  ByVal strMethodName, _
  [ ByVal objwbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="e2157-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e2157-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2157-111">*objWbemSink* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e2157-111">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2157-112">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e2157-112">Required.</span></span> <span data-ttu-id="e2157-113">Es el receptor del objeto que recibe los resultados de la llamada al método.</span><span class="sxs-lookup"><span data-stu-id="e2157-113">This is the object sink that receives the results of the method call.</span></span> <span data-ttu-id="e2157-114">Los parámetros de salida se envían al evento [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md) del receptor de objeto proporcionado.</span><span class="sxs-lookup"><span data-stu-id="e2157-114">The outbound parameters are sent to the [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) event of the supplied object sink.</span></span> <span data-ttu-id="e2157-115">Los resultados del mecanismo de llamada se envían al evento [**SWbemSink. Alcompleted**](swbemsink-oncompleted.md) del receptor de objetos proporcionado.</span><span class="sxs-lookup"><span data-stu-id="e2157-115">The results of the call mechanism are sent to the [**SWbemSink.OnCompleted**](swbemsink-oncompleted.md) event of the supplied object sink.</span></span> <span data-ttu-id="e2157-116">Tenga en cuenta que **SWbemSink. Alcompleted** no recibe el código de retorno del método.</span><span class="sxs-lookup"><span data-stu-id="e2157-116">Notice that **SWbemSink.OnCompleted** does not receive the return code of the method.</span></span> <span data-ttu-id="e2157-117">Sin embargo, recibe el código de retorno del mecanismo de devolución de llamada real y solo es útil para comprobar que se ha producido la llamada, o que se ha producido un error por motivos mecánicos.</span><span class="sxs-lookup"><span data-stu-id="e2157-117">However, it receives the return code of the actual call-return mechanism, and is only useful for verifying that the call occurred, or that it failed for mechanical reasons.</span></span> <span data-ttu-id="e2157-118">El código de resultado devuelto por el método se devuelve en el objeto de parámetro saliente proporcionado a **SWbemSink. OnObjectReady**.</span><span class="sxs-lookup"><span data-stu-id="e2157-118">The result code returned from the method is returned in the outbound parameter object supplied to **SWbemSink.OnObjectReady**.</span></span> <span data-ttu-id="e2157-119">Si se devuelve algún código de error, no se utiliza el objeto [**IWbemObjectSink**](iwbemobjectsink.md) proporcionado.</span><span class="sxs-lookup"><span data-stu-id="e2157-119">If any error code returns, then the supplied [**IWbemObjectSink**](iwbemobjectsink.md) object is not used.</span></span> <span data-ttu-id="e2157-120">Si la llamada se realiza correctamente, se llama a la implementación de **IWbemObjectSink** del usuario para indicar el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="e2157-120">If the call is successful, then the user's **IWbemObjectSink** implementation is called to indicate the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e2157-121">*strMethodName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e2157-121">*strMethodName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2157-122">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e2157-122">Required.</span></span> <span data-ttu-id="e2157-123">Es el nombre del método para el objeto.</span><span class="sxs-lookup"><span data-stu-id="e2157-123">This is the name of the method for the object.</span></span>

</dd> <dt>

<span data-ttu-id="e2157-124">*objwbemInParams* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e2157-124">*objwbemInParams* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e2157-125">Este es un objeto [**SWbemObject**](swbemobject.md) que contiene los parámetros de entrada para el método que se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="e2157-125">This is an [**SWbemObject**](swbemobject.md) object that contains the input parameters for the method being executed.</span></span> <span data-ttu-id="e2157-126">De forma predeterminada, este parámetro es indefinido.</span><span class="sxs-lookup"><span data-stu-id="e2157-126">By default, this parameter is undefined.</span></span> <span data-ttu-id="e2157-127">Para obtener más información, consulte [construir objetos Parameters](constructing-inparameters-objects.md) y [analizar objetos Parameters](parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="e2157-127">For more information, see [Constructing InParameters Objects](constructing-inparameters-objects.md) and [Parsing OutParameters Objects](parsing-outparameters-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2157-128">*iFlags* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e2157-128">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e2157-129">Entero que determina el comportamiento de la llamada.</span><span class="sxs-lookup"><span data-stu-id="e2157-129">Integer that determines the behavior of the call.</span></span> <span data-ttu-id="e2157-130">Este parámetro puede aceptar los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="e2157-130">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="e2157-131"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="e2157-131"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="e2157-132">Hace que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**SWbemSink. OnProgress**](swbemsink-onprogress.md) para el receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="e2157-132">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="e2157-133"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="e2157-133"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="e2157-134">Impide que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**OnProgress**](swbemsink-onprogress.md) para el receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="e2157-134">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e2157-135">*objwbemNamedValueSet* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e2157-135">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e2157-136">Normalmente, es indefinido.</span><span class="sxs-lookup"><span data-stu-id="e2157-136">Typically, it is undefined.</span></span> <span data-ttu-id="e2157-137">De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que atiende la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e2157-137">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="e2157-138">Un proveedor que admite o requiere tal información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.</span><span class="sxs-lookup"><span data-stu-id="e2157-138">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="e2157-139">*objWbemAsyncContext* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e2157-139">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e2157-140">Se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que devuelve al receptor del objeto para identificar el origen de la llamada asincrónica original.</span><span class="sxs-lookup"><span data-stu-id="e2157-140">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="e2157-141">Utilice este parámetro si va a realizar varias llamadas asincrónicas mediante el mismo receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="e2157-141">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="e2157-142">Para usar este parámetro, cree un objeto **SWbemNamedValueSet** y use el método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) para agregar un valor que identifique la llamada asincrónica que está realizando.</span><span class="sxs-lookup"><span data-stu-id="e2157-142">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="e2157-143">Este objeto **SWbemNamedValueSet** se devuelve al receptor del objeto y el origen de la llamada se puede extraer mediante el método [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="e2157-143">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="e2157-144">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="e2157-144">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2157-145">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e2157-145">Return value</span></span>

<span data-ttu-id="e2157-146">Este método no tiene ningún valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="e2157-146">This method has no return values.</span></span> <span data-ttu-id="e2157-147">Si la llamada es correcta, se proporciona un objeto [**Parameters**](swbemmethod-outparameters.md) , que también es un objeto [**SWbemObject**](swbemobject.md) , al receptor especificado en *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="e2157-147">If the call is successful, an [**OutParameters**](swbemmethod-outparameters.md) object, which is also an [**SWbemObject**](swbemobject.md) object, is supplied to the sink specified in *objWbemSink*.</span></span> <span data-ttu-id="e2157-148">El objeto **Parameters** devuelto contiene los parámetros de salida y el valor devuelto para el método que se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="e2157-148">The returned **OutParameters** object contains the output parameters and return value for the method being executed.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e2157-149">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="e2157-149">Error codes</span></span>

<span data-ttu-id="e2157-150">Después de completar el **método \_ ExecMethodAsync** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="e2157-150">After completion of the **ExecMethodAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="e2157-151">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="e2157-151">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="e2157-152">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="e2157-152">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="e2157-153">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="e2157-153">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="e2157-154">La clase especificada no era válida.</span><span class="sxs-lookup"><span data-stu-id="e2157-154">Specified class was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="e2157-155">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="e2157-155">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="e2157-156">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="e2157-156">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="e2157-157">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="e2157-157">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="e2157-158">Memoria insuficiente para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="e2157-158">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e2157-159">**wbemErrInvalidMethod** -2147749934 (0x8004102E)</span><span class="sxs-lookup"><span data-stu-id="e2157-159">**wbemErrInvalidMethod** - 2147749934 (0x8004102E)</span></span>
</dt> <dd>

<span data-ttu-id="e2157-160">El método solicitado no estaba disponible.</span><span class="sxs-lookup"><span data-stu-id="e2157-160">Requested method was not available.</span></span>

</dd> <dt>

<span data-ttu-id="e2157-161">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="e2157-161">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="e2157-162">El usuario actual no está autorizado para ejecutar el método.</span><span class="sxs-lookup"><span data-stu-id="e2157-162">Current user was not authorized to execute the method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e2157-163">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e2157-163">Remarks</span></span>

<span data-ttu-id="e2157-164">Use el método **SWbemObject.Exe\_ cMethodAsync** como alternativa al acceso directo para ejecutar un método de [*proveedor*](gloss-p.md) cuando no se puede ejecutar un método directamente.</span><span class="sxs-lookup"><span data-stu-id="e2157-164">Use the **SWbemObject.ExecMethodAsync\_** method as an alternative to direct access for executing a [*provider method*](gloss-p.md) when you cannot execute a method directly.</span></span> <span data-ttu-id="e2157-165">Por ejemplo, si el método tiene parámetros out, utilice el método **SWbemObject.Exe\_ cMethodAsync** con un lenguaje de scripting que no admita parámetros de salida.</span><span class="sxs-lookup"><span data-stu-id="e2157-165">For example, if your method has out parameters, use the **SWbemObject.ExecMethodAsync\_** method with a scripting language that does not support output parameters.</span></span> <span data-ttu-id="e2157-166">De lo contrario, se recomienda invocar un método mediante el acceso directo.</span><span class="sxs-lookup"><span data-stu-id="e2157-166">Otherwise, it is recommended that you invoke a method using direct access.</span></span> <span data-ttu-id="e2157-167">Para obtener más información, vea [manipular la información de clase e instancia](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="e2157-167">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

<span data-ttu-id="e2157-168">Esta llamada se devuelve inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="e2157-168">This call returns immediately.</span></span> <span data-ttu-id="e2157-169">Los objetos y el estado solicitados se devuelven al autor de la llamada mediante devoluciones de llamada entregadas al receptor que se especifica en *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="e2157-169">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="e2157-170">Para procesar cada objeto cuando llegue, cree un *objWbemSink*. Subrutina de evento [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="e2157-170">To process each object when it arrives, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="e2157-171">Después de que se devuelvan todos los objetos, puede realizar el procesamiento final en la implementación de *objWbemSink*. Evento [**Alcompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="e2157-171">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="e2157-172">Una devolución de llamada asincrónica permite que un usuario no autenticado proporcione datos al receptor.</span><span class="sxs-lookup"><span data-stu-id="e2157-172">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="e2157-173">Esto supone riesgos de seguridad para los scripts y las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="e2157-173">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="e2157-174">Para eliminar los riesgos, utilice la comunicación semisincrónica o la comunicación sincrónica.</span><span class="sxs-lookup"><span data-stu-id="e2157-174">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="e2157-175">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="e2157-175">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="e2157-176">Si el método que se ejecuta tiene parámetros de entrada, el objeto [**Parameters**](swbemmethod-inparameters.md) y el parámetro *objWbemInParam* se deben construir tal y como se describe en construir objetos [Parameters](constructing-inparameters-objects.md) y [analizar objetos Parameters](parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="e2157-176">If the method being executed has input parameters, the [**InParameters**](swbemmethod-inparameters.md) object and *objWbemInParam* parameter must be constructed as described in [Constructing InParameters Objects](constructing-inparameters-objects.md) and [Parsing OutParameters Objects](parsing-outparameters-objects.md).</span></span>

<span data-ttu-id="e2157-177">En el método **\_ cMethodAsyncSWbemObject.Exe** se supone que el objeto representado por [**SWbemObject**](swbemobject.md) contiene el método que se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="e2157-177">The **SWbemObject.ExecMethodAsync\_** method assumes the object represented by [**SWbemObject**](swbemobject.md) contains the method to execute.</span></span> <span data-ttu-id="e2157-178">El método [**cMethodAsyncSWbemServices.Exe**](swbemservices-execmethodasync.md) requiere una ruta de acceso al objeto.</span><span class="sxs-lookup"><span data-stu-id="e2157-178">The [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md) method requires an object path.</span></span>

## <a name="examples"></a><span data-ttu-id="e2157-179">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e2157-179">Examples</span></span>

<span data-ttu-id="e2157-180">En el ejemplo siguiente se muestra el método [**ExecMethodAsync**](swbemservices-execmethodasync.md) .</span><span class="sxs-lookup"><span data-stu-id="e2157-180">The following example shows the [**ExecMethodAsync**](swbemservices-execmethodasync.md) method.</span></span> <span data-ttu-id="e2157-181">El script crea un objeto de [**\_ proceso de Win32**](/windows/desktop/CIMWin32Prov/win32-process) que representa un proceso que ejecuta el Bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="e2157-181">The script creates a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) object that represents a process that is running Notepad.</span></span> <span data-ttu-id="e2157-182">Muestra cómo configurar el objeto [**Parameters**](swbemmethod-inparameters.md) y cómo obtener los resultados de un objeto [**Parameters**](swbemmethod-outparameters.md) .</span><span class="sxs-lookup"><span data-stu-id="e2157-182">It shows setting up of [**InParameters**](swbemmethod-inparameters.md) object, and how to obtain results from an [**OutParameters**](swbemmethod-outparameters.md) object.</span></span>

<span data-ttu-id="e2157-183">Para obtener un script que muestra las mismas operaciones realizadas sincrónicamente, vea [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md).</span><span class="sxs-lookup"><span data-stu-id="e2157-183">For a script that shows the same operations performed synchronously, see [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md).</span></span> <span data-ttu-id="e2157-184">Para obtener un ejemplo de uso de acceso directo, consulte [**Create method in Class Win32 \_ Process**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process).</span><span class="sxs-lookup"><span data-stu-id="e2157-184">For an example using direct access, see [**Create Method in Class Win32\_Process**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process).</span></span> <span data-ttu-id="e2157-185">Para obtener un ejemplo de la misma operación mediante un objeto [**SWbemServices**](swbemservices.md) , vea [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md).</span><span class="sxs-lookup"><span data-stu-id="e2157-185">For an example of the same operation using an [**SWbemServices**](swbemservices.md) object, see [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md).</span></span>


```VB
On Error Resume Next

'Get a Win32_Process class description
Set oProcess = GetObject("winmgmts:Win32_Process")

' Create the SWbemMethod.InParameters object
' to hold the input parameter needed
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains a class object that defines
' the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object so SWbemObject.SpawnInstance_
' can be called to create it.
Set oInParams = oProcess.Methods_("Create"). _
    InParameters.SpawnInstance_

' Specify the name of the process to be run.
oInParams.CommandLine = "Notepad.exe"

' Create a sink to receive event resulting
' from the ExecMethodAsync call.
Set Sink = wscript.CreateObject( _
    "WbemScripting.SWbemSink", "Sink_")

' Call the Win32_Process.Create method asynchronously. Set up a 
' wait so the results of the method execution can be returned to 
' the sink subroutines.
bDone = false

' Call SWbemObject.ExecMethodAsync on the oProcess object.
oProcess.ExecMethodAsync_ Sink, "Create", oInParams, 0 
' 
while not bDone
    wscript.sleep 1000
wend

' Sink subroutines
sub Sink_OnObjectReady(oOutParams, oContext)
    wscript.echo "Sink_OnObjectReady subroutine " _
    & VBNewLine & "ReturnValue = " _
    & oOutParams.ReturnValue & VBNewLine & _
    "ProcessId = " & oOutParams.ProcessId
end sub

sub Sink_OnCompleted(HResult, LastErrorObj, oContext)
    wscript.echo "Sink_OnCompleted subroutine, hresult = " _
    & hex(HResult)
    bdone = true
end sub
```



## <a name="requirements"></a><span data-ttu-id="e2157-186">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2157-186">Requirements</span></span>



| <span data-ttu-id="e2157-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2157-187">Requirement</span></span> | <span data-ttu-id="e2157-188">Value</span><span class="sxs-lookup"><span data-stu-id="e2157-188">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2157-189">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2157-189">Minimum supported client</span></span><br/> | <span data-ttu-id="e2157-190">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e2157-190">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e2157-191">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2157-191">Minimum supported server</span></span><br/> | <span data-ttu-id="e2157-192">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e2157-192">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e2157-193">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e2157-193">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2157-194"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2157-194"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e2157-195">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e2157-195">Type library</span></span><br/>             | <dl> <span data-ttu-id="e2157-196"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e2157-196"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e2157-197">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e2157-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2157-198"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2157-198"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e2157-199">CLSID</span><span class="sxs-lookup"><span data-stu-id="e2157-199">CLSID</span></span><br/>                    | <span data-ttu-id="e2157-200">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="e2157-200">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="e2157-201">IID</span><span class="sxs-lookup"><span data-stu-id="e2157-201">IID</span></span><br/>                      | <span data-ttu-id="e2157-202">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="e2157-202">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="e2157-203">Vea también</span><span class="sxs-lookup"><span data-stu-id="e2157-203">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2157-204">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="e2157-204">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="e2157-205">**SWbemServices.ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="e2157-205">**SWbemServices.ExecMethodAsync**</span></span>](swbemservices-execmethodasync.md)
</dt> </dl>

 

