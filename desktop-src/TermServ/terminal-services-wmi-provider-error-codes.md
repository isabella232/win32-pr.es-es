---
title: Códigos de error del proveedor WMI de Servicios de Escritorio remoto (Wbemcli. h)
description: Errores devueltos por el proveedor de WMI de Servicios de Escritorio remoto. Para obtener una lista de otros errores de WMI, vea constantes error de WMI.
ms.assetid: 1e68c41d-f321-4bc5-ba30-b69f5ba741eb
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WBEM_E_FAILED
- WBEM_E_NOT_FOUND
- WBEM_E_PROVIDER_FAILURE
- WBEM_E_TYPE_MISMATCH
- WBEM_E_OUT_OF_MEMORY
- WBEM_E_INVALID_PARAMETER
- WBEM_E_NOT_AVAILABLE
- WBEM_E_NOT_SUPPORTED
- WBEM_E_INVALID_NAMESPACE
- WBEM_E_INVALID_OBJECT
- WBEM_E_INITIALIZATION_FAILURE
- WBEM_E_INVALID_OPERATION
- WBEM_E_INVALID_QUERY
- WBEM_E_INVALID_QUERY_TYPE
- WBEM_E_ALREADY_EXISTS
- WBEM_E_INVALID_SYNTAX
- WBEM_E_READ_ONLY
- WBEM_E_PROVIDER_NOT_CAPABLE
- WBEM_E_ILLEGAL_NULL
- WBEM_E_VALUE_OUT_OF_RANGE
- WBEM_E_INVALID_METHOD
- WBEM_E_INVALID_METHOD_PARAMETERS
- WBEM_E_INVALID_OBJECT_PATH
api_location:
- Wbemcli.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 252015a5d80a1487033ad285ce3080f4d666f0c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535374"
---
# <a name="remote-desktop-services-wmi-provider-error-codes"></a><span data-ttu-id="faeb1-104">Códigos de error del proveedor de Servicios de Escritorio remoto WMI</span><span class="sxs-lookup"><span data-stu-id="faeb1-104">Remote Desktop Services WMI provider error codes</span></span>

<span data-ttu-id="faeb1-105">En la lista siguiente se enumeran los errores de WMI devueltos por el proveedor de WMI de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="faeb1-105">The following list lists the WMI errors returned by the Remote Desktop Services WMI provider.</span></span> <span data-ttu-id="faeb1-106">Para obtener una lista de otros errores de WMI, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants).</span><span class="sxs-lookup"><span data-stu-id="faeb1-106">For a list of other WMI errors, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants).</span></span>

<dl> <dt>

<span data-ttu-id="faeb1-107"><span id="WBEM_E_FAILED"></span><span id="wbem_e_failed"></span>**error de WBEM \_ E \_**</span><span class="sxs-lookup"><span data-stu-id="faeb1-107"><span id="WBEM_E_FAILED"></span><span id="wbem_e_failed"></span>**WBEM\_E\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="faeb1-108">2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="faeb1-108">2147749889 (0x80041001)</span></span>
</dt> <dt>



<span data-ttu-id="faeb1-109">Error en la llamada al método.</span><span class="sxs-lookup"><span data-stu-id="faeb1-109">The method call failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="faeb1-110"><span id="WBEM_E_NOT_FOUND"></span><span id="wbem_e_not_found"></span>**WBEM \_ E \_ no \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="faeb1-110"><span id="WBEM_E_NOT_FOUND"></span><span id="wbem_e_not_found"></span>**WBEM\_E\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="faeb1-111">2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="faeb1-111">2147749890 (0x80041002)</span></span>
</dt> <dt>



<span data-ttu-id="faeb1-112">No se encontró el objeto.</span><span class="sxs-lookup"><span data-stu-id="faeb1-112">The object could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="faeb1-113"><span id="WBEM_E_PROVIDER_FAILURE"></span><span id="wbem_e_provider_failure"></span>**error del proveedor de WBEM \_ E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="faeb1-113"><span id="WBEM_E_PROVIDER_FAILURE"></span><span id="wbem_e_provider_failure"></span>**WBEM\_E\_PROVIDER\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="faeb1-114">2147749892 (0x80041004)</span><span class="sxs-lookup"><span data-stu-id="faeb1-114">2147749892 (0x80041004)</span></span>
</dt> <dt>



