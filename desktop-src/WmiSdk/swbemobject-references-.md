---
description: El método References \_ del objeto SWbemObject devuelve una colección de todas las clases o instancias de asociación que hacen referencia al objeto actual.
ms.assetid: ba02da47-0bb2-40e1-af50-1c42b4be2abd
ms.tgt_platform: multiple
title: Método SWbemObject.References_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.References_
- ISWbemObject.References_
- ISWbemObject.References_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3349ff104a5f0730ee99735a230d265fffd1333f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913205"
---
# <a name="swbemobjectreferences_-method"></a><span data-ttu-id="d22a1-103">SWbemObject. References ( \_ método)</span><span class="sxs-lookup"><span data-stu-id="d22a1-103">SWbemObject.References\_ method</span></span>

<span data-ttu-id="d22a1-104">El **método \_ References** del objeto [**SWbemObject**](swbemobject.md) devuelve una colección de todas las clases o instancias de asociación que hacen referencia al objeto actual.</span><span class="sxs-lookup"><span data-stu-id="d22a1-104">The **References\_** method of the [**SWbemObject**](swbemobject.md) object returns a collection of all association classes or instances that refer to the current object.</span></span>

<span data-ttu-id="d22a1-105">Este método realiza la misma función que las [referencias de](references-of-statement.md) la consulta WQL.</span><span class="sxs-lookup"><span data-stu-id="d22a1-105">This method performs the same function as the [REFERENCES OF](references-of-statement.md) WQL query.</span></span>

<span data-ttu-id="d22a1-106">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="d22a1-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d22a1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d22a1-107">Syntax</span></span>


