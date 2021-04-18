---
description: La \_ clase de error CIM contiene información sobre el error de una operación CIM.
ms.assetid: 35acecbd-b972-45b4-9616-2047bba8fd41
title: CIM_Error (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Error
- CIM_Error.ErrorType
- CIM_Error.OtherErrorType
- CIM_Error.OwningEntity
- CIM_Error.MessageID
- CIM_Error.Message
- CIM_Error.MessageArguments
- CIM_Error.PerceivedSeverity
- CIM_Error.ProbableCause
- CIM_Error.ProbableCauseDescription
- CIM_Error.RecommendedActions
- CIM_Error.ErrorSource
- CIM_Error.ErrorSourceFormat
- CIM_Error.OtherErrorSourceFormat
- CIM_Error.CIMStatusCode
- CIM_Error.CIMStatusCodeDescription
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 59ae2527478235c14a8f856319178afe00c02a98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360128"
---
# <a name="cim_error-class"></a><span data-ttu-id="1415f-103">CIM ( \_ clase de error)</span><span class="sxs-lookup"><span data-stu-id="1415f-103">CIM\_Error class</span></span>

<span data-ttu-id="1415f-104">La clase de **\_ error CIM** contiene información sobre el error de una operación CIM.</span><span class="sxs-lookup"><span data-stu-id="1415f-104">The **CIM\_Error** class contains information about the failure of a CIM operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="1415f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1415f-105">Syntax</span></span>

``` syntax
[Indication, Abstract, Version("2.22.1"), Exception, UMLPackagePath("CIM::Interop"), AMENDMENT]
class CIM_Error
{
  uint16 ErrorType;
  string OtherErrorType;
  string OwningEntity;
  string MessageID;
  string Message;
  string MessageArguments[];
  uint16 PerceivedSeverity;
  uint16 ProbableCause;
  string ProbableCauseDescription;
  string RecommendedActions[];
  string ErrorSource;
  uint16 ErrorSourceFormat = 0;
  string OtherErrorSourceFormat;
  uint32 CIMStatusCode;
  string CIMStatusCodeDescription;
};
```

## <a name="members"></a><span data-ttu-id="1415f-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="1415f-106">Members</span></span>

<span data-ttu-id="1415f-107">La clase de **\_ error CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1415f-107">The **CIM\_Error** class has these types of members:</span></span>

-   [<span data-ttu-id="1415f-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1415f-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1415f-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1415f-109">Properties</span></span>

<span data-ttu-id="1415f-110">La clase de **\_ error CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1415f-110">The **CIM\_Error** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1415f-111">**CIMStatusCode**</span><span class="sxs-lookup"><span data-stu-id="1415f-111">**CIMStatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1415f-112">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1415f-112">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1415f-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1415f-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1415f-114">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DSP0201. ERROR de DMTF \| . CÓDIGO \| 2,3 "," DSP0200. DMTF \| CIMError \| 1,3 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ error de CIM**.**CIMStatusCodeDescription**")</span><span class="sxs-lookup"><span data-stu-id="1415f-114">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DSP0201.DMTF\|ERROR.CODE\|2.3", "DSP0200.DMTF\|CIMError\|1.3"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**CIMStatusCodeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="1415f-115">El código de estado de CIM que caracteriza esta instancia.</span><span class="sxs-lookup"><span data-stu-id="1415f-115">The CIM status code that characterizes this instance.</span></span> <span data-ttu-id="1415f-116">Esta propiedad define los códigos de estado que puede devolver un servidor CIM o un agente de escucha.</span><span class="sxs-lookup"><span data-stu-id="1415f-116">This property defines the status codes that can be return by a CIM server or listener.</span></span>

<dt>

<span id="CIM_ERR_FAILED"></span><span id="cim_err_failed"></span>

<span data-ttu-id="1415f-117"><span id="CIM_ERR_FAILED"></span><span id="cim_err_failed"></span>**CIM \_ \_Error de Err** (1)</span><span class="sxs-lookup"><span data-stu-id="1415f-117"><span id="CIM_ERR_FAILED"></span><span id="cim_err_failed"></span>**CIM\_ERR\_FAILED** (1)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-118">Se produjo un error general que no está incluido en un código de error más específico.</span><span class="sxs-lookup"><span data-stu-id="1415f-118">A general error occurred that is not covered by a more specific error code.</span></span>

</dd> <dt>

<span id="CIM_ERR_ACCESS_DENIED"></span><span id="cim_err_access_denied"></span>

<span data-ttu-id="1415f-119"><span id="CIM_ERR_ACCESS_DENIED"></span><span id="cim_err_access_denied"></span>**CIM \_ ERROR de \_ acceso \_ denegado** (2)</span><span class="sxs-lookup"><span data-stu-id="1415f-119"><span id="CIM_ERR_ACCESS_DENIED"></span><span id="cim_err_access_denied"></span>**CIM\_ERR\_ACCESS\_DENIED** (2)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-120">El acceso a un recurso CIM no estaba disponible para el cliente.</span><span class="sxs-lookup"><span data-stu-id="1415f-120">Access to a CIM resource was not available to the client.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_NAMESPACE"></span><span id="cim_err_invalid_namespace"></span>

<span data-ttu-id="1415f-121"><span id="CIM_ERR_INVALID_NAMESPACE"></span><span id="cim_err_invalid_namespace"></span>**CIM \_ ERROR \_ de \_ espacio de nombres no válido** (3)</span><span class="sxs-lookup"><span data-stu-id="1415f-121"><span id="CIM_ERR_INVALID_NAMESPACE"></span><span id="cim_err_invalid_namespace"></span>**CIM\_ERR\_INVALID\_NAMESPACE** (3)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-122">El espacio de nombres de destino no existe.</span><span class="sxs-lookup"><span data-stu-id="1415f-122">The target namespace does not exist.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_PARAMETER"></span><span id="cim_err_invalid_parameter"></span>

<span data-ttu-id="1415f-123"><span id="CIM_ERR_INVALID_PARAMETER"></span><span id="cim_err_invalid_parameter"></span>**CIM \_ ERROR \_ de \_ parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="1415f-123"><span id="CIM_ERR_INVALID_PARAMETER"></span><span id="cim_err_invalid_parameter"></span>**CIM\_ERR\_INVALID\_PARAMETER** (4)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-124">Uno o varios valores de parámetro pasados al método no eran válidos.</span><span class="sxs-lookup"><span data-stu-id="1415f-124">One or more parameter values passed to the method were invalid.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_CLASS"></span><span id="cim_err_invalid_class"></span>

<span data-ttu-id="1415f-125"><span id="CIM_ERR_INVALID_CLASS"></span><span id="cim_err_invalid_class"></span>**CIM \_ ERR \_ ( \_ clase no válida** ) (5)</span><span class="sxs-lookup"><span data-stu-id="1415f-125"><span id="CIM_ERR_INVALID_CLASS"></span><span id="cim_err_invalid_class"></span>**CIM\_ERR\_INVALID\_CLASS** (5)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-126">La clase especificada no existe.</span><span class="sxs-lookup"><span data-stu-id="1415f-126">The specified Class does not exist.</span></span>

</dd> <dt>

<span id="CIM_ERR_NOT_FOUND"></span><span id="cim_err_not_found"></span>

<span data-ttu-id="1415f-127"><span id="CIM_ERR_NOT_FOUND"></span><span id="cim_err_not_found"></span>**CIM \_ \_No \_ se encontró el error** (6)</span><span class="sxs-lookup"><span data-stu-id="1415f-127"><span id="CIM_ERR_NOT_FOUND"></span><span id="cim_err_not_found"></span>**CIM\_ERR\_NOT\_FOUND** (6)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-128">No se encontró el objeto solicitado.</span><span class="sxs-lookup"><span data-stu-id="1415f-128">The requested object could not be found.</span></span>

</dd> <dt>

<span id="CIM_ERR_NOT_SUPPORTED"></span><span id="cim_err_not_supported"></span>

<span data-ttu-id="1415f-129"><span id="CIM_ERR_NOT_SUPPORTED"></span><span id="cim_err_not_supported"></span>**CIM \_ \_No se \_ admite el error** (7)</span><span class="sxs-lookup"><span data-stu-id="1415f-129"><span id="CIM_ERR_NOT_SUPPORTED"></span><span id="cim_err_not_supported"></span>**CIM\_ERR\_NOT\_SUPPORTED** (7)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-130">No se admite la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="1415f-130">The requested operation is not supported.</span></span>

</dd> <dt>

<span id="CIM_ERR_CLASS_HAS_CHILDREN"></span><span id="cim_err_class_has_children"></span>

<span data-ttu-id="1415f-131"><span id="CIM_ERR_CLASS_HAS_CHILDREN"></span><span id="cim_err_class_has_children"></span>**CIM \_ La \_ clase Err \_ tiene \_ elementos secundarios** (8)</span><span class="sxs-lookup"><span data-stu-id="1415f-131"><span id="CIM_ERR_CLASS_HAS_CHILDREN"></span><span id="cim_err_class_has_children"></span>**CIM\_ERR\_CLASS\_HAS\_CHILDREN** (8)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-132">No se puede realizar la operación en esta clase porque tiene instancias.</span><span class="sxs-lookup"><span data-stu-id="1415f-132">Operation cannot be carried out on this class since it has instances.</span></span>

</dd> <dt>

<span id="CIM_ERR_CLASS_HAS_INSTANCES"></span><span id="cim_err_class_has_instances"></span>

<span data-ttu-id="1415f-133"><span id="CIM_ERR_CLASS_HAS_INSTANCES"></span><span id="cim_err_class_has_instances"></span>**CIM \_ La \_ clase Err \_ tiene \_ instancias** (9)</span><span class="sxs-lookup"><span data-stu-id="1415f-133"><span id="CIM_ERR_CLASS_HAS_INSTANCES"></span><span id="cim_err_class_has_instances"></span>**CIM\_ERR\_CLASS\_HAS\_INSTANCES** (9)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-134">No se puede realizar la operación en esta clase porque tiene instancias.</span><span class="sxs-lookup"><span data-stu-id="1415f-134">Operation cannot be carried out on this class since it has instances.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_SUPERCLASS"></span><span id="cim_err_invalid_superclass"></span>

<span data-ttu-id="1415f-135"><span id="CIM_ERR_INVALID_SUPERCLASS"></span><span id="cim_err_invalid_superclass"></span>**CIM \_ ERROR \_ de \_ superclase no válida** (10)</span><span class="sxs-lookup"><span data-stu-id="1415f-135"><span id="CIM_ERR_INVALID_SUPERCLASS"></span><span id="cim_err_invalid_superclass"></span>**CIM\_ERR\_INVALID\_SUPERCLASS** (10)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-136">No se puede realizar la operación porque la superclase especificada no existe.</span><span class="sxs-lookup"><span data-stu-id="1415f-136">Operation cannot be carried out since the specified superclass does not exist.</span></span>

</dd> <dt>

<span id="CIM_ERR_ALREADY_EXISTS"></span><span id="cim_err_already_exists"></span>

<span data-ttu-id="1415f-137"><span id="CIM_ERR_ALREADY_EXISTS"></span><span id="cim_err_already_exists"></span>**CIM \_ ERR \_ ya \_ existe** (11)</span><span class="sxs-lookup"><span data-stu-id="1415f-137"><span id="CIM_ERR_ALREADY_EXISTS"></span><span id="cim_err_already_exists"></span>**CIM\_ERR\_ALREADY\_EXISTS** (11)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-138">No se puede realizar la operación porque ya existe un objeto.</span><span class="sxs-lookup"><span data-stu-id="1415f-138">Operation cannot be carried out because an object already exists.</span></span>

</dd> <dt>

<span id="CIM_ERR_NO_SUCH_PROPERTY"></span><span id="cim_err_no_such_property"></span>

<span data-ttu-id="1415f-139"><span id="CIM_ERR_NO_SUCH_PROPERTY"></span><span id="cim_err_no_such_property"></span>**CIM \_ NO se trata de una \_ \_ \_ propiedad de este tipo** (12)</span><span class="sxs-lookup"><span data-stu-id="1415f-139"><span id="CIM_ERR_NO_SUCH_PROPERTY"></span><span id="cim_err_no_such_property"></span>**CIM\_ERR\_NO\_SUCH\_PROPERTY** (12)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-140">La propiedad especificada no existe.</span><span class="sxs-lookup"><span data-stu-id="1415f-140">The specified Property does not exist.</span></span>

</dd> <dt>

<span id="CIM_ERR_TYPE_MISMATCH"></span><span id="cim_err_type_mismatch"></span>

<span data-ttu-id="1415f-141"><span id="CIM_ERR_TYPE_MISMATCH"></span><span id="cim_err_type_mismatch"></span>**CIM \_ ERROR \_ de \_ coincidencia de tipos** (13)</span><span class="sxs-lookup"><span data-stu-id="1415f-141"><span id="CIM_ERR_TYPE_MISMATCH"></span><span id="cim_err_type_mismatch"></span>**CIM\_ERR\_TYPE\_MISMATCH** (13)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-142">El valor proporcionado no es compatible con el tipo.</span><span class="sxs-lookup"><span data-stu-id="1415f-142">The value supplied is incompatible with the type.</span></span>

</dd> <dt>

<span id="CIM_ERR_QUERY_LANGUAGE_NOT_SUPPORTED"></span><span id="cim_err_query_language_not_supported"></span>

<span data-ttu-id="1415f-143"><span id="CIM_ERR_QUERY_LANGUAGE_NOT_SUPPORTED"></span><span id="cim_err_query_language_not_supported"></span>**CIM \_ \_No se \_ \_ \_ admite el lenguaje de consulta de Err** (14)</span><span class="sxs-lookup"><span data-stu-id="1415f-143"><span id="CIM_ERR_QUERY_LANGUAGE_NOT_SUPPORTED"></span><span id="cim_err_query_language_not_supported"></span>**CIM\_ERR\_QUERY\_LANGUAGE\_NOT\_SUPPORTED** (14)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-144">No se reconoce o no se admite el lenguaje de consulta.</span><span class="sxs-lookup"><span data-stu-id="1415f-144">The query language is not recognized or supported.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_QUERY"></span><span id="cim_err_invalid_query"></span>

<span data-ttu-id="1415f-145"><span id="CIM_ERR_INVALID_QUERY"></span><span id="cim_err_invalid_query"></span>**CIM \_ ERROR \_ de \_ consulta no válida** (15)</span><span class="sxs-lookup"><span data-stu-id="1415f-145"><span id="CIM_ERR_INVALID_QUERY"></span><span id="cim_err_invalid_query"></span>**CIM\_ERR\_INVALID\_QUERY** (15)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-146">La consulta no es válida para el lenguaje de consulta especificado.</span><span class="sxs-lookup"><span data-stu-id="1415f-146">The query is not valid for the specified query language.</span></span>

</dd> <dt>

<span id="CIM_ERR_METHOD_NOT_AVAILABLE"></span><span id="cim_err_method_not_available"></span>

<span data-ttu-id="1415f-147"><span id="CIM_ERR_METHOD_NOT_AVAILABLE"></span><span id="cim_err_method_not_available"></span>**CIM \_ \_Método Err \_ no \_ disponible** (16)</span><span class="sxs-lookup"><span data-stu-id="1415f-147"><span id="CIM_ERR_METHOD_NOT_AVAILABLE"></span><span id="cim_err_method_not_available"></span>**CIM\_ERR\_METHOD\_NOT\_AVAILABLE** (16)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-148">No se pudo ejecutar el método extrínseco.</span><span class="sxs-lookup"><span data-stu-id="1415f-148">The extrinsic Method could not be executed.</span></span>

</dd> <dt>

<span id="CIM_ERR_METHOD_NOT_FOUND"></span><span id="cim_err_method_not_found"></span>

<span data-ttu-id="1415f-149"><span id="CIM_ERR_METHOD_NOT_FOUND"></span><span id="cim_err_method_not_found"></span>**CIM \_ \_ \_ No \_ se encontró el método Err** (17)</span><span class="sxs-lookup"><span data-stu-id="1415f-149"><span id="CIM_ERR_METHOD_NOT_FOUND"></span><span id="cim_err_method_not_found"></span>**CIM\_ERR\_METHOD\_NOT\_FOUND** (17)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-150">El método extrínseco especificado no existe.</span><span class="sxs-lookup"><span data-stu-id="1415f-150">The specified extrinsic Method does not exist.</span></span>

</dd> <dt>

<span id="CIM_ERR_UNEXPECTED_RESPONSE"></span><span id="cim_err_unexpected_response"></span>

<span data-ttu-id="1415f-151"><span id="CIM_ERR_UNEXPECTED_RESPONSE"></span><span id="cim_err_unexpected_response"></span>**CIM \_ ERROR \_ de \_ respuesta inesperada** (18)</span><span class="sxs-lookup"><span data-stu-id="1415f-151"><span id="CIM_ERR_UNEXPECTED_RESPONSE"></span><span id="cim_err_unexpected_response"></span>**CIM\_ERR\_UNEXPECTED\_RESPONSE** (18)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-152">No se esperaba la respuesta devuelta a la operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="1415f-152">The returned response to the asynchronous operation was not expected.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_RESPONSE_DESTINATION"></span><span id="cim_err_invalid_response_destination"></span>

<span data-ttu-id="1415f-153"><span id="CIM_ERR_INVALID_RESPONSE_DESTINATION"></span><span id="cim_err_invalid_response_destination"></span>**CIM \_ ERROR \_ de \_ \_ destino de respuesta no válido** (19)</span><span class="sxs-lookup"><span data-stu-id="1415f-153"><span id="CIM_ERR_INVALID_RESPONSE_DESTINATION"></span><span id="cim_err_invalid_response_destination"></span>**CIM\_ERR\_INVALID\_RESPONSE\_DESTINATION** (19)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-154">El destino especificado para la respuesta asincrónica no es válido.</span><span class="sxs-lookup"><span data-stu-id="1415f-154">The specified destination for the asynchronous response is not valid.</span></span>

</dd> <dt>

<span id="CIM_ERR_NAMESPACE_NOT_EMPTY"></span><span id="cim_err_namespace_not_empty"></span>

<span data-ttu-id="1415f-155"><span id="CIM_ERR_NAMESPACE_NOT_EMPTY"></span><span id="cim_err_namespace_not_empty"></span>**CIM \_ El \_ espacio de nombres Err \_ no \_ está vacío** (20)</span><span class="sxs-lookup"><span data-stu-id="1415f-155"><span id="CIM_ERR_NAMESPACE_NOT_EMPTY"></span><span id="cim_err_namespace_not_empty"></span>**CIM\_ERR\_NAMESPACE\_NOT\_EMPTY** (20)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-156">El espacio de nombres especificado no está vacío.</span><span class="sxs-lookup"><span data-stu-id="1415f-156">The specified Namespace is not empty.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_ENUMERATION_CONTEXT"></span><span id="cim_err_invalid_enumeration_context"></span>

<span data-ttu-id="1415f-157"><span id="CIM_ERR_INVALID_ENUMERATION_CONTEXT"></span><span id="cim_err_invalid_enumeration_context"></span>**CIM \_ ERROR en el \_ \_ \_ contexto de enumeración no válido** (21)</span><span class="sxs-lookup"><span data-stu-id="1415f-157"><span id="CIM_ERR_INVALID_ENUMERATION_CONTEXT"></span><span id="cim_err_invalid_enumeration_context"></span>**CIM\_ERR\_INVALID\_ENUMERATION\_CONTEXT** (21)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-158">El contexto de enumeración proporcionado no es válido.</span><span class="sxs-lookup"><span data-stu-id="1415f-158">The enumeration context supplied is not valid.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_OPERATION_TIMEOUT"></span><span id="cim_err_invalid_operation_timeout"></span>

<span data-ttu-id="1415f-159"><span id="CIM_ERR_INVALID_OPERATION_TIMEOUT"></span><span id="cim_err_invalid_operation_timeout"></span>**CIM \_ ERROR \_ de \_ tiempo de \_ espera de operación no válida** (22)</span><span class="sxs-lookup"><span data-stu-id="1415f-159"><span id="CIM_ERR_INVALID_OPERATION_TIMEOUT"></span><span id="cim_err_invalid_operation_timeout"></span>**CIM\_ERR\_INVALID\_OPERATION\_TIMEOUT** (22)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-160">El espacio de nombres especificado no está vacío.</span><span class="sxs-lookup"><span data-stu-id="1415f-160">The specified Namespace is not empty.</span></span>

</dd> <dt>

<span id="CIM_ERR_PULL_HAS_BEEN_ABANDONED"></span><span id="cim_err_pull_has_been_abandoned"></span>

<span data-ttu-id="1415f-161"><span id="CIM_ERR_PULL_HAS_BEEN_ABANDONED"></span><span id="cim_err_pull_has_been_abandoned"></span>**CIM \_ Se \_ ha \_ \_ \_ abandonado la extracción de Err** (23)</span><span class="sxs-lookup"><span data-stu-id="1415f-161"><span id="CIM_ERR_PULL_HAS_BEEN_ABANDONED"></span><span id="cim_err_pull_has_been_abandoned"></span>**CIM\_ERR\_PULL\_HAS\_BEEN\_ABANDONED** (23)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-162">El espacio de nombres especificado no está vacío.</span><span class="sxs-lookup"><span data-stu-id="1415f-162">The specified Namespace is not empty.</span></span>

</dd> <dt>

<span id="CIM_ERR_PULL_CANNOT_BE_ABANDONED"></span><span id="cim_err_pull_cannot_be_abandoned"></span>

<span data-ttu-id="1415f-163"><span id="CIM_ERR_PULL_CANNOT_BE_ABANDONED"></span><span id="cim_err_pull_cannot_be_abandoned"></span>**CIM \_ \_ \_ No se puede \_ \_ abandonar la extracción de Err** (24)</span><span class="sxs-lookup"><span data-stu-id="1415f-163"><span id="CIM_ERR_PULL_CANNOT_BE_ABANDONED"></span><span id="cim_err_pull_cannot_be_abandoned"></span>**CIM\_ERR\_PULL\_CANNOT\_BE\_ABANDONED** (24)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-164">Error al intentar abandonar una operación de extracción.</span><span class="sxs-lookup"><span data-stu-id="1415f-164">The attempt to abandon a pull operation has failed.</span></span>

</dd> <dt>

<span id="CIM_ERR_FILTERED_ENUMERATION_NOT_SUPPORTED"></span><span id="cim_err_filtered_enumeration_not_supported"></span>

<span data-ttu-id="1415f-165"><span id="CIM_ERR_FILTERED_ENUMERATION_NOT_SUPPORTED"></span><span id="cim_err_filtered_enumeration_not_supported"></span>**CIM \_ \_ \_ No se \_ \_ admite la enumeración filtrada de Err** (25)</span><span class="sxs-lookup"><span data-stu-id="1415f-165"><span id="CIM_ERR_FILTERED_ENUMERATION_NOT_SUPPORTED"></span><span id="cim_err_filtered_enumeration_not_supported"></span>**CIM\_ERR\_FILTERED\_ENUMERATION\_NOT\_SUPPORTED** (25)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-166">No se admiten los Enumeratrions filtrados.</span><span class="sxs-lookup"><span data-stu-id="1415f-166">Filtered Enumeratrions are not supported.</span></span>

</dd> <dt>

<span id="CIM_ERR_CONTINUATION_ON_ERROR_NOT_SUPPORTED"></span><span id="cim_err_continuation_on_error_not_supported"></span>

<span data-ttu-id="1415f-167"><span id="CIM_ERR_CONTINUATION_ON_ERROR_NOT_SUPPORTED"></span><span id="cim_err_continuation_on_error_not_supported"></span>**CIM \_ \_No se \_ \_ \_ \_ admite la continuación de Err en el error** (26)</span><span class="sxs-lookup"><span data-stu-id="1415f-167"><span id="CIM_ERR_CONTINUATION_ON_ERROR_NOT_SUPPORTED"></span><span id="cim_err_continuation_on_error_not_supported"></span>**CIM\_ERR\_CONTINUATION\_ON\_ERROR\_NOT\_SUPPORTED** (26)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-168">No se admite continuar después de un error.</span><span class="sxs-lookup"><span data-stu-id="1415f-168">Continue on error is not supported.</span></span>

</dd> <dt>

<span id="CIM_ERR_SERVER_LIMITS_EXCEEDED"></span><span id="cim_err_server_limits_exceeded"></span>

<span data-ttu-id="1415f-169"><span id="CIM_ERR_SERVER_LIMITS_EXCEEDED"></span><span id="cim_err_server_limits_exceeded"></span>**CIM \_ Se \_ han \_ \_ superado los límites de servidor de Err** (27)</span><span class="sxs-lookup"><span data-stu-id="1415f-169"><span id="CIM_ERR_SERVER_LIMITS_EXCEEDED"></span><span id="cim_err_server_limits_exceeded"></span>**CIM\_ERR\_SERVER\_LIMITS\_EXCEEDED** (27)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-170">Se han superado los límites del servidor WBEM (por ejemplo, memoria, conexiones, etc.).</span><span class="sxs-lookup"><span data-stu-id="1415f-170">The WBEM Server limits have been exceeded (e.g. memory, connections, ...).</span></span>

</dd> <dt>

<span id="CIM_ERR_SERVER_IS_SHUTTING_DOWN"></span><span id="cim_err_server_is_shutting_down"></span>

<span data-ttu-id="1415f-171"><span id="CIM_ERR_SERVER_IS_SHUTTING_DOWN"></span><span id="cim_err_server_is_shutting_down"></span>**CIM \_ El \_ servidor de Err \_ se está \_ cerrando \_** (28)</span><span class="sxs-lookup"><span data-stu-id="1415f-171"><span id="CIM_ERR_SERVER_IS_SHUTTING_DOWN"></span><span id="cim_err_server_is_shutting_down"></span>**CIM\_ERR\_SERVER\_IS\_SHUTTING\_DOWN** (28)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-172">El servidor WBEM se está cerrando.</span><span class="sxs-lookup"><span data-stu-id="1415f-172">The WBEM Server is shutting down.</span></span>

</dd> <dt>

<span id="CIM_ERR_QUERY_FEATURE_NOT_SUPPORTED"></span><span id="cim_err_query_feature_not_supported"></span>

<span data-ttu-id="1415f-173"><span id="CIM_ERR_QUERY_FEATURE_NOT_SUPPORTED"></span><span id="cim_err_query_feature_not_supported"></span>**CIM \_ \_No se \_ \_ \_ admite la característica de consulta Err** (29)</span><span class="sxs-lookup"><span data-stu-id="1415f-173"><span id="CIM_ERR_QUERY_FEATURE_NOT_SUPPORTED"></span><span id="cim_err_query_feature_not_supported"></span>**CIM\_ERR\_QUERY\_FEATURE\_NOT\_SUPPORTED** (29)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-174">No se admite la característica de consulta especificada.</span><span class="sxs-lookup"><span data-stu-id="1415f-174">The specified Query Feature is not supported.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="1415f-175"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="1415f-175"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1415f-176">**CIMStatusCodeDescription**</span><span class="sxs-lookup"><span data-stu-id="1415f-176">**CIMStatusCodeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1415f-177">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1415f-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1415f-178">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1415f-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1415f-179">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DSP0201. ERROR de DMTF \| . Descripción \| 2,3 "," DSP0200. DMTF \| CIMError \| 1,3 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ error de CIM**.**CIMStatusCode**")</span><span class="sxs-lookup"><span data-stu-id="1415f-179">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DSP0201.DMTF\|ERROR.DESCRIPTION\|2.3", "DSP0200.DMTF\|CIMError\|1.3"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**CIMStatusCode**")</span></span>
</dt> </dl>

