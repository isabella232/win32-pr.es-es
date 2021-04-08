---
description: El método Associatorsrs \_ del objeto SWbemObject devuelve una colección de objetos (clases o instancias) que están asociados al objeto actual.
ms.assetid: 79f01853-c649-4cbe-b2fa-cff38fb4b733
ms.tgt_platform: multiple
title: Método SWbemObject.Associators_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Associators_
- ISWbemObject.Associators_
- ISWbemObject.Associators_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1f9ff4536936661ece54b5bff29e500ce6e98d3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002649"
---
# <a name="swbemobjectassociators_-method"></a><span data-ttu-id="4f80b-103">SWbemObject. Associatorst ( \_ método)</span><span class="sxs-lookup"><span data-stu-id="4f80b-103">SWbemObject.Associators\_ method</span></span>

<span data-ttu-id="4f80b-104">El método **associatorsrs \_** del objeto [**SWbemObject**](swbemobject.md) devuelve una colección de objetos (clases o instancias) que están asociados al objeto actual.</span><span class="sxs-lookup"><span data-stu-id="4f80b-104">The **Associators\_** method of the [**SWbemObject**](swbemobject.md) object returns a collection of objects (classes or instances) that are associated with the current object.</span></span> <span data-ttu-id="4f80b-105">Estos objetos devueltos se denominan puntos de conexión.</span><span class="sxs-lookup"><span data-stu-id="4f80b-105">These returned objects are called endpoints.</span></span> <span data-ttu-id="4f80b-106">Este método realiza la misma función que realizan los asociados de la consulta WQL.</span><span class="sxs-lookup"><span data-stu-id="4f80b-106">This method performs the same function that the ASSOCIATORS OF WQL query performs.</span></span>

<span data-ttu-id="4f80b-107">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="4f80b-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4f80b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4f80b-108">Syntax</span></span>


