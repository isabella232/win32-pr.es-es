---
description: 'Método SWbemServices.AssociatorsOfAsync: devuelve una colección de objetos (clases o instancias) denominados puntos de conexión asociados a un objeto especificado.'
ms.assetid: 3969d90f-d39c-40f1-9328-fc1afbaa53b1
ms.tgt_platform: multiple
title: Método SWbemServices.AssociatorsOfAsync (Wbemdisp.h)
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
ms.openlocfilehash: 4b16eed97c891b4b4f5bd283496868d99f9e0fbc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103673"
---
# <a name="swbemservicesassociatorsofasync-method"></a><span data-ttu-id="08e1d-103">Método SWbemServices.AssociatorsOfAsync</span><span class="sxs-lookup"><span data-stu-id="08e1d-103">SWbemServices.AssociatorsOfAsync method</span></span>

<span data-ttu-id="08e1d-104">El **método AssociatorsOfAsync** del objeto [**SWbemServices**](swbemservices.md) devuelve una colección de objetos (clases o instancias) denominados puntos de conexión asociados a un objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="08e1d-104">The **AssociatorsOfAsync** method of the [**SWbemServices**](swbemservices.md) object returns a collection of objects (classes or instances) called endpoints that are associated with a specified object.</span></span> <span data-ttu-id="08e1d-105">La llamada a **AssociatorsOfAsync** se devuelve inmediatamente y los resultados y el estado se devuelven al autor de la llamada a través de eventos entregados al receptor especificado en *objWbemSink.*</span><span class="sxs-lookup"><span data-stu-id="08e1d-105">The call to **AssociatorsOfAsync** returns immediately, and the results and status are returned to the caller through events delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="08e1d-106">Para controlar cada objeto devuelto, cree *un objeto objWbemSink*. [**Controlador de eventos OnObjectReady.**](swbemsink-onobjectready.md)</span><span class="sxs-lookup"><span data-stu-id="08e1d-106">To handle each returned object, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event handler.</span></span>