```VB
objWbemObjectSet = .References_( _
  [ ByVal strResultClass ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="d22a1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d22a1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d22a1-109">*strResultClass* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="d22a1-109">*strResultClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d22a1-110">Cadena que contiene un nombre de clase.</span><span class="sxs-lookup"><span data-stu-id="d22a1-110">String that contains a class name.</span></span> <span data-ttu-id="d22a1-111">Si se especifica, este parámetro indica que los objetos de asociación devueltos deben pertenecer a la clase especificada en este parámetro o derivarse de ella.</span><span class="sxs-lookup"><span data-stu-id="d22a1-111">If specified, this parameter indicates that the returned association objects must belong to or be derived from the class specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="d22a1-112">*strRole* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="d22a1-112">*strRole* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d22a1-113">Cadena que contiene un nombre de propiedad.</span><span class="sxs-lookup"><span data-stu-id="d22a1-113">String that contains a property name.</span></span> <span data-ttu-id="d22a1-114">Si se especifica, este parámetro indica que los objetos de asociación devueltos se deben limitar a aquellos en los que el objeto de origen desempeña un rol específico.</span><span class="sxs-lookup"><span data-stu-id="d22a1-114">If specified, this parameter indicates that the returned association objects must be limited to those in which the source object plays a specific role.</span></span> <span data-ttu-id="d22a1-115">El rol se define mediante el nombre de una propiedad especificada (que debe ser una propiedad de referencia) de una asociación.</span><span class="sxs-lookup"><span data-stu-id="d22a1-115">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="d22a1-116">*bClassesOnly* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="d22a1-116">*bClassesOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d22a1-117">Valor booleano que indica si se debe devolver o no una lista de nombres de clase en lugar de instancias reales de las clases.</span><span class="sxs-lookup"><span data-stu-id="d22a1-117">Boolean value that indicates whether or not a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="d22a1-118">Estas son las clases a las que pertenecen los objetos de asociación.</span><span class="sxs-lookup"><span data-stu-id="d22a1-118">These are the classes to which the association objects belong.</span></span> <span data-ttu-id="d22a1-119">El valor predeterminado de este parámetro es **false**.</span><span class="sxs-lookup"><span data-stu-id="d22a1-119">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d22a1-120">*bSchemaOnly* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="d22a1-120">*bSchemaOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d22a1-121">Valor booleano que indica si la consulta se aplica o no al esquema en lugar de a los datos.</span><span class="sxs-lookup"><span data-stu-id="d22a1-121">Boolean value that indicates whether or not the query applies to the schema rather than the data.</span></span> <span data-ttu-id="d22a1-122">El valor predeterminado de este parámetro es **false**.</span><span class="sxs-lookup"><span data-stu-id="d22a1-122">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="d22a1-123">Solo se puede establecer en **true** si el objeto en el que se invoca este método es una clase.</span><span class="sxs-lookup"><span data-stu-id="d22a1-123">It can only be set to **TRUE** if the object on which this method is invoked is a class.</span></span> <span data-ttu-id="d22a1-124">Cuando se establece en **true**, el conjunto de extremos devueltos representa las clases que están asociadas adecuadamente a la clase de origen en el esquema.</span><span class="sxs-lookup"><span data-stu-id="d22a1-124">When set to **TRUE**, the set of returned endpoints represents classes that are suitably associated with the source class in the schema.</span></span>

</dd> <dt>

<span data-ttu-id="d22a1-125">*strRequiredQualifier* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="d22a1-125">*strRequiredQualifier* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d22a1-126">Cadena que contiene un nombre de calificador.</span><span class="sxs-lookup"><span data-stu-id="d22a1-126">String that contains a qualifier name.</span></span> <span data-ttu-id="d22a1-127">Si se especifica, este parámetro indica que los objetos de asociación devueltos deben incluir el calificador especificado.</span><span class="sxs-lookup"><span data-stu-id="d22a1-127">If specified, this parameter indicates that the returned association objects must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="d22a1-128">*iFlags* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="d22a1-128">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d22a1-129">Entero que especifica marcas adicionales para la operación.</span><span class="sxs-lookup"><span data-stu-id="d22a1-129">Integer specifying additional flags to the operation.</span></span> <span data-ttu-id="d22a1-130">El valor predeterminado para este parámetro es **wbemFlagReturnImmediately**, que dirige la llamada para que se devuelva inmediatamente en lugar de esperar hasta que se complete la consulta.</span><span class="sxs-lookup"><span data-stu-id="d22a1-130">The default for this parameter is **wbemFlagReturnImmediately**, which directs the call to return immediately rather than wait until the query has completed.</span></span> <span data-ttu-id="d22a1-131">Este parámetro puede aceptar los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="d22a1-131">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="d22a1-132"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="d22a1-132"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="d22a1-133">Hace que se devuelva un enumerador de solo avance.</span><span class="sxs-lookup"><span data-stu-id="d22a1-133">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="d22a1-134">Los enumeradores de solo avance suelen ser mucho más rápidos y usan menos memoria que los enumeradores convencionales, pero no permiten llamadas a [**SWbemObject. \_ Clone**](swbemobject-clone-.md).</span><span class="sxs-lookup"><span data-stu-id="d22a1-134">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span data-ttu-id="d22a1-135"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional \* \* \* \* (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="d22a1-135"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>\*\*\*\*wbemFlagBidirectional\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="d22a1-136">Hace que Instrumental de administración de Windows (WMI) Conserve punteros a objetos de la enumeración hasta que el cliente libere el enumerador.</span><span class="sxs-lookup"><span data-stu-id="d22a1-136">Causes Windows Management Instrumentation (WMI) to retain pointers to objects of the enumeration until the client releases the enumerator.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="d22a1-137"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="d22a1-137"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="d22a1-138">Hace que la llamada se devuelva inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="d22a1-138">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="d22a1-139"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* \* (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="d22a1-139"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="d22a1-140">Hace que esta llamada se bloquee hasta que se complete la consulta.</span><span class="sxs-lookup"><span data-stu-id="d22a1-140">Causes this call to block until the query has completed.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="d22a1-141"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="d22a1-141"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="d22a1-142">Hace que WMI devuelva datos de modificación de clase con la definición de clase base.</span><span class="sxs-lookup"><span data-stu-id="d22a1-142">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="d22a1-143">Para obtener más información acerca de los calificadores modificados, consulte [localizar información de clase WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="d22a1-143">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d22a1-144">*objwbemNamedValueSet* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="d22a1-144">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d22a1-145">Normalmente, esto no está definido.</span><span class="sxs-lookup"><span data-stu-id="d22a1-145">Typically, this is undefined.</span></span> <span data-ttu-id="d22a1-146">De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que atiende la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d22a1-146">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="d22a1-147">Un proveedor que admite o requiere tal información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.</span><span class="sxs-lookup"><span data-stu-id="d22a1-147">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d22a1-148">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d22a1-148">Return value</span></span>

<span data-ttu-id="d22a1-149">Si la llamada se realiza correctamente, se devuelve un objeto [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="d22a1-149">If the call is successful, an [**SWbemObjectSet**](swbemobjectset.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d22a1-150">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="d22a1-150">Error codes</span></span>

<span data-ttu-id="d22a1-151">Después de completar el método **References \_** , el objeto **Err** puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="d22a1-151">After the completion of the **References\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="d22a1-152">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="d22a1-152">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="d22a1-153">El usuario actual no tiene permiso para ver una o varias de las clases devueltas por la llamada.</span><span class="sxs-lookup"><span data-stu-id="d22a1-153">Current user does not have permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="d22a1-154">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="d22a1-154">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="d22a1-155">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="d22a1-155">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="d22a1-156">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="d22a1-156">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="d22a1-157">Se especificó un parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="d22a1-157">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="d22a1-158">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="d22a1-158">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="d22a1-159">Memoria insuficiente para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="d22a1-159">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d22a1-160">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d22a1-160">Remarks</span></span>

<span data-ttu-id="d22a1-161">Para obtener más información sobre las referencias de la consulta WQL asociada, las instancias de origen y los objetos de asociación, vea [ASSOCIATORS OF Statement](associators-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="d22a1-161">For more information about the REFERENCES OF associated WQL query, source instances, and association objects, see [ASSOCIATORS OF Statement](associators-of-statement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d22a1-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d22a1-162">Requirements</span></span>



| <span data-ttu-id="d22a1-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="d22a1-163">Requirement</span></span> | <span data-ttu-id="d22a1-164">Value</span><span class="sxs-lookup"><span data-stu-id="d22a1-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d22a1-165">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d22a1-165">Minimum supported client</span></span><br/> | <span data-ttu-id="d22a1-166">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d22a1-166">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d22a1-167">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d22a1-167">Minimum supported server</span></span><br/> | <span data-ttu-id="d22a1-168">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d22a1-168">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d22a1-169">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d22a1-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="d22a1-170"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d22a1-170"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d22a1-171">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d22a1-171">Type library</span></span><br/>             | <dl> <span data-ttu-id="d22a1-172"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d22a1-172"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d22a1-173">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d22a1-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d22a1-174"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d22a1-174"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d22a1-175">CLSID</span><span class="sxs-lookup"><span data-stu-id="d22a1-175">CLSID</span></span><br/>                    | <span data-ttu-id="d22a1-176">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="d22a1-176">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="d22a1-177">IID</span><span class="sxs-lookup"><span data-stu-id="d22a1-177">IID</span></span><br/>                      | <span data-ttu-id="d22a1-178">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="d22a1-178">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="d22a1-179">Vea también</span><span class="sxs-lookup"><span data-stu-id="d22a1-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d22a1-180">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="d22a1-180">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="d22a1-181">**SWbemObject. ASSOCIATORS\_**</span><span class="sxs-lookup"><span data-stu-id="d22a1-181">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
</dt> <dt>

[<span data-ttu-id="d22a1-182">**SWbemServices. AssociatorsOf**</span><span class="sxs-lookup"><span data-stu-id="d22a1-182">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-associatorsof.md)
</dt> <dt>

[<span data-ttu-id="d22a1-183">**SWbemServices. References**</span><span class="sxs-lookup"><span data-stu-id="d22a1-183">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
</dt> </dl>

 

 