<span data-ttu-id="1415f-180">Cadena de forma libre que contiene una descripción inteligible del valor de la propiedad **CIMStatusCode** .</span><span class="sxs-lookup"><span data-stu-id="1415f-180">A free-form string that contains a human-readable description of the **CIMStatusCode** property value.</span></span>

> [!Note]  
> <span data-ttu-id="1415f-181">Esta descripción puede extenderse, pero debe ser coherente con la definición de **CIMStatusCode**.</span><span class="sxs-lookup"><span data-stu-id="1415f-181">This description may extend, but must be consistent with the definition of **CIMStatusCode**.</span></span>

 

</dd> <dt>

<span data-ttu-id="1415f-182">**ErrorSource**</span><span class="sxs-lookup"><span data-stu-id="1415f-182">**ErrorSource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1415f-183">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1415f-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1415f-184">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1415f-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1415f-185">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ error de CIM**.**ErrorSourceFormat**")</span><span class="sxs-lookup"><span data-stu-id="1415f-185">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**ErrorSourceFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="1415f-186">Información que identifica la entidad que generó el error.</span><span class="sxs-lookup"><span data-stu-id="1415f-186">Information that identifies the entity that generated the error.</span></span> <span data-ttu-id="1415f-187">Si el esquema CIM modela la entidad, esta propiedad contiene la ruta de acceso a la instancia codificada como un parámetro de cadena.</span><span class="sxs-lookup"><span data-stu-id="1415f-187">If the entity is modeled by the CIM Schema, this property contains the path to the instance encoded as a string parameter.</span></span> <span data-ttu-id="1415f-188">De lo contrario, la propiedad contiene una cadena que asigna un nombre a la entidad que generó el error.</span><span class="sxs-lookup"><span data-stu-id="1415f-188">Otherwise, the property contains a string that names the entity that generated the error.</span></span> <span data-ttu-id="1415f-189">El formato de esta propiedad se especifica mediante la propiedad **ErrorSourceFormat** .</span><span class="sxs-lookup"><span data-stu-id="1415f-189">The format of this property is specified by the **ErrorSourceFormat** property.</span></span>

