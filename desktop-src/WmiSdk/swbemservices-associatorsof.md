---
description: Devuelve una colección de objetos (clases o instancias) denominada puntos de conexión que están asociados a un objeto especificado.
ms.assetid: a78e6701-6779-4a02-b811-23b2da4f4167
ms.tgt_platform: multiple
title: Método SWbemServices. AssociatorsOf (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.AssociatorsOf
- ISWbemServices.AssociatorsOf
- ISWbemServices.AssociatorsOf
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0208ef23158d71a5174fcb6759acba1d64bd09a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667585"
---
# <a name="swbemservicesassociatorsof-method"></a><span data-ttu-id="7d65b-103">SWbemServices. AssociatorsOf, método</span><span class="sxs-lookup"><span data-stu-id="7d65b-103">SWbemServices.AssociatorsOf method</span></span>

<span data-ttu-id="7d65b-104">El método **AssociatorsOf** del objeto [**SWbemServices**](swbemservices.md) devuelve una colección de objetos (clases o instancias) denominados extremos que están asociados a un objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="7d65b-104">The **AssociatorsOf** method of the [**SWbemServices**](swbemservices.md) object returns a collection of objects (classes or instances) called endpoints that are associated with a specified object.</span></span> <span data-ttu-id="7d65b-105">Este método realiza la misma función que realizan los asociados de la consulta WQL.</span><span class="sxs-lookup"><span data-stu-id="7d65b-105">This method performs the same function that the ASSOCIATORS OF WQL query performs.</span></span>

<span data-ttu-id="7d65b-106">De forma predeterminada, se llama a este método en el modo semisincrónico.</span><span class="sxs-lookup"><span data-stu-id="7d65b-106">This method is called in the semisynchronous mode by default.</span></span> <span data-ttu-id="7d65b-107">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="7d65b-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="7d65b-108">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="7d65b-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7d65b-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7d65b-109">Syntax</span></span>


```VB
objWbemObjectSet = .AssociatorsOf( _
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
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="7d65b-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7d65b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d65b-111">*strObjectPath*</span><span class="sxs-lookup"><span data-stu-id="7d65b-111">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="7d65b-112">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7d65b-112">Required.</span></span> <span data-ttu-id="7d65b-113">Cadena que contiene la ruta de acceso del objeto de la clase o instancia de origen.</span><span class="sxs-lookup"><span data-stu-id="7d65b-113">String that contains the object path of the source class or instance.</span></span> <span data-ttu-id="7d65b-114">Para obtener más información, vea [Descripción de la ubicación de un objeto WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="7d65b-114">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="7d65b-115">*strAssocClass* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="7d65b-115">*strAssocClass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7d65b-116">Cadena que contiene una clase de asociación.</span><span class="sxs-lookup"><span data-stu-id="7d65b-116">String that contains an association class.</span></span> <span data-ttu-id="7d65b-117">Si se especifica, este parámetro indica que los extremos devueltos deben estar asociados al origen a través de la clase de asociación especificada o de una clase que se deriva de esta clase de asociación.</span><span class="sxs-lookup"><span data-stu-id="7d65b-117">If specified, this parameter indicates that the returned endpoints must be associated with the source through the specified association class or a class that is derived from this association class.</span></span>

</dd> <dt>

<span data-ttu-id="7d65b-118">*strResultClass* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="7d65b-118">*strResultClass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7d65b-119">Cadena que contiene un nombre de clase.</span><span class="sxs-lookup"><span data-stu-id="7d65b-119">String that contains a class name.</span></span> <span data-ttu-id="7d65b-120">Si se especifica, este parámetro opcional indica que los extremos devueltos deben pertenecer a la clase especificada en este parámetro o derivarse de ella.</span><span class="sxs-lookup"><span data-stu-id="7d65b-120">If specified, this optional parameter indicates that the returned endpoints must belong to or be derived from the class specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="7d65b-121">*strResultRole* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="7d65b-121">*strResultRole* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7d65b-122">Cadena que contiene un nombre de propiedad.</span><span class="sxs-lookup"><span data-stu-id="7d65b-122">String that contains a property name.</span></span> <span data-ttu-id="7d65b-123">Si se especifica, este parámetro indica que los extremos devueltos deben desempeñar un rol determinado en su asociación con el objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="7d65b-123">If specified, this parameter indicates that the returned endpoints must play a particular role in their association with the source object.</span></span> <span data-ttu-id="7d65b-124">El rol se define mediante el nombre de una propiedad especificada (que debe ser una propiedad de referencia) de una asociación.</span><span class="sxs-lookup"><span data-stu-id="7d65b-124">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="7d65b-125">*strRole* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="7d65b-125">*strRole* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7d65b-126">Cadena que contiene un nombre de propiedad.</span><span class="sxs-lookup"><span data-stu-id="7d65b-126">String that contains a property name.</span></span> <span data-ttu-id="7d65b-127">Si se especifica, este parámetro indica que los extremos devueltos deben participar en una asociación con el objeto de origen en el que el objeto de origen desempeña un rol determinado.</span><span class="sxs-lookup"><span data-stu-id="7d65b-127">If specified, this parameter indicates that the returned endpoints must participate in an association with the source object in which the source object plays a particular role.</span></span> <span data-ttu-id="7d65b-128">El rol se define mediante el nombre de una propiedad especificada (que debe ser una propiedad de referencia) de una asociación.</span><span class="sxs-lookup"><span data-stu-id="7d65b-128">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="7d65b-129">*bClassesOnly* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="7d65b-129">*bClassesOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7d65b-130">Valor booleano que indica si se debe devolver una lista de nombres de clase en lugar de instancias reales de las clases.</span><span class="sxs-lookup"><span data-stu-id="7d65b-130">Boolean value that indicates whether a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="7d65b-131">Estas son las clases a las que pertenecen las instancias de extremo.</span><span class="sxs-lookup"><span data-stu-id="7d65b-131">These are the classes to which the endpoint instances belong.</span></span> <span data-ttu-id="7d65b-132">El valor predeterminado de este parámetro es **false**.</span><span class="sxs-lookup"><span data-stu-id="7d65b-132">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="7d65b-133">*bSchemaOnly* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="7d65b-133">*bSchemaOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7d65b-134">Valor booleano que indica si la consulta se aplica al esquema en lugar de a los datos.</span><span class="sxs-lookup"><span data-stu-id="7d65b-134">Boolean value that indicates whether the query applies to the schema rather than the data.</span></span> <span data-ttu-id="7d65b-135">El valor predeterminado de este parámetro es **false**.</span><span class="sxs-lookup"><span data-stu-id="7d65b-135">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="7d65b-136">Solo se puede establecer en **true** si el parámetro *strObjectPath* especifica la ruta de acceso del objeto de una clase.</span><span class="sxs-lookup"><span data-stu-id="7d65b-136">It can only be set to **TRUE** if the *strObjectPath* parameter specifies the object path of a class.</span></span> <span data-ttu-id="7d65b-137">Cuando se establece en **true**, el conjunto de extremos devueltos representa las clases que están asociadas adecuadamente a la clase de origen en el esquema.</span><span class="sxs-lookup"><span data-stu-id="7d65b-137">When set to **TRUE**, the set of returned endpoints represent classes that are suitably associated with the source class in schema.</span></span>

</dd> <dt>

<span data-ttu-id="7d65b-138">*strRequiredAssocQualifier* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="7d65b-138">*strRequiredAssocQualifier* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7d65b-139">Cadena que contiene un nombre de calificador.</span><span class="sxs-lookup"><span data-stu-id="7d65b-139">String that contains a qualifier name.</span></span> <span data-ttu-id="7d65b-140">Si se especifica, este parámetro indica que los extremos devueltos deben asociarse con el objeto de origen a través de una clase de asociación que incluye el calificador especificado.</span><span class="sxs-lookup"><span data-stu-id="7d65b-140">If specified, this parameter indicates that the returned endpoints must be associated with the source object through an association class that includes the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="7d65b-141">*strRequiredQualifier* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="7d65b-141">*strRequiredQualifier* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7d65b-142">Cadena que contiene un nombre de calificador.</span><span class="sxs-lookup"><span data-stu-id="7d65b-142">String that contains a qualifier name.</span></span> <span data-ttu-id="7d65b-143">Si se especifica, este parámetro indica que los extremos devueltos deben incluir el calificador especificado.</span><span class="sxs-lookup"><span data-stu-id="7d65b-143">If specified, this parameter indicates that the returned endpoints must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="7d65b-144">*iFlags* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="7d65b-144">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7d65b-145">Entero que especifica las marcas adicionales para la operación.</span><span class="sxs-lookup"><span data-stu-id="7d65b-145">Integer that specifies additional flags to the operation.</span></span> <span data-ttu-id="7d65b-146">El valor predeterminado de este parámetro es **wbemFlagReturnImmediately**, que llama al método en el modo semisincrónico.</span><span class="sxs-lookup"><span data-stu-id="7d65b-146">The default value for this parameter is **wbemFlagReturnImmediately**, which calls the method in the semisynchronous mode.</span></span> <span data-ttu-id="7d65b-147">Este parámetro puede aceptar los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="7d65b-147">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="7d65b-148"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="7d65b-148"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="7d65b-149">Hace que se devuelva un enumerador de solo avance.</span><span class="sxs-lookup"><span data-stu-id="7d65b-149">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="7d65b-150">Los enumeradores de solo avance suelen ser mucho más rápidos y usan menos memoria que los enumeradores convencionales, pero no permiten llamadas a [**SWbemObject. \_ Clone**](swbemobject-clone-.md).</span><span class="sxs-lookup"><span data-stu-id="7d65b-150">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span data-ttu-id="7d65b-151"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional \* \* \* \* (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="7d65b-151"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>\*\*\*\*wbemFlagBidirectional\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="7d65b-152">Hace que WMI conserve punteros a objetos de la enumeración hasta que el cliente libere el enumerador.</span><span class="sxs-lookup"><span data-stu-id="7d65b-152">Causes WMI to retain pointers to objects of the enumeration until the client releases the enumerator.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="7d65b-153"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="7d65b-153"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="7d65b-154">Hace que la llamada se devuelva inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="7d65b-154">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="7d65b-155"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* \* (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="7d65b-155"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="7d65b-156">Hace que esta llamada se bloquee hasta que se complete la consulta.</span><span class="sxs-lookup"><span data-stu-id="7d65b-156">Causes this call to block until the query has completed.</span></span> <span data-ttu-id="7d65b-157">Esta marca llama al método en modo sincrónico.</span><span class="sxs-lookup"><span data-stu-id="7d65b-157">This flag calls the method in synchronous mode.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="7d65b-158"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="7d65b-158"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="7d65b-159">Hace que WMI devuelva datos de modificación de clase junto con la definición de clase base.</span><span class="sxs-lookup"><span data-stu-id="7d65b-159">Causes WMI to return class amendment data along with the base class definition.</span></span> <span data-ttu-id="7d65b-160">Para obtener más información, consulte [localizar información de clase WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="7d65b-160">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="7d65b-161">*objwbemNamedValueSet* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="7d65b-161">*objwbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7d65b-162">Normalmente, esto no está definido.</span><span class="sxs-lookup"><span data-stu-id="7d65b-162">Typically, this is undefined.</span></span> <span data-ttu-id="7d65b-163">De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que atiende la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7d65b-163">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="7d65b-164">Un proveedor que admite o requiere tal información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.</span><span class="sxs-lookup"><span data-stu-id="7d65b-164">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d65b-165">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7d65b-165">Return value</span></span>

<span data-ttu-id="7d65b-166">Si la llamada se realiza correctamente, se devuelve un objeto [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="7d65b-166">If the call is successful, an [**SWbemObjectSet**](swbemobjectset.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7d65b-167">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="7d65b-167">Error codes</span></span>

<span data-ttu-id="7d65b-168">Después de completar el método **AssociatorsOf** , el objeto **Err** puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="7d65b-168">After the completion of the **AssociatorsOf** method, the **Err** object may contain one of the error codes in the following list.</span></span>

> [!Note]  
> <span data-ttu-id="7d65b-169">Una colección devuelta con cero elementos no es un error.</span><span class="sxs-lookup"><span data-stu-id="7d65b-169">A returned collection with zero elements is not an error.</span></span>

 

<dl> <dt>

<span data-ttu-id="7d65b-170">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="7d65b-170">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="7d65b-171">El usuario actual no tiene permiso para ver una o varias de las clases devueltas por la llamada.</span><span class="sxs-lookup"><span data-stu-id="7d65b-171">Current user does not have the permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="7d65b-172">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="7d65b-172">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="7d65b-173">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="7d65b-173">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="7d65b-174">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="7d65b-174">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="7d65b-175">Se especificó un parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="7d65b-175">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="7d65b-176">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="7d65b-176">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="7d65b-177">Memoria insuficiente para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="7d65b-177">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="7d65b-178">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="7d65b-178">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="7d65b-179">No se encontró el elemento solicitado.</span><span class="sxs-lookup"><span data-stu-id="7d65b-179">Requested item was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7d65b-180">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7d65b-180">Remarks</span></span>

<span data-ttu-id="7d65b-181">El método recupera las instancias de recursos administrados que están asociadas a un recurso especificado a través de una o varias clases de asociación.</span><span class="sxs-lookup"><span data-stu-id="7d65b-181">The method retrieves the instances of managed resources that are associated with a specified resource through one or more association classes.</span></span> <span data-ttu-id="7d65b-182">Proporcione la ruta de acceso del objeto para el punto de conexión de origen y AssociatorsOf devuelve los recursos administrados en el extremo opuesto.</span><span class="sxs-lookup"><span data-stu-id="7d65b-182">You provide the object path for the originating endpoint, and AssociatorsOf returns the managed resources at the opposite endpoint.</span></span> <span data-ttu-id="7d65b-183">El método AssociatorsOf realiza la misma función que realizan los asociados de la consulta WQL.</span><span class="sxs-lookup"><span data-stu-id="7d65b-183">The AssociatorsOf method performs the same function that the ASSOCIATORS OF WQL query performs.</span></span>

<span data-ttu-id="7d65b-184">Para obtener más información sobre los ASOCIAdores de la consulta WQL, las instancias de origen y los puntos de conexión, vea [ASSOCIATORS OF Statement](associators-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="7d65b-184">For more information about the ASSOCIATORS OF WQL query, source instances, and endpoints, see [ASSOCIATORS OF Statement](associators-of-statement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7d65b-185">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d65b-185">Requirements</span></span>



| <span data-ttu-id="7d65b-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d65b-186">Requirement</span></span> | <span data-ttu-id="7d65b-187">Value</span><span class="sxs-lookup"><span data-stu-id="7d65b-187">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d65b-188">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7d65b-188">Minimum supported client</span></span><br/> | <span data-ttu-id="7d65b-189">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7d65b-189">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7d65b-190">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7d65b-190">Minimum supported server</span></span><br/> | <span data-ttu-id="7d65b-191">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7d65b-191">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7d65b-192">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7d65b-192">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d65b-193"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d65b-193"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7d65b-194">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="7d65b-194">Type library</span></span><br/>             | <dl> <span data-ttu-id="7d65b-195"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7d65b-195"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7d65b-196">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7d65b-196">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d65b-197"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d65b-197"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7d65b-198">CLSID</span><span class="sxs-lookup"><span data-stu-id="7d65b-198">CLSID</span></span><br/>                    | <span data-ttu-id="7d65b-199">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="7d65b-199">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="7d65b-200">IID</span><span class="sxs-lookup"><span data-stu-id="7d65b-200">IID</span></span><br/>                      | <span data-ttu-id="7d65b-201">\_ISWBEMSERVICES IID</span><span class="sxs-lookup"><span data-stu-id="7d65b-201">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="7d65b-202">Vea también</span><span class="sxs-lookup"><span data-stu-id="7d65b-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d65b-203">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="7d65b-203">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="7d65b-204">**SWbemObject. ASSOCIATORS\_**</span><span class="sxs-lookup"><span data-stu-id="7d65b-204">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
</dt> <dt>

[<span data-ttu-id="7d65b-205">**SWbemObject.AssociatorsAsync\_**</span><span class="sxs-lookup"><span data-stu-id="7d65b-205">**SWbemObject.AssociatorsAsync\_**</span></span>](swbemobject-associatorsasync-.md)
</dt> <dt>

[<span data-ttu-id="7d65b-206">**SWbemServices. AssociatorsOfAsync**</span><span class="sxs-lookup"><span data-stu-id="7d65b-206">**SWbemServices.AssociatorsOfAsync**</span></span>](swbemservices-associatorsofasync.md)
</dt> <dt>

[<span data-ttu-id="7d65b-207">**SWbemObject. References\_**</span><span class="sxs-lookup"><span data-stu-id="7d65b-207">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
</dt> <dt>

[<span data-ttu-id="7d65b-208">**SWbemServices. References**</span><span class="sxs-lookup"><span data-stu-id="7d65b-208">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
</dt> </dl>

 

 