<span data-ttu-id="faeb1-115">El proveedor ha producido un error en algún momento distinto de durante la inicialización.</span><span class="sxs-lookup"><span data-stu-id="faeb1-115">The provider has failed at some time other than during initialization.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="faeb1-116"><span id="WBEM_E_TYPE_MISMATCH"></span><span id="wbem_e_type_mismatch"></span>**\_ \_ no coinciden los tipos E de WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="faeb1-116"><span id="WBEM_E_TYPE_MISMATCH"></span><span id="wbem_e_type_mismatch"></span>**WBEM\_E\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="faeb1-117">2147749893 (0x80041005)</span><span class="sxs-lookup"><span data-stu-id="faeb1-117">2147749893 (0x80041005)</span></span>
</dt> <dt>



<span data-ttu-id="faeb1-118">Se ha producido un error de coincidencia de tipos.</span><span class="sxs-lookup"><span data-stu-id="faeb1-118">A type mismatch has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="faeb1-119"><span id="WBEM_E_OUT_OF_MEMORY"></span><span id="wbem_e_out_of_memory"></span>**\_ \_ memoria insuficiente \_ de \_ WBEM**</span><span class="sxs-lookup"><span data-stu-id="faeb1-119"><span id="WBEM_E_OUT_OF_MEMORY"></span><span id="wbem_e_out_of_memory"></span>**WBEM\_E\_OUT\_OF\_MEMORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="faeb1-120">2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="faeb1-120">2147749894 (0x80041006)</span></span>
</dt> <dt>



<span data-ttu-id="faeb1-121">No había memoria suficiente para la operación.</span><span class="sxs-lookup"><span data-stu-id="faeb1-121">There was not enough memory for the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="faeb1-122"><span id="WBEM_E_INVALID_PARAMETER"></span><span id="wbem_e_invalid_parameter"></span>**\_ \_ parámetro no válido de WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="faeb1-122"><span id="WBEM_E_INVALID_PARAMETER"></span><span id="wbem_e_invalid_parameter"></span>**WBEM\_E\_INVALID\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="faeb1-123">2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="faeb1-123">2147749896 (0x80041008)</span></span>
</dt> <dt>



<span data-ttu-id="faeb1-124">Uno de los parámetros de la llamada no es correcto.</span><span class="sxs-lookup"><span data-stu-id="faeb1-124">One of the parameters to the call is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="faeb1-125"><span id="WBEM_E_NOT_AVAILABLE"></span><span id="wbem_e_not_available"></span>**WBEM \_ E \_ no \_ disponible**</span><span class="sxs-lookup"><span data-stu-id="faeb1-125"><span id="WBEM_E_NOT_AVAILABLE"></span><span id="wbem_e_not_available"></span>**WBEM\_E\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="faeb1-126">2147749897 (0x80041009)</span><span class="sxs-lookup"><span data-stu-id="faeb1-126">2147749897 (0x80041009)</span></span>
</dt> <dt>



<span data-ttu-id="faeb1-127">El recurso, que suele ser un servidor remoto, no está actualmente disponible.</span><span class="sxs-lookup"><span data-stu-id="faeb1-127">The resource, typically a remote server, is not currently available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="faeb1-128"><span id="WBEM_E_NOT_SUPPORTED"></span><span id="wbem_e_not_supported"></span>**WBEM \_ E \_ no \_ compatible**</span><span class="sxs-lookup"><span data-stu-id="faeb1-128"><span id="WBEM_E_NOT_SUPPORTED"></span><span id="wbem_e_not_supported"></span>**WBEM\_E\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="faeb1-129">2147749900 (0x8004100C)</span><span class="sxs-lookup"><span data-stu-id="faeb1-129">2147749900 (0x8004100C)</span></span>
</dt> <dt>



<span data-ttu-id="faeb1-130">No se admite esta característica u operación.</span><span class="sxs-lookup"><span data-stu-id="faeb1-130">The feature or operation is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="faeb1-131"><span id="WBEM_E_INVALID_NAMESPACE"></span><span id="wbem_e_invalid_namespace"></span>**\_espacio de \_ nombres no válido de WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="faeb1-131"><span id="WBEM_E_INVALID_NAMESPACE"></span><span id="wbem_e_invalid_namespace"></span>**WBEM\_E\_INVALID\_NAMESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="faeb1-132">2147749902 (0x8004100E)</span><span class="sxs-lookup"><span data-stu-id="faeb1-132">2147749902 (0x8004100E)</span></span>
</dt> <dt>