</dd> <dt>

<span data-ttu-id="1415f-190">**ErrorSourceFormat**</span><span class="sxs-lookup"><span data-stu-id="1415f-190">**ErrorSourceFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1415f-191">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1415f-191">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1415f-192">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1415f-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1415f-193">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ error de CIM**.**ErrorSource**","**\_ error de CIM**.**OtherErrorSourceFormat**")</span><span class="sxs-lookup"><span data-stu-id="1415f-193">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**ErrorSource**", "**CIM\_Error**.**OtherErrorSourceFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="1415f-194">Formato de la propiedad **ErrorSource** .</span><span class="sxs-lookup"><span data-stu-id="1415f-194">The format of the **ErrorSource** property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1415f-195"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="1415f-195"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-196">Una aplicación cliente CIM no reconoce el formato o lo interpreta de forma significativa.</span><span class="sxs-lookup"><span data-stu-id="1415f-196">The format is unknown or not meaningfully interpretable by a CIM client application.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1415f-197"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="1415f-197"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-198">El formato se define mediante el valor de la propiedad **OtherErrorSourceFormat** .</span><span class="sxs-lookup"><span data-stu-id="1415f-198">The format is defined by the value of the **OtherErrorSourceFormat** property.</span></span>

</dd> <dt>

<span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>

<span data-ttu-id="1415f-199"><span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2)</span><span class="sxs-lookup"><span data-stu-id="1415f-199"><span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-200">Una ruta de acceso de objeto CIM tal y como se define en la especificación de infraestructura CIM.</span><span class="sxs-lookup"><span data-stu-id="1415f-200">A CIM Object Path as defined in the CIM Infrastructure specification.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="1415f-201"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="1415f-201"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1415f-202">**ErrorType**</span><span class="sxs-lookup"><span data-stu-id="1415f-202">**ErrorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1415f-203">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1415f-203">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1415f-204">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1415f-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1415f-205">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ error de CIM**.**OtherErrorType**")</span><span class="sxs-lookup"><span data-stu-id="1415f-205">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**OtherErrorType**")</span></span>
</dt> </dl>

<span data-ttu-id="1415f-206">El tipo de error principal.</span><span class="sxs-lookup"><span data-stu-id="1415f-206">The primary error type.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1415f-207"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="1415f-207"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1415f-208"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="1415f-208"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Communications_Error"></span><span id="communications_error"></span><span id="COMMUNICATIONS_ERROR"></span>

<span data-ttu-id="1415f-209"><span id="Communications_Error"></span><span id="communications_error"></span><span id="COMMUNICATIONS_ERROR"></span>**Error de comunicaciones** (2)</span><span class="sxs-lookup"><span data-stu-id="1415f-209"><span id="Communications_Error"></span><span id="communications_error"></span><span id="COMMUNICATIONS_ERROR"></span>**Communications Error** (2)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-210">Los errores de este tipo están asociados principalmente a los procedimientos y/o procesos necesarios para transmitir información de un punto a otro.</span><span class="sxs-lookup"><span data-stu-id="1415f-210">Errors of this type are principally associated with the procedures and/or processes required to convey information from one point to another.</span></span>

</dd> <dt>

<span id="Quality_of_Service_Error"></span><span id="quality_of_service_error"></span><span id="QUALITY_OF_SERVICE_ERROR"></span>

<span data-ttu-id="1415f-211"><span id="Quality_of_Service_Error"></span><span id="quality_of_service_error"></span><span id="QUALITY_OF_SERVICE_ERROR"></span>**Error de calidad de servicio** (3)</span><span class="sxs-lookup"><span data-stu-id="1415f-211"><span id="Quality_of_Service_Error"></span><span id="quality_of_service_error"></span><span id="QUALITY_OF_SERVICE_ERROR"></span>**Quality of Service Error** (3)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-212">Los errores de este tipo están asociados principalmente a errores que dan lugar a una funcionalidad o un rendimiento reducidos.</span><span class="sxs-lookup"><span data-stu-id="1415f-212">Errors of this type are principally associated with failures that result in reduced functionality or performance.</span></span>

</dd> <dt>

<span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>