<span data-ttu-id="08e1d-107">Una vez que llegan todos los objetos, el procesamiento se realiza en *objWbemSink*. [**Evento OnCompleted.**](swbemsink-oncompleted.md)</span><span class="sxs-lookup"><span data-stu-id="08e1d-107">After all the objects arrive, processing is done in the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span> <span data-ttu-id="08e1d-108">Este método realiza la misma función que la consulta ASSOCIATORS OF WQL.</span><span class="sxs-lookup"><span data-stu-id="08e1d-108">This method performs the same function that the ASSOCIATORS OF WQL query performs.</span></span> <span data-ttu-id="08e1d-109">Para obtener más información sobre cómo crear un receptor, vea [Recibir un evento WMI](receiving-a-wmi-event.md).</span><span class="sxs-lookup"><span data-stu-id="08e1d-109">For more information about creating a sink, see [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

<span data-ttu-id="08e1d-110">Se llama al método en modo asincrónico.</span><span class="sxs-lookup"><span data-stu-id="08e1d-110">The method is called in the asynchronous mode.</span></span> <span data-ttu-id="08e1d-111">Para obtener más información, vea [Llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="08e1d-111">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="08e1d-112">Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="08e1d-112">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="08e1d-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="08e1d-113">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="08e1d-114">Parámetros</span><span class="sxs-lookup"><span data-stu-id="08e1d-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08e1d-115">*objWbemSink*</span><span class="sxs-lookup"><span data-stu-id="08e1d-115">*objWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="08e1d-116">Necesario.</span><span class="sxs-lookup"><span data-stu-id="08e1d-116">Required.</span></span> <span data-ttu-id="08e1d-117">Receptor de objetos que recibe los objetos de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="08e1d-117">Object sink that receives the objects asynchronously.</span></span> <span data-ttu-id="08e1d-118">Cree un [**objeto SWbemSink**](swbemsink.md) para recibir los objetos.</span><span class="sxs-lookup"><span data-stu-id="08e1d-118">Create an [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="08e1d-119">*strObjectPath*</span><span class="sxs-lookup"><span data-stu-id="08e1d-119">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="08e1d-120">Necesario.</span><span class="sxs-lookup"><span data-stu-id="08e1d-120">Required.</span></span> <span data-ttu-id="08e1d-121">Cadena que contiene la ruta de acceso del objeto de la clase o instancia de origen.</span><span class="sxs-lookup"><span data-stu-id="08e1d-121">String that contains the object path of the source class or instance.</span></span> <span data-ttu-id="08e1d-122">Para obtener más información, [vea Describir la ubicación de un objeto WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="08e1d-122">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="08e1d-123">*strAssocClass* \[ Opcional\]</span><span class="sxs-lookup"><span data-stu-id="08e1d-123">*strAssocClass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="08e1d-124">Cadena que contiene una clase de asociación.</span><span class="sxs-lookup"><span data-stu-id="08e1d-124">String that contains an association class.</span></span> <span data-ttu-id="08e1d-125">Cuando se especifica, este parámetro indica que los puntos de conexión devueltos deben asociarse con el origen a través de la clase de asociación especificada o una clase derivada de esta clase de asociación.</span><span class="sxs-lookup"><span data-stu-id="08e1d-125">When specified, this parameter indicates that the returned endpoints must be associated with the source through the specified association class or a class derived from this association class.</span></span>

</dd> <dt>

<span data-ttu-id="08e1d-126">*strResultClass* \[ Opcional\]</span><span class="sxs-lookup"><span data-stu-id="08e1d-126">*strResultClass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="08e1d-127">Cadena que contiene un nombre de clase.</span><span class="sxs-lookup"><span data-stu-id="08e1d-127">String that contains a class name.</span></span> <span data-ttu-id="08e1d-128">Si se especifica, este parámetro opcional indica que los puntos de conexión devueltos deben pertenecer a o derivarse de la clase especificada en este parámetro.</span><span class="sxs-lookup"><span data-stu-id="08e1d-128">If specified, this optional parameter indicates that the returned endpoints must belong to or be derived from the class specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="08e1d-129">*strResultRole* \[ Opcional\]</span><span class="sxs-lookup"><span data-stu-id="08e1d-129">*strResultRole* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="08e1d-130">Cadena que contiene un nombre de propiedad.</span><span class="sxs-lookup"><span data-stu-id="08e1d-130">String that contains a property name.</span></span> <span data-ttu-id="08e1d-131">Si se especifica, este parámetro indica que los puntos de conexión devueltos deben desempeñar un rol determinado en su asociación con el objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="08e1d-131">If specified, this parameter indicates that the returned endpoints must play a particular role in their association with the source object.</span></span> <span data-ttu-id="08e1d-132">El rol se define mediante el nombre de una propiedad especificada (que debe ser una propiedad de referencia) de una asociación.</span><span class="sxs-lookup"><span data-stu-id="08e1d-132">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="08e1d-133">*strRole* \[ Opcional\]</span><span class="sxs-lookup"><span data-stu-id="08e1d-133">*strRole* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="08e1d-134">Cadena que contiene un nombre de propiedad.</span><span class="sxs-lookup"><span data-stu-id="08e1d-134">String that contains a property name.</span></span> <span data-ttu-id="08e1d-135">Si se especifica, este parámetro indica que los puntos de conexión devueltos deben participar en una asociación con el objeto de origen en el que el objeto de origen desempeña un rol determinado.</span><span class="sxs-lookup"><span data-stu-id="08e1d-135">If specified, this parameter indicates that the returned endpoints must participate in an association with the source object in which the source object plays a particular role.</span></span> <span data-ttu-id="08e1d-136">El rol se define mediante el nombre de una propiedad especificada (que debe ser una propiedad de referencia) de una asociación.</span><span class="sxs-lookup"><span data-stu-id="08e1d-136">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="08e1d-137">*bClassesOnly* \[ Opcional\]</span><span class="sxs-lookup"><span data-stu-id="08e1d-137">*bClassesOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="08e1d-138">Valor booleano que indica si se debe devolver una lista de nombres de clase en lugar de instancias reales de las clases.</span><span class="sxs-lookup"><span data-stu-id="08e1d-138">Boolean value that indicates whether a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="08e1d-139">Estas son las clases a las que pertenecen las instancias de punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="08e1d-139">These are the classes to which the endpoint instances belong.</span></span> <span data-ttu-id="08e1d-140">El valor predeterminado de este parámetro es **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="08e1d-140">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="08e1d-141">*bSchemaOnly* \[ Opcional\]</span><span class="sxs-lookup"><span data-stu-id="08e1d-141">*bSchemaOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="08e1d-142">Valor booleano que indica si la consulta se aplica al esquema en lugar de a los datos.</span><span class="sxs-lookup"><span data-stu-id="08e1d-142">Boolean value that indicates whether the query applies to the schema rather than the data.</span></span> <span data-ttu-id="08e1d-143">El valor predeterminado de este parámetro es **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="08e1d-143">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="08e1d-144">Solo se puede establecer en **TRUE si** el *parámetro strObjectPath* especifica la ruta de acceso del objeto de una clase.</span><span class="sxs-lookup"><span data-stu-id="08e1d-144">It can only be set to **TRUE** if the *strObjectPath* parameter specifies the object path of a class.</span></span> <span data-ttu-id="08e1d-145">Cuando se establece en **TRUE**, el conjunto de puntos de conexión devueltos representa clases que están asociadas adecuadamente a la clase de origen en el esquema.</span><span class="sxs-lookup"><span data-stu-id="08e1d-145">When set to **TRUE**, the set of returned endpoints represent classes that are suitably associated with the source class in schema.</span></span>

</dd> <dt>

<span data-ttu-id="08e1d-146">*strRequiredAssocQualifier* \[ Opcional\]</span><span class="sxs-lookup"><span data-stu-id="08e1d-146">*strRequiredAssocQualifier* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="08e1d-147">Cadena que contiene un nombre de calificador.</span><span class="sxs-lookup"><span data-stu-id="08e1d-147">String that contains a qualifier name.</span></span> <span data-ttu-id="08e1d-148">Si se especifica, este parámetro indica que los puntos de conexión devueltos deben asociarse al objeto de origen a través de una clase de asociación que incluya el calificador especificado.</span><span class="sxs-lookup"><span data-stu-id="08e1d-148">If specified, this parameter indicates that the returned endpoints must be associated with the source object through an association class that includes the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="08e1d-149">*strRequiredQualifier* \[ Opcional\]</span><span class="sxs-lookup"><span data-stu-id="08e1d-149">*strRequiredQualifier* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="08e1d-150">Cadena que contiene un nombre de calificador.</span><span class="sxs-lookup"><span data-stu-id="08e1d-150">String that contains a qualifier name.</span></span> <span data-ttu-id="08e1d-151">Si se especifica, este parámetro indica que los puntos de conexión devueltos deben incluir el calificador especificado.</span><span class="sxs-lookup"><span data-stu-id="08e1d-151">If specified, this parameter indicates that the returned endpoints must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="08e1d-152">*iFlags* \[ Opcional\]</span><span class="sxs-lookup"><span data-stu-id="08e1d-152">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="08e1d-153">Entero que especifica las marcas adicionales para la operación.</span><span class="sxs-lookup"><span data-stu-id="08e1d-153">Integer that specifies the additional flags to the operation.</span></span> <span data-ttu-id="08e1d-154">El valor predeterminado de este parámetro **es wbemFlagDontSendStatus.**</span><span class="sxs-lookup"><span data-stu-id="08e1d-154">The default for this parameter is **wbemFlagDontSendStatus**.</span></span> <span data-ttu-id="08e1d-155">Este parámetro puede aceptar los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="08e1d-155">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="08e1d-156"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus\*\* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="08e1d-156"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="08e1d-157">Hace que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**OnProgress**](swbemsink-onprogress.md) para el receptor del objeto.</span><span class="sxs-lookup"><span data-stu-id="08e1d-157">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="08e1d-158"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus\*\* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="08e1d-158"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="08e1d-159">Impide que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**OnProgress**](swbemsink-onprogress.md) para el receptor del objeto.</span><span class="sxs-lookup"><span data-stu-id="08e1d-159">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="08e1d-160"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers\*\* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="08e1d-160"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="08e1d-161">Hace que WMI devuelva datos de modificación de clase junto con la definición de clase base.</span><span class="sxs-lookup"><span data-stu-id="08e1d-161">Causes WMI to return class amendment data along with the base class definition.</span></span> <span data-ttu-id="08e1d-162">Para obtener más información sobre los calificadores modificados, vea [Localización de información de clase WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="08e1d-162">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="08e1d-163">*objWbemNamedValueSet* \[ Opcional\]</span><span class="sxs-lookup"><span data-stu-id="08e1d-163">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="08e1d-164">Normalmente, esto no está definido.</span><span class="sxs-lookup"><span data-stu-id="08e1d-164">Typically, this is undefined.</span></span> <span data-ttu-id="08e1d-165">De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que está atendiendo la solicitud.</span><span class="sxs-lookup"><span data-stu-id="08e1d-165">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="08e1d-166">Un proveedor que admita o requiera dicha información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.</span><span class="sxs-lookup"><span data-stu-id="08e1d-166">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="08e1d-167">*objWbemAsyncContext* \[ Opcional\]</span><span class="sxs-lookup"><span data-stu-id="08e1d-167">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="08e1d-168">Objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que vuelve al receptor del objeto para identificar el origen de la llamada asincrónica original.</span><span class="sxs-lookup"><span data-stu-id="08e1d-168">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="08e1d-169">Use este parámetro si realiza varias llamadas asincrónicas con el mismo receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="08e1d-169">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="08e1d-170">Para usar este parámetro, cree un objeto **SWbemNamedValueSet** y use el método [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) para agregar un valor que identifique la llamada asincrónica que está realizando.</span><span class="sxs-lookup"><span data-stu-id="08e1d-170">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="08e1d-171">Este **objeto SWbemNamedValueSet** se devuelve al receptor del objeto y el origen de la llamada se puede extraer mediante el método [**SWbemNamedValueSet.Item.**](swbemnamedvalueset-item.md)</span><span class="sxs-lookup"><span data-stu-id="08e1d-171">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="08e1d-172">Para obtener más información, vea [Llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="08e1d-172">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08e1d-173">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="08e1d-173">Return value</span></span>

<span data-ttu-id="08e1d-174">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="08e1d-174">This method does not return a value.</span></span> <span data-ttu-id="08e1d-175">Si se realiza correctamente, el receptor recibe un [**evento OnObjectReady**](swbemsink-onobjectready.md) por instancia.</span><span class="sxs-lookup"><span data-stu-id="08e1d-175">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="08e1d-176">Después de la última instancia, el receptor del objeto recibe [**un evento OnCompleted.**](swbemsink-oncompleted.md)</span><span class="sxs-lookup"><span data-stu-id="08e1d-176">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="08e1d-177">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="08e1d-177">Error codes</span></span>

<span data-ttu-id="08e1d-178">Después de completar el método **AssociatorsOfAsync,** el [objeto Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="08e1d-178">After the completion of the **AssociatorsOfAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="08e1d-179">**wbemErrAccessDenied:** 2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="08e1d-179">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="08e1d-180">El usuario actual no tiene permiso para ver una o varias de las clases devueltas por la llamada.</span><span class="sxs-lookup"><span data-stu-id="08e1d-180">Current user does not have the permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="08e1d-181">**wbemErrFailed:** 2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="08e1d-181">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="08e1d-182">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="08e1d-182">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="08e1d-183">**wbemErrInvalidParameter:** 2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="08e1d-183">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="08e1d-184">Se especificó un parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="08e1d-184">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="08e1d-185">**wbemErrOutOfMemory-** 2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="08e1d-185">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="08e1d-186">No hay suficiente memoria para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="08e1d-186">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="08e1d-187">**wbemErrNotFound** - 2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="08e1d-187">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="08e1d-188">No se encontró el elemento solicitado.</span><span class="sxs-lookup"><span data-stu-id="08e1d-188">Requested item was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="08e1d-189">Comentarios</span><span class="sxs-lookup"><span data-stu-id="08e1d-189">Remarks</span></span>

<span data-ttu-id="08e1d-190">Esta llamada se devuelve inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="08e1d-190">This call returns immediately.</span></span> <span data-ttu-id="08e1d-191">Los objetos y el estado solicitados se devuelven al autor de la llamada a través de devoluciones de llamada entregadas al receptor que se especifica en *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="08e1d-191">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="08e1d-192">Para procesar cada objeto cuando vuelva, cree *un objeto objWbemSink*. [**Subrutina de eventos OnObjectReady.**](swbemsink-onobjectready.md)</span><span class="sxs-lookup"><span data-stu-id="08e1d-192">To process each object when it returns, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="08e1d-193">Una vez devueltos todos los objetos, puede realizar el procesamiento final en la implementación de *objWbemSink*. [**Evento OnCompleted.**](swbemsink-oncompleted.md)</span><span class="sxs-lookup"><span data-stu-id="08e1d-193">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="08e1d-194">Una devolución de llamada asincrónica permite que un usuario no autenticado proporcione datos al receptor.</span><span class="sxs-lookup"><span data-stu-id="08e1d-194">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="08e1d-195">Esto supone riesgos de seguridad para los scripts y las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="08e1d-195">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="08e1d-196">Para eliminar los riesgos, vea [Establecer la seguridad en una llamada asincrónica.](setting-security-on-an-asynchronous-call.md)</span><span class="sxs-lookup"><span data-stu-id="08e1d-196">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="08e1d-197">Use el *parámetro objWbemAsyncContext en* scripts para comprobar el origen de una llamada.</span><span class="sxs-lookup"><span data-stu-id="08e1d-197">Use the *objWbemAsyncContext* parameter in scripts to verify the source of a call.</span></span>

## <a name="requirements"></a><span data-ttu-id="08e1d-198">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08e1d-198">Requirements</span></span>



| <span data-ttu-id="08e1d-199">Requisito</span><span class="sxs-lookup"><span data-stu-id="08e1d-199">Requirement</span></span> | <span data-ttu-id="08e1d-200">Valor</span><span class="sxs-lookup"><span data-stu-id="08e1d-200">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="08e1d-201">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08e1d-201">Minimum supported client</span></span><br/> | <span data-ttu-id="08e1d-202">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="08e1d-202">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="08e1d-203">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08e1d-203">Minimum supported server</span></span><br/> | <span data-ttu-id="08e1d-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="08e1d-204">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="08e1d-205">Encabezado</span><span class="sxs-lookup"><span data-stu-id="08e1d-205">Header</span></span><br/>                   | <dl> <span data-ttu-id="08e1d-206"><dt>Wbemdisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="08e1d-206"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="08e1d-207">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="08e1d-207">Type library</span></span><br/>             | <dl> <span data-ttu-id="08e1d-208"><dt>Wbemdisp.tlb</dt></span><span class="sxs-lookup"><span data-stu-id="08e1d-208"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="08e1d-209">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="08e1d-209">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08e1d-210"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08e1d-210"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="08e1d-211">CLSID</span><span class="sxs-lookup"><span data-stu-id="08e1d-211">CLSID</span></span><br/>                    | <span data-ttu-id="08e1d-212">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="08e1d-212">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="08e1d-213">IID</span><span class="sxs-lookup"><span data-stu-id="08e1d-213">IID</span></span><br/>                      | <span data-ttu-id="08e1d-214">IID \_ ISWbemServices</span><span class="sxs-lookup"><span data-stu-id="08e1d-214">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="08e1d-215">Consulte también</span><span class="sxs-lookup"><span data-stu-id="08e1d-215">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08e1d-216">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="08e1d-216">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="08e1d-217">**SWbemObject.Associators\_**</span><span class="sxs-lookup"><span data-stu-id="08e1d-217">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
</dt> <dt>

[<span data-ttu-id="08e1d-218">**SWbemObject.AssociatorsAsync\_**</span><span class="sxs-lookup"><span data-stu-id="08e1d-218">**SWbemObject.AssociatorsAsync\_**</span></span>](swbemobject-associatorsasync-.md)
</dt> <dt>

[<span data-ttu-id="08e1d-219">**SWbemObject.References\_**</span><span class="sxs-lookup"><span data-stu-id="08e1d-219">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
</dt> <dt>

[<span data-ttu-id="08e1d-220">**SWbemObject.ReferencesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="08e1d-220">**SWbemObject.ReferencesAsync\_**</span></span>](swbemobject-referencesasync-.md)
</dt> <dt>

[<span data-ttu-id="08e1d-221">**SWbemServices.ReferencesTo**</span><span class="sxs-lookup"><span data-stu-id="08e1d-221">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
</dt> <dt>

[<span data-ttu-id="08e1d-222">**SWbemServices.ReferencesToAsync**</span><span class="sxs-lookup"><span data-stu-id="08e1d-222">**SWbemServices.ReferencesToAsync**</span></span>](swbemservices-referencestoasync.md)
</dt> </dl>

 

