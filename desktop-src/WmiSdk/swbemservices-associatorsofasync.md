---
description: Devuelve una colección de objetos (clases o instancias) denominada puntos de conexión que están asociados a un objeto especificado.
ms.assetid: 3969d90f-d39c-40f1-9328-fc1afbaa53b1
ms.tgt_platform: multiple
title: Método SWbemServices. AssociatorsOfAsync (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.AssociatorsOfAsync
- ISWbemServices.AssociatorsOfAsync
- ISWbemServices.AssociatorsOfAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d83f2eb33b7cd2d6ce6345d9b40a2367539dfec7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715722"
---
# <a name="swbemservicesassociatorsofasync-method"></a><span data-ttu-id="97804-103">SWbemServices. AssociatorsOfAsync, método</span><span class="sxs-lookup"><span data-stu-id="97804-103">SWbemServices.AssociatorsOfAsync method</span></span>

<span data-ttu-id="97804-104">El método **AssociatorsOfAsync** del objeto [**SWbemServices**](swbemservices.md) devuelve una colección de objetos (clases o instancias) denominados extremos que están asociados a un objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="97804-104">The **AssociatorsOfAsync** method of the [**SWbemServices**](swbemservices.md) object returns a collection of objects (classes or instances) called endpoints that are associated with a specified object.</span></span> <span data-ttu-id="97804-105">La llamada a **AssociatorsOfAsync** se devuelve inmediatamente, y los resultados y el estado se devuelven al autor de la llamada a través de los eventos entregados al receptor especificado en *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="97804-105">The call to **AssociatorsOfAsync** returns immediately, and the results and status are returned to the caller through events delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="97804-106">Para controlar cada objeto devuelto, cree un *objWbemSink*. Controlador de eventos [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="97804-106">To handle each returned object, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event handler.</span></span>

<span data-ttu-id="97804-107">Después de que lleguen todos los objetos, el procesamiento se realiza en *objWbemSink*. Evento [**Alcompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="97804-107">After all the objects arrive, processing is done in the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span> <span data-ttu-id="97804-108">Este método realiza la misma función que realizan los asociados de la consulta WQL.</span><span class="sxs-lookup"><span data-stu-id="97804-108">This method performs the same function that the ASSOCIATORS OF WQL query performs.</span></span> <span data-ttu-id="97804-109">Para obtener más información acerca de la creación de un receptor, consulte [recibir un evento WMI](receiving-a-wmi-event.md).</span><span class="sxs-lookup"><span data-stu-id="97804-109">For more information about creating a sink, see [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

<span data-ttu-id="97804-110">Se llama al método en el modo asincrónico.</span><span class="sxs-lookup"><span data-stu-id="97804-110">The method is called in the asynchronous mode.</span></span> <span data-ttu-id="97804-111">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="97804-111">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="97804-112">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="97804-112">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="97804-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="97804-113">Syntax</span></span>


```VB
SWbemServices.AssociatorsOfAsync( _
  ByVal objWbemSink, _
  ByVal strObjectPath, _
  [ ByVal strAssocClass ], _
  [ ByVal strResultClass ], _
  [ ByVal strResultRole ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredAssocQualifier ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="97804-114">Parámetros</span><span class="sxs-lookup"><span data-stu-id="97804-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97804-115">*objWbemSink*</span><span class="sxs-lookup"><span data-stu-id="97804-115">*objWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="97804-116">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="97804-116">Required.</span></span> <span data-ttu-id="97804-117">Receptor de objeto que recibe los objetos de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="97804-117">Object sink that receives the objects asynchronously.</span></span> <span data-ttu-id="97804-118">Cree un objeto [**SWbemSink**](swbemsink.md) para recibir los objetos.</span><span class="sxs-lookup"><span data-stu-id="97804-118">Create an [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="97804-119">*strObjectPath*</span><span class="sxs-lookup"><span data-stu-id="97804-119">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="97804-120">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="97804-120">Required.</span></span> <span data-ttu-id="97804-121">Cadena que contiene la ruta de acceso del objeto de la clase o instancia de origen.</span><span class="sxs-lookup"><span data-stu-id="97804-121">String that contains the object path of the source class or instance.</span></span> <span data-ttu-id="97804-122">Para obtener más información, vea [Descripción de la ubicación de un objeto WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="97804-122">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="97804-123">*strAssocClass* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="97804-123">*strAssocClass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="97804-124">Cadena que contiene una clase de asociación.</span><span class="sxs-lookup"><span data-stu-id="97804-124">String that contains an association class.</span></span> <span data-ttu-id="97804-125">Cuando se especifica, este parámetro indica que los extremos devueltos deben estar asociados al origen a través de la clase de asociación especificada o una clase derivada de esta clase de asociación.</span><span class="sxs-lookup"><span data-stu-id="97804-125">When specified, this parameter indicates that the returned endpoints must be associated with the source through the specified association class or a class derived from this association class.</span></span>

</dd> <dt>

<span data-ttu-id="97804-126">*strResultClass* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="97804-126">*strResultClass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="97804-127">Cadena que contiene un nombre de clase.</span><span class="sxs-lookup"><span data-stu-id="97804-127">String that contains a class name.</span></span> <span data-ttu-id="97804-128">Si se especifica, este parámetro opcional indica que los extremos devueltos deben pertenecer a la clase especificada en este parámetro o derivarse de ella.</span><span class="sxs-lookup"><span data-stu-id="97804-128">If specified, this optional parameter indicates that the returned endpoints must belong to or be derived from the class specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="97804-129">*strResultRole* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="97804-129">*strResultRole* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="97804-130">Cadena que contiene un nombre de propiedad.</span><span class="sxs-lookup"><span data-stu-id="97804-130">String that contains a property name.</span></span> <span data-ttu-id="97804-131">Si se especifica, este parámetro indica que los extremos devueltos deben desempeñar un rol determinado en su asociación con el objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="97804-131">If specified, this parameter indicates that the returned endpoints must play a particular role in their association with the source object.</span></span> <span data-ttu-id="97804-132">El rol se define mediante el nombre de una propiedad especificada (que debe ser una propiedad de referencia) de una asociación.</span><span class="sxs-lookup"><span data-stu-id="97804-132">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="97804-133">*strRole* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="97804-133">*strRole* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="97804-134">Cadena que contiene un nombre de propiedad.</span><span class="sxs-lookup"><span data-stu-id="97804-134">String that contains a property name.</span></span> <span data-ttu-id="97804-135">Si se especifica, este parámetro indica que los extremos devueltos deben participar en una asociación con el objeto de origen en el que el objeto de origen desempeña un rol determinado.</span><span class="sxs-lookup"><span data-stu-id="97804-135">If specified, this parameter indicates that the returned endpoints must participate in an association with the source object in which the source object plays a particular role.</span></span> <span data-ttu-id="97804-136">El rol se define mediante el nombre de una propiedad especificada (que debe ser una propiedad de referencia) de una asociación.</span><span class="sxs-lookup"><span data-stu-id="97804-136">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="97804-137">*bClassesOnly* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="97804-137">*bClassesOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="97804-138">Valor booleano que indica si se debe devolver una lista de nombres de clase en lugar de instancias reales de las clases.</span><span class="sxs-lookup"><span data-stu-id="97804-138">Boolean value that indicates whether a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="97804-139">Estas son las clases a las que pertenecen las instancias de extremo.</span><span class="sxs-lookup"><span data-stu-id="97804-139">These are the classes to which the endpoint instances belong.</span></span> <span data-ttu-id="97804-140">El valor predeterminado de este parámetro es **false**.</span><span class="sxs-lookup"><span data-stu-id="97804-140">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="97804-141">*bSchemaOnly* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="97804-141">*bSchemaOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="97804-142">Valor booleano que indica si la consulta se aplica al esquema en lugar de a los datos.</span><span class="sxs-lookup"><span data-stu-id="97804-142">Boolean value that indicates whether the query applies to the schema rather than the data.</span></span> <span data-ttu-id="97804-143">El valor predeterminado de este parámetro es **false**.</span><span class="sxs-lookup"><span data-stu-id="97804-143">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="97804-144">Solo se puede establecer en **true** si el parámetro *strObjectPath* especifica la ruta de acceso del objeto de una clase.</span><span class="sxs-lookup"><span data-stu-id="97804-144">It can only be set to **TRUE** if the *strObjectPath* parameter specifies the object path of a class.</span></span> <span data-ttu-id="97804-145">Cuando se establece en **true**, el conjunto de extremos devueltos representa las clases que están asociadas adecuadamente a la clase de origen en el esquema.</span><span class="sxs-lookup"><span data-stu-id="97804-145">When set to **TRUE**, the set of returned endpoints represent classes that are suitably associated with the source class in schema.</span></span>

</dd> <dt>

<span data-ttu-id="97804-146">*strRequiredAssocQualifier* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="97804-146">*strRequiredAssocQualifier* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="97804-147">Cadena que contiene un nombre de calificador.</span><span class="sxs-lookup"><span data-stu-id="97804-147">String that contains a qualifier name.</span></span> <span data-ttu-id="97804-148">Si se especifica, este parámetro indica que los extremos devueltos deben asociarse con el objeto de origen a través de una clase de asociación que incluye el calificador especificado.</span><span class="sxs-lookup"><span data-stu-id="97804-148">If specified, this parameter indicates that the returned endpoints must be associated with the source object through an association class that includes the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="97804-149">*strRequiredQualifier* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="97804-149">*strRequiredQualifier* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="97804-150">Cadena que contiene un nombre de calificador.</span><span class="sxs-lookup"><span data-stu-id="97804-150">String that contains a qualifier name.</span></span> <span data-ttu-id="97804-151">Si se especifica, este parámetro indica que los extremos devueltos deben incluir el calificador especificado.</span><span class="sxs-lookup"><span data-stu-id="97804-151">If specified, this parameter indicates that the returned endpoints must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="97804-152">*iFlags* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="97804-152">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="97804-153">Entero que especifica las marcas adicionales para la operación.</span><span class="sxs-lookup"><span data-stu-id="97804-153">Integer that specifies the additional flags to the operation.</span></span> <span data-ttu-id="97804-154">El valor predeterminado para este parámetro es **wbemFlagDontSendStatus**.</span><span class="sxs-lookup"><span data-stu-id="97804-154">The default for this parameter is **wbemFlagDontSendStatus**.</span></span> <span data-ttu-id="97804-155">Este parámetro puede aceptar los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="97804-155">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="97804-156"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="97804-156"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="97804-157">Hace que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**OnProgress**](swbemsink-onprogress.md) para el receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="97804-157">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="97804-158"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="97804-158"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="97804-159">Impide que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**OnProgress**](swbemsink-onprogress.md) para el receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="97804-159">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="97804-160"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="97804-160"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="97804-161">Hace que WMI devuelva datos de modificación de clase junto con la definición de clase base.</span><span class="sxs-lookup"><span data-stu-id="97804-161">Causes WMI to return class amendment data along with the base class definition.</span></span> <span data-ttu-id="97804-162">Para obtener más información acerca de los calificadores modificados, consulte [localizar información de clase WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="97804-162">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="97804-163">*objWbemNamedValueSet* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="97804-163">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="97804-164">Normalmente, esto no está definido.</span><span class="sxs-lookup"><span data-stu-id="97804-164">Typically, this is undefined.</span></span> <span data-ttu-id="97804-165">De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que atiende la solicitud.</span><span class="sxs-lookup"><span data-stu-id="97804-165">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="97804-166">Un proveedor que admite o requiere tal información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.</span><span class="sxs-lookup"><span data-stu-id="97804-166">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="97804-167">*objWbemAsyncContext* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="97804-167">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="97804-168">Un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que devuelve al receptor del objeto para identificar el origen de la llamada asincrónica original.</span><span class="sxs-lookup"><span data-stu-id="97804-168">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="97804-169">Utilice este parámetro si va a realizar varias llamadas asincrónicas mediante el mismo receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="97804-169">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="97804-170">Para usar este parámetro, cree un objeto **SWbemNamedValueSet** y use el método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) para agregar un valor que identifique la llamada asincrónica que está realizando.</span><span class="sxs-lookup"><span data-stu-id="97804-170">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="97804-171">Este objeto **SWbemNamedValueSet** se devuelve al receptor del objeto y el origen de la llamada se puede extraer mediante el método [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="97804-171">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="97804-172">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="97804-172">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97804-173">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="97804-173">Return value</span></span>

<span data-ttu-id="97804-174">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="97804-174">This method does not return a value.</span></span> <span data-ttu-id="97804-175">Si se realiza correctamente, el receptor recibe un evento [**OnObjectReady**](swbemsink-onobjectready.md) por cada instancia.</span><span class="sxs-lookup"><span data-stu-id="97804-175">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="97804-176">Después de la última instancia, el receptor del objeto recibe un evento [**alcompleto**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="97804-176">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="97804-177">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="97804-177">Error codes</span></span>

<span data-ttu-id="97804-178">Después de completar el método **AssociatorsOfAsync** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="97804-178">After the completion of the **AssociatorsOfAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="97804-179">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="97804-179">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="97804-180">El usuario actual no tiene permiso para ver una o varias de las clases devueltas por la llamada.</span><span class="sxs-lookup"><span data-stu-id="97804-180">Current user does not have the permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="97804-181">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="97804-181">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="97804-182">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="97804-182">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="97804-183">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="97804-183">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="97804-184">Se especificó un parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="97804-184">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="97804-185">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="97804-185">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="97804-186">Memoria insuficiente para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="97804-186">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="97804-187">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="97804-187">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="97804-188">No se encontró el elemento solicitado.</span><span class="sxs-lookup"><span data-stu-id="97804-188">Requested item was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="97804-189">Observaciones</span><span class="sxs-lookup"><span data-stu-id="97804-189">Remarks</span></span>

<span data-ttu-id="97804-190">Esta llamada se devuelve inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="97804-190">This call returns immediately.</span></span> <span data-ttu-id="97804-191">Los objetos y el estado solicitados se devuelven al autor de la llamada mediante devoluciones de llamada entregadas al receptor que se especifica en *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="97804-191">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="97804-192">Para procesar cada objeto cuando vuelva, cree un *objWbemSink*. Subrutina de evento [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="97804-192">To process each object when it returns, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="97804-193">Después de que se devuelvan todos los objetos, puede realizar el procesamiento final en la implementación de *objWbemSink*. Evento [**Alcompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="97804-193">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="97804-194">Una devolución de llamada asincrónica permite que un usuario no autenticado proporcione datos al receptor.</span><span class="sxs-lookup"><span data-stu-id="97804-194">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="97804-195">Esto supone riesgos de seguridad para los scripts y las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="97804-195">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="97804-196">Para eliminar los riesgos, consulte [configuración de la seguridad en una llamada asincrónica](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="97804-196">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="97804-197">Use el parámetro *objWbemAsyncContext* en scripts para comprobar el origen de una llamada.</span><span class="sxs-lookup"><span data-stu-id="97804-197">Use the *objWbemAsyncContext* parameter in scripts to verify the source of a call.</span></span>

## <a name="requirements"></a><span data-ttu-id="97804-198">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97804-198">Requirements</span></span>



| <span data-ttu-id="97804-199">Requisito</span><span class="sxs-lookup"><span data-stu-id="97804-199">Requirement</span></span> | <span data-ttu-id="97804-200">Value</span><span class="sxs-lookup"><span data-stu-id="97804-200">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="97804-201">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97804-201">Minimum supported client</span></span><br/> | <span data-ttu-id="97804-202">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="97804-202">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="97804-203">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97804-203">Minimum supported server</span></span><br/> | <span data-ttu-id="97804-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="97804-204">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="97804-205">Encabezado</span><span class="sxs-lookup"><span data-stu-id="97804-205">Header</span></span><br/>                   | <dl> <span data-ttu-id="97804-206"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="97804-206"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="97804-207">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="97804-207">Type library</span></span><br/>             | <dl> <span data-ttu-id="97804-208"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="97804-208"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="97804-209">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="97804-209">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97804-210"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97804-210"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="97804-211">CLSID</span><span class="sxs-lookup"><span data-stu-id="97804-211">CLSID</span></span><br/>                    | <span data-ttu-id="97804-212">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="97804-212">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="97804-213">IID</span><span class="sxs-lookup"><span data-stu-id="97804-213">IID</span></span><br/>                      | <span data-ttu-id="97804-214">\_ISWBEMSERVICES IID</span><span class="sxs-lookup"><span data-stu-id="97804-214">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="97804-215">Vea también</span><span class="sxs-lookup"><span data-stu-id="97804-215">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97804-216">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="97804-216">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="97804-217">**SWbemObject. ASSOCIATORS\_**</span><span class="sxs-lookup"><span data-stu-id="97804-217">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
</dt> <dt>

[<span data-ttu-id="97804-218">**SWbemObject.AssociatorsAsync\_**</span><span class="sxs-lookup"><span data-stu-id="97804-218">**SWbemObject.AssociatorsAsync\_**</span></span>](swbemobject-associatorsasync-.md)
</dt> <dt>

[<span data-ttu-id="97804-219">**SWbemObject. References\_**</span><span class="sxs-lookup"><span data-stu-id="97804-219">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
</dt> <dt>

[<span data-ttu-id="97804-220">**SWbemObject.ReferencesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="97804-220">**SWbemObject.ReferencesAsync\_**</span></span>](swbemobject-referencesasync-.md)
</dt> <dt>

[<span data-ttu-id="97804-221">**SWbemServices. References**</span><span class="sxs-lookup"><span data-stu-id="97804-221">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
</dt> <dt>

[<span data-ttu-id="97804-222">**SWbemServices. ReferencesToAsync**</span><span class="sxs-lookup"><span data-stu-id="97804-222">**SWbemServices.ReferencesToAsync**</span></span>](swbemservices-referencestoasync.md)
</dt> </dl>

 