<span data-ttu-id="faeb1-133">No se pudo encontrar el espacio de nombres especificado.</span><span class="sxs-lookup"><span data-stu-id="faeb1-133">The specified namespace could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="faeb1-134"><span id="WBEM_E_INVALID_OBJECT"></span><span id="wbem_e_invalid_object"></span>**\_ \_ objeto no válido de WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="faeb1-134"><span id="WBEM_E_INVALID_OBJECT"></span><span id="wbem_e_invalid_object"></span>**WBEM\_E\_INVALID\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="faeb1-135">2147749903 (0x8004100F)</span><span class="sxs-lookup"><span data-stu-id="faeb1-135">2147749903 (0x8004100F)</span></span>
</dt> <dt>



<span data-ttu-id="faeb1-136">La instancia especificada no es válida.</span><span class="sxs-lookup"><span data-stu-id="faeb1-136">The specified instance is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="faeb1-137"><span id="WBEM_E_INITIALIZATION_FAILURE"></span><span id="wbem_e_initialization_failure"></span>**\_error de \_ inicialización de WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="faeb1-137"><span id="WBEM_E_INITIALIZATION_FAILURE"></span><span id="wbem_e_initialization_failure"></span>**WBEM\_E\_INITIALIZATION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="faeb1-138">2147749908 (0x80041014)</span><span class="sxs-lookup"><span data-stu-id="faeb1-138">2147749908 (0x80041014)</span></span>
</dt> <dt>



<span data-ttu-id="faeb1-139">Un módulo, como un proveedor, no se pudo inicializar por razones internas.</span><span class="sxs-lookup"><span data-stu-id="faeb1-139">A module, such as a provider, failed to initialize for internal reasons.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="faeb1-140"><span id="WBEM_E_INVALID_OPERATION"></span><span id="wbem_e_invalid_operation"></span>**\_ \_ operación no válida de WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="faeb1-140"><span id="WBEM_E_INVALID_OPERATION"></span><span id="wbem_e_invalid_operation"></span>**WBEM\_E\_INVALID\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="faeb1-141">2147749910 (0x80041016)</span><span class="sxs-lookup"><span data-stu-id="faeb1-141">2147749910 (0x80041016)</span></span>
</dt> <dt>



<span data-ttu-id="faeb1-142">La operación solicitada no es válida.</span><span class="sxs-lookup"><span data-stu-id="faeb1-142">The requested operation is not valid.</span></span> <span data-ttu-id="faeb1-143">Normalmente, este error está relacionado con intentos no válidos de eliminar clases o propiedades.</span><span class="sxs-lookup"><span data-stu-id="faeb1-143">This error usually applies to invalid attempts to delete classes or properties.</span></span> <span data-ttu-id="faeb1-144">Este error se devuelve en un intento de modificar una propiedad de invalidación de servidor a través del control de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="faeb1-144">This error is returned on an attempt to modify a server-override property through group policy control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="faeb1-145"><span id="WBEM_E_INVALID_QUERY"></span><span id="wbem_e_invalid_query"></span>**\_ \_ consulta no válida de WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="faeb1-145"><span id="WBEM_E_INVALID_QUERY"></span><span id="wbem_e_invalid_query"></span>**WBEM\_E\_INVALID\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="faeb1-146">2147749911 (0x80041017)</span><span class="sxs-lookup"><span data-stu-id="faeb1-146">2147749911 (0x80041017)</span></span>
</dt> <dt>



<span data-ttu-id="faeb1-147">La consulta no era válida sintácticamente.</span><span class="sxs-lookup"><span data-stu-id="faeb1-147">The query was not syntactically valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="faeb1-148"><span id="WBEM_E_INVALID_QUERY_TYPE"></span><span id="wbem_e_invalid_query_type"></span>**\_tipo de consulta WBEM E \_ no válido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="faeb1-148"><span id="WBEM_E_INVALID_QUERY_TYPE"></span><span id="wbem_e_invalid_query_type"></span>**WBEM\_E\_INVALID\_QUERY\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="faeb1-149">2147749912 (0x80041018)</span><span class="sxs-lookup"><span data-stu-id="faeb1-149">2147749912 (0x80041018)</span></span>
</dt> <dt>



<span data-ttu-id="faeb1-150">No se admite el lenguaje de consulta solicitado.</span><span class="sxs-lookup"><span data-stu-id="faeb1-150">The requested query language is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="faeb1-151"><span id="WBEM_E_ALREADY_EXISTS"></span><span id="wbem_e_already_exists"></span>**WBEM \_ E \_ ya \_ existe**</span><span class="sxs-lookup"><span data-stu-id="faeb1-151"><span id="WBEM_E_ALREADY_EXISTS"></span><span id="wbem_e_already_exists"></span>**WBEM\_E\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="faeb1-152">2147749913 (0x80041019)</span><span class="sxs-lookup"><span data-stu-id="faeb1-152">2147749913 (0x80041019)</span></span>
</dt> <dt>