<span data-ttu-id="1415f-213"><span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>**Error de software** (4)</span><span class="sxs-lookup"><span data-stu-id="1415f-213"><span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>**Software Error** (4)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-214">Un error de este tipo está asociado principalmente a un software o un error de procesamiento.</span><span class="sxs-lookup"><span data-stu-id="1415f-214">Error of this type are principally associated with a software or processing fault.</span></span>

</dd> <dt>

<span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>

<span data-ttu-id="1415f-215"><span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>**Error de hardware** (5)</span><span class="sxs-lookup"><span data-stu-id="1415f-215"><span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>**Hardware Error** (5)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-216">Los errores de este tipo están asociados principalmente a un error de hardware o de equipo.</span><span class="sxs-lookup"><span data-stu-id="1415f-216">Errors of this type are principally associated with an equipment or hardware failure.</span></span>

</dd> <dt>

<span id="Environmental_Error"></span><span id="environmental_error"></span><span id="ENVIRONMENTAL_ERROR"></span>

<span data-ttu-id="1415f-217"><span id="Environmental_Error"></span><span id="environmental_error"></span><span id="ENVIRONMENTAL_ERROR"></span>**Error de entorno** (6)</span><span class="sxs-lookup"><span data-stu-id="1415f-217"><span id="Environmental_Error"></span><span id="environmental_error"></span><span id="ENVIRONMENTAL_ERROR"></span>**Environmental Error** (6)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-218">otras consideraciones del entorno.</span><span class="sxs-lookup"><span data-stu-id="1415f-218">other environmental considerations.</span></span>

</dd> <dt>

<span id="Security_Error"></span><span id="security_error"></span><span id="SECURITY_ERROR"></span>

<span data-ttu-id="1415f-219"><span id="Security_Error"></span><span id="security_error"></span><span id="SECURITY_ERROR"></span>**Error de seguridad** (7)</span><span class="sxs-lookup"><span data-stu-id="1415f-219"><span id="Security_Error"></span><span id="security_error"></span><span id="SECURITY_ERROR"></span>**Security Error** (7)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-220">Los errores de este tipo están asociados a infracciones de seguridad, detección de virus y problemas similares.</span><span class="sxs-lookup"><span data-stu-id="1415f-220">Errors of this type are associated with security violations, detection of viruses, and similar issues.</span></span>

</dd> <dt>

<span id="Oversubscription_Error"></span><span id="oversubscription_error"></span><span id="OVERSUBSCRIPTION_ERROR"></span>

<span data-ttu-id="1415f-221"><span id="Oversubscription_Error"></span><span id="oversubscription_error"></span><span id="OVERSUBSCRIPTION_ERROR"></span>**Error de sobresuscripción** (8)</span><span class="sxs-lookup"><span data-stu-id="1415f-221"><span id="Oversubscription_Error"></span><span id="oversubscription_error"></span><span id="OVERSUBSCRIPTION_ERROR"></span>**Oversubscription Error** (8)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-222">Los errores de este tipo están asociados principalmente al error de asignación de recursos suficientes para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="1415f-222">Errors of this type are principally associated with the failure to allocate sufficient resources to complete the operation.</span></span>

</dd> <dt>

<span id="Unavailable_Resource_Error"></span><span id="unavailable_resource_error"></span><span id="UNAVAILABLE_RESOURCE_ERROR"></span>

<span data-ttu-id="1415f-223"><span id="Unavailable_Resource_Error"></span><span id="unavailable_resource_error"></span><span id="UNAVAILABLE_RESOURCE_ERROR"></span>**Error de recurso no disponible** (9)</span><span class="sxs-lookup"><span data-stu-id="1415f-223"><span id="Unavailable_Resource_Error"></span><span id="unavailable_resource_error"></span><span id="UNAVAILABLE_RESOURCE_ERROR"></span>**Unavailable Resource Error** (9)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-224">Los errores de este tipo están asociados principalmente al error de acceso a un recurso necesario.</span><span class="sxs-lookup"><span data-stu-id="1415f-224">Errors of this type are principally associated with the failure to access a required resource.</span></span>

</dd> <dt>

<span id="Unsupported_Operation_Error"></span><span id="unsupported_operation_error"></span><span id="UNSUPPORTED_OPERATION_ERROR"></span>

<span data-ttu-id="1415f-225"><span id="Unsupported_Operation_Error"></span><span id="unsupported_operation_error"></span><span id="UNSUPPORTED_OPERATION_ERROR"></span>**Error de operación no compatible** (10)</span><span class="sxs-lookup"><span data-stu-id="1415f-225"><span id="Unsupported_Operation_Error"></span><span id="unsupported_operation_error"></span><span id="UNSUPPORTED_OPERATION_ERROR"></span>**Unsupported Operation Error** (10)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-226">Los errores de este tipo están asociados principalmente a las solicitudes que no se admiten.</span><span class="sxs-lookup"><span data-stu-id="1415f-226">Errors of this type are principally associated with requests that are not supported.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="1415f-227"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="1415f-227"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1415f-228">**Message**</span><span class="sxs-lookup"><span data-stu-id="1415f-228">**Message**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1415f-229">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1415f-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1415f-230">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1415f-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1415f-231">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ error de CIM**.**MessageID**","**\_ error de CIM**.**MessageArguments**")</span><span class="sxs-lookup"><span data-stu-id="1415f-231">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**MessageID**", "**CIM\_Error**.**MessageArguments**")</span></span>
</dt> </dl>

<span data-ttu-id="1415f-232">Mensaje con formato.</span><span class="sxs-lookup"><span data-stu-id="1415f-232">The formatted message.</span></span>

> [!Note]  
> <span data-ttu-id="1415f-233">Este mensaje se crea combinando los elementos dinámicos de la propiedad **MessageArguments** con los elementos estáticos de la propiedad **MessageID** y agregándolos después a un registro de mensajes o catálogo asociado a **OwningEntity**.</span><span class="sxs-lookup"><span data-stu-id="1415f-233">This message is created by combining dynamic elements of the **MessageArguments** property with the static elements of the **MessageID** property, and then adding them to a message registry or catalog associated with the **OwningEntity**.</span></span>

 

</dd> <dt>

<span data-ttu-id="1415f-234">**MessageArguments**</span><span class="sxs-lookup"><span data-stu-id="1415f-234">**MessageArguments**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1415f-235">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="1415f-235">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1415f-236">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1415f-236">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1415f-237">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ error de CIM**.**MessageID**","**\_ error de CIM**.**Mensaje**")</span><span class="sxs-lookup"><span data-stu-id="1415f-237">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**MessageID**", "**CIM\_Error**.**Message**")</span></span>
</dt> </dl>

<span data-ttu-id="1415f-238">Una matriz que contiene el contenido dinámico del mensaje.</span><span class="sxs-lookup"><span data-stu-id="1415f-238">An array that contains the dynamic content of the message.</span></span>

</dd> <dt>

<span data-ttu-id="1415f-239">**Identificador**</span><span class="sxs-lookup"><span data-stu-id="1415f-239">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1415f-240">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1415f-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1415f-241">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1415f-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1415f-242">Calificadores: [**required**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ error**.**Mensaje**","**\_ error de CIM**.**MessageArguments**")</span><span class="sxs-lookup"><span data-stu-id="1415f-242">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**Message**", "**CIM\_Error**.**MessageArguments**")</span></span>
</dt> </dl>

<span data-ttu-id="1415f-243">Cadena opaca que identifica de forma única, dentro del ámbito de OwningEntity, el formato del mensaje.</span><span class="sxs-lookup"><span data-stu-id="1415f-243">An opaque string that uniquely identifies, within the scope of the OwningEntity, the format of the Message.</span></span>

</dd> <dt>

<span data-ttu-id="1415f-244">**OtherErrorSourceFormat**</span><span class="sxs-lookup"><span data-stu-id="1415f-244">**OtherErrorSourceFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1415f-245">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1415f-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1415f-246">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1415f-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1415f-247">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ error de CIM**.**ErrorSourceFormat**")</span><span class="sxs-lookup"><span data-stu-id="1415f-247">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**ErrorSourceFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="1415f-248">Una cadena que define el valor de **ErrorSourceFormat** cuando **ErrorSourceFormat** se establece en "1" (otro).</span><span class="sxs-lookup"><span data-stu-id="1415f-248">A string that defines the **ErrorSourceFormat** value when **ErrorSourceFormat** is set to "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="1415f-249">**OtherErrorType**</span><span class="sxs-lookup"><span data-stu-id="1415f-249">**OtherErrorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1415f-250">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1415f-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1415f-251">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1415f-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1415f-252">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ error de CIM**.**ErrorType**")</span><span class="sxs-lookup"><span data-stu-id="1415f-252">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**ErrorType**")</span></span>
</dt> </dl>

<span data-ttu-id="1415f-253">Cadena de forma libre que describe el valor de **ErrorType** cuando se establece en "1" (otro).</span><span class="sxs-lookup"><span data-stu-id="1415f-253">A free-form string that describes the **ErrorType** value when it is set to "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="1415f-254">**OwningEntity**</span><span class="sxs-lookup"><span data-stu-id="1415f-254">**OwningEntity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1415f-255">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1415f-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1415f-256">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1415f-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1415f-257">IDENTIFICADOR único de la entidad que posee el formato del mensaje descrito por esta instancia.</span><span class="sxs-lookup"><span data-stu-id="1415f-257">The unique ID of the entity that owns the format of the message described by this instance.</span></span>

> [!Note]  
> <span data-ttu-id="1415f-258">Esta propiedad debe incluir un nombre con copyright, marca registrada o único que sea propiedad de la entidad de negocio o del cuerpo de los estándares que haya definido el formato de mensaje.</span><span class="sxs-lookup"><span data-stu-id="1415f-258">This property must include a copyrighted, trademarked, or unique name that is owned by the business entity or standards body that defined the message format.</span></span>

 

</dd> <dt>

<span data-ttu-id="1415f-259">**PerceivedSeverity**</span><span class="sxs-lookup"><span data-stu-id="1415f-259">**PerceivedSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1415f-260">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1415f-260">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1415f-261">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1415f-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1415f-262">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("RECOMMENDATION. itu \| X733. Gravedad percibida ")</span><span class="sxs-lookup"><span data-stu-id="1415f-262">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Perceived severity")</span></span>
</dt> </dl>

<span data-ttu-id="1415f-263">Una descripción de la gravedad del error desde el punto de vista del elemento que envió el mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="1415f-263">A description of the error severity from the point of view of the element that sent the error message.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1415f-264"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="1415f-264"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-265">la gravedad percibida de la indicación es desconocida o indeterminada.</span><span class="sxs-lookup"><span data-stu-id="1415f-265">the Perceived Severity of the indication is unknown or indeterminate.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1415f-266"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="1415f-266"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-267">Indica que el valor de la gravedad se puede encontrar en la propiedad **OtherSeverity** .</span><span class="sxs-lookup"><span data-stu-id="1415f-267">Indicates that the Severity's value can be found in the **OtherSeverity** property.</span></span>

</dd> <dt>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>

<span data-ttu-id="1415f-268"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Información** (2)</span><span class="sxs-lookup"><span data-stu-id="1415f-268"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Information** (2)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-269">La información se debe utilizar al proporcionar una respuesta informativa.</span><span class="sxs-lookup"><span data-stu-id="1415f-269">Information should be used when providing an informative response.</span></span>

</dd> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>

