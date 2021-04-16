---
description: El \_ método AssociatorsAsync de SWbemObject obtiene objetos (clases o instancias) que están asociados al objeto actual. Estos objetos se denominan puntos de conexión. Este método realiza la misma función que realizan los asociados de la consulta WQL.
ms.assetid: c71e11cd-39a5-40d8-b279-f5ee9ff3ae04
ms.tgt_platform: multiple
title: Método SWbemObject.AssociatorsAsync_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.AssociatorsAsync_
- ISWbemObject.AssociatorsAsync_
- ISWbemObject.AssociatorsAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: fe7a592327b6952308e44ac054fb94e21aa6d6b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706054"
---
# <a name="swbemobjectassociatorsasync_-method"></a><span data-ttu-id="b64e3-105">SWbemObject. AssociatorsAsync, \_ método</span><span class="sxs-lookup"><span data-stu-id="b64e3-105">SWbemObject.AssociatorsAsync\_ method</span></span>

<span data-ttu-id="b64e3-106">El **método \_ AssociatorsAsync** de [**SWbemObject**](swbemobject.md) obtiene objetos (clases o instancias) que están asociados al objeto actual.</span><span class="sxs-lookup"><span data-stu-id="b64e3-106">The **AssociatorsAsync\_** method of [**SWbemObject**](swbemobject.md) obtains objects (classes or instances) that are associated with the current object.</span></span> <span data-ttu-id="b64e3-107">Estos objetos se denominan puntos de conexión.</span><span class="sxs-lookup"><span data-stu-id="b64e3-107">These objects are called endpoints.</span></span> <span data-ttu-id="b64e3-108">Este método realiza la misma función que realizan los asociados de la consulta WQL.</span><span class="sxs-lookup"><span data-stu-id="b64e3-108">This method performs the same function that the ASSOCIATORS OF WQL query performs.</span></span>

<span data-ttu-id="b64e3-109">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="b64e3-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b64e3-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b64e3-110">Syntax</span></span>