```VB
objWbemObjectSet = .Associators_( _
  [ ByVal strAssocClass ], _
  [ ByVal strResultClass ], _
  [ ByVal strResultRole ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredAssocQualifier ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="4f80b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4f80b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f80b-110">*strAssocClass* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="4f80b-110">*strAssocClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4f80b-111">Cadena que contiene una clase de asociación.</span><span class="sxs-lookup"><span data-stu-id="4f80b-111">String that contains an association class.</span></span> <span data-ttu-id="4f80b-112">Si se especifica, este parámetro indica que los extremos devueltos deben asociarse con el origen a través de la clase de asociación especificada o una clase derivada de esta clase de asociación.</span><span class="sxs-lookup"><span data-stu-id="4f80b-112">If specified, this parameter indicates that the returned endpoints must be associated with the source through the specified association class or a class derived from this association class.</span></span>

</dd> <dt>

<span data-ttu-id="4f80b-113">*strResultClass* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="4f80b-113">*strResultClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4f80b-114">Cadena que contiene un nombre de clase.</span><span class="sxs-lookup"><span data-stu-id="4f80b-114">String that contains a class name.</span></span> <span data-ttu-id="4f80b-115">Si se especifica, este parámetro indica que los extremos devueltos deben pertenecer a la clase especificada en este parámetro o derivarse de ella.</span><span class="sxs-lookup"><span data-stu-id="4f80b-115">If specified, this parameter indicates that the returned endpoints must belong to or be derived from the class specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="4f80b-116">*strResultRole* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="4f80b-116">*strResultRole* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4f80b-117">Cadena que contiene un nombre de propiedad.</span><span class="sxs-lookup"><span data-stu-id="4f80b-117">String that contains a property name.</span></span> <span data-ttu-id="4f80b-118">Si se especifica, este parámetro indica que los extremos devueltos deben desempeñar un rol determinado en su asociación con el objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="4f80b-118">If specified, this parameter indicates that the returned endpoints must play a particular role in their association with the source object.</span></span> <span data-ttu-id="4f80b-119">El rol se define mediante el nombre de una propiedad especificada (que debe ser una propiedad de referencia) de una asociación.</span><span class="sxs-lookup"><span data-stu-id="4f80b-119">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="4f80b-120">*strRole* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="4f80b-120">*strRole* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4f80b-121">Cadena que contiene un nombre de propiedad.</span><span class="sxs-lookup"><span data-stu-id="4f80b-121">String that contains a property name.</span></span> <span data-ttu-id="4f80b-122">Si se especifica, este parámetro indica que los extremos devueltos deben participar en una asociación con el objeto de origen en el que el objeto de origen desempeña un rol determinado.</span><span class="sxs-lookup"><span data-stu-id="4f80b-122">If specified, this parameter indicates that the returned endpoints must participate in an association with the source object in which the source object plays a particular role.</span></span> <span data-ttu-id="4f80b-123">El rol se define mediante el nombre de una propiedad especificada (que debe ser una propiedad de referencia) de una asociación.</span><span class="sxs-lookup"><span data-stu-id="4f80b-123">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="4f80b-124">*bClassesOnly* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="4f80b-124">*bClassesOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4f80b-125">Valor booleano que indica si se debe devolver una lista de nombres de clase en lugar de instancias reales de las clases.</span><span class="sxs-lookup"><span data-stu-id="4f80b-125">Boolean value that indicates whether a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="4f80b-126">Estas son las clases a las que pertenecen las instancias de extremo.</span><span class="sxs-lookup"><span data-stu-id="4f80b-126">These are the classes to which the endpoint instances belong.</span></span> <span data-ttu-id="4f80b-127">El valor predeterminado de este parámetro es **false**.</span><span class="sxs-lookup"><span data-stu-id="4f80b-127">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="4f80b-128">*bSchemaOnly* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="4f80b-128">*bSchemaOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4f80b-129">Se trata de un valor booleano que indica si la consulta se aplica al esquema en lugar de a los datos.</span><span class="sxs-lookup"><span data-stu-id="4f80b-129">This is a Boolean value that indicates whether the query applies to the schema rather than the data.</span></span> <span data-ttu-id="4f80b-130">El valor predeterminado de este parámetro es **false**.</span><span class="sxs-lookup"><span data-stu-id="4f80b-130">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="4f80b-131">Solo se puede establecer en **true** si el objeto en el que se invoca este método es una clase.</span><span class="sxs-lookup"><span data-stu-id="4f80b-131">It can only be set to **TRUE** if the object on which this method is invoked is a class.</span></span> <span data-ttu-id="4f80b-132">Cuando se establece en **true**, el conjunto de extremos devueltos representa las clases que están asociadas adecuadamente a la clase de origen en el esquema.</span><span class="sxs-lookup"><span data-stu-id="4f80b-132">When set to **TRUE**, the set of returned endpoints represent classes that are suitably associated with the source class in the schema.</span></span>

</dd> <dt>

<span data-ttu-id="4f80b-133">*strRequiredAssocQualifier* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="4f80b-133">*strRequiredAssocQualifier* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4f80b-134">Cadena que contiene un nombre de calificador.</span><span class="sxs-lookup"><span data-stu-id="4f80b-134">String that contains a qualifier name.</span></span> <span data-ttu-id="4f80b-135">Este parámetro, si se especifica, indica que los extremos devueltos deben asociarse con el objeto de origen a través de una clase de asociación que incluye el calificador especificado.</span><span class="sxs-lookup"><span data-stu-id="4f80b-135">This parameter, if specified, indicates that the returned endpoints must be associated with the source object through an association class that includes the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="4f80b-136">*strRequiredQualifier* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="4f80b-136">*strRequiredQualifier* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4f80b-137">Cadena que contiene un nombre de calificador.</span><span class="sxs-lookup"><span data-stu-id="4f80b-137">String that contains a qualifier name.</span></span> <span data-ttu-id="4f80b-138">Este parámetro, si se especifica, indica que los extremos devueltos deben incluir el calificador especificado.</span><span class="sxs-lookup"><span data-stu-id="4f80b-138">This parameter, if specified, indicates that the returned endpoints must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="4f80b-139">*iFlags* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="4f80b-139">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4f80b-140">Entero que especifica marcas adicionales para la operación.</span><span class="sxs-lookup"><span data-stu-id="4f80b-140">Integer specifying additional flags to the operation.</span></span> <span data-ttu-id="4f80b-141">El valor predeterminado para este parámetro es **wbemFlagReturnImmediately**, que dirige la llamada para que se devuelva inmediatamente en lugar de esperar hasta que se complete la consulta.</span><span class="sxs-lookup"><span data-stu-id="4f80b-141">The default for this parameter is **wbemFlagReturnImmediately**, which directs the call to return immediately rather than wait until the query has completed.</span></span> <span data-ttu-id="4f80b-142">Este parámetro puede aceptar los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="4f80b-142">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="4f80b-143"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="4f80b-143"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="4f80b-144">Hace que se devuelva un enumerador de solo avance.</span><span class="sxs-lookup"><span data-stu-id="4f80b-144">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="4f80b-145">Los enumeradores de solo avance suelen ser mucho más rápidos y usan menos memoria que los enumeradores convencionales, pero no permiten llamadas a [**SWbemObject. \_ Clone**](swbemobject-clone-.md).</span><span class="sxs-lookup"><span data-stu-id="4f80b-145">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span data-ttu-id="4f80b-146"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional \* \* \* \* (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="4f80b-146"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>\*\*\*\*wbemFlagBidirectional\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="4f80b-147">Hace que WMI conserve punteros a objetos de la enumeración hasta que el cliente libere el enumerador.</span><span class="sxs-lookup"><span data-stu-id="4f80b-147">Causes WMI to retain pointers to objects of the enumeration until the client releases the enumerator.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="4f80b-148"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="4f80b-148"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="4f80b-149">Hace que la llamada se devuelva inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="4f80b-149">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="4f80b-150"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* \* (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="4f80b-150"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="4f80b-151">Hace que esta llamada se bloquee hasta que se complete la consulta.</span><span class="sxs-lookup"><span data-stu-id="4f80b-151">Causes this call to block until the query has completed.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="4f80b-152"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="4f80b-152"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="4f80b-153">Hace que WMI devuelva datos de modificación de clase con la definición de clase base.</span><span class="sxs-lookup"><span data-stu-id="4f80b-153">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="4f80b-154">La inclusión de esta marca hace que el texto del calificador de la descripción localizada esté disponible para las clases, propiedades y métodos.</span><span class="sxs-lookup"><span data-stu-id="4f80b-154">Including this flag makes the localized description qualifier text available for classes, properties and methods.</span></span> <span data-ttu-id="4f80b-155">Para obtener más información acerca de los calificadores modificados, consulte [localizar información de clase WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="4f80b-155">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4f80b-156">*objwbemNamedValueSet* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="4f80b-156">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4f80b-157">Normalmente, esto no está definido.</span><span class="sxs-lookup"><span data-stu-id="4f80b-157">Typically, this is undefined.</span></span> <span data-ttu-id="4f80b-158">De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que atiende la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4f80b-158">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="4f80b-159">Un proveedor que admite o requiere tal información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.</span><span class="sxs-lookup"><span data-stu-id="4f80b-159">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f80b-160">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4f80b-160">Return value</span></span>

<span data-ttu-id="4f80b-161">Si la llamada se realiza correctamente, se devuelve un objeto [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="4f80b-161">If the call is successful, an [**SWbemObjectSet**](swbemobjectset.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4f80b-162">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="4f80b-162">Error codes</span></span>

<span data-ttu-id="4f80b-163">Después de completar el método **associatorsrs \_** , el objeto **Err** puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="4f80b-163">After completion of the **Associators\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="4f80b-164">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="4f80b-164">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="4f80b-165">El usuario actual no tiene permiso para ver una o varias de las clases devueltas por la llamada.</span><span class="sxs-lookup"><span data-stu-id="4f80b-165">The current user does not have permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="4f80b-166">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="4f80b-166">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="4f80b-167">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="4f80b-167">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="4f80b-168">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="4f80b-168">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="4f80b-169">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="4f80b-169">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="4f80b-170">**wbemErrOutOfMemory** -2147749894</span><span class="sxs-lookup"><span data-stu-id="4f80b-170">**wbemErrOutOfMemory** - 2147749894</span></span>
</dt> <dd>

<span data-ttu-id="4f80b-171">Memoria insuficiente para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="4f80b-171">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4f80b-172">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4f80b-172">Remarks</span></span>

<span data-ttu-id="4f80b-173">Para obtener más información acerca de los asociados de la consulta WQL asociada, las instancias de origen y los puntos de conexión, consulte [ASSOCIATORS OF Statement](associators-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="4f80b-173">For more information about the ASSOCIATORS OF associated WQL query, source instances, and endpoints, see [ASSOCIATORS OF Statement](associators-of-statement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4f80b-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f80b-174">Requirements</span></span>



| <span data-ttu-id="4f80b-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f80b-175">Requirement</span></span> | <span data-ttu-id="4f80b-176">Value</span><span class="sxs-lookup"><span data-stu-id="4f80b-176">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f80b-177">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4f80b-177">Minimum supported client</span></span><br/> | <span data-ttu-id="4f80b-178">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4f80b-178">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4f80b-179">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4f80b-179">Minimum supported server</span></span><br/> | <span data-ttu-id="4f80b-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4f80b-180">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4f80b-181">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4f80b-181">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f80b-182"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f80b-182"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4f80b-183">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="4f80b-183">Type library</span></span><br/>             | <dl> <span data-ttu-id="4f80b-184"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4f80b-184"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4f80b-185">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4f80b-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f80b-186"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f80b-186"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4f80b-187">CLSID</span><span class="sxs-lookup"><span data-stu-id="4f80b-187">CLSID</span></span><br/>                    | <span data-ttu-id="4f80b-188">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="4f80b-188">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="4f80b-189">IID</span><span class="sxs-lookup"><span data-stu-id="4f80b-189">IID</span></span><br/>                      | <span data-ttu-id="4f80b-190">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="4f80b-190">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="4f80b-191">Vea también</span><span class="sxs-lookup"><span data-stu-id="4f80b-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f80b-192">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="4f80b-192">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="4f80b-193">**SWbemObject. References\_**</span><span class="sxs-lookup"><span data-stu-id="4f80b-193">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
</dt> <dt>

[<span data-ttu-id="4f80b-194">**SWbemServices. AssociatorsOf**</span><span class="sxs-lookup"><span data-stu-id="4f80b-194">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-associatorsof.md)
</dt> <dt>

[<span data-ttu-id="4f80b-195">**SWbemServices. References**</span><span class="sxs-lookup"><span data-stu-id="4f80b-195">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
</dt> </dl>

 

 