<span data-ttu-id="faeb1-153">En una operación PUT, se especificó la marca **wbemChangeFlagCreateOnly** , pero la instancia ya existe.</span><span class="sxs-lookup"><span data-stu-id="faeb1-153">In a put operation, the **wbemChangeFlagCreateOnly** flag was specified, but the instance already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="faeb1-154"><span id="WBEM_E_INVALID_SYNTAX"></span><span id="wbem_e_invalid_syntax"></span>**\_ \_ sintaxis no válida de WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="faeb1-154"><span id="WBEM_E_INVALID_SYNTAX"></span><span id="wbem_e_invalid_syntax"></span>**WBEM\_E\_INVALID\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="faeb1-155">2147749921 (0x80041021)</span><span class="sxs-lookup"><span data-stu-id="faeb1-155">2147749921 (0x80041021)</span></span>
</dt> <dt>



<span data-ttu-id="faeb1-156">La consulta no es válida sintácticamente.</span><span class="sxs-lookup"><span data-stu-id="faeb1-156">Query is not syntactically valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="faeb1-157"><span id="WBEM_E_READ_ONLY"></span><span id="wbem_e_read_only"></span>**WBEM \_ E \_ \_ solo lectura**</span><span class="sxs-lookup"><span data-stu-id="faeb1-157"><span id="WBEM_E_READ_ONLY"></span><span id="wbem_e_read_only"></span>**WBEM\_E\_READ\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="faeb1-158">2147749923 (0x80041023)</span><span class="sxs-lookup"><span data-stu-id="faeb1-158">2147749923 (0x80041023)</span></span>
</dt> <dt>



<span data-ttu-id="faeb1-159">La propiedad que intenta modificar es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="faeb1-159">The property that you are attempting to modify is read-only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="faeb1-160"><span id="WBEM_E_PROVIDER_NOT_CAPABLE"></span><span id="wbem_e_provider_not_capable"></span>**proveedor de WBEM \_ E \_ \_ no \_ compatible**</span><span class="sxs-lookup"><span data-stu-id="faeb1-160"><span id="WBEM_E_PROVIDER_NOT_CAPABLE"></span><span id="wbem_e_provider_not_capable"></span>**WBEM\_E\_PROVIDER\_NOT\_CAPABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="faeb1-161">2147749924 (0x80041024)</span><span class="sxs-lookup"><span data-stu-id="faeb1-161">2147749924 (0x80041024)</span></span>
</dt> <dt>



<span data-ttu-id="faeb1-162">El proveedor no puede realizar la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="faeb1-162">The provider cannot perform the requested operation.</span></span> <span data-ttu-id="faeb1-163">La operación podría incluir una consulta demasiado compleja, recuperar una instancia, crear una clase, actualizar una clase, eliminar una clase o enumerar una clase.</span><span class="sxs-lookup"><span data-stu-id="faeb1-163">The operation could include a query that is too complex, retrieving an instance, creating a class, updating a class, deleting a class, or enumerating a class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="faeb1-164"><span id="WBEM_E_ILLEGAL_NULL"></span><span id="wbem_e_illegal_null"></span>**WBEM \_ E \_ no válido \_ null**</span><span class="sxs-lookup"><span data-stu-id="faeb1-164"><span id="WBEM_E_ILLEGAL_NULL"></span><span id="wbem_e_illegal_null"></span>**WBEM\_E\_ILLEGAL\_NULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="faeb1-165">2147749928 (0x80041028)</span><span class="sxs-lookup"><span data-stu-id="faeb1-165">2147749928 (0x80041028)</span></span>
</dt> <dt>