```VB
SWbemObject.AssociatorsAsync_( _
  ByVal objWbemSink, _
  [ ByVal strAssocClass ], _
  [ ByVal strResultClass ], _
  [ ByVal strResultRole ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredAssocQualifier ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="b64e3-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b64e3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b64e3-112">*objWbemSink* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b64e3-112">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b64e3-113">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b64e3-113">Required.</span></span> <span data-ttu-id="b64e3-114">Receptor de objeto que recibe los objetos de forma asincrónica como una devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="b64e3-114">Object sink that receives the objects asynchronously as a callback.</span></span>

</dd> <dt>

<span data-ttu-id="b64e3-115">*strAssocClass* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b64e3-115">*strAssocClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b64e3-116">Cadena que contiene una clase de asociación.</span><span class="sxs-lookup"><span data-stu-id="b64e3-116">String that contains an association class.</span></span> <span data-ttu-id="b64e3-117">Si se especifica, este parámetro indica que los extremos devueltos deben asociarse con el origen a través de la clase de asociación especificada o una clase derivada de esta clase de asociación.</span><span class="sxs-lookup"><span data-stu-id="b64e3-117">If specified, this parameter indicates that the returned endpoints must be associated with the source through the specified association class or a class derived from this association class.</span></span>

</dd> <dt>

<span data-ttu-id="b64e3-118">*strResultClass* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b64e3-118">*strResultClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b64e3-119">Cadena que contiene un nombre de clase.</span><span class="sxs-lookup"><span data-stu-id="b64e3-119">String that contains a class name.</span></span> <span data-ttu-id="b64e3-120">Si se especifica, este parámetro indica que los extremos devueltos deben pertenecer a la clase especificada en este parámetro o derivarse de ella.</span><span class="sxs-lookup"><span data-stu-id="b64e3-120">If specified, this parameter indicates that the returned endpoints must belong to or be derived from the class specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b64e3-121">*strResultRole* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b64e3-121">*strResultRole* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b64e3-122">Cadena que contiene un nombre de propiedad.</span><span class="sxs-lookup"><span data-stu-id="b64e3-122">String that contains a property name.</span></span> <span data-ttu-id="b64e3-123">Si se especifica, este parámetro indica que los extremos devueltos deben desempeñar un rol determinado en su asociación con el objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="b64e3-123">If specified, this parameter indicates that the returned endpoints must play a particular role in their association with the source object.</span></span> <span data-ttu-id="b64e3-124">El rol se define mediante el nombre de una propiedad especificada (que debe ser una propiedad de referencia) de una asociación.</span><span class="sxs-lookup"><span data-stu-id="b64e3-124">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="b64e3-125">*strRole* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b64e3-125">*strRole* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b64e3-126">Cadena que contiene un nombre de propiedad.</span><span class="sxs-lookup"><span data-stu-id="b64e3-126">String that contains a property name.</span></span> <span data-ttu-id="b64e3-127">Si se especifica, este parámetro indica que los extremos devueltos deben participar en una asociación con el objeto de origen en el que el objeto de origen desempeña un rol determinado.</span><span class="sxs-lookup"><span data-stu-id="b64e3-127">If specified, this parameter indicates that the returned endpoints must participate in an association with the source object in which the source object plays a particular role.</span></span> <span data-ttu-id="b64e3-128">El rol se define mediante el nombre de una propiedad especificada (que debe ser una propiedad de referencia) de una asociación.</span><span class="sxs-lookup"><span data-stu-id="b64e3-128">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="b64e3-129">*bClassesOnly* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b64e3-129">*bClassesOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b64e3-130">Valor booleano que indica si se debe devolver una lista de nombres de clase en lugar de instancias reales de las clases.</span><span class="sxs-lookup"><span data-stu-id="b64e3-130">Boolean value that indicates whether a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="b64e3-131">Estas son las clases a las que pertenecen las instancias de extremo.</span><span class="sxs-lookup"><span data-stu-id="b64e3-131">These are the classes to which the endpoint instances belong.</span></span> <span data-ttu-id="b64e3-132">El valor predeterminado de este parámetro es **false**.</span><span class="sxs-lookup"><span data-stu-id="b64e3-132">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="b64e3-133">*bSchemaOnly* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b64e3-133">*bSchemaOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b64e3-134">Valor booleano que indica si la consulta se aplica al esquema en lugar de a los datos.</span><span class="sxs-lookup"><span data-stu-id="b64e3-134">Boolean value that indicates whether the query applies to the schema rather than the data.</span></span> <span data-ttu-id="b64e3-135">El valor predeterminado de este parámetro es **false**.</span><span class="sxs-lookup"><span data-stu-id="b64e3-135">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="b64e3-136">Solo se puede establecer en **true** si el objeto en el que se invoca este método es una clase.</span><span class="sxs-lookup"><span data-stu-id="b64e3-136">It can only be set to **TRUE** if the object on which this method is invoked is a class.</span></span> <span data-ttu-id="b64e3-137">Cuando se establece en **true**, el conjunto de extremos devueltos representa las clases que están asociadas adecuadamente a la clase de origen en el esquema.</span><span class="sxs-lookup"><span data-stu-id="b64e3-137">When set to **TRUE**, the set of returned endpoints represent classes that are suitably associated with the source class in the schema.</span></span>

</dd> <dt>

<span data-ttu-id="b64e3-138">*strRequiredAssocQualifier* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b64e3-138">*strRequiredAssocQualifier* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b64e3-139">Cadena que contiene un nombre de calificador.</span><span class="sxs-lookup"><span data-stu-id="b64e3-139">String that contains a qualifier name.</span></span> <span data-ttu-id="b64e3-140">Si se especifica, este parámetro indica que los extremos devueltos deben asociarse con el objeto de origen a través de una clase de asociación que incluye el calificador especificado.</span><span class="sxs-lookup"><span data-stu-id="b64e3-140">If specified, this parameter indicates that the returned endpoints must be associated with the source object through an association class that includes the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="b64e3-141">*strRequiredQualifier* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b64e3-141">*strRequiredQualifier* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b64e3-142">Cadena que contiene un nombre de calificador.</span><span class="sxs-lookup"><span data-stu-id="b64e3-142">String that contains a qualifier name.</span></span> <span data-ttu-id="b64e3-143">Si se especifica, este parámetro indica que los extremos devueltos deben incluir el calificador especificado.</span><span class="sxs-lookup"><span data-stu-id="b64e3-143">If specified, this parameter indicates that the returned endpoints must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="b64e3-144">*iFlags* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b64e3-144">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b64e3-145">Entero que especifica marcas adicionales para la operación.</span><span class="sxs-lookup"><span data-stu-id="b64e3-145">Integer specifying additional flags to the operation.</span></span> <span data-ttu-id="b64e3-146">Este parámetro puede aceptar los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="b64e3-146">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="b64e3-147"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="b64e3-147"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="b64e3-148">Hace que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**SWbemSink. OnProgress**](swbemsink-onprogress.md) para el receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="b64e3-148">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="b64e3-149"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="b64e3-149"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="b64e3-150">Impide que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**OnProgress**](swbemsink-onprogress.md) para el receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="b64e3-150">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="b64e3-151"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="b64e3-151"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="b64e3-152">Hace que WMI devuelva las descripciones de clase y propiedad localizadas.</span><span class="sxs-lookup"><span data-stu-id="b64e3-152">Causes WMI to return the localized class and property descriptions.</span></span> <span data-ttu-id="b64e3-153">Para obtener más información, consulte [localizar información de clase WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="b64e3-153">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b64e3-154">*objwbemNamedValueSet* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b64e3-154">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b64e3-155">Normalmente, esto no está definido.</span><span class="sxs-lookup"><span data-stu-id="b64e3-155">Typically, this is undefined.</span></span> <span data-ttu-id="b64e3-156">De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que atiende la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b64e3-156">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="b64e3-157">Un proveedor que admite o requiere tal información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.</span><span class="sxs-lookup"><span data-stu-id="b64e3-157">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="b64e3-158">*objWbemAsyncContext* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b64e3-158">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b64e3-159">Se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que devuelve al receptor del objeto para identificar el origen de la llamada asincrónica original.</span><span class="sxs-lookup"><span data-stu-id="b64e3-159">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="b64e3-160">Utilice este parámetro si va a realizar varias llamadas asincrónicas mediante el mismo receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="b64e3-160">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="b64e3-161">Para usar este parámetro, cree un objeto **SWbemNamedValueSet** y use el método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) para agregar un valor que identifique la llamada asincrónica que está realizando.</span><span class="sxs-lookup"><span data-stu-id="b64e3-161">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="b64e3-162">Este objeto **SWbemNamedValueSet** se devuelve al receptor del objeto y el origen de la llamada se puede extraer mediante el método [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="b64e3-162">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="b64e3-163">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="b64e3-163">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b64e3-164">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b64e3-164">Return value</span></span>

<span data-ttu-id="b64e3-165">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b64e3-165">This method does not return a value.</span></span> <span data-ttu-id="b64e3-166">Si se realiza correctamente, el receptor recibe un evento [**OnObjectReady**](swbemsink-onobjectready.md) por cada instancia.</span><span class="sxs-lookup"><span data-stu-id="b64e3-166">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="b64e3-167">Después de la última instancia, el receptor del objeto recibe un evento [**alcompleto**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="b64e3-167">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b64e3-168">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="b64e3-168">Error codes</span></span>

<span data-ttu-id="b64e3-169">Después de completar el **método \_ AssociatorsAsync** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="b64e3-169">After completion of the **AssociatorsAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="b64e3-170">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="b64e3-170">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="b64e3-171">El usuario actual no tiene permiso para ver una o varias de las clases devueltas por la llamada.</span><span class="sxs-lookup"><span data-stu-id="b64e3-171">The current user does not have permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="b64e3-172">**wbemErrFailed** -2147449889 (0x7FFF7C21)</span><span class="sxs-lookup"><span data-stu-id="b64e3-172">**wbemErrFailed** - 2147449889 (0x7FFF7C21)</span></span>
</dt> <dd>

<span data-ttu-id="b64e3-173">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="b64e3-173">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="b64e3-174">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="b64e3-174">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="b64e3-175">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="b64e3-175">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="b64e3-176">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="b64e3-176">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="b64e3-177">Memoria insuficiente para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="b64e3-177">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b64e3-178">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b64e3-178">Remarks</span></span>

<span data-ttu-id="b64e3-179">Esta llamada se devuelve inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="b64e3-179">This call returns immediately.</span></span> <span data-ttu-id="b64e3-180">Los objetos y el estado solicitados se devuelven al autor de la llamada a través de las devoluciones de llamada entregadas al receptor que se especifica en *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="b64e3-180">The requested objects and status are returned to the caller through call-backs delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="b64e3-181">Para procesar cada objeto cuando llegue, cree un *objWbemSink*. Subrutina de evento [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="b64e3-181">To process each object when it arrives, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="b64e3-182">Después de que se devuelvan todos los objetos, puede realizar el procesamiento final en la implementación de *objWbemSink*. Evento [**Alcompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="b64e3-182">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="b64e3-183">Una devolución de llamada asincrónica permite que un usuario no autenticado proporcione datos al receptor.</span><span class="sxs-lookup"><span data-stu-id="b64e3-183">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="b64e3-184">Esto supone riesgos de seguridad para los scripts y las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="b64e3-184">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="b64e3-185">Para eliminar los riesgos, utilice la comunicación semisincrónica o la comunicación sincrónica.</span><span class="sxs-lookup"><span data-stu-id="b64e3-185">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="b64e3-186">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="b64e3-186">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="b64e3-187">Para obtener más información sobre los asociados de consultas WQL asociadas, instancias de origen y extremos, vea [ASSOCIATORS OF Statement](associators-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="b64e3-187">For more information about the ASSOCIATORS OF associated WQL queries, source instances, and endpoints, see [ASSOCIATORS OF Statement](associators-of-statement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b64e3-188">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b64e3-188">Requirements</span></span>



| <span data-ttu-id="b64e3-189">Requisito</span><span class="sxs-lookup"><span data-stu-id="b64e3-189">Requirement</span></span> | <span data-ttu-id="b64e3-190">Value</span><span class="sxs-lookup"><span data-stu-id="b64e3-190">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b64e3-191">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b64e3-191">Minimum supported client</span></span><br/> | <span data-ttu-id="b64e3-192">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b64e3-192">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b64e3-193">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b64e3-193">Minimum supported server</span></span><br/> | <span data-ttu-id="b64e3-194">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b64e3-194">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b64e3-195">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b64e3-195">Header</span></span><br/>                   | <dl> <span data-ttu-id="b64e3-196"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b64e3-196"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b64e3-197">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b64e3-197">Type library</span></span><br/>             | <dl> <span data-ttu-id="b64e3-198"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b64e3-198"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b64e3-199">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b64e3-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b64e3-200"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b64e3-200"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b64e3-201">CLSID</span><span class="sxs-lookup"><span data-stu-id="b64e3-201">CLSID</span></span><br/>                    | <span data-ttu-id="b64e3-202">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="b64e3-202">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="b64e3-203">IID</span><span class="sxs-lookup"><span data-stu-id="b64e3-203">IID</span></span><br/>                      | <span data-ttu-id="b64e3-204">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="b64e3-204">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="b64e3-205">Vea también</span><span class="sxs-lookup"><span data-stu-id="b64e3-205">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b64e3-206">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="b64e3-206">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="b64e3-207">**SWbemServices. AssociatorsOfAsync**</span><span class="sxs-lookup"><span data-stu-id="b64e3-207">**SWbemServices.AssociatorsOfAsync**</span></span>](swbemservices-associatorsofasync.md)
</dt> <dt>

[<span data-ttu-id="b64e3-208">**SWbemObject. References\_**</span><span class="sxs-lookup"><span data-stu-id="b64e3-208">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
</dt> <dt>

[<span data-ttu-id="b64e3-209">**SWbemServices. References**</span><span class="sxs-lookup"><span data-stu-id="b64e3-209">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
</dt> </dl>

 