<span data-ttu-id="1415f-270"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Degradado/ADVERTENCIA** (3)</span><span class="sxs-lookup"><span data-stu-id="1415f-270"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Degraded/Warning** (3)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-271">Debe usarse cuando sea adecuado para permitir que el usuario decida si es necesario realizar alguna acción.</span><span class="sxs-lookup"><span data-stu-id="1415f-271">Should be used when its appropriate to let the user decide if action is needed.</span></span>

</dd> <dt>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>

<span data-ttu-id="1415f-272"><span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Secundaria** (4)</span><span class="sxs-lookup"><span data-stu-id="1415f-272"><span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Minor** (4)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-273">La acción es necesaria, pero la situación no es seria en este momento.</span><span class="sxs-lookup"><span data-stu-id="1415f-273">Action is needed, but the situation is not serious at this time.</span></span>

</dd> <dt>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>

<span data-ttu-id="1415f-274"><span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Principal** (5)</span><span class="sxs-lookup"><span data-stu-id="1415f-274"><span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Major** (5)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-275">La acción es necesaria ahora.</span><span class="sxs-lookup"><span data-stu-id="1415f-275">Action is needed NOW.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="1415f-276"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** (6)</span><span class="sxs-lookup"><span data-stu-id="1415f-276"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (6)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-277">La acción es necesaria ahora y el ámbito es amplio (es posible que se produzca una interrupción inminente en un recurso crítico).</span><span class="sxs-lookup"><span data-stu-id="1415f-277">Action is needed NOW and the scope is broad (perhaps an imminent outage to a critical resource will result).</span></span>

</dd> <dt>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>

<span data-ttu-id="1415f-278"><span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**Irrecuperable/no recuperable** (7)</span><span class="sxs-lookup"><span data-stu-id="1415f-278"><span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**Fatal/NonRecoverable** (7)</span></span>


</dt> <dd>

<span data-ttu-id="1415f-279">se produjo un error, pero es demasiado tarde para tomar medidas correctivas.</span><span class="sxs-lookup"><span data-stu-id="1415f-279">an error occurred, but it's too late to take remedial action.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="1415f-280"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="1415f-280"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1415f-281">**ProbableCause**</span><span class="sxs-lookup"><span data-stu-id="1415f-281">**ProbableCause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1415f-282">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1415f-282">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1415f-283">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1415f-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1415f-284">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("RECOMMENDATION. itu \| X733. Causa probable: "," recommendation. ITU \| M3100. probableCause "," ITU-IANA-Alarm-TC "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ error de CIM**.**ProbableCauseDescription**")</span><span class="sxs-lookup"><span data-stu-id="1415f-284">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Probable cause", "Recommendation.ITU\|M3100.probableCause", "ITU-IANA-ALARM-TC"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**ProbableCauseDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="1415f-285">Una descripción de la causa probable del error.</span><span class="sxs-lookup"><span data-stu-id="1415f-285">A description of te probable cause of the error.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1415f-286">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="1415f-286">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1415f-287">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="1415f-287">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter_Card_Error"></span><span id="adapter_card_error"></span><span id="ADAPTER_CARD_ERROR"></span>

<span data-ttu-id="1415f-288">**Error de tarjeta/adaptador** (2)</span><span class="sxs-lookup"><span data-stu-id="1415f-288">**Adapter/Card Error** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Subsystem_Failure"></span><span id="application_subsystem_failure"></span><span id="APPLICATION_SUBSYSTEM_FAILURE"></span>

<span data-ttu-id="1415f-289">**Error del subsistema de aplicación** (3)</span><span class="sxs-lookup"><span data-stu-id="1415f-289">**Application Subsystem Failure** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bandwidth_Reduced"></span><span id="bandwidth_reduced"></span><span id="BANDWIDTH_REDUCED"></span>

<span data-ttu-id="1415f-290">**Ancho de banda reducido** (4)</span><span class="sxs-lookup"><span data-stu-id="1415f-290">**Bandwidth Reduced** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Connection_Establishment_Error"></span><span id="connection_establishment_error"></span><span id="CONNECTION_ESTABLISHMENT_ERROR"></span>

<span data-ttu-id="1415f-291">**Error de establecimiento de conexión** (5)</span><span class="sxs-lookup"><span data-stu-id="1415f-291">**Connection Establishment Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Communications_Protocol_Error"></span><span id="communications_protocol_error"></span><span id="COMMUNICATIONS_PROTOCOL_ERROR"></span>

<span data-ttu-id="1415f-292">**Error de protocolo de comunicaciones** (6)</span><span class="sxs-lookup"><span data-stu-id="1415f-292">**Communications Protocol Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Communications_Subsystem_Failure"></span><span id="communications_subsystem_failure"></span><span id="COMMUNICATIONS_SUBSYSTEM_FAILURE"></span>

<span data-ttu-id="1415f-293">**Error del subsistema de comunicaciones** (7)</span><span class="sxs-lookup"><span data-stu-id="1415f-293">**Communications Subsystem Failure** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Configuration_Customization_Error"></span><span id="configuration_customization_error"></span><span id="CONFIGURATION_CUSTOMIZATION_ERROR"></span>

<span data-ttu-id="1415f-294">**Error de configuración/personalización** (8)</span><span class="sxs-lookup"><span data-stu-id="1415f-294">**Configuration/Customization Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Congestion"></span><span id="congestion"></span><span id="CONGESTION"></span>

<span data-ttu-id="1415f-295">**Congestión** (9)</span><span class="sxs-lookup"><span data-stu-id="1415f-295">**Congestion** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrupt_Data"></span><span id="corrupt_data"></span><span id="CORRUPT_DATA"></span>

<span data-ttu-id="1415f-296">**Datos dañados** (10)</span><span class="sxs-lookup"><span data-stu-id="1415f-296">**Corrupt Data** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CPU_Cycles_Limit_Exceeded"></span><span id="cpu_cycles_limit_exceeded"></span><span id="CPU_CYCLES_LIMIT_EXCEEDED"></span>

<span data-ttu-id="1415f-297">Se **superó el límite de ciclos de CPU** (11)</span><span class="sxs-lookup"><span data-stu-id="1415f-297">**CPU Cycles Limit Exceeded** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Dataset_Modem_Error"></span><span id="dataset_modem_error"></span><span id="DATASET_MODEM_ERROR"></span>

<span data-ttu-id="1415f-298">**Error de conjunto** de</span><span class="sxs-lookup"><span data-stu-id="1415f-298">**Dataset/Modem Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded_Signal"></span><span id="degraded_signal"></span><span id="DEGRADED_SIGNAL"></span>

<span data-ttu-id="1415f-299">**Señal degradada** (13)</span><span class="sxs-lookup"><span data-stu-id="1415f-299">**Degraded Signal** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="DTE-DCE_Interface_Error"></span><span id="dte-dce_interface_error"></span><span id="DTE-DCE_INTERFACE_ERROR"></span>

<span data-ttu-id="1415f-300">**Error de la interfaz DTE-DCE** (14)</span><span class="sxs-lookup"><span data-stu-id="1415f-300">**DTE-DCE Interface Error** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Enclosure_Door_Open"></span><span id="enclosure_door_open"></span><span id="ENCLOSURE_DOOR_OPEN"></span>

<span data-ttu-id="1415f-301">Abertura de la **puerta del gabinete** (15)</span><span class="sxs-lookup"><span data-stu-id="1415f-301">**Enclosure Door Open** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Equipment_Malfunction"></span><span id="equipment_malfunction"></span><span id="EQUIPMENT_MALFUNCTION"></span>

<span data-ttu-id="1415f-302">**Funcionamiento incorrecto del equipo** (16)</span><span class="sxs-lookup"><span data-stu-id="1415f-302">**Equipment Malfunction** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Excessive_Vibration"></span><span id="excessive_vibration"></span><span id="EXCESSIVE_VIBRATION"></span>

<span data-ttu-id="1415f-303">**Vibración excesiva** (17)</span><span class="sxs-lookup"><span data-stu-id="1415f-303">**Excessive Vibration** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="File_Format_Error"></span><span id="file_format_error"></span><span id="FILE_FORMAT_ERROR"></span>

<span data-ttu-id="1415f-304">**Error de formato de archivo** (18)</span><span class="sxs-lookup"><span data-stu-id="1415f-304">**File Format Error** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Fire_Detected"></span><span id="fire_detected"></span><span id="FIRE_DETECTED"></span>

<span data-ttu-id="1415f-305">**Desencadenamiento detectado** (19)</span><span class="sxs-lookup"><span data-stu-id="1415f-305">**Fire Detected** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Flood_Detected"></span><span id="flood_detected"></span><span id="FLOOD_DETECTED"></span>

<span data-ttu-id="1415f-306">**Inundación detectada** (20)</span><span class="sxs-lookup"><span data-stu-id="1415f-306">**Flood Detected** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Framing_Error"></span><span id="framing_error"></span><span id="FRAMING_ERROR"></span>

<span data-ttu-id="1415f-307">**Error de tramas** (21)</span><span class="sxs-lookup"><span data-stu-id="1415f-307">**Framing Error** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HVAC_Problem"></span><span id="hvac_problem"></span><span id="HVAC_PROBLEM"></span>

<span data-ttu-id="1415f-308">**Problema de HVAC** (22)</span><span class="sxs-lookup"><span data-stu-id="1415f-308">**HVAC Problem** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="Humidity_Unacceptable"></span><span id="humidity_unacceptable"></span><span id="HUMIDITY_UNACCEPTABLE"></span>

<span data-ttu-id="1415f-309">**Humedad inaceptable** (23)</span><span class="sxs-lookup"><span data-stu-id="1415f-309">**Humidity Unacceptable** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Device_Error"></span><span id="i_o_device_error"></span><span id="I_O_DEVICE_ERROR"></span>

<span data-ttu-id="1415f-310">**Error de dispositivo de e/s** (24)</span><span class="sxs-lookup"><span data-stu-id="1415f-310">**I/O Device Error** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="Input_Device_Error"></span><span id="input_device_error"></span><span id="INPUT_DEVICE_ERROR"></span>

<span data-ttu-id="1415f-311">**Error de dispositivo de entrada** (25)</span><span class="sxs-lookup"><span data-stu-id="1415f-311">**Input Device Error** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LAN_Error"></span><span id="lan_error"></span><span id="LAN_ERROR"></span>

<span data-ttu-id="1415f-312">**Error de LAN** (26)</span><span class="sxs-lookup"><span data-stu-id="1415f-312">**LAN Error** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Toxic_Leak_Detected"></span><span id="non-toxic_leak_detected"></span><span id="NON-TOXIC_LEAK_DETECTED"></span>

<span data-ttu-id="1415f-313">**Pérdida no tóxica detectada** (27)</span><span class="sxs-lookup"><span data-stu-id="1415f-313">**Non-Toxic Leak Detected** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Local_Node_Transmission_Error"></span><span id="local_node_transmission_error"></span><span id="LOCAL_NODE_TRANSMISSION_ERROR"></span>

<span data-ttu-id="1415f-314">**Error de transmisión del nodo local** (28)</span><span class="sxs-lookup"><span data-stu-id="1415f-314">**Local Node Transmission Error** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Frame"></span><span id="loss_of_frame"></span><span id="LOSS_OF_FRAME"></span>

<span data-ttu-id="1415f-315">**Pérdida de fotograma** (29)</span><span class="sxs-lookup"><span data-stu-id="1415f-315">**Loss of Frame** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Signal"></span><span id="loss_of_signal"></span><span id="LOSS_OF_SIGNAL"></span>

