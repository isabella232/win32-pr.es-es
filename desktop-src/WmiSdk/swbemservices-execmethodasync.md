---
description: 'SWbemServices.Exemétodo cMethodAsync: ejecuta un método exportado por un proveedor de métodos.'
ms.assetid: 933a4c64-7538-474e-9f6f-f94da6066b46
ms.tgt_platform: multiple
title: SWbemServices.Exemétodo cMethodAsync (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecMethodAsync
- ISWbemServices.ExecMethodAsync
- ISWbemServices.ExecMethodAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: fcdcd70b567a737cb8686ac841dc1ce0b55d3996
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105593"
---
# <a name="swbemservicesexecmethodasync-method"></a><span data-ttu-id="d2bc7-103">SWbemServices.Exemétodo cMethodAsync</span><span class="sxs-lookup"><span data-stu-id="d2bc7-103">SWbemServices.ExecMethodAsync method</span></span>

<span data-ttu-id="d2bc7-104">El **método ExecMethodAsync** del objeto [**SWbemServices**](swbemservices.md) ejecuta un método exportado por un proveedor de métodos.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-104">The **ExecMethodAsync** method of the [**SWbemServices**](swbemservices.md) object executes a method that is exported by a method provider.</span></span> <span data-ttu-id="d2bc7-105">La llamada vuelve inmediatamente al cliente mientras los parámetros de entrada se reenvía al proveedor adecuado donde se ejecuta el método.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-105">The call immediately returns to the client while the inbound parameters are forwarded to the appropriate provider where the method executes.</span></span> <span data-ttu-id="d2bc7-106">La información y el estado se devuelven al autor de la llamada a través de eventos entregados al receptor que se especifica en *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-106">Information and status are returned to the caller through events delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="d2bc7-107">El proveedor, en lugar Instrumental de administración de Windows (WMI), implementa el método .</span><span class="sxs-lookup"><span data-stu-id="d2bc7-107">The provider, rather than Windows Management Instrumentation (WMI), implements the method.</span></span>

<span data-ttu-id="d2bc7-108">Se llama al método en modo asincrónico.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-108">The method is called in the asynchronous mode.</span></span> <span data-ttu-id="d2bc7-109">Para obtener más información, vea [Llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="d2bc7-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="d2bc7-110">Para obtener más información y una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="d2bc7-110">For more information and an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d2bc7-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d2bc7-111">Syntax</span></span>


```VB
SWbemServices.ExecMethodAsync( _
  ByVal objWbemSink, _
  ByVal strObjectPath, _
  ByVal strMethodName, _
  [ ByVal objWbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="d2bc7-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d2bc7-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2bc7-113">*objWbemSink*</span><span class="sxs-lookup"><span data-stu-id="d2bc7-113">*objWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="d2bc7-114">Necesario.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-114">Required.</span></span> <span data-ttu-id="d2bc7-115">Cree un [**objeto SWbemSink**](swbemsink.md) para recibir los objetos.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-115">Create an [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span> <span data-ttu-id="d2bc7-116">Receptor de objeto que recibe el resultado de la llamada al método.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-116">Object sink that receives the result of the method call.</span></span> <span data-ttu-id="d2bc7-117">Los parámetros de salida se envían al [**evento SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) del receptor de objetos proporcionado.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-117">The outbound parameters are sent to the [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) event of the supplied object sink.</span></span> <span data-ttu-id="d2bc7-118">Los resultados del mecanismo de llamada se envían al evento [**SWbemSink.OnCompleted**](swbemsink-oncompleted.md) del receptor de objetos proporcionado.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-118">The results of the call mechanism are sent to the [**SWbemSink.OnCompleted**](swbemsink-oncompleted.md) event of the supplied object sink.</span></span> <span data-ttu-id="d2bc7-119">Tenga en cuenta **que SWbemSink.OnCompleted** no recibe el código de retorno del método WMI.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-119">Be aware that **SWbemSink.OnCompleted** does not receive the return code of the WMI method.</span></span> <span data-ttu-id="d2bc7-120">Sin embargo, recibe el código de retorno del mecanismo de devolución de llamadas real y solo es útil para comprobar que la llamada se produjo o que se produjo un error por motivos mecánicos.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-120">However, it receives the return code of the actual call-return mechanism, and is only useful for verifying that the call occurred or that it failed for mechanical reasons.</span></span> <span data-ttu-id="d2bc7-121">El código de resultado que se devuelve del método WMI se devuelve en el objeto de parámetro de salida proporcionado a **SWbemSink.OnObjectReady**.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-121">The result code that is returned from the WMI method is returned in the outbound parameter object supplied to **SWbemSink.OnObjectReady**.</span></span> <span data-ttu-id="d2bc7-122">Si se devuelve algún código de error, no se usa el objeto [**IWbemObjectSink**](iwbemobjectsink.md) proporcionado.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-122">If any error code is returned, then the supplied [**IWbemObjectSink**](iwbemobjectsink.md) object is not used.</span></span> <span data-ttu-id="d2bc7-123">Si la llamada se realiza correctamente, se llama a la implementación **IWbemObjectSink** del usuario para indicar el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-123">If the call is successful, then the user's **IWbemObjectSink** implementation is called to indicate the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d2bc7-124">*strObjectPath*</span><span class="sxs-lookup"><span data-stu-id="d2bc7-124">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="d2bc7-125">Necesario.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-125">Required.</span></span> <span data-ttu-id="d2bc7-126">Cadena que contiene la ruta de acceso del objeto para el que se ejecuta el método.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-126">A string that contains the object path of the object for which the method is executed.</span></span> <span data-ttu-id="d2bc7-127">Para obtener más información, [vea Describir la ubicación de un objeto WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="d2bc7-127">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="d2bc7-128">*strMethodName*</span><span class="sxs-lookup"><span data-stu-id="d2bc7-128">*strMethodName*</span></span> 
</dt> <dd>

<span data-ttu-id="d2bc7-129">Necesario.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-129">Required.</span></span> <span data-ttu-id="d2bc7-130">Nombre del método que se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-130">The name of the method to execute.</span></span>

</dd> <dt>

<span data-ttu-id="d2bc7-131">*objWbemInParams* \[ Opcional\]</span><span class="sxs-lookup"><span data-stu-id="d2bc7-131">*objWbemInParams* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d2bc7-132">Objeto [**SWbemObject**](swbemobject.md) que contiene los parámetros de entrada para el método que se ejecuta.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-132">An [**SWbemObject**](swbemobject.md) object that contains the input parameters for the method that is executed.</span></span> <span data-ttu-id="d2bc7-133">De forma predeterminada, este parámetro no está definido.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-133">By default, this parameter is undefined.</span></span> <span data-ttu-id="d2bc7-134">Para obtener más información, vea [Construir objetos InParameters y Analizar objetos OutParameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="d2bc7-134">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="d2bc7-135">*iFlags* \[ Opcional\]</span><span class="sxs-lookup"><span data-stu-id="d2bc7-135">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d2bc7-136">Entero que determina el comportamiento de la llamada.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-136">Integer that determines the behavior of the call.</span></span> <span data-ttu-id="d2bc7-137">Este parámetro puede aceptar los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-137">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="d2bc7-138"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus\*\* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="d2bc7-138"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="d2bc7-139">Hace que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**OnProgress**](swbemsink-onprogress.md) para el receptor del objeto.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-139">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="d2bc7-140"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus\*\* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="d2bc7-140"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="d2bc7-141">Impide que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**OnProgress**](swbemsink-onprogress.md) para el receptor del objeto.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-141">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d2bc7-142">*objWbemNamedValueSet* \[ Opcional\]</span><span class="sxs-lookup"><span data-stu-id="d2bc7-142">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d2bc7-143">Normalmente, esto no está definido.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-143">Typically, this is undefined.</span></span> <span data-ttu-id="d2bc7-144">De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que está atendiendo la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-144">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="d2bc7-145">Un proveedor que admita o requiera dicha información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-145">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="d2bc7-146">*objWbemAsyncContext* \[ Opcional\]</span><span class="sxs-lookup"><span data-stu-id="d2bc7-146">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d2bc7-147">Objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que vuelve al receptor del objeto para identificar el origen de la llamada asincrónica original.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-147">A [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="d2bc7-148">Use este parámetro si realiza varias llamadas asincrónicas con el mismo receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-148">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="d2bc7-149">Para usar este parámetro, cree un objeto **SWbemNamedValueSet** y use el método [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) para agregar un valor que identifique la llamada asincrónica que está realizando.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-149">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="d2bc7-150">Este **objeto SWbemNamedValueSet** se devuelve al receptor del objeto y el origen de la llamada se puede extraer mediante el método [**SWbemNamedValueSet.Item.**](swbemnamedvalueset-item.md)</span><span class="sxs-lookup"><span data-stu-id="d2bc7-150">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="d2bc7-151">Para obtener más información, vea [Realizar una llamada asincrónica con VBScript.](making-an-asynchronous-call-with-vbscript.md)</span><span class="sxs-lookup"><span data-stu-id="d2bc7-151">For more information, see [Making an Asynchronous Call with VBScript](making-an-asynchronous-call-with-vbscript.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2bc7-152">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d2bc7-152">Return value</span></span>

<span data-ttu-id="d2bc7-153">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-153">This method does not return a value.</span></span> <span data-ttu-id="d2bc7-154">Si la llamada se realiza correctamente, se proporciona un objeto [**OutParameters,**](swbemmethod-outparameters.md) que también es [**un objeto SWbemObject**](swbemobject.md) al receptor especificado en *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-154">If the call is successful, an [**OutParameters**](swbemmethod-outparameters.md) object, which is also an [**SWbemObject**](swbemobject.md) is supplied to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="d2bc7-155">El objeto **OutParameters** devuelto contiene los parámetros de salida y el valor devuelto para el método que se ejecuta.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-155">The returned **OutParameters** object contains the output parameters and return value for the method being executed.</span></span> <span data-ttu-id="d2bc7-156">Para obtener más información, [vea Construir objetos InParameters y Analizar objetos OutParameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="d2bc7-156">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="d2bc7-157">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="d2bc7-157">Error codes</span></span>

<span data-ttu-id="d2bc7-158">Después de completar el método **ExecMethodAsync,** el [objeto Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener uno de los códigos de error enumerados en la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-158">After the completion of the **ExecMethodAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes listed in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="d2bc7-159">**wbemErrFailed:** 2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="d2bc7-159">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="d2bc7-160">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-160">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="d2bc7-161">**wbemErrInvalidClass** : 2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="d2bc7-161">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="d2bc7-162">La clase especificada no era válida.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-162">Specified class was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d2bc7-163">**wbemErrInvalidParameter:** 2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="d2bc7-163">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="d2bc7-164">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-164">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d2bc7-165">**wbemErrOutOfMemory-** 2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="d2bc7-165">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="d2bc7-166">No hay suficiente memoria para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-166">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d2bc7-167">**wbemErrInvalidMethod:** 2147749934 (0x8004102E)</span><span class="sxs-lookup"><span data-stu-id="d2bc7-167">**wbemErrInvalidMethod** - 2147749934 (0x8004102E)</span></span>
</dt> <dd>

<span data-ttu-id="d2bc7-168">El método solicitado no estaba disponible.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-168">Requested method was not available.</span></span>

</dd> <dt>

<span data-ttu-id="d2bc7-169">**wbemErrAccessDenied:** 2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="d2bc7-169">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="d2bc7-170">El usuario actual no estaba autorizado para ejecutar el método .</span><span class="sxs-lookup"><span data-stu-id="d2bc7-170">Current user was not authorized to execute the method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d2bc7-171">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d2bc7-171">Remarks</span></span>

<span data-ttu-id="d2bc7-172">Si el método ejecutado tiene parámetros de entrada, el objeto [**InParameters**](swbemmethod-inparameters.md) del parámetro *objWbemInParam* debe ser el mismo que la descripción de los temas Construcción de objetos InParameters y Análisis de [objetos OutParameters.](constructing-inparameters-objects-and-parsing-outparameters-objects.md)</span><span class="sxs-lookup"><span data-stu-id="d2bc7-172">If the method executed has input parameters, the [**InParameters**](swbemmethod-inparameters.md) object in the *objWbemInParam* parameter must be the same as the description in the [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md) topics.</span></span>

<span data-ttu-id="d2bc7-173">Use **SWbemServices.ExecMethodAsync** como alternativa al acceso directo [](gloss-p.md) para ejecutar un método de proveedor cuando no sea posible ejecutar un método directamente.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-173">Use **SWbemServices.ExecMethodAsync** as an alternative to direct access for executing a [*provider method*](gloss-p.md) when it is not possible to execute a method directly.</span></span> <span data-ttu-id="d2bc7-174">Por ejemplo, úselo con un lenguaje de scripting que no admita parámetros de salida, es decir, si el método tiene parámetros OUT.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-174">For example, use it with a scripting language that does not support output parameters, that is, if your method has OUT parameters.</span></span> <span data-ttu-id="d2bc7-175">De lo contrario, se recomienda usar el acceso directo para invocar un método.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-175">Otherwise, it is recommended that you use direct access to invoke a method.</span></span> <span data-ttu-id="d2bc7-176">Para obtener más información, vea [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="d2bc7-176">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

<span data-ttu-id="d2bc7-177">El **SWbemServices.ExecMethodAsync** requiere una ruta de acceso de objeto.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-177">The **SWbemServices.ExecMethodAsync** method requires an object path.</span></span> <span data-ttu-id="d2bc7-178">Si el script ya contiene un [**objeto SWbemObject,**](swbemobject.md) puede llamar a [**SWbemObject.ExecMethodAsync**](swbemobject-execmethodasync-.md).</span><span class="sxs-lookup"><span data-stu-id="d2bc7-178">If the script already contains an [**SWbemObject**](swbemobject.md) object, you can call [**SWbemObject.ExecMethodAsync**](swbemobject-execmethodasync-.md).</span></span>

<span data-ttu-id="d2bc7-179">Esta llamada se devuelve inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-179">This call returns immediately.</span></span> <span data-ttu-id="d2bc7-180">La información de estado se devuelve al autor de la llamada a través de las llamadas devueltas al receptor que se especifica en *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-180">The status information is returned to the caller through call-backs delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="d2bc7-181">Para continuar el procesamiento cuando se complete la llamada, implemente una subrutina para *objWbemSink*. [**Evento OnCompleted.**](swbemsink-oncompleted.md)</span><span class="sxs-lookup"><span data-stu-id="d2bc7-181">To continue processing when the call is completed, implement a subroutine for the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="d2bc7-182">Una devolución de llamada asincrónica permite que un usuario no autenticado proporcione datos al receptor.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-182">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="d2bc7-183">Esto supone riesgos de seguridad para los scripts y las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-183">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="d2bc7-184">Para obtener más información sobre cómo eliminar los riesgos, vea [Establecer la seguridad en una llamada asincrónica.](setting-security-on-an-asynchronous-call.md)</span><span class="sxs-lookup"><span data-stu-id="d2bc7-184">For more information about how to eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="d2bc7-185">Use el *parámetro objWbemAsyncContext* para comprobar el origen de una llamada.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-185">Use the *objWbemAsyncContext* parameter to verify the source of a call.</span></span>

## <a name="examples"></a><span data-ttu-id="d2bc7-186">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d2bc7-186">Examples</span></span>

<span data-ttu-id="d2bc7-187">En el ejemplo de código siguiente se muestra **el método ExecMethodAsync.**</span><span class="sxs-lookup"><span data-stu-id="d2bc7-187">The following code example shows the **ExecMethodAsync** method.</span></span> <span data-ttu-id="d2bc7-188">El script crea un [**objeto Proceso de Win32 \_**](/windows/desktop/CIMWin32Prov/win32-process) que representa un proceso que ejecuta el Bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="d2bc7-188">The script creates a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) object that represents a process that is running Notepad.</span></span> <span data-ttu-id="d2bc7-189">Muestra la configuración de un objeto [**InParameters**](swbemmethod-inparameters.md) y cómo obtener los resultados de [**un objeto OutParameters.**](swbemmethod-outparameters.md)</span><span class="sxs-lookup"><span data-stu-id="d2bc7-189">It shows the setting up of an [**InParameters**](swbemmethod-inparameters.md) object and how to obtain results from an [**OutParameters**](swbemmethod-outparameters.md) object.</span></span> <span data-ttu-id="d2bc7-190">Para obtener un script que muestre las mismas operaciones realizadas sincrónicamente, [**veaSWbemServices.ExecMethod**](swbemservices-execmethod.md).</span><span class="sxs-lookup"><span data-stu-id="d2bc7-190">For a script that shows the same operations performed synchronously, see [**SWbemServices.ExecMethod**](swbemservices-execmethod.md).</span></span> <span data-ttu-id="d2bc7-191">Para obtener un ejemplo del uso del acceso directo, vea [Create Method in Class Win32 \_ Process](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process).</span><span class="sxs-lookup"><span data-stu-id="d2bc7-191">For an example of using direct access, see [Create Method in Class Win32\_Process](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process).</span></span> <span data-ttu-id="d2bc7-192">Para obtener un ejemplo de la misma operación [**mediante SWbemObject**](swbemobject.md), [**veaSWbemObject.ExecMethodAsync**](swbemobject-execmethodasync-.md).</span><span class="sxs-lookup"><span data-stu-id="d2bc7-192">For an example of the same operation using [**SWbemObject**](swbemobject.md), see [**SWbemObject.ExecMethodAsync**](swbemobject-execmethodasync-.md).</span></span>


```VB
' Connect to WMI.
set Services = getobject("winmgmts:root\cimv2")

' Obtain the class definition object
' of a Win32_Process object.
Set oProcess = Services.Get("Win32_Process")

' Create the SWbemMethod.InParameters object
' to hold the input parameter required
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains a class object that defines
' the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object, so SWbemObject.SpawnInstance_ 
' can be called to create it.

Set oInParams = oProcess.Methods_("Create"). _
    InParameters.SpawnInstance_
oInParams.CommandLine = "Notepad.exe"

' Create sink to receive event resulting
' from the ExecMethodAsync call.
set Sink = wscript.CreateObject( _
    "WbemScripting.SWbemSink","Sink_")

' Call SWbemServices.ExecMethodAsync
' with the WMI path Win32_Process.

bDone = false
Services.ExecMethodAsync Sink, _
     "Win32_Process", "Create", oInParams

' Call the Win32_Process.Create method asynchronously.
' Set up a wait so the results of the method
' execution can be returned to 
' the sink subroutines.

while not bDone    
    wscript.sleep 1000  
wend

' Sink subroutines
sub Sink_OnObjectReady(oOutParams, oContext)
    wscript.echo "Sink_OnObjectReady subroutine " _ 
        &VBCR & "ReturnValue = " _
        & oOutParams.ReturnValue &VBCR & _
        "ProcessId = " & oOutParams.ProcessId
end sub

sub Sink_OnCompleted(HResult, LastErrorObj, oContext)
    wscript.echo "Sink_OnCompleted subroutine, hresult = " _
        & hex(HResult)
    bdone = true
end sub
```



## <a name="requirements"></a><span data-ttu-id="d2bc7-193">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2bc7-193">Requirements</span></span>



| <span data-ttu-id="d2bc7-194">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2bc7-194">Requirement</span></span> | <span data-ttu-id="d2bc7-195">Valor</span><span class="sxs-lookup"><span data-stu-id="d2bc7-195">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2bc7-196">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d2bc7-196">Minimum supported client</span></span><br/> | <span data-ttu-id="d2bc7-197">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d2bc7-197">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d2bc7-198">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d2bc7-198">Minimum supported server</span></span><br/> | <span data-ttu-id="d2bc7-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d2bc7-199">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d2bc7-200">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d2bc7-200">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2bc7-201"><dt>Wbemdisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="d2bc7-201"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d2bc7-202">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d2bc7-202">Type library</span></span><br/>             | <dl> <span data-ttu-id="d2bc7-203"><dt>Wbemdisp.tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d2bc7-203"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d2bc7-204">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d2bc7-204">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2bc7-205"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2bc7-205"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d2bc7-206">CLSID</span><span class="sxs-lookup"><span data-stu-id="d2bc7-206">CLSID</span></span><br/>                    | <span data-ttu-id="d2bc7-207">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="d2bc7-207">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="d2bc7-208">IID</span><span class="sxs-lookup"><span data-stu-id="d2bc7-208">IID</span></span><br/>                      | <span data-ttu-id="d2bc7-209">IID \_ ISWbemServices</span><span class="sxs-lookup"><span data-stu-id="d2bc7-209">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="d2bc7-210">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d2bc7-210">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2bc7-211">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="d2bc7-211">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="d2bc7-212">**SWbemObject.ExecMethod\_**</span><span class="sxs-lookup"><span data-stu-id="d2bc7-212">**SWbemObject.ExecMethod\_**</span></span>](swbemobject-execmethod-.md)
</dt> <dt>

[<span data-ttu-id="d2bc7-213">**SWbemObject.ExecMethodAsync\_**</span><span class="sxs-lookup"><span data-stu-id="d2bc7-213">**SWbemObject.ExecMethodAsync\_**</span></span>](swbemobject-execmethodasync-.md)
</dt> <dt>

[<span data-ttu-id="d2bc7-214">**SWbemServices.ExecMethod**</span><span class="sxs-lookup"><span data-stu-id="d2bc7-214">**SWbemServices.ExecMethod**</span></span>](swbemservices-execmethod.md)
</dt> <dt>

[<span data-ttu-id="d2bc7-215">Llamar a un método provider</span><span class="sxs-lookup"><span data-stu-id="d2bc7-215">Calling a Provider Method</span></span>](calling-a-provider-method.md)
</dt> <dt>

[<span data-ttu-id="d2bc7-216">Manipulación de la información de clase e instancia</span><span class="sxs-lookup"><span data-stu-id="d2bc7-216">Manipulating Class and Instance Information</span></span>](manipulating-class-and-instance-information.md)
</dt> </dl>

 

