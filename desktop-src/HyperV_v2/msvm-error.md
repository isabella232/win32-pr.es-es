---
description: Contiene información sobre la gravedad, la causa, las acciones recomendadas y otros datos relacionados con el error de una operación CIM.
ms.assetid: 128B9ECE-D26C-4A7D-BFB7-69CD986B0DBA
title: Msvm_Error (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Error
- Msvm_Error.ErrorType
- Msvm_Error.OtherErrorType
- Msvm_Error.OwningEntity
- Msvm_Error.MessageID
- Msvm_Error.Message
- Msvm_Error.MessageArguments
- Msvm_Error.PerceivedSeverity
- Msvm_Error.ProbableCause
- Msvm_Error.ProbableCauseDescription
- Msvm_Error.RecommendedActions
- Msvm_Error.ErrorSource
- Msvm_Error.ErrorSourceFormat
- Msvm_Error.OtherErrorSourceFormat
- Msvm_Error.CIMStatusCode
- Msvm_Error.CIMStatusCodeDescription
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 56b3b30f1d64146db2554d097b11104df09ba018
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082719"
---
# <a name="msvm_error-class"></a><span data-ttu-id="b405d-103">MSVM ( \_ clase de error)</span><span class="sxs-lookup"><span data-stu-id="b405d-103">Msvm\_Error class</span></span>

<span data-ttu-id="b405d-104">Una clase especializada que contiene información sobre la gravedad, la causa, las acciones recomendadas y otros datos relacionados con el error de una operación CIM.</span><span class="sxs-lookup"><span data-stu-id="b405d-104">A specialized class that contains information about the severity, cause, recommended actions, and other data related to the failure of a CIM Operation.</span></span>

<span data-ttu-id="b405d-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b405d-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b405d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b405d-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Error : CIM_Error
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

## <a name="members"></a><span data-ttu-id="b405d-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="b405d-107">Members</span></span>

<span data-ttu-id="b405d-108">La clase de **\_ error MSVM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b405d-108">The **Msvm\_Error** class has these types of members:</span></span>

-   [<span data-ttu-id="b405d-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b405d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b405d-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b405d-110">Properties</span></span>

<span data-ttu-id="b405d-111">La clase de **\_ error MSVM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b405d-111">The **Msvm\_Error** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b405d-112">**CIMStatusCode**</span><span class="sxs-lookup"><span data-stu-id="b405d-112">**CIMStatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b405d-113">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b405d-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b405d-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b405d-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b405d-115">El código de estado de CIM que caracteriza esta instancia.</span><span class="sxs-lookup"><span data-stu-id="b405d-115">The CIM status code that characterizes this instance.</span></span> <span data-ttu-id="b405d-116">Esta propiedad define los códigos de estado que pueden ser devueltos por un servidor CIM compatible o un agente de escucha.</span><span class="sxs-lookup"><span data-stu-id="b405d-116">This property defines the status codes that may be return by a conforming CIM Server or Listener.</span></span> <span data-ttu-id="b405d-117">No todos los códigos de estado son válidos para cada operación.</span><span class="sxs-lookup"><span data-stu-id="b405d-117">Not all status codes are valid for each operation.</span></span> <span data-ttu-id="b405d-118">La especificación de cada operación debe definir los códigos de estado que puede devolver esa operación.</span><span class="sxs-lookup"><span data-stu-id="b405d-118">The specification for each operation should define the status codes that may be returned by that operation.</span></span> <span data-ttu-id="b405d-119">Se definen los siguientes valores para el código de estado de CIM.</span><span class="sxs-lookup"><span data-stu-id="b405d-119">The following values for CIM status code are defined.</span></span> <span data-ttu-id="b405d-120">Esta propiedad se hereda del [**\_ error de CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b405d-120">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>



| <span data-ttu-id="b405d-121">Value</span><span class="sxs-lookup"><span data-stu-id="b405d-121">Value</span></span>                                                                                                                                                                                                                                                                                          | <span data-ttu-id="b405d-122">Significado</span><span class="sxs-lookup"><span data-stu-id="b405d-122">Meaning</span></span>                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <span id="CIM_ERR_FAILED"></span><span id="cim_err_failed"></span><dl> <span data-ttu-id="b405d-123"><dt>**CIM \_ \_Error de Err**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b405d-123"><dt>**CIM\_ERR\_FAILED**</dt> <dt>1</dt></span></span> </dl>                                                                       | <span data-ttu-id="b405d-124">Se produjo un error general que no está incluido en un código de error más específico.</span><span class="sxs-lookup"><span data-stu-id="b405d-124">A general error occurred that is not covered by a more specific error code.</span></span><br/>    |
| <span id="CIM_ERR_ACCESS_DENIED"></span><span id="cim_err_access_denied"></span><dl> <span data-ttu-id="b405d-125"><dt>**CIM \_ ERROR de \_ acceso \_ denegado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b405d-125"><dt>**CIM\_ERR\_ACCESS\_DENIED**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="b405d-126">El acceso a un recurso CIM no estaba disponible para el cliente.</span><span class="sxs-lookup"><span data-stu-id="b405d-126">Access to a CIM resource was not available to the client.</span></span><br/>                      |
| <span id="CIM_ERR_INVALID_NAMESPACE"></span><span id="cim_err_invalid_namespace"></span><dl> <span data-ttu-id="b405d-127"><dt>**CIM \_ ERROR \_ de \_ espacio de nombres 3 no válido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b405d-127"><dt>**CIM\_ERR\_INVALID\_NAMESPACE**</dt> <dt>3</dt></span></span> </dl>                                     | <span data-ttu-id="b405d-128">El espacio de nombres de destino no existe.</span><span class="sxs-lookup"><span data-stu-id="b405d-128">The target namespace does not exist.</span></span><br/>                                           |
| <span id="CIM_ERR_INVALID_PARAMETER"></span><span id="cim_err_invalid_parameter"></span><dl> <span data-ttu-id="b405d-129"><dt>**CIM \_ ERROR \_ de \_ parámetro 4 no válido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b405d-129"><dt>**CIM\_ERR\_INVALID\_PARAMETER**</dt> <dt>4</dt></span></span> </dl>                                     | <span data-ttu-id="b405d-130">Uno o varios valores de parámetro pasados al método no eran válidos.</span><span class="sxs-lookup"><span data-stu-id="b405d-130">One or more parameter values passed to the method were invalid.</span></span><br/>                |
| <span id="CIM_ERR_INVALID_CLASS"></span><span id="cim_err_invalid_class"></span><dl> <span data-ttu-id="b405d-131"><dt>**CIM \_ ERR \_ \_ clase 5 no válida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b405d-131"><dt>**CIM\_ERR\_INVALID\_CLASS**</dt> <dt>5</dt></span></span> </dl>                                                 | <span data-ttu-id="b405d-132">La clase especificada no existe.</span><span class="sxs-lookup"><span data-stu-id="b405d-132">The specified class does not exist.</span></span><br/>                                            |
| <span id="CIM_ERR_NOT_FOUND"></span><span id="cim_err_not_found"></span><dl> <span data-ttu-id="b405d-133"><dt>**CIM \_ \_No \_ se encontró el error**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="b405d-133"><dt>**CIM\_ERR\_NOT\_FOUND**</dt> <dt>6</dt></span></span> </dl>                                                             | <span data-ttu-id="b405d-134">No se encontró el objeto solicitado.</span><span class="sxs-lookup"><span data-stu-id="b405d-134">The requested object could not be found.</span></span><br/>                                       |
| <span id="CIM_ERR_NOT_SUPPORTED"></span><span id="cim_err_not_supported"></span><dl> <span data-ttu-id="b405d-135"><dt>**CIM \_ \_No se \_ admite el error**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="b405d-135"><dt>**CIM\_ERR\_NOT\_SUPPORTED**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="b405d-136">No se admite la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="b405d-136">The requested operation is not supported.</span></span><br/>                                      |
| <span id="CIM_ERR_CLASS_HAS_CHILDREN"></span><span id="cim_err_class_has_children"></span><dl> <span data-ttu-id="b405d-137"><dt>**CIM \_ La \_ clase Err \_ tiene los \_ elementos secundarios**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="b405d-137"><dt>**CIM\_ERR\_CLASS\_HAS\_CHILDREN**</dt> <dt>8</dt></span></span> </dl>                                 | <span data-ttu-id="b405d-138">La operación no se puede llevar a cabo en esta clase porque tiene instancias.</span><span class="sxs-lookup"><span data-stu-id="b405d-138">Operation cannot be carried out on this class because it has instances.</span></span><br/>        |
| <span id="CIM_ERR_CLASS_HAS_INSTANCES"></span><span id="cim_err_class_has_instances"></span><dl> <span data-ttu-id="b405d-139"><dt>**CIM \_ La \_ clase Err \_ tiene \_ instancias**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="b405d-139"><dt>**CIM\_ERR\_CLASS\_HAS\_INSTANCES**</dt> <dt>9</dt></span></span> </dl>                              | <span data-ttu-id="b405d-140">No se puede realizar la operación en esta clase porque tiene instancias.</span><span class="sxs-lookup"><span data-stu-id="b405d-140">Operation cannot be carried out on this class since it has instances.</span></span><br/>          |
| <span id="CIM_ERR_INVALID_SUPERCLASS"></span><span id="cim_err_invalid_superclass"></span><dl> <span data-ttu-id="b405d-141"><dt>**CIM \_ ERROR de la \_ \_ superclase 10 no válida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b405d-141"><dt>**CIM\_ERR\_INVALID\_SUPERCLASS**</dt> <dt>10</dt></span></span> </dl>                                 | <span data-ttu-id="b405d-142">No se puede realizar la operación porque la superclase especificada no existe.</span><span class="sxs-lookup"><span data-stu-id="b405d-142">Operation cannot be carried out since the specified superclass does not exist.</span></span><br/> |
| <span id="CIM_ERR_ALREADY_EXISTS"></span><span id="cim_err_already_exists"></span><dl> <span data-ttu-id="b405d-143"><dt>**CIM \_ ERR \_ ya \_ existe**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="b405d-143"><dt>**CIM\_ERR\_ALREADY\_EXISTS**</dt> <dt>11</dt></span></span> </dl>                                             | <span data-ttu-id="b405d-144">No se puede realizar la operación porque ya existe un objeto.</span><span class="sxs-lookup"><span data-stu-id="b405d-144">Operation cannot be carried out because an object already exists.</span></span><br/>              |
| <span id="CIM_ERR_NO_SUCH_PROPERTY"></span><span id="cim_err_no_such_property"></span><dl> <span data-ttu-id="b405d-145"><dt>**CIM \_ NO se trata de la \_ \_ \_ propiedad**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="b405d-145"><dt>**CIM\_ERR\_NO\_SUCH\_PROPERTY**</dt> <dt>12</dt></span></span> </dl>                                      | <span data-ttu-id="b405d-146">La propiedad especificada no existe.</span><span class="sxs-lookup"><span data-stu-id="b405d-146">The specified Property does not exist.</span></span><br/>                                         |
| <span id="CIM_ERR_TYPE_MISMATCH"></span><span id="cim_err_type_mismatch"></span><dl> <span data-ttu-id="b405d-147"><dt>**CIM \_ Error \_ de \_ coincidencia de tipo de error**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="b405d-147"><dt>**CIM\_ERR\_TYPE\_MISMATCH**</dt> <dt>13</dt></span></span> </dl>                                                | <span data-ttu-id="b405d-148">El valor proporcionado no es compatible con el tipo.</span><span class="sxs-lookup"><span data-stu-id="b405d-148">The value supplied is incompatible with the type.</span></span><br/>                              |
| <span id="CIM_ERR_QUERY_LANGUAGE_NOT_SUPPORTED"></span><span id="cim_err_query_language_not_supported"></span><dl> <span data-ttu-id="b405d-149"><dt>**CIM \_ \_No se \_ \_ \_ admite el lenguaje de consulta de Err**</dt> <dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="b405d-149"><dt>**CIM\_ERR\_QUERY\_LANGUAGE\_NOT\_SUPPORTED**</dt> <dt>14</dt></span></span> </dl> | <span data-ttu-id="b405d-150">No se reconoce o no se admite el lenguaje de consulta.</span><span class="sxs-lookup"><span data-stu-id="b405d-150">The query language is not recognized or supported.</span></span><br/>                             |
| <span id="CIM_ERR_INVALID_QUERY"></span><span id="cim_err_invalid_query"></span><dl> <span data-ttu-id="b405d-151"><dt>**CIM \_ ERR \_ \_ consulta no válida**</dt> <dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="b405d-151"><dt>**CIM\_ERR\_INVALID\_QUERY**</dt> <dt>15</dt></span></span> </dl>                                                | <span data-ttu-id="b405d-152">La consulta no es válida para el lenguaje de consulta especificado.</span><span class="sxs-lookup"><span data-stu-id="b405d-152">The query is not valid for the specified query language.</span></span><br/>                       |
| <span id="CIM_ERR_METHOD_NOT_AVAILABLE"></span><span id="cim_err_method_not_available"></span><dl> <span data-ttu-id="b405d-153"><dt>**CIM \_ \_Método Err \_ no \_ disponible**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="b405d-153"><dt>**CIM\_ERR\_METHOD\_NOT\_AVAILABLE**</dt> <dt>16</dt></span></span> </dl>                          | <span data-ttu-id="b405d-154">No se pudo ejecutar el método extrínseco.</span><span class="sxs-lookup"><span data-stu-id="b405d-154">The extrinsic method could not be executed.</span></span><br/>                                    |
| <span id="CIM_ERR_METHOD_NOT_FOUND"></span><span id="cim_err_method_not_found"></span><dl> <span data-ttu-id="b405d-155"><dt>**CIM \_ \_Método Err \_ no \_ encontrado**</dt> <dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="b405d-155"><dt>**CIM\_ERR\_METHOD\_NOT\_FOUND**</dt> <dt>17</dt></span></span> </dl>                                      | <span data-ttu-id="b405d-156">El método extrínseco especificado no existe.</span><span class="sxs-lookup"><span data-stu-id="b405d-156">The specified extrinsic method does not exist.</span></span><br/>                                 |
| <span id="CIM_ERR_UNEXPECTED_RESPONSE"></span><span id="cim_err_unexpected_response"></span><dl> <span data-ttu-id="b405d-157"><dt>**CIM \_ \_ \_ Respuesta inesperada de Err**</dt> <dt>18</dt></span><span class="sxs-lookup"><span data-stu-id="b405d-157"><dt>**CIM\_ERR\_UNEXPECTED\_RESPONSE**</dt> <dt>18</dt></span></span> </dl>                              | <span data-ttu-id="b405d-158">No se esperaba la respuesta devuelta a la operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="b405d-158">The returned response to the asynchronous operation was not expected.</span></span><br/>          |
| <span id="CIM_ERR_INVALID_RESPONSE_DESTINATION"></span><span id="cim_err_invalid_response_destination"></span><dl> <span data-ttu-id="b405d-159"><dt>**CIM \_ ERROR \_ de \_ \_ destino de respuesta no válido**</dt> <dt>19</dt></span><span class="sxs-lookup"><span data-stu-id="b405d-159"><dt>**CIM\_ERR\_INVALID\_RESPONSE\_DESTINATION**</dt> <dt>19</dt></span></span> </dl>  | <span data-ttu-id="b405d-160">El destino especificado para la respuesta asincrónica no es válido.</span><span class="sxs-lookup"><span data-stu-id="b405d-160">The specified destination for the asynchronous response is not valid.</span></span><br/>          |
| <span id="CIM_ERR_NAMESPACE_NOT_EMPTY"></span><span id="cim_err_namespace_not_empty"></span><dl> <span data-ttu-id="b405d-161"><dt>**CIM \_ \_Espacio de nombres Err \_ no \_ vacío**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="b405d-161"><dt>**CIM\_ERR\_NAMESPACE\_NOT\_EMPTY**</dt> <dt>20</dt></span></span> </dl>                             | <span data-ttu-id="b405d-162">El espacio de nombres especificado no está vacío.</span><span class="sxs-lookup"><span data-stu-id="b405d-162">The specified namespace is not empty.</span></span><br/>                                          |
| <span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span><dl> <span data-ttu-id="b405d-163"><dt>**DMTF reservado**</dt> <dt>21 = *valor*</dt></span><span class="sxs-lookup"><span data-stu-id="b405d-163"><dt>**DMTF Reserved**</dt> <dt>21 = *value* </dt></span></span> </dl>                            | <span data-ttu-id="b405d-164">Valores reservados.</span><span class="sxs-lookup"><span data-stu-id="b405d-164">Reserved values.</span></span><br/>                                                               |



 

</dd> <dt>

<span data-ttu-id="b405d-165">**CIMStatusCodeDescription**</span><span class="sxs-lookup"><span data-stu-id="b405d-165">**CIMStatusCodeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b405d-166">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b405d-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b405d-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b405d-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b405d-168">Cadena que contiene una descripción legible por el usuario de la propiedad **CIMStatusCode** .</span><span class="sxs-lookup"><span data-stu-id="b405d-168">A string containing a user-readable description of the **CIMStatusCode** property.</span></span> <span data-ttu-id="b405d-169">Esta descripción puede extender, pero debe ser coherente con, la definición de **CIMStatusCode**.</span><span class="sxs-lookup"><span data-stu-id="b405d-169">This description may extend, but must be consistent with, the definition of **CIMStatusCode**.</span></span> <span data-ttu-id="b405d-170">Esta propiedad se hereda del [**\_ error de CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b405d-170">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b405d-171">**ErrorSource**</span><span class="sxs-lookup"><span data-stu-id="b405d-171">**ErrorSource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b405d-172">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b405d-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b405d-173">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b405d-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b405d-174">La información de identificación de la entidad (la instancia) que genera el error.</span><span class="sxs-lookup"><span data-stu-id="b405d-174">The identifying information of the entity (the instance) generating the error.</span></span> <span data-ttu-id="b405d-175">Si esta entidad se modela en el esquema CIM, esta propiedad contiene la ruta de acceso de la instancia codificada como un parámetro de cadena.</span><span class="sxs-lookup"><span data-stu-id="b405d-175">If this entity is modeled in the CIM Schema, this property contains the path of the instance encoded as a string parameter.</span></span> <span data-ttu-id="b405d-176">Si no se modela, la propiedad contiene alguna cadena de identificación que nombra la entidad que generó el error.</span><span class="sxs-lookup"><span data-stu-id="b405d-176">If not modeled, the property contains some identifying string that names the entity that generated the error.</span></span> <span data-ttu-id="b405d-177">Se da formato a la ruta de acceso o a la cadena de identificación según la propiedad **ErrorSourceFormat** .</span><span class="sxs-lookup"><span data-stu-id="b405d-177">The path or identifying string is formatted per the **ErrorSourceFormat** property.</span></span> <span data-ttu-id="b405d-178">Esta propiedad se hereda del [**\_ error de CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b405d-178">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b405d-179">**ErrorSourceFormat**</span><span class="sxs-lookup"><span data-stu-id="b405d-179">**ErrorSourceFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b405d-180">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b405d-180">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b405d-181">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b405d-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b405d-182">El formato de la propiedad **ErrorSource** se interpreta según el valor de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="b405d-182">The format of the **ErrorSource** property is interpretable based on the value of this property.</span></span> <span data-ttu-id="b405d-183">Esta propiedad se hereda del [**\_ error de CIM**](/previous-versions//cc150671(v=vs.85))y siempre está establecida en 0.</span><span class="sxs-lookup"><span data-stu-id="b405d-183">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)), and it is always set to 0.</span></span>



| <span data-ttu-id="b405d-184">Value</span><span class="sxs-lookup"><span data-stu-id="b405d-184">Value</span></span>                                                                                                                                                                                                                                                        | <span data-ttu-id="b405d-185">Significado</span><span class="sxs-lookup"><span data-stu-id="b405d-185">Meaning</span></span>                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="b405d-186"><dt>**Desconocido**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b405d-186"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="b405d-187">Una aplicación cliente CIM no reconoce el formato o lo interpreta de forma significativa.</span><span class="sxs-lookup"><span data-stu-id="b405d-187">The format is unknown or not meaningfully interpretable by a CIM client application.</span></span><br/>                                         |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="b405d-188"><dt>**Otro**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b405d-188"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                          | <span data-ttu-id="b405d-189">El formato se define mediante el valor de la propiedad **OtherErrorSourceFormat** .</span><span class="sxs-lookup"><span data-stu-id="b405d-189">The format is defined by the value of the **OtherErrorSourceFormat** property.</span></span><br/>                                               |
| <span id="CIMObjectHandle"></span><span id="cimobjecthandle"></span><span id="CIMOBJECTHANDLE"></span><dl> <span data-ttu-id="b405d-190"><dt>**CIMObjectHandle**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b405d-190"><dt>**CIMObjectHandle**</dt> <dt>2 </dt></span></span> </dl> | <span data-ttu-id="b405d-191">Un identificador de objeto CIM, codificado mediante la sintaxis MOF definida para el objectHandle que no es de terminal, se usa para identificar la entidad.</span><span class="sxs-lookup"><span data-stu-id="b405d-191">A CIM Object Handle, encoded using the MOF syntax defined for the objectHandle non-terminal, is used to identify the entity.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b405d-192">**ErrorType**</span><span class="sxs-lookup"><span data-stu-id="b405d-192">**ErrorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b405d-193">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b405d-193">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b405d-194">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b405d-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b405d-195">Clasificación principal del error.</span><span class="sxs-lookup"><span data-stu-id="b405d-195">Primary classification of the error.</span></span> <span data-ttu-id="b405d-196">Se definen los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="b405d-196">The following values are defined.</span></span> <span data-ttu-id="b405d-197">Esta propiedad se hereda del [**\_ error de CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b405d-197">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>



| <span data-ttu-id="b405d-198">Value</span><span class="sxs-lookup"><span data-stu-id="b405d-198">Value</span></span>                                                                                                                                                                                                                                                                                                         | <span data-ttu-id="b405d-199">Significado</span><span class="sxs-lookup"><span data-stu-id="b405d-199">Meaning</span></span>                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="b405d-200"><dt>**Desconocido**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b405d-200"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                                                   |                                                                                                                                                          |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="b405d-201"><dt>**Otro**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b405d-201"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                                                           |                                                                                                                                                          |
| <span id="Communications_Error"></span><span id="communications_error"></span><span id="COMMUNICATIONS_ERROR"></span><dl> <span data-ttu-id="b405d-202"><dt>**Error de comunicaciones**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b405d-202"><dt>**Communications Error**</dt> <dt>2</dt></span></span> </dl>                               | <span data-ttu-id="b405d-203">Los errores de este tipo están asociados principalmente a los procedimientos y/o procesos necesarios para transmitir información de un punto a otro.</span><span class="sxs-lookup"><span data-stu-id="b405d-203">Errors of this type are principally associated with the procedures and/or processes required to convey information from one point to another.</span></span><br/> |
| <span id="Quality_of_Service_Error"></span><span id="quality_of_service_error"></span><span id="QUALITY_OF_SERVICE_ERROR"></span><dl> <span data-ttu-id="b405d-204"><dt>**Error de calidad de servicio**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="b405d-204"><dt>**Quality of Service Error**</dt> <dt>3</dt></span></span> </dl>               | <span data-ttu-id="b405d-205">Los errores de este tipo están asociados principalmente a errores que dan lugar a una funcionalidad o un rendimiento reducidos.</span><span class="sxs-lookup"><span data-stu-id="b405d-205">Errors of this type are principally associated with failures that result in reduced functionality or performance.</span></span><br/>                             |
| <span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span><dl> <span data-ttu-id="b405d-206"><dt>**Error de software**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="b405d-206"><dt>**Software Error**</dt> <dt>4</dt></span></span> </dl>                                                       | <span data-ttu-id="b405d-207">Un error de este tipo está asociado principalmente a un software o un error de procesamiento.</span><span class="sxs-lookup"><span data-stu-id="b405d-207">Error of this type are principally associated with a software or processing fault.</span></span><br/>                                                            |
| <span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span><dl> <span data-ttu-id="b405d-208"><dt>**Error de hardware**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="b405d-208"><dt>**Hardware Error**</dt> <dt>5</dt></span></span> </dl>                                                       | <span data-ttu-id="b405d-209">Los errores de este tipo están asociados principalmente a un error de hardware o de equipo.</span><span class="sxs-lookup"><span data-stu-id="b405d-209">Errors of this type are principally associated with an equipment or hardware failure.</span></span><br/>                                                         |
| <span id="Environmental_Error"></span><span id="environmental_error"></span><span id="ENVIRONMENTAL_ERROR"></span><dl> <span data-ttu-id="b405d-210"><dt>**Error de entorno**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="b405d-210"><dt>**Environmental Error**</dt> <dt>6</dt></span></span> </dl>                                   | <span data-ttu-id="b405d-211">Los errores de este tipo están asociados principalmente a una condición de error relacionada con la instalación u otras consideraciones del entorno.</span><span class="sxs-lookup"><span data-stu-id="b405d-211">Errors of this type are principally associated with a failure condition relating to the facility, or other environmental considerations.</span></span><br/>      |
| <span id="Security_Error"></span><span id="security_error"></span><span id="SECURITY_ERROR"></span><dl> <span data-ttu-id="b405d-212"><dt>**Error de seguridad**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="b405d-212"><dt>**Security Error**</dt> <dt>7</dt></span></span> </dl>                                                       | <span data-ttu-id="b405d-213">Los errores de este tipo están asociados a infracciones de seguridad, detección de virus y problemas similares.</span><span class="sxs-lookup"><span data-stu-id="b405d-213">Errors of this type are associated with security violations, detection of viruses, and similar issues.</span></span><br/>                                        |
| <span id="Oversubscription_Error"></span><span id="oversubscription_error"></span><span id="OVERSUBSCRIPTION_ERROR"></span><dl> <span data-ttu-id="b405d-214"><dt>**Error de sobresuscripción**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="b405d-214"><dt>**Oversubscription Error**</dt> <dt>8</dt></span></span> </dl>                       | <span data-ttu-id="b405d-215">Los errores de este tipo están asociados principalmente al error de asignación de recursos suficientes para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="b405d-215">Errors of this type are principally associated with the failure to allocate sufficient resources to complete the operation.</span></span><br/>                   |
| <span id="Unavailable_Resource_Error"></span><span id="unavailable_resource_error"></span><span id="UNAVAILABLE_RESOURCE_ERROR"></span><dl> <span data-ttu-id="b405d-216"><dt>**Error de recurso no disponible**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="b405d-216"><dt>**Unavailable Resource Error**</dt> <dt>9</dt></span></span> </dl>       | <span data-ttu-id="b405d-217">Los errores de este tipo están asociados principalmente al error de acceso a un recurso necesario.</span><span class="sxs-lookup"><span data-stu-id="b405d-217">Errors of this type are principally associated with the failure to access a required resource.</span></span><br/>                                                |
| <span id="Unsupported_Operation_Error"></span><span id="unsupported_operation_error"></span><span id="UNSUPPORTED_OPERATION_ERROR"></span><dl> <span data-ttu-id="b405d-218"><dt>**Error de operación 10 no compatible**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b405d-218"><dt>**Unsupported Operation Error**</dt> <dt>10 </dt></span></span> </dl> | <span data-ttu-id="b405d-219">Los errores de este tipo están asociados principalmente a las solicitudes que no se admiten.</span><span class="sxs-lookup"><span data-stu-id="b405d-219">Errors of this type are principally associated with requests that are not supported.</span></span><br/>                                                          |



 

</dd> <dt>

<span data-ttu-id="b405d-220">**Message**</span><span class="sxs-lookup"><span data-stu-id="b405d-220">**Message**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b405d-221">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b405d-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b405d-222">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b405d-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b405d-223">Mensaje con formato.</span><span class="sxs-lookup"><span data-stu-id="b405d-223">The formatted message.</span></span> <span data-ttu-id="b405d-224">Este mensaje se crea aplicando el contenido dinámico del mensaje, que se describe en **MessageArguments**, a la cadena de formato identificada de forma única, dentro del ámbito de **OwningEntity**, por **MessageID**.</span><span class="sxs-lookup"><span data-stu-id="b405d-224">This message is constructed by applying the dynamic content of the message, described in **MessageArguments**, to the format string uniquely identified, within the scope of the **OwningEntity**, by **MessageID**.</span></span> <span data-ttu-id="b405d-225">Esta propiedad se hereda del [**\_ error de CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b405d-225">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b405d-226">**MessageArguments**</span><span class="sxs-lookup"><span data-stu-id="b405d-226">**MessageArguments**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b405d-227">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="b405d-227">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b405d-228">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b405d-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b405d-229">Una matriz que contiene el contenido dinámico del mensaje.</span><span class="sxs-lookup"><span data-stu-id="b405d-229">An array containing the dynamic content of the message.</span></span> <span data-ttu-id="b405d-230">Esta propiedad se hereda del [**\_ error de CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b405d-230">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b405d-231">**Identificador**</span><span class="sxs-lookup"><span data-stu-id="b405d-231">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b405d-232">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b405d-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b405d-233">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b405d-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b405d-234">Cadena opaca que identifica de forma única, dentro del ámbito de **OwningEntity**, el formato del mensaje.</span><span class="sxs-lookup"><span data-stu-id="b405d-234">An opaque string that uniquely identifies, within the scope of the **OwningEntity**, the format of the message.</span></span> <span data-ttu-id="b405d-235">Esta propiedad se hereda del [**\_ error de CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b405d-235">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b405d-236">**OtherErrorSourceFormat**</span><span class="sxs-lookup"><span data-stu-id="b405d-236">**OtherErrorSourceFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b405d-237">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b405d-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b405d-238">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b405d-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b405d-239">Cadena que define los valores de "otros" para **ErrorSourceFormat**.</span><span class="sxs-lookup"><span data-stu-id="b405d-239">A string defining "Other" values for **ErrorSourceFormat**.</span></span> <span data-ttu-id="b405d-240">Este valor debe establecerse en un valor distinto de NULL cuando **ErrorSourceFormat** se establece en un valor de 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="b405d-240">This value must be set to a non-NULL value when **ErrorSourceFormat** is set to a value of 1 (Other).</span></span> <span data-ttu-id="b405d-241">Para todos los demás valores de **ErrorSourceFormat**, el valor de esta cadena debe establecerse en **null**.</span><span class="sxs-lookup"><span data-stu-id="b405d-241">For all other values of **ErrorSourceFormat**, the value of this string must be set to **Null**.</span></span> <span data-ttu-id="b405d-242">Esta propiedad se hereda del [**\_ error de CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b405d-242">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b405d-243">**OtherErrorType**</span><span class="sxs-lookup"><span data-stu-id="b405d-243">**OtherErrorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b405d-244">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b405d-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b405d-245">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b405d-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b405d-246">Cadena que describe el valor de **ErrorType** cuando se especifica 1, (otro), como **ErrorType**.</span><span class="sxs-lookup"><span data-stu-id="b405d-246">A string that describes the **ErrorType** when 1, (Other), is specified as the **ErrorType**.</span></span> <span data-ttu-id="b405d-247">Esta propiedad se hereda del [**\_ error de CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b405d-247">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b405d-248">**OwningEntity**</span><span class="sxs-lookup"><span data-stu-id="b405d-248">**OwningEntity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b405d-249">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b405d-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b405d-250">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b405d-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b405d-251">Cadena que identifica de forma única la entidad propietaria de la definición del formato del mensaje descrito en esta instancia.</span><span class="sxs-lookup"><span data-stu-id="b405d-251">A string that uniquely identifies the entity that owns the definition of the format of the message described in this instance.</span></span> <span data-ttu-id="b405d-252">**OwningEntity** debe incluir un nombre de propiedad intelectual, marca registrada o de otro tipo, que sea propiedad de la entidad comercial o el cuerpo de los estándares que defina el formato.</span><span class="sxs-lookup"><span data-stu-id="b405d-252">**OwningEntity** must include a copyrighted, trademarked, or otherwise unique name that is owned by the business entity or standards body defining the format.</span></span> <span data-ttu-id="b405d-253">Esta propiedad se hereda del [**\_ error de CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b405d-253">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b405d-254">**PerceivedSeverity**</span><span class="sxs-lookup"><span data-stu-id="b405d-254">**PerceivedSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b405d-255">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b405d-255">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b405d-256">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b405d-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b405d-257">Un valor enumerado que describe la gravedad del error desde el punto de vista del notificador: 2-Low debe usarse para problemas no críticos, como parámetros no válidos, uso incorrecto, funcionalidad no admitida.</span><span class="sxs-lookup"><span data-stu-id="b405d-257">An enumerated value that describes the severity of the error from the notifier's point of view: 2 - Low should be used for noncritical issues such as invalid parameters, incorrect usage, unsupported functionality.</span></span> <span data-ttu-id="b405d-258">se debe usar 3-media para indicar que la acción es necesaria, pero la situación no es grave en este momento.</span><span class="sxs-lookup"><span data-stu-id="b405d-258">3 - Medium should be used to indicate action is needed, but the situation is not serious at this time.</span></span> <span data-ttu-id="b405d-259">4-alto debe usarse para indicar que la acción es necesaria ahora.</span><span class="sxs-lookup"><span data-stu-id="b405d-259">4 - High should be used to indicate action is needed now.</span></span> <span data-ttu-id="b405d-260">5: se debe usar fatal para indicar una pérdida de datos o un error irrecuperable del sistema o servicio.</span><span class="sxs-lookup"><span data-stu-id="b405d-260">5 - Fatal should be used to indicate a loss of data or unrecoverable system or service failure.</span></span> <span data-ttu-id="b405d-261">Esta propiedad se hereda del [**\_ error de CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b405d-261">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="b405d-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="b405d-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-263"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Bajo** (2)</span><span class="sxs-lookup"><span data-stu-id="b405d-263"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Low** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-264"><span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>**Medio** (3)</span><span class="sxs-lookup"><span data-stu-id="b405d-264"><span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>**Medium** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-265"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**Alto** (4)</span><span class="sxs-lookup"><span data-stu-id="b405d-265"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**High** (4)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-266"><span id="Fatal_"></span><span id="fatal_"></span><span id="FATAL_"></span>**Grave** (5)</span><span class="sxs-lookup"><span data-stu-id="b405d-266"><span id="Fatal_"></span><span id="fatal_"></span><span id="FATAL_"></span>**Fatal** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b405d-267">**ProbableCause**</span><span class="sxs-lookup"><span data-stu-id="b405d-267">**ProbableCause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b405d-268">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b405d-268">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b405d-269">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b405d-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b405d-270">Valor enumerado que describe la causa probable del error.</span><span class="sxs-lookup"><span data-stu-id="b405d-270">An enumerated value that describes the probable cause of the error.</span></span> <span data-ttu-id="b405d-271">Esta propiedad se hereda del [**\_ error de CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b405d-271">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="b405d-272"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="b405d-272"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-273"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="b405d-273"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-274"><span id="Adapter_Card_Error"></span><span id="adapter_card_error"></span><span id="ADAPTER_CARD_ERROR"></span>**Error de tarjeta/adaptador** (2)</span><span class="sxs-lookup"><span data-stu-id="b405d-274"><span id="Adapter_Card_Error"></span><span id="adapter_card_error"></span><span id="ADAPTER_CARD_ERROR"></span>**Adapter/Card Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-275"><span id="Application_Subsystem_Failure"></span><span id="application_subsystem_failure"></span><span id="APPLICATION_SUBSYSTEM_FAILURE"></span>**Error del subsistema de aplicación** (3)</span><span class="sxs-lookup"><span data-stu-id="b405d-275"><span id="Application_Subsystem_Failure"></span><span id="application_subsystem_failure"></span><span id="APPLICATION_SUBSYSTEM_FAILURE"></span>**Application Subsystem Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-276"><span id="Bandwidth_Reduced"></span><span id="bandwidth_reduced"></span><span id="BANDWIDTH_REDUCED"></span>**Ancho de banda reducido** (4)</span><span class="sxs-lookup"><span data-stu-id="b405d-276"><span id="Bandwidth_Reduced"></span><span id="bandwidth_reduced"></span><span id="BANDWIDTH_REDUCED"></span>**Bandwidth Reduced** (4)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-277"><span id="Connection_Establishment_Error"></span><span id="connection_establishment_error"></span><span id="CONNECTION_ESTABLISHMENT_ERROR"></span>**Error de establecimiento de conexión** (5)</span><span class="sxs-lookup"><span data-stu-id="b405d-277"><span id="Connection_Establishment_Error"></span><span id="connection_establishment_error"></span><span id="CONNECTION_ESTABLISHMENT_ERROR"></span>**Connection Establishment Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-278"><span id="Communications_Protocol_Error"></span><span id="communications_protocol_error"></span><span id="COMMUNICATIONS_PROTOCOL_ERROR"></span>**Error de protocolo de comunicaciones** (6)</span><span class="sxs-lookup"><span data-stu-id="b405d-278"><span id="Communications_Protocol_Error"></span><span id="communications_protocol_error"></span><span id="COMMUNICATIONS_PROTOCOL_ERROR"></span>**Communications Protocol Error** (6)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-279"><span id="Communications_Subsystem_Failure"></span><span id="communications_subsystem_failure"></span><span id="COMMUNICATIONS_SUBSYSTEM_FAILURE"></span>**Error del subsistema de comunicaciones** (7)</span><span class="sxs-lookup"><span data-stu-id="b405d-279"><span id="Communications_Subsystem_Failure"></span><span id="communications_subsystem_failure"></span><span id="COMMUNICATIONS_SUBSYSTEM_FAILURE"></span>**Communications Subsystem Failure** (7)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-280"><span id="Configuration_Customization_Error"></span><span id="configuration_customization_error"></span><span id="CONFIGURATION_CUSTOMIZATION_ERROR"></span>**Error de configuración/personalización** (8)</span><span class="sxs-lookup"><span data-stu-id="b405d-280"><span id="Configuration_Customization_Error"></span><span id="configuration_customization_error"></span><span id="CONFIGURATION_CUSTOMIZATION_ERROR"></span>**Configuration/Customization Error** (8)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-281"><span id="Congestion"></span><span id="congestion"></span><span id="CONGESTION"></span>**Congestión** (9)</span><span class="sxs-lookup"><span data-stu-id="b405d-281"><span id="Congestion"></span><span id="congestion"></span><span id="CONGESTION"></span>**Congestion** (9)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-282"><span id="Corrupt_Data"></span><span id="corrupt_data"></span><span id="CORRUPT_DATA"></span>**Datos dañados** (10)</span><span class="sxs-lookup"><span data-stu-id="b405d-282"><span id="Corrupt_Data"></span><span id="corrupt_data"></span><span id="CORRUPT_DATA"></span>**Corrupt Data** (10)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-283"><span id="CPU_Cycles_Limit_Exceeded"></span><span id="cpu_cycles_limit_exceeded"></span><span id="CPU_CYCLES_LIMIT_EXCEEDED"></span>Se **superó el límite de ciclos de CPU** (11)</span><span class="sxs-lookup"><span data-stu-id="b405d-283"><span id="CPU_Cycles_Limit_Exceeded"></span><span id="cpu_cycles_limit_exceeded"></span><span id="CPU_CYCLES_LIMIT_EXCEEDED"></span>**CPU Cycles Limit Exceeded** (11)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-284"><span id="Dataset_Modem_Error"></span><span id="dataset_modem_error"></span><span id="DATASET_MODEM_ERROR"></span>**Error de conjunto** de</span><span class="sxs-lookup"><span data-stu-id="b405d-284"><span id="Dataset_Modem_Error"></span><span id="dataset_modem_error"></span><span id="DATASET_MODEM_ERROR"></span>**Dataset/Modem Error** (12)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-285"><span id="Degraded_Signal"></span><span id="degraded_signal"></span><span id="DEGRADED_SIGNAL"></span>**Señal degradada** (13)</span><span class="sxs-lookup"><span data-stu-id="b405d-285"><span id="Degraded_Signal"></span><span id="degraded_signal"></span><span id="DEGRADED_SIGNAL"></span>**Degraded Signal** (13)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-286"><span id="DTE-DCE_Interface_Error"></span><span id="dte-dce_interface_error"></span><span id="DTE-DCE_INTERFACE_ERROR"></span>**Error de la interfaz DTE-DCE** (14)</span><span class="sxs-lookup"><span data-stu-id="b405d-286"><span id="DTE-DCE_Interface_Error"></span><span id="dte-dce_interface_error"></span><span id="DTE-DCE_INTERFACE_ERROR"></span>**DTE-DCE Interface Error** (14)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-287"><span id="Enclosure_Door_Open"></span><span id="enclosure_door_open"></span><span id="ENCLOSURE_DOOR_OPEN"></span>Abertura de la **puerta del gabinete** (15)</span><span class="sxs-lookup"><span data-stu-id="b405d-287"><span id="Enclosure_Door_Open"></span><span id="enclosure_door_open"></span><span id="ENCLOSURE_DOOR_OPEN"></span>**Enclosure Door Open** (15)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-288"><span id="Equipment_Malfunction"></span><span id="equipment_malfunction"></span><span id="EQUIPMENT_MALFUNCTION"></span>**Funcionamiento incorrecto del equipo** (16)</span><span class="sxs-lookup"><span data-stu-id="b405d-288"><span id="Equipment_Malfunction"></span><span id="equipment_malfunction"></span><span id="EQUIPMENT_MALFUNCTION"></span>**Equipment Malfunction** (16)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-289"><span id="Excessive_Vibration"></span><span id="excessive_vibration"></span><span id="EXCESSIVE_VIBRATION"></span>**Vibración excesiva** (17)</span><span class="sxs-lookup"><span data-stu-id="b405d-289"><span id="Excessive_Vibration"></span><span id="excessive_vibration"></span><span id="EXCESSIVE_VIBRATION"></span>**Excessive Vibration** (17)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-290"><span id="File_Format_Error"></span><span id="file_format_error"></span><span id="FILE_FORMAT_ERROR"></span>**Error de formato de archivo** (18)</span><span class="sxs-lookup"><span data-stu-id="b405d-290"><span id="File_Format_Error"></span><span id="file_format_error"></span><span id="FILE_FORMAT_ERROR"></span>**File Format Error** (18)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-291"><span id="Fire_Detected"></span><span id="fire_detected"></span><span id="FIRE_DETECTED"></span>**Desencadenamiento detectado** (19)</span><span class="sxs-lookup"><span data-stu-id="b405d-291"><span id="Fire_Detected"></span><span id="fire_detected"></span><span id="FIRE_DETECTED"></span>**Fire Detected** (19)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-292"><span id="Flood_Detected"></span><span id="flood_detected"></span><span id="FLOOD_DETECTED"></span>**Inundación detectada** (20)</span><span class="sxs-lookup"><span data-stu-id="b405d-292"><span id="Flood_Detected"></span><span id="flood_detected"></span><span id="FLOOD_DETECTED"></span>**Flood Detected** (20)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-293"><span id="Framing_Error"></span><span id="framing_error"></span><span id="FRAMING_ERROR"></span>**Error de tramas** (21)</span><span class="sxs-lookup"><span data-stu-id="b405d-293"><span id="Framing_Error"></span><span id="framing_error"></span><span id="FRAMING_ERROR"></span>**Framing Error** (21)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-294"><span id="HVAC_Problem"></span><span id="hvac_problem"></span><span id="HVAC_PROBLEM"></span>**Problema de HVAC** (22)</span><span class="sxs-lookup"><span data-stu-id="b405d-294"><span id="HVAC_Problem"></span><span id="hvac_problem"></span><span id="HVAC_PROBLEM"></span>**HVAC Problem** (22)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-295"><span id="Humidity_Unacceptable"></span><span id="humidity_unacceptable"></span><span id="HUMIDITY_UNACCEPTABLE"></span>**Humedad inaceptable** (23)</span><span class="sxs-lookup"><span data-stu-id="b405d-295"><span id="Humidity_Unacceptable"></span><span id="humidity_unacceptable"></span><span id="HUMIDITY_UNACCEPTABLE"></span>**Humidity Unacceptable** (23)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-296"><span id="I_O_Device_Error"></span><span id="i_o_device_error"></span><span id="I_O_DEVICE_ERROR"></span>**Error de dispositivo de e/s** (24)</span><span class="sxs-lookup"><span data-stu-id="b405d-296"><span id="I_O_Device_Error"></span><span id="i_o_device_error"></span><span id="I_O_DEVICE_ERROR"></span>**I/O Device Error** (24)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-297"><span id="Input_Device_Error"></span><span id="input_device_error"></span><span id="INPUT_DEVICE_ERROR"></span>**Error de dispositivo de entrada** (25)</span><span class="sxs-lookup"><span data-stu-id="b405d-297"><span id="Input_Device_Error"></span><span id="input_device_error"></span><span id="INPUT_DEVICE_ERROR"></span>**Input Device Error** (25)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-298"><span id="LAN_Error"></span><span id="lan_error"></span><span id="LAN_ERROR"></span>**Error de LAN** (26)</span><span class="sxs-lookup"><span data-stu-id="b405d-298"><span id="LAN_Error"></span><span id="lan_error"></span><span id="LAN_ERROR"></span>**LAN Error** (26)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-299"><span id="Non-Toxic_Leak_Detected"></span><span id="non-toxic_leak_detected"></span><span id="NON-TOXIC_LEAK_DETECTED"></span>**Pérdida no tóxica detectada** (27)</span><span class="sxs-lookup"><span data-stu-id="b405d-299"><span id="Non-Toxic_Leak_Detected"></span><span id="non-toxic_leak_detected"></span><span id="NON-TOXIC_LEAK_DETECTED"></span>**Non-Toxic Leak Detected** (27)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-300"><span id="Local_Node_Transmission_Error"></span><span id="local_node_transmission_error"></span><span id="LOCAL_NODE_TRANSMISSION_ERROR"></span>**Error de transmisión del nodo local** (28)</span><span class="sxs-lookup"><span data-stu-id="b405d-300"><span id="Local_Node_Transmission_Error"></span><span id="local_node_transmission_error"></span><span id="LOCAL_NODE_TRANSMISSION_ERROR"></span>**Local Node Transmission Error** (28)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-301"><span id="Loss_of_Frame"></span><span id="loss_of_frame"></span><span id="LOSS_OF_FRAME"></span>**Pérdida de fotograma** (29)</span><span class="sxs-lookup"><span data-stu-id="b405d-301"><span id="Loss_of_Frame"></span><span id="loss_of_frame"></span><span id="LOSS_OF_FRAME"></span>**Loss of Frame** (29)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-302"><span id="Loss_of_Signal"></span><span id="loss_of_signal"></span><span id="LOSS_OF_SIGNAL"></span>**Pérdida de señal** (30)</span><span class="sxs-lookup"><span data-stu-id="b405d-302"><span id="Loss_of_Signal"></span><span id="loss_of_signal"></span><span id="LOSS_OF_SIGNAL"></span>**Loss of Signal** (30)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-303"><span id="__31____________Material_Supply_Exhausted"></span><span id="__31____________material_supply_exhausted"></span><span id="__31____________MATERIAL_SUPPLY_EXHAUSTED"></span>**//31 suministro de material agotado** (31)</span><span class="sxs-lookup"><span data-stu-id="b405d-303"><span id="__31____________Material_Supply_Exhausted"></span><span id="__31____________material_supply_exhausted"></span><span id="__31____________MATERIAL_SUPPLY_EXHAUSTED"></span>**//31 Material Supply Exhausted** (31)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-304"><span id="Multiplexer_Problem"></span><span id="multiplexer_problem"></span><span id="MULTIPLEXER_PROBLEM"></span>**Problema del multiplexor** (32)</span><span class="sxs-lookup"><span data-stu-id="b405d-304"><span id="Multiplexer_Problem"></span><span id="multiplexer_problem"></span><span id="MULTIPLEXER_PROBLEM"></span>**Multiplexer Problem** (32)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-305"><span id="Out_of_Memory"></span><span id="out_of_memory"></span><span id="OUT_OF_MEMORY"></span>**Memoria insuficiente** (33)</span><span class="sxs-lookup"><span data-stu-id="b405d-305"><span id="Out_of_Memory"></span><span id="out_of_memory"></span><span id="OUT_OF_MEMORY"></span>**Out of Memory** (33)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-306"><span id="Output_Device_Error"></span><span id="output_device_error"></span><span id="OUTPUT_DEVICE_ERROR"></span>**Error de dispositivo de salida** (34)</span><span class="sxs-lookup"><span data-stu-id="b405d-306"><span id="Output_Device_Error"></span><span id="output_device_error"></span><span id="OUTPUT_DEVICE_ERROR"></span>**Output Device Error** (34)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-307"><span id="Performance_Degraded"></span><span id="performance_degraded"></span><span id="PERFORMANCE_DEGRADED"></span>**Rendimiento degradado** (35)</span><span class="sxs-lookup"><span data-stu-id="b405d-307"><span id="Performance_Degraded"></span><span id="performance_degraded"></span><span id="PERFORMANCE_DEGRADED"></span>**Performance Degraded** (35)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-308"><span id="Power_Problem"></span><span id="power_problem"></span><span id="POWER_PROBLEM"></span>**Problema de energía** (36)</span><span class="sxs-lookup"><span data-stu-id="b405d-308"><span id="Power_Problem"></span><span id="power_problem"></span><span id="POWER_PROBLEM"></span>**Power Problem** (36)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-309"><span id="Pressure_Unacceptable"></span><span id="pressure_unacceptable"></span><span id="PRESSURE_UNACCEPTABLE"></span>**Presión inaceptable** (37)</span><span class="sxs-lookup"><span data-stu-id="b405d-309"><span id="Pressure_Unacceptable"></span><span id="pressure_unacceptable"></span><span id="PRESSURE_UNACCEPTABLE"></span>**Pressure Unacceptable** (37)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-310"><span id="Processor_Problem__Internal_Machine_Error_"></span><span id="processor_problem__internal_machine_error_"></span><span id="PROCESSOR_PROBLEM__INTERNAL_MACHINE_ERROR_"></span>**Problema del procesador (error interno de la máquina)** (38)</span><span class="sxs-lookup"><span data-stu-id="b405d-310"><span id="Processor_Problem__Internal_Machine_Error_"></span><span id="processor_problem__internal_machine_error_"></span><span id="PROCESSOR_PROBLEM__INTERNAL_MACHINE_ERROR_"></span>**Processor Problem (Internal Machine Error)** (38)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-311"><span id="Pump_Failure"></span><span id="pump_failure"></span><span id="PUMP_FAILURE"></span>**Error de bombeo** (39)</span><span class="sxs-lookup"><span data-stu-id="b405d-311"><span id="Pump_Failure"></span><span id="pump_failure"></span><span id="PUMP_FAILURE"></span>**Pump Failure** (39)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-312"><span id="Queue_Size_Exceeded"></span><span id="queue_size_exceeded"></span><span id="QUEUE_SIZE_EXCEEDED"></span>**Tamaño de cola superado** (40)</span><span class="sxs-lookup"><span data-stu-id="b405d-312"><span id="Queue_Size_Exceeded"></span><span id="queue_size_exceeded"></span><span id="QUEUE_SIZE_EXCEEDED"></span>**Queue Size Exceeded** (40)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-313"><span id="Receive_Failure"></span><span id="receive_failure"></span><span id="RECEIVE_FAILURE"></span>**Error de recepción** (41)</span><span class="sxs-lookup"><span data-stu-id="b405d-313"><span id="Receive_Failure"></span><span id="receive_failure"></span><span id="RECEIVE_FAILURE"></span>**Receive Failure** (41)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-314"><span id="Receiver_Failure"></span><span id="receiver_failure"></span><span id="RECEIVER_FAILURE"></span>**Error del receptor** (42)</span><span class="sxs-lookup"><span data-stu-id="b405d-314"><span id="Receiver_Failure"></span><span id="receiver_failure"></span><span id="RECEIVER_FAILURE"></span>**Receiver Failure** (42)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-315"><span id="Remote_Node_Transmission_Error"></span><span id="remote_node_transmission_error"></span><span id="REMOTE_NODE_TRANSMISSION_ERROR"></span>**Error de transmisión de nodo remoto** (43)</span><span class="sxs-lookup"><span data-stu-id="b405d-315"><span id="Remote_Node_Transmission_Error"></span><span id="remote_node_transmission_error"></span><span id="REMOTE_NODE_TRANSMISSION_ERROR"></span>**Remote Node Transmission Error** (43)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-316"><span id="Resource_at_or_Nearing_Capacity"></span><span id="resource_at_or_nearing_capacity"></span><span id="RESOURCE_AT_OR_NEARING_CAPACITY"></span>**Recursos a la capacidad o en proximidad** (44)</span><span class="sxs-lookup"><span data-stu-id="b405d-316"><span id="Resource_at_or_Nearing_Capacity"></span><span id="resource_at_or_nearing_capacity"></span><span id="RESOURCE_AT_OR_NEARING_CAPACITY"></span>**Resource at or Nearing Capacity** (44)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-317"><span id="Response_Time_Excessive"></span><span id="response_time_excessive"></span><span id="RESPONSE_TIME_EXCESSIVE"></span>**Tiempo de respuesta excesivo** (45)</span><span class="sxs-lookup"><span data-stu-id="b405d-317"><span id="Response_Time_Excessive"></span><span id="response_time_excessive"></span><span id="RESPONSE_TIME_EXCESSIVE"></span>**Response Time Excessive** (45)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-318"><span id="Retransmission_Rate_Excessive"></span><span id="retransmission_rate_excessive"></span><span id="RETRANSMISSION_RATE_EXCESSIVE"></span>**Tasa de retransmisión excesiva** (46)</span><span class="sxs-lookup"><span data-stu-id="b405d-318"><span id="Retransmission_Rate_Excessive"></span><span id="retransmission_rate_excessive"></span><span id="RETRANSMISSION_RATE_EXCESSIVE"></span>**Retransmission Rate Excessive** (46)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-319"><span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>**Error de software** (47)</span><span class="sxs-lookup"><span data-stu-id="b405d-319"><span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>**Software Error** (47)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-320"><span id="Software_Program_Abnormally_Terminated"></span><span id="software_program_abnormally_terminated"></span><span id="SOFTWARE_PROGRAM_ABNORMALLY_TERMINATED"></span>**Programa de software finalizado** de manera anómala (48)</span><span class="sxs-lookup"><span data-stu-id="b405d-320"><span id="Software_Program_Abnormally_Terminated"></span><span id="software_program_abnormally_terminated"></span><span id="SOFTWARE_PROGRAM_ABNORMALLY_TERMINATED"></span>**Software Program Abnormally Terminated** (48)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-321"><span id="Software_Program_Error__Incorrect_Results_"></span><span id="software_program_error__incorrect_results_"></span><span id="SOFTWARE_PROGRAM_ERROR__INCORRECT_RESULTS_"></span>**Error del programa de software (resultados incorrectos)** (49)</span><span class="sxs-lookup"><span data-stu-id="b405d-321"><span id="Software_Program_Error__Incorrect_Results_"></span><span id="software_program_error__incorrect_results_"></span><span id="SOFTWARE_PROGRAM_ERROR__INCORRECT_RESULTS_"></span>**Software Program Error (Incorrect Results)** (49)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-322"><span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>**Problema de capacidad de almacenamiento** (50)</span><span class="sxs-lookup"><span data-stu-id="b405d-322"><span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>**Storage Capacity Problem** (50)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-323"><span id="Temperature_Unacceptable"></span><span id="temperature_unacceptable"></span><span id="TEMPERATURE_UNACCEPTABLE"></span>**Temperatura inaceptable** (51)</span><span class="sxs-lookup"><span data-stu-id="b405d-323"><span id="Temperature_Unacceptable"></span><span id="temperature_unacceptable"></span><span id="TEMPERATURE_UNACCEPTABLE"></span>**Temperature Unacceptable** (51)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-324"><span id="Threshold_Crossed"></span><span id="threshold_crossed"></span><span id="THRESHOLD_CROSSED"></span>**Umbral superado** (52)</span><span class="sxs-lookup"><span data-stu-id="b405d-324"><span id="Threshold_Crossed"></span><span id="threshold_crossed"></span><span id="THRESHOLD_CROSSED"></span>**Threshold Crossed** (52)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-325"><span id="Timing_Problem"></span><span id="timing_problem"></span><span id="TIMING_PROBLEM"></span>**Problema de sincronización** (53)</span><span class="sxs-lookup"><span data-stu-id="b405d-325"><span id="Timing_Problem"></span><span id="timing_problem"></span><span id="TIMING_PROBLEM"></span>**Timing Problem** (53)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-326"><span id="Toxic_Leak_Detected"></span><span id="toxic_leak_detected"></span><span id="TOXIC_LEAK_DETECTED"></span>**Pérdida tóxica detectada** (54)</span><span class="sxs-lookup"><span data-stu-id="b405d-326"><span id="Toxic_Leak_Detected"></span><span id="toxic_leak_detected"></span><span id="TOXIC_LEAK_DETECTED"></span>**Toxic Leak Detected** (54)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-327"><span id="Transmit_Failure"></span><span id="transmit_failure"></span><span id="TRANSMIT_FAILURE"></span>**Error de transmisión** (55)</span><span class="sxs-lookup"><span data-stu-id="b405d-327"><span id="Transmit_Failure"></span><span id="transmit_failure"></span><span id="TRANSMIT_FAILURE"></span>**Transmit Failure** (55)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-328"><span id="Transmitter_Failure"></span><span id="transmitter_failure"></span><span id="TRANSMITTER_FAILURE"></span>**Error de transmisor** (56)</span><span class="sxs-lookup"><span data-stu-id="b405d-328"><span id="Transmitter_Failure"></span><span id="transmitter_failure"></span><span id="TRANSMITTER_FAILURE"></span>**Transmitter Failure** (56)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-329"><span id="Underlying_Resource_Unavailable"></span><span id="underlying_resource_unavailable"></span><span id="UNDERLYING_RESOURCE_UNAVAILABLE"></span>**Recurso subyacente no disponible** (57)</span><span class="sxs-lookup"><span data-stu-id="b405d-329"><span id="Underlying_Resource_Unavailable"></span><span id="underlying_resource_unavailable"></span><span id="UNDERLYING_RESOURCE_UNAVAILABLE"></span>**Underlying Resource Unavailable** (57)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-330"><span id="Version_Mismatch"></span><span id="version_mismatch"></span><span id="VERSION_MISMATCH"></span>**Discrepancia de versiones** (58)</span><span class="sxs-lookup"><span data-stu-id="b405d-330"><span id="Version_Mismatch"></span><span id="version_mismatch"></span><span id="VERSION_MISMATCH"></span>**Version Mismatch** (58)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-331"><span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>**Alerta anterior desactivada** (59)</span><span class="sxs-lookup"><span data-stu-id="b405d-331"><span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>**Previous Alert Cleared** (59)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-332"><span id="__60____________Login_Attempts_Failed"></span><span id="__60____________login_attempts_failed"></span><span id="__60____________LOGIN_ATTEMPTS_FAILED"></span>**//error de intentos de inicio de sesión de 60** (60)</span><span class="sxs-lookup"><span data-stu-id="b405d-332"><span id="__60____________Login_Attempts_Failed"></span><span id="__60____________login_attempts_failed"></span><span id="__60____________LOGIN_ATTEMPTS_FAILED"></span>**//60 Login Attempts Failed** (60)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-333"><span id="Software_Virus_Detected"></span><span id="software_virus_detected"></span><span id="SOFTWARE_VIRUS_DETECTED"></span>**Virus de software detectado** (61)</span><span class="sxs-lookup"><span data-stu-id="b405d-333"><span id="Software_Virus_Detected"></span><span id="software_virus_detected"></span><span id="SOFTWARE_VIRUS_DETECTED"></span>**Software Virus Detected** (61)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-334"><span id="Hardware_Security_Breached"></span><span id="hardware_security_breached"></span><span id="HARDWARE_SECURITY_BREACHED"></span>**Seguridad de hardware infringida** (62)</span><span class="sxs-lookup"><span data-stu-id="b405d-334"><span id="Hardware_Security_Breached"></span><span id="hardware_security_breached"></span><span id="HARDWARE_SECURITY_BREACHED"></span>**Hardware Security Breached** (62)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-335"><span id="Denial_of_Service_Detected"></span><span id="denial_of_service_detected"></span><span id="DENIAL_OF_SERVICE_DETECTED"></span>**Denegación de servicio detectada** (63)</span><span class="sxs-lookup"><span data-stu-id="b405d-335"><span id="Denial_of_Service_Detected"></span><span id="denial_of_service_detected"></span><span id="DENIAL_OF_SERVICE_DETECTED"></span>**Denial of Service Detected** (63)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-336"><span id="Security_Credential_Mismatch"></span><span id="security_credential_mismatch"></span><span id="SECURITY_CREDENTIAL_MISMATCH"></span>**No coincide la credencial de seguridad** (64)</span><span class="sxs-lookup"><span data-stu-id="b405d-336"><span id="Security_Credential_Mismatch"></span><span id="security_credential_mismatch"></span><span id="SECURITY_CREDENTIAL_MISMATCH"></span>**Security Credential Mismatch** (64)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-337"><span id="Unauthorized_Access"></span><span id="unauthorized_access"></span><span id="UNAUTHORIZED_ACCESS"></span>**Acceso no autorizado** (65)</span><span class="sxs-lookup"><span data-stu-id="b405d-337"><span id="Unauthorized_Access"></span><span id="unauthorized_access"></span><span id="UNAUTHORIZED_ACCESS"></span>**Unauthorized Access** (65)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-338"><span id="Alarm_Received"></span><span id="alarm_received"></span><span id="ALARM_RECEIVED"></span>**Alarma recibida** (66)</span><span class="sxs-lookup"><span data-stu-id="b405d-338"><span id="Alarm_Received"></span><span id="alarm_received"></span><span id="ALARM_RECEIVED"></span>**Alarm Received** (66)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-339"><span id="Loss_of_Pointer"></span><span id="loss_of_pointer"></span><span id="LOSS_OF_POINTER"></span>**Pérdida de puntero** (67)</span><span class="sxs-lookup"><span data-stu-id="b405d-339"><span id="Loss_of_Pointer"></span><span id="loss_of_pointer"></span><span id="LOSS_OF_POINTER"></span>**Loss of Pointer** (67)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-340"><span id="Payload_Mismatch"></span><span id="payload_mismatch"></span><span id="PAYLOAD_MISMATCH"></span>Error de **coincidencia de carga** (68)</span><span class="sxs-lookup"><span data-stu-id="b405d-340"><span id="Payload_Mismatch"></span><span id="payload_mismatch"></span><span id="PAYLOAD_MISMATCH"></span>**Payload Mismatch** (68)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-341"><span id="Transmission_Error"></span><span id="transmission_error"></span><span id="TRANSMISSION_ERROR"></span>**Error de transmisión** (69)</span><span class="sxs-lookup"><span data-stu-id="b405d-341"><span id="Transmission_Error"></span><span id="transmission_error"></span><span id="TRANSMISSION_ERROR"></span>**Transmission Error** (69)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-342"><span id="Excessive_Error_Rate"></span><span id="excessive_error_rate"></span><span id="EXCESSIVE_ERROR_RATE"></span>**Tasa de errores excesiva** (70)</span><span class="sxs-lookup"><span data-stu-id="b405d-342"><span id="Excessive_Error_Rate"></span><span id="excessive_error_rate"></span><span id="EXCESSIVE_ERROR_RATE"></span>**Excessive Error Rate** (70)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-343"><span id="Trace_Problem"></span><span id="trace_problem"></span><span id="TRACE_PROBLEM"></span>**Problema de seguimiento** (71)</span><span class="sxs-lookup"><span data-stu-id="b405d-343"><span id="Trace_Problem"></span><span id="trace_problem"></span><span id="TRACE_PROBLEM"></span>**Trace Problem** (71)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-344"><span id="Element_Unavailable"></span><span id="element_unavailable"></span><span id="ELEMENT_UNAVAILABLE"></span>**Elemento no disponible** (72)</span><span class="sxs-lookup"><span data-stu-id="b405d-344"><span id="Element_Unavailable"></span><span id="element_unavailable"></span><span id="ELEMENT_UNAVAILABLE"></span>**Element Unavailable** (72)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-345"><span id="Element_Missing"></span><span id="element_missing"></span><span id="ELEMENT_MISSING"></span>**Falta el elemento** (73)</span><span class="sxs-lookup"><span data-stu-id="b405d-345"><span id="Element_Missing"></span><span id="element_missing"></span><span id="ELEMENT_MISSING"></span>**Element Missing** (73)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-346"><span id="Loss_of_Multi_Frame"></span><span id="loss_of_multi_frame"></span><span id="LOSS_OF_MULTI_FRAME"></span>**Pérdida de varios fotogramas** (74)</span><span class="sxs-lookup"><span data-stu-id="b405d-346"><span id="Loss_of_Multi_Frame"></span><span id="loss_of_multi_frame"></span><span id="LOSS_OF_MULTI_FRAME"></span>**Loss of Multi Frame** (74)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-347"><span id="Broadcast_Channel_Failure"></span><span id="broadcast_channel_failure"></span><span id="BROADCAST_CHANNEL_FAILURE"></span>**Error de canal de difusión** (75)</span><span class="sxs-lookup"><span data-stu-id="b405d-347"><span id="Broadcast_Channel_Failure"></span><span id="broadcast_channel_failure"></span><span id="BROADCAST_CHANNEL_FAILURE"></span>**Broadcast Channel Failure** (75)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-348"><span id="Invalid_Message_Received"></span><span id="invalid_message_received"></span><span id="INVALID_MESSAGE_RECEIVED"></span>Se **recibió un mensaje no válido** (76)</span><span class="sxs-lookup"><span data-stu-id="b405d-348"><span id="Invalid_Message_Received"></span><span id="invalid_message_received"></span><span id="INVALID_MESSAGE_RECEIVED"></span>**Invalid Message Received** (76)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-349"><span id="Routing_Failure"></span><span id="routing_failure"></span><span id="ROUTING_FAILURE"></span>**Error de enrutamiento** (77)</span><span class="sxs-lookup"><span data-stu-id="b405d-349"><span id="Routing_Failure"></span><span id="routing_failure"></span><span id="ROUTING_FAILURE"></span>**Routing Failure** (77)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-350"><span id="Backplane_Failure"></span><span id="backplane_failure"></span><span id="BACKPLANE_FAILURE"></span>**Error de backplane** (78)</span><span class="sxs-lookup"><span data-stu-id="b405d-350"><span id="Backplane_Failure"></span><span id="backplane_failure"></span><span id="BACKPLANE_FAILURE"></span>**Backplane Failure** (78)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-351"><span id="Identifier_Duplication"></span><span id="identifier_duplication"></span><span id="IDENTIFIER_DUPLICATION"></span>**Duplicación de identificadores** (79)</span><span class="sxs-lookup"><span data-stu-id="b405d-351"><span id="Identifier_Duplication"></span><span id="identifier_duplication"></span><span id="IDENTIFIER_DUPLICATION"></span>**Identifier Duplication** (79)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-352"><span id="Protection_Path_Failure"></span><span id="protection_path_failure"></span><span id="PROTECTION_PATH_FAILURE"></span>**Error de ruta de protección** (80)</span><span class="sxs-lookup"><span data-stu-id="b405d-352"><span id="Protection_Path_Failure"></span><span id="protection_path_failure"></span><span id="PROTECTION_PATH_FAILURE"></span>**Protection Path Failure** (80)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-353"><span id="Sync_Loss_or_Mismatch"></span><span id="sync_loss_or_mismatch"></span><span id="SYNC_LOSS_OR_MISMATCH"></span>**Pérdida o desigualdad de sincronización** (81)</span><span class="sxs-lookup"><span data-stu-id="b405d-353"><span id="Sync_Loss_or_Mismatch"></span><span id="sync_loss_or_mismatch"></span><span id="SYNC_LOSS_OR_MISMATCH"></span>**Sync Loss or Mismatch** (81)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-354"><span id="Terminal_Problem"></span><span id="terminal_problem"></span><span id="TERMINAL_PROBLEM"></span>**Problema de terminal** (82)</span><span class="sxs-lookup"><span data-stu-id="b405d-354"><span id="Terminal_Problem"></span><span id="terminal_problem"></span><span id="TERMINAL_PROBLEM"></span>**Terminal Problem** (82)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-355"><span id="Real_Time_Clock_Failure"></span><span id="real_time_clock_failure"></span><span id="REAL_TIME_CLOCK_FAILURE"></span>**Error de reloj en tiempo real** (83)</span><span class="sxs-lookup"><span data-stu-id="b405d-355"><span id="Real_Time_Clock_Failure"></span><span id="real_time_clock_failure"></span><span id="REAL_TIME_CLOCK_FAILURE"></span>**Real Time Clock Failure** (83)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-356"><span id="Antenna_Failure"></span><span id="antenna_failure"></span><span id="ANTENNA_FAILURE"></span>**Error de antena** (84)</span><span class="sxs-lookup"><span data-stu-id="b405d-356"><span id="Antenna_Failure"></span><span id="antenna_failure"></span><span id="ANTENNA_FAILURE"></span>**Antenna Failure** (84)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-357"><span id="Battery_Charging_Failure"></span><span id="battery_charging_failure"></span><span id="BATTERY_CHARGING_FAILURE"></span>**Error de carga** de la batería (85)</span><span class="sxs-lookup"><span data-stu-id="b405d-357"><span id="Battery_Charging_Failure"></span><span id="battery_charging_failure"></span><span id="BATTERY_CHARGING_FAILURE"></span>**Battery Charging Failure** (85)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-358"><span id="Disk_Failure"></span><span id="disk_failure"></span><span id="DISK_FAILURE"></span>**Error de disco** (86)</span><span class="sxs-lookup"><span data-stu-id="b405d-358"><span id="Disk_Failure"></span><span id="disk_failure"></span><span id="DISK_FAILURE"></span>**Disk Failure** (86)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-359"><span id="Frequency_Hopping_Failure"></span><span id="frequency_hopping_failure"></span><span id="FREQUENCY_HOPPING_FAILURE"></span>**Error de salto de frecuencia** (87)</span><span class="sxs-lookup"><span data-stu-id="b405d-359"><span id="Frequency_Hopping_Failure"></span><span id="frequency_hopping_failure"></span><span id="FREQUENCY_HOPPING_FAILURE"></span>**Frequency Hopping Failure** (87)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-360"><span id="Loss_of_Redundancy"></span><span id="loss_of_redundancy"></span><span id="LOSS_OF_REDUNDANCY"></span>**Pérdida de redundancia** (88)</span><span class="sxs-lookup"><span data-stu-id="b405d-360"><span id="Loss_of_Redundancy"></span><span id="loss_of_redundancy"></span><span id="LOSS_OF_REDUNDANCY"></span>**Loss of Redundancy** (88)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-361"><span id="Power_Supply_Failure"></span><span id="power_supply_failure"></span><span id="POWER_SUPPLY_FAILURE"></span>**Error** de la fuente de alimentación (89)</span><span class="sxs-lookup"><span data-stu-id="b405d-361"><span id="Power_Supply_Failure"></span><span id="power_supply_failure"></span><span id="POWER_SUPPLY_FAILURE"></span>**Power Supply Failure** (89)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-362"><span id="Signal_Quality_Problem"></span><span id="signal_quality_problem"></span><span id="SIGNAL_QUALITY_PROBLEM"></span>**Problema de calidad** de la señal (90)</span><span class="sxs-lookup"><span data-stu-id="b405d-362"><span id="Signal_Quality_Problem"></span><span id="signal_quality_problem"></span><span id="SIGNAL_QUALITY_PROBLEM"></span>**Signal Quality Problem** (90)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-363"><span id="__91____________Battery_Discharging"></span><span id="__91____________battery_discharging"></span><span id="__91____________BATTERY_DISCHARGING"></span>**//91 descargado** de la batería (91)</span><span class="sxs-lookup"><span data-stu-id="b405d-363"><span id="__91____________Battery_Discharging"></span><span id="__91____________battery_discharging"></span><span id="__91____________BATTERY_DISCHARGING"></span>**//91 Battery Discharging** (91)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-364"><span id="Battery_Failure"></span><span id="battery_failure"></span><span id="BATTERY_FAILURE"></span>**Error de batería** (92)</span><span class="sxs-lookup"><span data-stu-id="b405d-364"><span id="Battery_Failure"></span><span id="battery_failure"></span><span id="BATTERY_FAILURE"></span>**Battery Failure** (92)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-365"><span id="Commercial_Power_Problem"></span><span id="commercial_power_problem"></span><span id="COMMERCIAL_POWER_PROBLEM"></span>**Problema de alimentación comercial** (93)</span><span class="sxs-lookup"><span data-stu-id="b405d-365"><span id="Commercial_Power_Problem"></span><span id="commercial_power_problem"></span><span id="COMMERCIAL_POWER_PROBLEM"></span>**Commercial Power Problem** (93)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-366"><span id="Fan_Failure"></span><span id="fan_failure"></span><span id="FAN_FAILURE"></span>**Error de ventilador** (94)</span><span class="sxs-lookup"><span data-stu-id="b405d-366"><span id="Fan_Failure"></span><span id="fan_failure"></span><span id="FAN_FAILURE"></span>**Fan Failure** (94)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-367"><span id="Engine_Failure"></span><span id="engine_failure"></span><span id="ENGINE_FAILURE"></span>**Error del motor** (95)</span><span class="sxs-lookup"><span data-stu-id="b405d-367"><span id="Engine_Failure"></span><span id="engine_failure"></span><span id="ENGINE_FAILURE"></span>**Engine Failure** (95)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-368"><span id="Sensor_Failure"></span><span id="sensor_failure"></span><span id="SENSOR_FAILURE"></span>**Error del sensor** (96)</span><span class="sxs-lookup"><span data-stu-id="b405d-368"><span id="Sensor_Failure"></span><span id="sensor_failure"></span><span id="SENSOR_FAILURE"></span>**Sensor Failure** (96)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-369"><span id="Fuse_Failure"></span><span id="fuse_failure"></span><span id="FUSE_FAILURE"></span>**Error de fusible** (97)</span><span class="sxs-lookup"><span data-stu-id="b405d-369"><span id="Fuse_Failure"></span><span id="fuse_failure"></span><span id="FUSE_FAILURE"></span>**Fuse Failure** (97)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-370"><span id="Generator_Failure"></span><span id="generator_failure"></span><span id="GENERATOR_FAILURE"></span>**Error del generador** (98)</span><span class="sxs-lookup"><span data-stu-id="b405d-370"><span id="Generator_Failure"></span><span id="generator_failure"></span><span id="GENERATOR_FAILURE"></span>**Generator Failure** (98)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-371"><span id="Low_Battery"></span><span id="low_battery"></span><span id="LOW_BATTERY"></span>**Batería baja** (99)</span><span class="sxs-lookup"><span data-stu-id="b405d-371"><span id="Low_Battery"></span><span id="low_battery"></span><span id="LOW_BATTERY"></span>**Low Battery** (99)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-372"><span id="Low_Fuel"></span><span id="low_fuel"></span><span id="LOW_FUEL"></span>**Combustible bajo** (100)</span><span class="sxs-lookup"><span data-stu-id="b405d-372"><span id="Low_Fuel"></span><span id="low_fuel"></span><span id="LOW_FUEL"></span>**Low Fuel** (100)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-373"><span id="Low_Water"></span><span id="low_water"></span><span id="LOW_WATER"></span>**Bajo agua** (101)</span><span class="sxs-lookup"><span data-stu-id="b405d-373"><span id="Low_Water"></span><span id="low_water"></span><span id="LOW_WATER"></span>**Low Water** (101)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-374"><span id="Explosive_Gas"></span><span id="explosive_gas"></span><span id="EXPLOSIVE_GAS"></span>**Gas explosivo** (102)</span><span class="sxs-lookup"><span data-stu-id="b405d-374"><span id="Explosive_Gas"></span><span id="explosive_gas"></span><span id="EXPLOSIVE_GAS"></span>**Explosive Gas** (102)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-375"><span id="High_Winds"></span><span id="high_winds"></span><span id="HIGH_WINDS"></span>**Viento alto** (103)</span><span class="sxs-lookup"><span data-stu-id="b405d-375"><span id="High_Winds"></span><span id="high_winds"></span><span id="HIGH_WINDS"></span>**High Winds** (103)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-376"><span id="Ice_Buildup"></span><span id="ice_buildup"></span><span id="ICE_BUILDUP"></span>**Acumulación de hielo** (104)</span><span class="sxs-lookup"><span data-stu-id="b405d-376"><span id="Ice_Buildup"></span><span id="ice_buildup"></span><span id="ICE_BUILDUP"></span>**Ice Buildup** (104)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-377"><span id="Smoke"></span><span id="smoke"></span><span id="SMOKE"></span>**Humo** (105)</span><span class="sxs-lookup"><span data-stu-id="b405d-377"><span id="Smoke"></span><span id="smoke"></span><span id="SMOKE"></span>**Smoke** (105)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-378"><span id="Memory_Mismatch"></span><span id="memory_mismatch"></span><span id="MEMORY_MISMATCH"></span>**No coincide la memoria** (106)</span><span class="sxs-lookup"><span data-stu-id="b405d-378"><span id="Memory_Mismatch"></span><span id="memory_mismatch"></span><span id="MEMORY_MISMATCH"></span>**Memory Mismatch** (106)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-379"><span id="Out_of_CPU_Cycles"></span><span id="out_of_cpu_cycles"></span><span id="OUT_OF_CPU_CYCLES"></span>**Ciclos de CPU agotados** (107)</span><span class="sxs-lookup"><span data-stu-id="b405d-379"><span id="Out_of_CPU_Cycles"></span><span id="out_of_cpu_cycles"></span><span id="OUT_OF_CPU_CYCLES"></span>**Out of CPU Cycles** (107)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-380"><span id="Software_Environment_Problem"></span><span id="software_environment_problem"></span><span id="SOFTWARE_ENVIRONMENT_PROBLEM"></span>**Problema del entorno de software** (108)</span><span class="sxs-lookup"><span data-stu-id="b405d-380"><span id="Software_Environment_Problem"></span><span id="software_environment_problem"></span><span id="SOFTWARE_ENVIRONMENT_PROBLEM"></span>**Software Environment Problem** (108)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-381"><span id="Software_Download_Failure"></span><span id="software_download_failure"></span><span id="SOFTWARE_DOWNLOAD_FAILURE"></span>**Error de descarga de software** (109)</span><span class="sxs-lookup"><span data-stu-id="b405d-381"><span id="Software_Download_Failure"></span><span id="software_download_failure"></span><span id="SOFTWARE_DOWNLOAD_FAILURE"></span>**Software Download Failure** (109)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-382"><span id="Element_Reinitialized"></span><span id="element_reinitialized"></span><span id="ELEMENT_REINITIALIZED"></span>**Elemento reinicializado** (110)</span><span class="sxs-lookup"><span data-stu-id="b405d-382"><span id="Element_Reinitialized"></span><span id="element_reinitialized"></span><span id="ELEMENT_REINITIALIZED"></span>**Element Reinitialized** (110)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-383"><span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>**Tiempo de espera** (111)</span><span class="sxs-lookup"><span data-stu-id="b405d-383"><span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>**Timeout** (111)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-384"><span id="Logging_Problems"></span><span id="logging_problems"></span><span id="LOGGING_PROBLEMS"></span>**Problemas de registro** (112)</span><span class="sxs-lookup"><span data-stu-id="b405d-384"><span id="Logging_Problems"></span><span id="logging_problems"></span><span id="LOGGING_PROBLEMS"></span>**Logging Problems** (112)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-385"><span id="Leak_Detected"></span><span id="leak_detected"></span><span id="LEAK_DETECTED"></span>**Pérdida detectada** (113)</span><span class="sxs-lookup"><span data-stu-id="b405d-385"><span id="Leak_Detected"></span><span id="leak_detected"></span><span id="LEAK_DETECTED"></span>**Leak Detected** (113)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-386"><span id="Protection_Mechanism_Failure"></span><span id="protection_mechanism_failure"></span><span id="PROTECTION_MECHANISM_FAILURE"></span>**Error del mecanismo de protección** (114)</span><span class="sxs-lookup"><span data-stu-id="b405d-386"><span id="Protection_Mechanism_Failure"></span><span id="protection_mechanism_failure"></span><span id="PROTECTION_MECHANISM_FAILURE"></span>**Protection Mechanism Failure** (114)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-387"><span id="__115____________Protecting_Resource_Failure"></span><span id="__115____________protecting_resource_failure"></span><span id="__115____________PROTECTING_RESOURCE_FAILURE"></span>**//115 protección de errores de recursos** (115)</span><span class="sxs-lookup"><span data-stu-id="b405d-387"><span id="__115____________Protecting_Resource_Failure"></span><span id="__115____________protecting_resource_failure"></span><span id="__115____________PROTECTING_RESOURCE_FAILURE"></span>**//115 Protecting Resource Failure** (115)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-388"><span id="Database_Inconsistency"></span><span id="database_inconsistency"></span><span id="DATABASE_INCONSISTENCY"></span>Incoherencia de la **base de datos** (116)</span><span class="sxs-lookup"><span data-stu-id="b405d-388"><span id="Database_Inconsistency"></span><span id="database_inconsistency"></span><span id="DATABASE_INCONSISTENCY"></span>**Database Inconsistency** (116)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-389"><span id="Authentication_Failure"></span><span id="authentication_failure"></span><span id="AUTHENTICATION_FAILURE"></span>**Error de autenticación** (117)</span><span class="sxs-lookup"><span data-stu-id="b405d-389"><span id="Authentication_Failure"></span><span id="authentication_failure"></span><span id="AUTHENTICATION_FAILURE"></span>**Authentication Failure** (117)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-390"><span id="Breach_of_Confidentiality"></span><span id="breach_of_confidentiality"></span><span id="BREACH_OF_CONFIDENTIALITY"></span>**Infracción de la confidencialidad** (118)</span><span class="sxs-lookup"><span data-stu-id="b405d-390"><span id="Breach_of_Confidentiality"></span><span id="breach_of_confidentiality"></span><span id="BREACH_OF_CONFIDENTIALITY"></span>**Breach of Confidentiality** (118)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-391"><span id="Cable_Tamper"></span><span id="cable_tamper"></span><span id="CABLE_TAMPER"></span>**Manipulación de cables** (119)</span><span class="sxs-lookup"><span data-stu-id="b405d-391"><span id="Cable_Tamper"></span><span id="cable_tamper"></span><span id="CABLE_TAMPER"></span>**Cable Tamper** (119)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-392"><span id="Delayed_Information"></span><span id="delayed_information"></span><span id="DELAYED_INFORMATION"></span>**Información retrasada** (120)</span><span class="sxs-lookup"><span data-stu-id="b405d-392"><span id="Delayed_Information"></span><span id="delayed_information"></span><span id="DELAYED_INFORMATION"></span>**Delayed Information** (120)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-393"><span id="Duplicate_Information"></span><span id="duplicate_information"></span><span id="DUPLICATE_INFORMATION"></span>**Información duplicada** (121)</span><span class="sxs-lookup"><span data-stu-id="b405d-393"><span id="Duplicate_Information"></span><span id="duplicate_information"></span><span id="DUPLICATE_INFORMATION"></span>**Duplicate Information** (121)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-394"><span id="Information_Missing"></span><span id="information_missing"></span><span id="INFORMATION_MISSING"></span>**Falta información** (122)</span><span class="sxs-lookup"><span data-stu-id="b405d-394"><span id="Information_Missing"></span><span id="information_missing"></span><span id="INFORMATION_MISSING"></span>**Information Missing** (122)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-395"><span id="Information_Modification"></span><span id="information_modification"></span><span id="INFORMATION_MODIFICATION"></span>**Modificación** de la información (123)</span><span class="sxs-lookup"><span data-stu-id="b405d-395"><span id="Information_Modification"></span><span id="information_modification"></span><span id="INFORMATION_MODIFICATION"></span>**Information Modification** (123)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-396"><span id="Information_Out_of_Sequence"></span><span id="information_out_of_sequence"></span><span id="INFORMATION_OUT_OF_SEQUENCE"></span>**Información fuera de secuencia** (124)</span><span class="sxs-lookup"><span data-stu-id="b405d-396"><span id="Information_Out_of_Sequence"></span><span id="information_out_of_sequence"></span><span id="INFORMATION_OUT_OF_SEQUENCE"></span>**Information Out of Sequence** (124)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-397"><span id="Key_Expired"></span><span id="key_expired"></span><span id="KEY_EXPIRED"></span>**Clave expirada** (125)</span><span class="sxs-lookup"><span data-stu-id="b405d-397"><span id="Key_Expired"></span><span id="key_expired"></span><span id="KEY_EXPIRED"></span>**Key Expired** (125)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-398"><span id="Non-Repudiation_Failure"></span><span id="non-repudiation_failure"></span><span id="NON-REPUDIATION_FAILURE"></span>**Error sin repudio** (126)</span><span class="sxs-lookup"><span data-stu-id="b405d-398"><span id="Non-Repudiation_Failure"></span><span id="non-repudiation_failure"></span><span id="NON-REPUDIATION_FAILURE"></span>**Non-Repudiation Failure** (126)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-399"><span id="Out_of_Hours_Activity"></span><span id="out_of_hours_activity"></span><span id="OUT_OF_HOURS_ACTIVITY"></span>**Actividad fuera de horas** (127)</span><span class="sxs-lookup"><span data-stu-id="b405d-399"><span id="Out_of_Hours_Activity"></span><span id="out_of_hours_activity"></span><span id="OUT_OF_HOURS_ACTIVITY"></span>**Out of Hours Activity** (127)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-400"><span id="Out_of_Service"></span><span id="out_of_service"></span><span id="OUT_OF_SERVICE"></span>**Fuera de servicio** (128)</span><span class="sxs-lookup"><span data-stu-id="b405d-400"><span id="Out_of_Service"></span><span id="out_of_service"></span><span id="OUT_OF_SERVICE"></span>**Out of Service** (128)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-401"><span id="Procedural_Error"></span><span id="procedural_error"></span><span id="PROCEDURAL_ERROR"></span>**Error de procedimiento** (129)</span><span class="sxs-lookup"><span data-stu-id="b405d-401"><span id="Procedural_Error"></span><span id="procedural_error"></span><span id="PROCEDURAL_ERROR"></span>**Procedural Error** (129)</span></span>
</dt> <dt>

<span data-ttu-id="b405d-402"><span id="Unexpected_Information_"></span><span id="unexpected_information_"></span><span id="UNEXPECTED_INFORMATION_"></span>**Información inesperada** (130)</span><span class="sxs-lookup"><span data-stu-id="b405d-402"><span id="Unexpected_Information_"></span><span id="unexpected_information_"></span><span id="UNEXPECTED_INFORMATION_"></span>**Unexpected Information** (130 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b405d-403">**ProbableCauseDescription**</span><span class="sxs-lookup"><span data-stu-id="b405d-403">**ProbableCauseDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b405d-404">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b405d-404">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b405d-405">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b405d-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b405d-406">Cadena que describe la causa probable del error.</span><span class="sxs-lookup"><span data-stu-id="b405d-406">A string that describes the probable cause of the error.</span></span> <span data-ttu-id="b405d-407">Esta propiedad se hereda del [**\_ error de CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b405d-407">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b405d-408">**RecommendedActions**</span><span class="sxs-lookup"><span data-stu-id="b405d-408">**RecommendedActions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b405d-409">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="b405d-409">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b405d-410">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b405d-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b405d-411">Cadena que describe las acciones recomendadas que se deben realizar para resolver el error.</span><span class="sxs-lookup"><span data-stu-id="b405d-411">A string that describes recommended actions to take to resolve the error.</span></span> <span data-ttu-id="b405d-412">Esta propiedad se hereda del [**\_ error de CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b405d-412">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b405d-413">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b405d-413">Remarks</span></span>

<span data-ttu-id="b405d-414">El acceso a la clase de **\_ error MSVM** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="b405d-414">Access to the **Msvm\_Error** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="b405d-415">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="b405d-415">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="b405d-416">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b405d-416">Requirements</span></span>



| <span data-ttu-id="b405d-417">Requisito</span><span class="sxs-lookup"><span data-stu-id="b405d-417">Requirement</span></span> | <span data-ttu-id="b405d-418">Value</span><span class="sxs-lookup"><span data-stu-id="b405d-418">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b405d-419">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b405d-419">Minimum supported client</span></span><br/> | <span data-ttu-id="b405d-420">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="b405d-420">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b405d-421">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b405d-421">Minimum supported server</span></span><br/> | <span data-ttu-id="b405d-422">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="b405d-422">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b405d-423">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b405d-423">Namespace</span></span><br/>                | <span data-ttu-id="b405d-424">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="b405d-424">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b405d-425">MOF</span><span class="sxs-lookup"><span data-stu-id="b405d-425">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b405d-426"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b405d-426"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b405d-427">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b405d-427">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b405d-428"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b405d-428"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b405d-429">Vea también</span><span class="sxs-lookup"><span data-stu-id="b405d-429">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b405d-430">**Error de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="b405d-430">**CIM\_Error**</span></span>](cim-error.md)
</dt> <dt>

<span data-ttu-id="b405d-431">[**Error de CIM \_**](/previous-versions//cc150671(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b405d-431">[**CIM\_Error**](/previous-versions//cc150671(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b405d-432">Clases de administración de sistema virtual</span><span class="sxs-lookup"><span data-stu-id="b405d-432">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