<span data-ttu-id="1415f-316">**Pérdida de señal** (30)</span><span class="sxs-lookup"><span data-stu-id="1415f-316">**Loss of Signal** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Material_Supply_Exhausted"></span><span id="material_supply_exhausted"></span><span id="MATERIAL_SUPPLY_EXHAUSTED"></span>

<span data-ttu-id="1415f-317">**Suministro de material agotado** (31)</span><span class="sxs-lookup"><span data-stu-id="1415f-317">**Material Supply Exhausted** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiplexer_Problem"></span><span id="multiplexer_problem"></span><span id="MULTIPLEXER_PROBLEM"></span>

<span data-ttu-id="1415f-318">**Problema del multiplexor** (32)</span><span class="sxs-lookup"><span data-stu-id="1415f-318">**Multiplexer Problem** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_Memory"></span><span id="out_of_memory"></span><span id="OUT_OF_MEMORY"></span>

<span data-ttu-id="1415f-319">**Memoria insuficiente** (33)</span><span class="sxs-lookup"><span data-stu-id="1415f-319">**Out of Memory** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="Output_Device_Error"></span><span id="output_device_error"></span><span id="OUTPUT_DEVICE_ERROR"></span>

<span data-ttu-id="1415f-320">**Error de dispositivo de salida** (34)</span><span class="sxs-lookup"><span data-stu-id="1415f-320">**Output Device Error** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Performance_Degraded"></span><span id="performance_degraded"></span><span id="PERFORMANCE_DEGRADED"></span>

<span data-ttu-id="1415f-321">**Rendimiento degradado** (35)</span><span class="sxs-lookup"><span data-stu-id="1415f-321">**Performance Degraded** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Problem"></span><span id="power_problem"></span><span id="POWER_PROBLEM"></span>

<span data-ttu-id="1415f-322">**Problema de energía** (36)</span><span class="sxs-lookup"><span data-stu-id="1415f-322">**Power Problem** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Pressure_Unacceptable"></span><span id="pressure_unacceptable"></span><span id="PRESSURE_UNACCEPTABLE"></span>

<span data-ttu-id="1415f-323">**Presión inaceptable** (37)</span><span class="sxs-lookup"><span data-stu-id="1415f-323">**Pressure Unacceptable** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Processor_Problem__Internal_Machine_Error_"></span><span id="processor_problem__internal_machine_error_"></span><span id="PROCESSOR_PROBLEM__INTERNAL_MACHINE_ERROR_"></span>

<span data-ttu-id="1415f-324">**Problema del procesador (error interno de la máquina)** (38)</span><span class="sxs-lookup"><span data-stu-id="1415f-324">**Processor Problem (Internal Machine Error)** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pump_Failure"></span><span id="pump_failure"></span><span id="PUMP_FAILURE"></span>

<span data-ttu-id="1415f-325">**Error de bombeo** (39)</span><span class="sxs-lookup"><span data-stu-id="1415f-325">**Pump Failure** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Queue_Size_Exceeded"></span><span id="queue_size_exceeded"></span><span id="QUEUE_SIZE_EXCEEDED"></span>

<span data-ttu-id="1415f-326">**Tamaño de cola superado** (40)</span><span class="sxs-lookup"><span data-stu-id="1415f-326">**Queue Size Exceeded** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="Receive_Failure"></span><span id="receive_failure"></span><span id="RECEIVE_FAILURE"></span>

<span data-ttu-id="1415f-327">**Error de recepción** (41)</span><span class="sxs-lookup"><span data-stu-id="1415f-327">**Receive Failure** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Receiver_Failure"></span><span id="receiver_failure"></span><span id="RECEIVER_FAILURE"></span>

<span data-ttu-id="1415f-328">**Error del receptor** (42)</span><span class="sxs-lookup"><span data-stu-id="1415f-328">**Receiver Failure** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="Remote_Node_Transmission_Error"></span><span id="remote_node_transmission_error"></span><span id="REMOTE_NODE_TRANSMISSION_ERROR"></span>

<span data-ttu-id="1415f-329">**Error de transmisión de nodo remoto** (43)</span><span class="sxs-lookup"><span data-stu-id="1415f-329">**Remote Node Transmission Error** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="Resource_at_or_Nearing_Capacity"></span><span id="resource_at_or_nearing_capacity"></span><span id="RESOURCE_AT_OR_NEARING_CAPACITY"></span>

<span data-ttu-id="1415f-330">**Recursos a la capacidad o en proximidad** (44)</span><span class="sxs-lookup"><span data-stu-id="1415f-330">**Resource at or Nearing Capacity** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="Response_Time_Excessive"></span><span id="response_time_excessive"></span><span id="RESPONSE_TIME_EXCESSIVE"></span>

<span data-ttu-id="1415f-331">**Tiempo de respuesta excesivo** (45)</span><span class="sxs-lookup"><span data-stu-id="1415f-331">**Response Time Excessive** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="Retransmission_Rate_Excessive"></span><span id="retransmission_rate_excessive"></span><span id="RETRANSMISSION_RATE_EXCESSIVE"></span>

<span data-ttu-id="1415f-332">**Tasa de retransmisión excesiva** (46)</span><span class="sxs-lookup"><span data-stu-id="1415f-332">**Retransmission Rate Excessive** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>

<span data-ttu-id="1415f-333">**Error de software** (47)</span><span class="sxs-lookup"><span data-stu-id="1415f-333">**Software Error** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Program_Abnormally_Terminated"></span><span id="software_program_abnormally_terminated"></span><span id="SOFTWARE_PROGRAM_ABNORMALLY_TERMINATED"></span>

<span data-ttu-id="1415f-334">**Programa de software finalizado** de manera anómala (48)</span><span class="sxs-lookup"><span data-stu-id="1415f-334">**Software Program Abnormally Terminated** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Program_Error__Incorrect_Results_"></span><span id="software_program_error__incorrect_results_"></span><span id="SOFTWARE_PROGRAM_ERROR__INCORRECT_RESULTS_"></span>

<span data-ttu-id="1415f-335">**Error del programa de software (resultados incorrectos)** (49)</span><span class="sxs-lookup"><span data-stu-id="1415f-335">**Software Program Error (Incorrect Results)** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>

<span data-ttu-id="1415f-336">**Problema de capacidad de almacenamiento** (50)</span><span class="sxs-lookup"><span data-stu-id="1415f-336">**Storage Capacity Problem** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="Temperature_Unacceptable"></span><span id="temperature_unacceptable"></span><span id="TEMPERATURE_UNACCEPTABLE"></span>

<span data-ttu-id="1415f-337">**Temperatura inaceptable** (51)</span><span class="sxs-lookup"><span data-stu-id="1415f-337">**Temperature Unacceptable** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="Threshold_Crossed"></span><span id="threshold_crossed"></span><span id="THRESHOLD_CROSSED"></span>

<span data-ttu-id="1415f-338">**Umbral superado** (52)</span><span class="sxs-lookup"><span data-stu-id="1415f-338">**Threshold Crossed** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="Timing_Problem"></span><span id="timing_problem"></span><span id="TIMING_PROBLEM"></span>

<span data-ttu-id="1415f-339">**Problema de sincronización** (53)</span><span class="sxs-lookup"><span data-stu-id="1415f-339">**Timing Problem** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="Toxic_Leak_Detected"></span><span id="toxic_leak_detected"></span><span id="TOXIC_LEAK_DETECTED"></span>

<span data-ttu-id="1415f-340">**Pérdida tóxica detectada** (54)</span><span class="sxs-lookup"><span data-stu-id="1415f-340">**Toxic Leak Detected** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="Transmit_Failure"></span><span id="transmit_failure"></span><span id="TRANSMIT_FAILURE"></span>

<span data-ttu-id="1415f-341">**Error de transmisión** (55)</span><span class="sxs-lookup"><span data-stu-id="1415f-341">**Transmit Failure** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="Transmitter_Failure"></span><span id="transmitter_failure"></span><span id="TRANSMITTER_FAILURE"></span>

<span data-ttu-id="1415f-342">**Error de transmisor** (56)</span><span class="sxs-lookup"><span data-stu-id="1415f-342">**Transmitter Failure** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="Underlying_Resource_Unavailable"></span><span id="underlying_resource_unavailable"></span><span id="UNDERLYING_RESOURCE_UNAVAILABLE"></span>

<span data-ttu-id="1415f-343">**Recurso subyacente no disponible** (57)</span><span class="sxs-lookup"><span data-stu-id="1415f-343">**Underlying Resource Unavailable** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Version_Mismatch"></span><span id="version_mismatch"></span><span id="VERSION_MISMATCH"></span>

<span data-ttu-id="1415f-344">**Discrepancia de versiones** (58)</span><span class="sxs-lookup"><span data-stu-id="1415f-344">**Version Mismatch** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>

<span data-ttu-id="1415f-345">**Alerta anterior desactivada** (59)</span><span class="sxs-lookup"><span data-stu-id="1415f-345">**Previous Alert Cleared** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="Login_Attempts_Failed"></span><span id="login_attempts_failed"></span><span id="LOGIN_ATTEMPTS_FAILED"></span>

<span data-ttu-id="1415f-346">**Error de intentos de inicio de sesión** (60)</span><span class="sxs-lookup"><span data-stu-id="1415f-346">**Login Attempts Failed** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Virus_Detected"></span><span id="software_virus_detected"></span><span id="SOFTWARE_VIRUS_DETECTED"></span>

<span data-ttu-id="1415f-347">**Virus de software detectado** (61)</span><span class="sxs-lookup"><span data-stu-id="1415f-347">**Software Virus Detected** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Hardware_Security_Breached"></span><span id="hardware_security_breached"></span><span id="HARDWARE_SECURITY_BREACHED"></span>

<span data-ttu-id="1415f-348">**Seguridad de hardware infringida** (62)</span><span class="sxs-lookup"><span data-stu-id="1415f-348">**Hardware Security Breached** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="Denial_of_Service_Detected"></span><span id="denial_of_service_detected"></span><span id="DENIAL_OF_SERVICE_DETECTED"></span>

<span data-ttu-id="1415f-349">**Denegación de servicio detectada** (63)</span><span class="sxs-lookup"><span data-stu-id="1415f-349">**Denial of Service Detected** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Security_Credential_Mismatch"></span><span id="security_credential_mismatch"></span><span id="SECURITY_CREDENTIAL_MISMATCH"></span>

<span data-ttu-id="1415f-350">**No coincide la credencial de seguridad** (64)</span><span class="sxs-lookup"><span data-stu-id="1415f-350">**Security Credential Mismatch** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="Unauthorized_Access"></span><span id="unauthorized_access"></span><span id="UNAUTHORIZED_ACCESS"></span>

<span data-ttu-id="1415f-351">**Acceso no autorizado** (65)</span><span class="sxs-lookup"><span data-stu-id="1415f-351">**Unauthorized Access** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="Alarm_Received"></span><span id="alarm_received"></span><span id="ALARM_RECEIVED"></span>

<span data-ttu-id="1415f-352">**Alarma recibida** (66)</span><span class="sxs-lookup"><span data-stu-id="1415f-352">**Alarm Received** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Pointer"></span><span id="loss_of_pointer"></span><span id="LOSS_OF_POINTER"></span>