<span data-ttu-id="faeb1-166">Se especificó un valor de **Nothing** / **null** para una propiedad que no puede ser **Nothing** / **null**, como una marcada por un calificador de [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**indexado**](/windows/desktop/WmiSdk/optional-qualifiers)o [**not \_ null**](/windows/desktop/WmiSdk/optional-qualifiers) .</span><span class="sxs-lookup"><span data-stu-id="faeb1-166">A value of **Nothing**/**NULL** was specified for a property that cannot be **Nothing**/**NULL**, such as one that is marked by a [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Indexed**](/windows/desktop/WmiSdk/optional-qualifiers), or [**Not\_Null**](/windows/desktop/WmiSdk/optional-qualifiers) qualifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="faeb1-167"><span id="WBEM_E_VALUE_OUT_OF_RANGE"></span><span id="wbem_e_value_out_of_range"></span>**\_valor de WBEM E comprendido \_ \_ fuera \_ del \_ intervalo**</span><span class="sxs-lookup"><span data-stu-id="faeb1-167"><span id="WBEM_E_VALUE_OUT_OF_RANGE"></span><span id="wbem_e_value_out_of_range"></span>**WBEM\_E\_VALUE\_OUT\_OF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="faeb1-168">2147749931 (0x8004102B)</span><span class="sxs-lookup"><span data-stu-id="faeb1-168">2147749931 (0x8004102B)</span></span>
</dt> <dt>



<span data-ttu-id="faeb1-169">La solicitud se realizó con un valor fuera del intervalo o es incompatible con el tipo.</span><span class="sxs-lookup"><span data-stu-id="faeb1-169">The request was made with an out-of-range value, or is incompatible with the type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="faeb1-170"><span id="WBEM_E_INVALID_METHOD"></span><span id="wbem_e_invalid_method"></span>**WBEM \_ E \_ método no válido \_**</span><span class="sxs-lookup"><span data-stu-id="faeb1-170"><span id="WBEM_E_INVALID_METHOD"></span><span id="wbem_e_invalid_method"></span>**WBEM\_E\_INVALID\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="faeb1-171">2147749934 (0x8004102E)</span><span class="sxs-lookup"><span data-stu-id="faeb1-171">2147749934 (0x8004102E)</span></span>
</dt> <dt>



<span data-ttu-id="faeb1-172">El método solicitado no está disponible.</span><span class="sxs-lookup"><span data-stu-id="faeb1-172">The requested method is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="faeb1-173"><span id="WBEM_E_INVALID_METHOD_PARAMETERS"></span><span id="wbem_e_invalid_method_parameters"></span>**\_parámetros de \_ método no válido de WBEM E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="faeb1-173"><span id="WBEM_E_INVALID_METHOD_PARAMETERS"></span><span id="wbem_e_invalid_method_parameters"></span>**WBEM\_E\_INVALID\_METHOD\_PARAMETERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="faeb1-174">2147749935 (0x8004102F)</span><span class="sxs-lookup"><span data-stu-id="faeb1-174">2147749935 (0x8004102F)</span></span>
</dt> <dt>



<span data-ttu-id="faeb1-175">Los parámetros proporcionados para el método no son válidos.</span><span class="sxs-lookup"><span data-stu-id="faeb1-175">The parameters provided for the method are not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="faeb1-176"><span id="WBEM_E_INVALID_OBJECT_PATH"></span><span id="wbem_e_invalid_object_path"></span>**\_ruta de \_ objeto no válida de WBEM E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="faeb1-176"><span id="WBEM_E_INVALID_OBJECT_PATH"></span><span id="wbem_e_invalid_object_path"></span>**WBEM\_E\_INVALID\_OBJECT\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="faeb1-177">2147749946 (0x8004103A)</span><span class="sxs-lookup"><span data-stu-id="faeb1-177">2147749946 (0x8004103A)</span></span>
</dt> <dt>



<span data-ttu-id="faeb1-178">La ruta de acceso del objeto especificado no era válida.</span><span class="sxs-lookup"><span data-stu-id="faeb1-178">The specified object path was not valid.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="faeb1-179">Requisitos</span><span class="sxs-lookup"><span data-stu-id="faeb1-179">Requirements</span></span>



| <span data-ttu-id="faeb1-180">Requisito</span><span class="sxs-lookup"><span data-stu-id="faeb1-180">Requirement</span></span> | <span data-ttu-id="faeb1-181">Value</span><span class="sxs-lookup"><span data-stu-id="faeb1-181">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="faeb1-182">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="faeb1-182">Minimum supported client</span></span><br/> | <span data-ttu-id="faeb1-183">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="faeb1-183">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="faeb1-184">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="faeb1-184">Minimum supported server</span></span><br/> | <span data-ttu-id="faeb1-185">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="faeb1-185">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="faeb1-186">Encabezado</span><span class="sxs-lookup"><span data-stu-id="faeb1-186">Header</span></span><br/>                   | <dl> <span data-ttu-id="faeb1-187"><dt>Wbemcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="faeb1-187"><dt>Wbemcli.h</dt></span></span> </dl> |



 