<span data-ttu-id="1415f-353">**Pérdida de puntero** (67)</span><span class="sxs-lookup"><span data-stu-id="1415f-353">**Loss of Pointer** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="Payload_Mismatch"></span><span id="payload_mismatch"></span><span id="PAYLOAD_MISMATCH"></span>

<span data-ttu-id="1415f-354">Error de **coincidencia de carga** (68)</span><span class="sxs-lookup"><span data-stu-id="1415f-354">**Payload Mismatch** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Transmission_Error"></span><span id="transmission_error"></span><span id="TRANSMISSION_ERROR"></span>

<span data-ttu-id="1415f-355">**Error de transmisión** (69)</span><span class="sxs-lookup"><span data-stu-id="1415f-355">**Transmission Error** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Excessive_Error_Rate"></span><span id="excessive_error_rate"></span><span id="EXCESSIVE_ERROR_RATE"></span>

<span data-ttu-id="1415f-356">**Tasa de errores excesiva** (70)</span><span class="sxs-lookup"><span data-stu-id="1415f-356">**Excessive Error Rate** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Trace_Problem"></span><span id="trace_problem"></span><span id="TRACE_PROBLEM"></span>

<span data-ttu-id="1415f-357">**Problema de seguimiento** (71)</span><span class="sxs-lookup"><span data-stu-id="1415f-357">**Trace Problem** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Unavailable"></span><span id="element_unavailable"></span><span id="ELEMENT_UNAVAILABLE"></span>

<span data-ttu-id="1415f-358">**Elemento no disponible** (72)</span><span class="sxs-lookup"><span data-stu-id="1415f-358">**Element Unavailable** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Missing"></span><span id="element_missing"></span><span id="ELEMENT_MISSING"></span>

<span data-ttu-id="1415f-359">**Falta el elemento** (73)</span><span class="sxs-lookup"><span data-stu-id="1415f-359">**Element Missing** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Multi_Frame"></span><span id="loss_of_multi_frame"></span><span id="LOSS_OF_MULTI_FRAME"></span>

<span data-ttu-id="1415f-360">**Pérdida de varios fotogramas** (74)</span><span class="sxs-lookup"><span data-stu-id="1415f-360">**Loss of Multi Frame** (74)</span></span>


</dt> <dd></dd> <dt>

<span id="Broadcast_Channel_Failure"></span><span id="broadcast_channel_failure"></span><span id="BROADCAST_CHANNEL_FAILURE"></span>

<span data-ttu-id="1415f-361">**Error de canal de difusión** (75)</span><span class="sxs-lookup"><span data-stu-id="1415f-361">**Broadcast Channel Failure** (75)</span></span>


</dt> <dd></dd> <dt>

<span id="Invalid_Message_Received"></span><span id="invalid_message_received"></span><span id="INVALID_MESSAGE_RECEIVED"></span>

<span data-ttu-id="1415f-362">Se **recibió un mensaje no válido** (76)</span><span class="sxs-lookup"><span data-stu-id="1415f-362">**Invalid Message Received** (76)</span></span>


</dt> <dd></dd> <dt>

<span id="Routing_Failure"></span><span id="routing_failure"></span><span id="ROUTING_FAILURE"></span>

<span data-ttu-id="1415f-363">**Error de enrutamiento** (77)</span><span class="sxs-lookup"><span data-stu-id="1415f-363">**Routing Failure** (77)</span></span>


</dt> <dd></dd> <dt>

<span id="Backplane_Failure"></span><span id="backplane_failure"></span><span id="BACKPLANE_FAILURE"></span>

<span data-ttu-id="1415f-364">**Error de backplane** (78)</span><span class="sxs-lookup"><span data-stu-id="1415f-364">**Backplane Failure** (78)</span></span>


</dt> <dd></dd> <dt>

<span id="Identifier_Duplication"></span><span id="identifier_duplication"></span><span id="IDENTIFIER_DUPLICATION"></span>

<span data-ttu-id="1415f-365">**Duplicación de identificadores** (79)</span><span class="sxs-lookup"><span data-stu-id="1415f-365">**Identifier Duplication** (79)</span></span>


</dt> <dd></dd> <dt>

<span id="Protection_Path_Failure"></span><span id="protection_path_failure"></span><span id="PROTECTION_PATH_FAILURE"></span>

<span data-ttu-id="1415f-366">**Error de ruta de protección** (80)</span><span class="sxs-lookup"><span data-stu-id="1415f-366">**Protection Path Failure** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="Sync_Loss_or_Mismatch"></span><span id="sync_loss_or_mismatch"></span><span id="SYNC_LOSS_OR_MISMATCH"></span>

<span data-ttu-id="1415f-367">**Pérdida o desigualdad de sincronización** (81)</span><span class="sxs-lookup"><span data-stu-id="1415f-367">**Sync Loss or Mismatch** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="Terminal_Problem"></span><span id="terminal_problem"></span><span id="TERMINAL_PROBLEM"></span>

<span data-ttu-id="1415f-368">**Problema de terminal** (82)</span><span class="sxs-lookup"><span data-stu-id="1415f-368">**Terminal Problem** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="Real_Time_Clock_Failure"></span><span id="real_time_clock_failure"></span><span id="REAL_TIME_CLOCK_FAILURE"></span>

<span data-ttu-id="1415f-369">**Error de reloj en tiempo real** (83)</span><span class="sxs-lookup"><span data-stu-id="1415f-369">**Real Time Clock Failure** (83)</span></span>


</dt> <dd></dd> <dt>

<span id="Antenna_Failure"></span><span id="antenna_failure"></span><span id="ANTENNA_FAILURE"></span>

<span data-ttu-id="1415f-370">**Error de antena** (84)</span><span class="sxs-lookup"><span data-stu-id="1415f-370">**Antenna Failure** (84)</span></span>


</dt> <dd></dd> <dt>

<span id="Battery_Charging_Failure"></span><span id="battery_charging_failure"></span><span id="BATTERY_CHARGING_FAILURE"></span>

<span data-ttu-id="1415f-371">**Error de carga** de la batería (85)</span><span class="sxs-lookup"><span data-stu-id="1415f-371">**Battery Charging Failure** (85)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Failure"></span><span id="disk_failure"></span><span id="DISK_FAILURE"></span>

<span data-ttu-id="1415f-372">**Error de disco** (86)</span><span class="sxs-lookup"><span data-stu-id="1415f-372">**Disk Failure** (86)</span></span>


</dt> <dd></dd> <dt>

<span id="Frequency_Hopping_Failure"></span><span id="frequency_hopping_failure"></span><span id="FREQUENCY_HOPPING_FAILURE"></span>

<span data-ttu-id="1415f-373">**Error de salto de frecuencia** (87)</span><span class="sxs-lookup"><span data-stu-id="1415f-373">**Frequency Hopping Failure** (87)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Redundancy"></span><span id="loss_of_redundancy"></span><span id="LOSS_OF_REDUNDANCY"></span>

<span data-ttu-id="1415f-374">**Pérdida de redundancia** (88)</span><span class="sxs-lookup"><span data-stu-id="1415f-374">**Loss of Redundancy** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Supply_Failure"></span><span id="power_supply_failure"></span><span id="POWER_SUPPLY_FAILURE"></span>

<span data-ttu-id="1415f-375">**Error** de la fuente de alimentación (89)</span><span class="sxs-lookup"><span data-stu-id="1415f-375">**Power Supply Failure** (89)</span></span>


</dt> <dd></dd> <dt>

<span id="Signal_Quality_Problem"></span><span id="signal_quality_problem"></span><span id="SIGNAL_QUALITY_PROBLEM"></span>

<span data-ttu-id="1415f-376">**Problema de calidad** de la señal (90)</span><span class="sxs-lookup"><span data-stu-id="1415f-376">**Signal Quality Problem** (90)</span></span>


</dt> <dd></dd> <dt>

<span id="Battery_Discharging"></span><span id="battery_discharging"></span><span id="BATTERY_DISCHARGING"></span>

<span data-ttu-id="1415f-377">**Descarga** de la batería (91)</span><span class="sxs-lookup"><span data-stu-id="1415f-377">**Battery Discharging** (91)</span></span>


</dt> <dd></dd> <dt>

<span id="Battery_Failure"></span><span id="battery_failure"></span><span id="BATTERY_FAILURE"></span>

<span data-ttu-id="1415f-378">**Error de batería** (92)</span><span class="sxs-lookup"><span data-stu-id="1415f-378">**Battery Failure** (92)</span></span>


</dt> <dd></dd> <dt>

<span id="Commercial_Power_Problem"></span><span id="commercial_power_problem"></span><span id="COMMERCIAL_POWER_PROBLEM"></span>

<span data-ttu-id="1415f-379">**Problema de alimentación comercial** (93)</span><span class="sxs-lookup"><span data-stu-id="1415f-379">**Commercial Power Problem** (93)</span></span>


</dt> <dd></dd> <dt>

<span id="Fan_Failure"></span><span id="fan_failure"></span><span id="FAN_FAILURE"></span>

<span data-ttu-id="1415f-380">**Error de ventilador** (94)</span><span class="sxs-lookup"><span data-stu-id="1415f-380">**Fan Failure** (94)</span></span>


</dt> <dd></dd> <dt>

<span id="Engine_Failure"></span><span id="engine_failure"></span><span id="ENGINE_FAILURE"></span>

<span data-ttu-id="1415f-381">**Error del motor** (95)</span><span class="sxs-lookup"><span data-stu-id="1415f-381">**Engine Failure** (95)</span></span>


</dt> <dd></dd> <dt>

<span id="Sensor_Failure"></span><span id="sensor_failure"></span><span id="SENSOR_FAILURE"></span>

<span data-ttu-id="1415f-382">**Error del sensor** (96)</span><span class="sxs-lookup"><span data-stu-id="1415f-382">**Sensor Failure** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Fuse_Failure"></span><span id="fuse_failure"></span><span id="FUSE_FAILURE"></span>

<span data-ttu-id="1415f-383">**Error de fusible** (97)</span><span class="sxs-lookup"><span data-stu-id="1415f-383">**Fuse Failure** (97)</span></span>


</dt> <dd></dd> <dt>

<span id="Generator_Failure"></span><span id="generator_failure"></span><span id="GENERATOR_FAILURE"></span>

<span data-ttu-id="1415f-384">**Error del generador** (98)</span><span class="sxs-lookup"><span data-stu-id="1415f-384">**Generator Failure** (98)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Battery"></span><span id="low_battery"></span><span id="LOW_BATTERY"></span>

<span data-ttu-id="1415f-385">**Batería baja** (99)</span><span class="sxs-lookup"><span data-stu-id="1415f-385">**Low Battery** (99)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Fuel"></span><span id="low_fuel"></span><span id="LOW_FUEL"></span>

<span data-ttu-id="1415f-386">**Combustible bajo** (100)</span><span class="sxs-lookup"><span data-stu-id="1415f-386">**Low Fuel** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Water"></span><span id="low_water"></span><span id="LOW_WATER"></span>

<span data-ttu-id="1415f-387">**Bajo agua** (101)</span><span class="sxs-lookup"><span data-stu-id="1415f-387">**Low Water** (101)</span></span>


</dt> <dd></dd> <dt>

<span id="Explosive_Gas"></span><span id="explosive_gas"></span><span id="EXPLOSIVE_GAS"></span>

<span data-ttu-id="1415f-388">**Gas explosivo** (102)</span><span class="sxs-lookup"><span data-stu-id="1415f-388">**Explosive Gas** (102)</span></span>


</dt> <dd></dd> <dt>

<span id="High_Winds"></span><span id="high_winds"></span><span id="HIGH_WINDS"></span>

<span data-ttu-id="1415f-389">**Viento alto** (103)</span><span class="sxs-lookup"><span data-stu-id="1415f-389">**High Winds** (103)</span></span>


</dt> <dd></dd> <dt>

<span id="Ice_Buildup"></span><span id="ice_buildup"></span><span id="ICE_BUILDUP"></span>

<span data-ttu-id="1415f-390">**Acumulación de hielo** (104)</span><span class="sxs-lookup"><span data-stu-id="1415f-390">**Ice Buildup** (104)</span></span>


</dt> <dd></dd> <dt>

<span id="Smoke"></span><span id="smoke"></span><span id="SMOKE"></span>

<span data-ttu-id="1415f-391">**Humo** (105)</span><span class="sxs-lookup"><span data-stu-id="1415f-391">**Smoke** (105)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory_Mismatch"></span><span id="memory_mismatch"></span><span id="MEMORY_MISMATCH"></span>

<span data-ttu-id="1415f-392">**No coincide la memoria** (106)</span><span class="sxs-lookup"><span data-stu-id="1415f-392">**Memory Mismatch** (106)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_CPU_Cycles"></span><span id="out_of_cpu_cycles"></span><span id="OUT_OF_CPU_CYCLES"></span>

<span data-ttu-id="1415f-393">**Ciclos de CPU agotados** (107)</span><span class="sxs-lookup"><span data-stu-id="1415f-393">**Out of CPU Cycles** (107)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Environment_Problem"></span><span id="software_environment_problem"></span><span id="SOFTWARE_ENVIRONMENT_PROBLEM"></span>

<span data-ttu-id="1415f-394">**Problema del entorno de software** (108)</span><span class="sxs-lookup"><span data-stu-id="1415f-394">**Software Environment Problem** (108)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Download_Failure"></span><span id="software_download_failure"></span><span id="SOFTWARE_DOWNLOAD_FAILURE"></span>

<span data-ttu-id="1415f-395">**Error de descarga de software** (109)</span><span class="sxs-lookup"><span data-stu-id="1415f-395">**Software Download Failure** (109)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Reinitialized"></span><span id="element_reinitialized"></span><span id="ELEMENT_REINITIALIZED"></span>

<span data-ttu-id="1415f-396">**Elemento reinicializado** (110)</span><span class="sxs-lookup"><span data-stu-id="1415f-396">**Element Reinitialized** (110)</span></span>


</dt> <dd></dd> <dt>

<span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>

<span data-ttu-id="1415f-397">**Tiempo de espera** (111)</span><span class="sxs-lookup"><span data-stu-id="1415f-397">**Timeout** (111)</span></span>


</dt> <dd></dd> <dt>

<span id="Logging_Problems"></span><span id="logging_problems"></span><span id="LOGGING_PROBLEMS"></span>

<span data-ttu-id="1415f-398">**Problemas de registro** (112)</span><span class="sxs-lookup"><span data-stu-id="1415f-398">**Logging Problems** (112)</span></span>


</dt> <dd></dd> <dt>

<span id="Leak_Detected"></span><span id="leak_detected"></span><span id="LEAK_DETECTED"></span>

<span data-ttu-id="1415f-399">**Pérdida detectada** (113)</span><span class="sxs-lookup"><span data-stu-id="1415f-399">**Leak Detected** (113)</span></span>


</dt> <dd></dd> <dt>

<span id="Protection_Mechanism_Failure"></span><span id="protection_mechanism_failure"></span><span id="PROTECTION_MECHANISM_FAILURE"></span>

<span data-ttu-id="1415f-400">**Error del mecanismo de protección** (114)</span><span class="sxs-lookup"><span data-stu-id="1415f-400">**Protection Mechanism Failure** (114)</span></span>


</dt> <dd></dd> <dt>

<span id="Protecting_Resource_Failure"></span><span id="protecting_resource_failure"></span><span id="PROTECTING_RESOURCE_FAILURE"></span>

<span data-ttu-id="1415f-401">**Error de protección de recursos** (115)</span><span class="sxs-lookup"><span data-stu-id="1415f-401">**Protecting Resource Failure** (115)</span></span>


</dt> <dd></dd> <dt>

<span id="Database_Inconsistency"></span><span id="database_inconsistency"></span><span id="DATABASE_INCONSISTENCY"></span>

<span data-ttu-id="1415f-402">Incoherencia de la **base de datos** (116)</span><span class="sxs-lookup"><span data-stu-id="1415f-402">**Database Inconsistency** (116)</span></span>


</dt> <dd></dd> <dt>

<span id="Authentication_Failure"></span><span id="authentication_failure"></span><span id="AUTHENTICATION_FAILURE"></span>

<span data-ttu-id="1415f-403">**Error de autenticación** (117)</span><span class="sxs-lookup"><span data-stu-id="1415f-403">**Authentication Failure** (117)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_of_Confidentiality"></span><span id="breach_of_confidentiality"></span><span id="BREACH_OF_CONFIDENTIALITY"></span>

<span data-ttu-id="1415f-404">**Infracción de la confidencialidad** (118)</span><span class="sxs-lookup"><span data-stu-id="1415f-404">**Breach of Confidentiality** (118)</span></span>


</dt> <dd></dd> <dt>

<span id="Cable_Tamper"></span><span id="cable_tamper"></span><span id="CABLE_TAMPER"></span>

<span data-ttu-id="1415f-405">**Manipulación de cables** (119)</span><span class="sxs-lookup"><span data-stu-id="1415f-405">**Cable Tamper** (119)</span></span>


</dt> <dd></dd> <dt>

<span id="Delayed_Information"></span><span id="delayed_information"></span><span id="DELAYED_INFORMATION"></span>

<span data-ttu-id="1415f-406">**Información retrasada** (120)</span><span class="sxs-lookup"><span data-stu-id="1415f-406">**Delayed Information** (120)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplicate_Information"></span><span id="duplicate_information"></span><span id="DUPLICATE_INFORMATION"></span>

<span data-ttu-id="1415f-407">**Información duplicada** (121)</span><span class="sxs-lookup"><span data-stu-id="1415f-407">**Duplicate Information** (121)</span></span>


</dt> <dd></dd> <dt>

<span id="Information_Missing"></span><span id="information_missing"></span><span id="INFORMATION_MISSING"></span>

<span data-ttu-id="1415f-408">**Falta información** (122)</span><span class="sxs-lookup"><span data-stu-id="1415f-408">**Information Missing** (122)</span></span>


</dt> <dd></dd> <dt>

<span id="Information_Modification"></span><span id="information_modification"></span><span id="INFORMATION_MODIFICATION"></span>

<span data-ttu-id="1415f-409">**Modificación** de la información (123)</span><span class="sxs-lookup"><span data-stu-id="1415f-409">**Information Modification** (123)</span></span>


</dt> <dd></dd> <dt>

<span id="Information_Out_of_Sequence"></span><span id="information_out_of_sequence"></span><span id="INFORMATION_OUT_OF_SEQUENCE"></span>

<span data-ttu-id="1415f-410">**Información fuera de secuencia** (124)</span><span class="sxs-lookup"><span data-stu-id="1415f-410">**Information Out of Sequence** (124)</span></span>


</dt> <dd></dd> <dt>

<span id="Key_Expired"></span><span id="key_expired"></span><span id="KEY_EXPIRED"></span>

<span data-ttu-id="1415f-411">**Clave expirada** (125)</span><span class="sxs-lookup"><span data-stu-id="1415f-411">**Key Expired** (125)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Repudiation_Failure"></span><span id="non-repudiation_failure"></span><span id="NON-REPUDIATION_FAILURE"></span>

<span data-ttu-id="1415f-412">**Error sin repudio** (126)</span><span class="sxs-lookup"><span data-stu-id="1415f-412">**Non-Repudiation Failure** (126)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_Hours_Activity"></span><span id="out_of_hours_activity"></span><span id="OUT_OF_HOURS_ACTIVITY"></span>

<span data-ttu-id="1415f-413">**Actividad fuera de horas** (127)</span><span class="sxs-lookup"><span data-stu-id="1415f-413">**Out of Hours Activity** (127)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_Service"></span><span id="out_of_service"></span><span id="OUT_OF_SERVICE"></span>

<span data-ttu-id="1415f-414">**Fuera de servicio** (128)</span><span class="sxs-lookup"><span data-stu-id="1415f-414">**Out of Service** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="Procedural_Error"></span><span id="procedural_error"></span><span id="PROCEDURAL_ERROR"></span>

<span data-ttu-id="1415f-415">**Error de procedimiento** (129)</span><span class="sxs-lookup"><span data-stu-id="1415f-415">**Procedural Error** (129)</span></span>


</dt> <dd></dd> <dt>

<span id="Unexpected_Information"></span><span id="unexpected_information"></span><span id="UNEXPECTED_INFORMATION"></span>

<span data-ttu-id="1415f-416">**Información inesperada** (130)</span><span class="sxs-lookup"><span data-stu-id="1415f-416">**Unexpected Information** (130)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="1415f-417">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="1415f-417">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1415f-418">**ProbableCauseDescription**</span><span class="sxs-lookup"><span data-stu-id="1415f-418">**ProbableCauseDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1415f-419">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1415f-419">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1415f-420">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1415f-420">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1415f-421">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ error de CIM**.**ProbableCause**")</span><span class="sxs-lookup"><span data-stu-id="1415f-421">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**ProbableCause**")</span></span>
</dt> </dl>

<span data-ttu-id="1415f-422">Cadena de forma libre que describe la causa probable del error, cuando la propiedad **ProbableCause** se establece en "1" (otro).</span><span class="sxs-lookup"><span data-stu-id="1415f-422">A free-form string that describes the probable cause of the error, when the **ProbableCause** property is set to "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="1415f-423">**RecommendedActions**</span><span class="sxs-lookup"><span data-stu-id="1415f-423">**RecommendedActions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1415f-424">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="1415f-424">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1415f-425">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1415f-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1415f-426">Matriz de cadenas de formato libre que describen las acciones recomendadas que se deben realizar para resolver el error.</span><span class="sxs-lookup"><span data-stu-id="1415f-426">An array of free-form strings that describe the recommended actions to take to resolve the error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1415f-427">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1415f-427">Requirements</span></span>



| <span data-ttu-id="1415f-428">Requisito</span><span class="sxs-lookup"><span data-stu-id="1415f-428">Requirement</span></span> | <span data-ttu-id="1415f-429">Value</span><span class="sxs-lookup"><span data-stu-id="1415f-429">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1415f-430">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1415f-430">Minimum supported client</span></span><br/> | <span data-ttu-id="1415f-431">Windows 8</span><span class="sxs-lookup"><span data-stu-id="1415f-431">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="1415f-432">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1415f-432">Minimum supported server</span></span><br/> | <span data-ttu-id="1415f-433">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1415f-433">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="1415f-434">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1415f-434">Namespace</span></span><br/>                | <span data-ttu-id="1415f-435">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="1415f-435">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1415f-436">MOF</span><span class="sxs-lookup"><span data-stu-id="1415f-436">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1415f-437"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1415f-437"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1415f-438">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1415f-438">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1415f-439"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1415f-439"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

