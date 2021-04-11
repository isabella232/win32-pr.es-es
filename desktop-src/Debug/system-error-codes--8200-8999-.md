---
description: Describe los códigos de error 8200-8999 definidos en el archivo de encabezado WinError. h y está destinado a los desarrolladores.
ms.assetid: f16fdfa3-b080-47ee-a7dd-241fe2d24278
title: Códigos de error del sistema (8200-8999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 7500ae4c178999de8052b0858089604652dc5237
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274964"
---
# <a name="system-error-codes-8200-8999"></a><span data-ttu-id="3ad11-103">Códigos de error del sistema (8200-8999)</span><span class="sxs-lookup"><span data-stu-id="3ad11-103">System Error Codes (8200-8999)</span></span>

> [!NOTE]
> <span data-ttu-id="3ad11-104">Esta información está destinada a los desarrolladores que depuran errores del sistema.</span><span class="sxs-lookup"><span data-stu-id="3ad11-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="3ad11-105">En el caso de otros errores, como los problemas con Windows Update, hay una lista de recursos en la página [códigos de error](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="3ad11-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="3ad11-106">En la lista siguiente se describen los [códigos de error del sistema](system-error-codes.md) para los errores 8200 a 8999.</span><span class="sxs-lookup"><span data-stu-id="3ad11-106">The following list describes [system error codes](system-error-codes.md) for errors 8200 to 8999.</span></span> <span data-ttu-id="3ad11-107">La función [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve los resultados cuando se produce un error en muchas funciones.</span><span class="sxs-lookup"><span data-stu-id="3ad11-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="3ad11-108">Para recuperar el texto de la descripción del error en la aplicación, use la función [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con **el \_ mensaje format \_ from \_ System** Flag.</span><span class="sxs-lookup"><span data-stu-id="3ad11-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="3ad11-109"><span id="ERROR_DS_NOT_INSTALLED"></span><span id="error_ds_not_installed"></span>**ERROR \_ DS \_ no \_ instalado**</span><span class="sxs-lookup"><span data-stu-id="3ad11-109"><span id="ERROR_DS_NOT_INSTALLED"></span><span id="error_ds_not_installed"></span>**ERROR\_DS\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-110">8200 (0x2008)</span><span class="sxs-lookup"><span data-stu-id="3ad11-110">8200 (0x2008)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-111">Error al instalar el servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="3ad11-111">An error occurred while installing the directory service.</span></span> <span data-ttu-id="3ad11-112">Para obtener más información, vea el registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="3ad11-112">For more information, see the event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-113"><span id="ERROR_DS_MEMBERSHIP_EVALUATED_LOCALLY"></span><span id="error_ds_membership_evaluated_locally"></span>**ERROR de la \_ \_ pertenencia a DS \_ evaluada \_ localmente**</span><span class="sxs-lookup"><span data-stu-id="3ad11-113"><span id="ERROR_DS_MEMBERSHIP_EVALUATED_LOCALLY"></span><span id="error_ds_membership_evaluated_locally"></span>**ERROR\_DS\_MEMBERSHIP\_EVALUATED\_LOCALLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-114">8201 (0x2009)</span><span class="sxs-lookup"><span data-stu-id="3ad11-114">8201 (0x2009)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-115">El servicio de directorio evaluó las pertenencias a grupos localmente.</span><span class="sxs-lookup"><span data-stu-id="3ad11-115">The directory service evaluated group memberships locally.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-116"><span id="ERROR_DS_NO_ATTRIBUTE_OR_VALUE"></span><span id="error_ds_no_attribute_or_value"></span>**ERROR \_ DS \_ ningún \_ atributo \_ o \_ valor**</span><span class="sxs-lookup"><span data-stu-id="3ad11-116"><span id="ERROR_DS_NO_ATTRIBUTE_OR_VALUE"></span><span id="error_ds_no_attribute_or_value"></span>**ERROR\_DS\_NO\_ATTRIBUTE\_OR\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-117">8202 (0x200A)</span><span class="sxs-lookup"><span data-stu-id="3ad11-117">8202 (0x200A)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-118">El atributo o valor de servicio de directorio especificado no existe.</span><span class="sxs-lookup"><span data-stu-id="3ad11-118">The specified directory service attribute or value does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-119"><span id="ERROR_DS_INVALID_ATTRIBUTE_SYNTAX"></span><span id="error_ds_invalid_attribute_syntax"></span>**ERROR \_ de \_ \_ Sintaxis de atributo no válida de DS \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-119"><span id="ERROR_DS_INVALID_ATTRIBUTE_SYNTAX"></span><span id="error_ds_invalid_attribute_syntax"></span>**ERROR\_DS\_INVALID\_ATTRIBUTE\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-120">8203 (0x200B)</span><span class="sxs-lookup"><span data-stu-id="3ad11-120">8203 (0x200B)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-121">La sintaxis de atributo especificada para el servicio de directorio no es válida.</span><span class="sxs-lookup"><span data-stu-id="3ad11-121">The attribute syntax specified to the directory service is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-122"><span id="ERROR_DS_ATTRIBUTE_TYPE_UNDEFINED"></span><span id="error_ds_attribute_type_undefined"></span>**ERROR \_ de \_ tipo de atributo DS no \_ \_ definido**</span><span class="sxs-lookup"><span data-stu-id="3ad11-122"><span id="ERROR_DS_ATTRIBUTE_TYPE_UNDEFINED"></span><span id="error_ds_attribute_type_undefined"></span>**ERROR\_DS\_ATTRIBUTE\_TYPE\_UNDEFINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-123">8204 (0x200C)</span><span class="sxs-lookup"><span data-stu-id="3ad11-123">8204 (0x200C)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-124">No se ha definido el tipo de atributo especificado para el servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="3ad11-124">The attribute type specified to the directory service is not defined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-125"><span id="ERROR_DS_ATTRIBUTE_OR_VALUE_EXISTS"></span><span id="error_ds_attribute_or_value_exists"></span>**ERROR \_ el \_ atributo \_ o \_ valor de DS \_ existe**</span><span class="sxs-lookup"><span data-stu-id="3ad11-125"><span id="ERROR_DS_ATTRIBUTE_OR_VALUE_EXISTS"></span><span id="error_ds_attribute_or_value_exists"></span>**ERROR\_DS\_ATTRIBUTE\_OR\_VALUE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-126">8205 (0x200D)</span><span class="sxs-lookup"><span data-stu-id="3ad11-126">8205 (0x200D)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-127">El atributo o valor de servicio de directorio especificado ya existe.</span><span class="sxs-lookup"><span data-stu-id="3ad11-127">The specified directory service attribute or value already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-128"><span id="ERROR_DS_BUSY"></span><span id="error_ds_busy"></span>**ERROR de \_ DS \_ ocupado**</span><span class="sxs-lookup"><span data-stu-id="3ad11-128"><span id="ERROR_DS_BUSY"></span><span id="error_ds_busy"></span>**ERROR\_DS\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-129">8206 (0x200E)</span><span class="sxs-lookup"><span data-stu-id="3ad11-129">8206 (0x200E)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-130">El servicio de directorio está ocupado.</span><span class="sxs-lookup"><span data-stu-id="3ad11-130">The directory service is busy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-131"><span id="ERROR_DS_UNAVAILABLE"></span><span id="error_ds_unavailable"></span>**ERROR \_ DS \_ no disponible**</span><span class="sxs-lookup"><span data-stu-id="3ad11-131"><span id="ERROR_DS_UNAVAILABLE"></span><span id="error_ds_unavailable"></span>**ERROR\_DS\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-132">8207 (0x200F)</span><span class="sxs-lookup"><span data-stu-id="3ad11-132">8207 (0x200F)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-133">El servicio de directorio no está disponible.</span><span class="sxs-lookup"><span data-stu-id="3ad11-133">The directory service is unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-134"><span id="ERROR_DS_NO_RIDS_ALLOCATED"></span><span id="error_ds_no_rids_allocated"></span>**ERROR \_ DS \_ no \_ \_ asignado RID**</span><span class="sxs-lookup"><span data-stu-id="3ad11-134"><span id="ERROR_DS_NO_RIDS_ALLOCATED"></span><span id="error_ds_no_rids_allocated"></span>**ERROR\_DS\_NO\_RIDS\_ALLOCATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-135">8208 (0x2010)</span><span class="sxs-lookup"><span data-stu-id="3ad11-135">8208 (0x2010)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-136">El servicio de directorios no puede asignar un identificador relativo.</span><span class="sxs-lookup"><span data-stu-id="3ad11-136">The directory service was unable to allocate a relative identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-137"><span id="ERROR_DS_NO_MORE_RIDS"></span><span id="error_ds_no_more_rids"></span>**ERROR \_ DS \_ no hay \_ más \_ RID**</span><span class="sxs-lookup"><span data-stu-id="3ad11-137"><span id="ERROR_DS_NO_MORE_RIDS"></span><span id="error_ds_no_more_rids"></span>**ERROR\_DS\_NO\_MORE\_RIDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-138">8209 (0x2011)</span><span class="sxs-lookup"><span data-stu-id="3ad11-138">8209 (0x2011)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-139">El servicio de directorio ha agotado el grupo de identificadores relativos.</span><span class="sxs-lookup"><span data-stu-id="3ad11-139">The directory service has exhausted the pool of relative identifiers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-140"><span id="ERROR_DS_INCORRECT_ROLE_OWNER"></span><span id="error_ds_incorrect_role_owner"></span>**ERROR en el \_ \_ propietario del rol incorrecto de DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-140"><span id="ERROR_DS_INCORRECT_ROLE_OWNER"></span><span id="error_ds_incorrect_role_owner"></span>**ERROR\_DS\_INCORRECT\_ROLE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-141">8210 (0x2012)</span><span class="sxs-lookup"><span data-stu-id="3ad11-141">8210 (0x2012)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-142">No se pudo realizar la operación solicitada porque el servicio de directorio no es el maestro para ese tipo de operación.</span><span class="sxs-lookup"><span data-stu-id="3ad11-142">The requested operation could not be performed because the directory service is not the master for that type of operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-143"><span id="ERROR_DS_RIDMGR_INIT_ERROR"></span><span id="error_ds_ridmgr_init_error"></span>**error \_ de \_ inicialización de RIDMGR de DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-143"><span id="ERROR_DS_RIDMGR_INIT_ERROR"></span><span id="error_ds_ridmgr_init_error"></span>**ERROR\_DS\_RIDMGR\_INIT\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-144">8211 (0x2013)</span><span class="sxs-lookup"><span data-stu-id="3ad11-144">8211 (0x2013)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-145">El servicio de directorio no pudo inicializar el subsistema que asigna identificadores relativos.</span><span class="sxs-lookup"><span data-stu-id="3ad11-145">The directory service was unable to initialize the subsystem that allocates relative identifiers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-146"><span id="ERROR_DS_OBJ_CLASS_VIOLATION"></span><span id="error_ds_obj_class_violation"></span>**ERROR \_ de \_ \_ infracción de clase obj DS \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-146"><span id="ERROR_DS_OBJ_CLASS_VIOLATION"></span><span id="error_ds_obj_class_violation"></span>**ERROR\_DS\_OBJ\_CLASS\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-147">8212 (0x2014)</span><span class="sxs-lookup"><span data-stu-id="3ad11-147">8212 (0x2014)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-148">La operación solicitada no cumplió una o más restricciones asociadas a la clase del objeto.</span><span class="sxs-lookup"><span data-stu-id="3ad11-148">The requested operation did not satisfy one or more constraints associated with the class of the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-149"><span id="ERROR_DS_CANT_ON_NON_LEAF"></span><span id="error_ds_cant_on_non_leaf"></span>**ERROR \_ \_ de la peralte \_ de DS en \_ no \_ hoja**</span><span class="sxs-lookup"><span data-stu-id="3ad11-149"><span id="ERROR_DS_CANT_ON_NON_LEAF"></span><span id="error_ds_cant_on_non_leaf"></span>**ERROR\_DS\_CANT\_ON\_NON\_LEAF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-150">8213 (0x2015)</span><span class="sxs-lookup"><span data-stu-id="3ad11-150">8213 (0x2015)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-151">El servicio de directorio solo puede realizar la operación solicitada en un objeto hoja.</span><span class="sxs-lookup"><span data-stu-id="3ad11-151">The directory service can perform the requested operation only on a leaf object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-152"><span id="ERROR_DS_CANT_ON_RDN"></span><span id="error_ds_cant_on_rdn"></span>**ERROR \_ de DS no se pudo \_ \_ en \_ RDN**</span><span class="sxs-lookup"><span data-stu-id="3ad11-152"><span id="ERROR_DS_CANT_ON_RDN"></span><span id="error_ds_cant_on_rdn"></span>**ERROR\_DS\_CANT\_ON\_RDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-153">8214 (0x2016)</span><span class="sxs-lookup"><span data-stu-id="3ad11-153">8214 (0x2016)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-154">El servicio de directorio no puede realizar la operación solicitada en el atributo RDN de un objeto.</span><span class="sxs-lookup"><span data-stu-id="3ad11-154">The directory service cannot perform the requested operation on the RDN attribute of an object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-155"><span id="ERROR_DS_CANT_MOD_OBJ_CLASS"></span><span id="error_ds_cant_mod_obj_class"></span>**ERROR DS no se pudo \_ \_ mod ( \_ \_ \_ clase)**</span><span class="sxs-lookup"><span data-stu-id="3ad11-155"><span id="ERROR_DS_CANT_MOD_OBJ_CLASS"></span><span id="error_ds_cant_mod_obj_class"></span>**ERROR\_DS\_CANT\_MOD\_OBJ\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-156">8215 (0x2017)</span><span class="sxs-lookup"><span data-stu-id="3ad11-156">8215 (0x2017)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-157">El servicio de directorio detectó un intento de modificar la clase de objeto de un objeto.</span><span class="sxs-lookup"><span data-stu-id="3ad11-157">The directory service detected an attempt to modify the object class of an object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-158"><span id="ERROR_DS_CROSS_DOM_MOVE_ERROR"></span><span id="error_ds_cross_dom_move_error"></span>**error \_ de \_ \_ movimiento entre Dom cruzado \_ de DS \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-158"><span id="ERROR_DS_CROSS_DOM_MOVE_ERROR"></span><span id="error_ds_cross_dom_move_error"></span>**ERROR\_DS\_CROSS\_DOM\_MOVE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-159">8216 (0x2018)</span><span class="sxs-lookup"><span data-stu-id="3ad11-159">8216 (0x2018)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-160">No se pudo realizar la operación de movimiento entre dominios solicitada.</span><span class="sxs-lookup"><span data-stu-id="3ad11-160">The requested cross-domain move operation could not be performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-161"><span id="ERROR_DS_GC_NOT_AVAILABLE"></span><span id="error_ds_gc_not_available"></span>**ERROR \_ de \_ GC de DS \_ no \_ disponible**</span><span class="sxs-lookup"><span data-stu-id="3ad11-161"><span id="ERROR_DS_GC_NOT_AVAILABLE"></span><span id="error_ds_gc_not_available"></span>**ERROR\_DS\_GC\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-162">8217 (0x2019)</span><span class="sxs-lookup"><span data-stu-id="3ad11-162">8217 (0x2019)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-163">No se puede establecer contacto con el servidor de catálogo global.</span><span class="sxs-lookup"><span data-stu-id="3ad11-163">Unable to contact the global catalog server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-164"><span id="ERROR_SHARED_POLICY"></span><span id="error_shared_policy"></span>**\_Directiva compartida de errores \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-164"><span id="ERROR_SHARED_POLICY"></span><span id="error_shared_policy"></span>**ERROR\_SHARED\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-165">8218 (0x201A)</span><span class="sxs-lookup"><span data-stu-id="3ad11-165">8218 (0x201A)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-166">El objeto de Directiva se comparte y solo puede modificarse en la raíz.</span><span class="sxs-lookup"><span data-stu-id="3ad11-166">The policy object is shared and can only be modified at the root.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-167"><span id="ERROR_POLICY_OBJECT_NOT_FOUND"></span><span id="error_policy_object_not_found"></span>**\_ \_ \_ no \_ se encontró el objeto de directiva de error**</span><span class="sxs-lookup"><span data-stu-id="3ad11-167"><span id="ERROR_POLICY_OBJECT_NOT_FOUND"></span><span id="error_policy_object_not_found"></span>**ERROR\_POLICY\_OBJECT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-168">8219 (0x201B)</span><span class="sxs-lookup"><span data-stu-id="3ad11-168">8219 (0x201B)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-169">El objeto de Directiva no existe.</span><span class="sxs-lookup"><span data-stu-id="3ad11-169">The policy object does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-170"><span id="ERROR_POLICY_ONLY_IN_DS"></span><span id="error_policy_only_in_ds"></span>**\_directiva \_ de error solo \_ en \_ DS**</span><span class="sxs-lookup"><span data-stu-id="3ad11-170"><span id="ERROR_POLICY_ONLY_IN_DS"></span><span id="error_policy_only_in_ds"></span>**ERROR\_POLICY\_ONLY\_IN\_DS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-171">8220 (0x201C)</span><span class="sxs-lookup"><span data-stu-id="3ad11-171">8220 (0x201C)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-172">La información de directiva solicitada solo está en el servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="3ad11-172">The requested policy information is only in the directory service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-173"><span id="ERROR_PROMOTION_ACTIVE"></span><span id="error_promotion_active"></span>**promoción de errores \_ \_ activa**</span><span class="sxs-lookup"><span data-stu-id="3ad11-173"><span id="ERROR_PROMOTION_ACTIVE"></span><span id="error_promotion_active"></span>**ERROR\_PROMOTION\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-174">8221 (0x201D)</span><span class="sxs-lookup"><span data-stu-id="3ad11-174">8221 (0x201D)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-175">La promoción del controlador de dominio está activa actualmente.</span><span class="sxs-lookup"><span data-stu-id="3ad11-175">A domain controller promotion is currently active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-176"><span id="ERROR_NO_PROMOTION_ACTIVE"></span><span id="error_no_promotion_active"></span>**ERROR: \_ no hay ninguna \_ promoción \_ activa**</span><span class="sxs-lookup"><span data-stu-id="3ad11-176"><span id="ERROR_NO_PROMOTION_ACTIVE"></span><span id="error_no_promotion_active"></span>**ERROR\_NO\_PROMOTION\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-177">8222 (0x201E)</span><span class="sxs-lookup"><span data-stu-id="3ad11-177">8222 (0x201E)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-178">La promoción del controlador de dominio no está activa actualmente.</span><span class="sxs-lookup"><span data-stu-id="3ad11-178">A domain controller promotion is not currently active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-179"><span id="ERROR_DS_OPERATIONS_ERROR"></span><span id="error_ds_operations_error"></span>**error \_ de \_ operaciones de DS \_ error**</span><span class="sxs-lookup"><span data-stu-id="3ad11-179"><span id="ERROR_DS_OPERATIONS_ERROR"></span><span id="error_ds_operations_error"></span>**ERROR\_DS\_OPERATIONS\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-180">8224 (0x2020)</span><span class="sxs-lookup"><span data-stu-id="3ad11-180">8224 (0x2020)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-181">Se produjo un error de operación.</span><span class="sxs-lookup"><span data-stu-id="3ad11-181">An operations error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-182"><span id="ERROR_DS_PROTOCOL_ERROR"></span><span id="error_ds_protocol_error"></span>**error \_ de \_ Protocolo de DS \_ error**</span><span class="sxs-lookup"><span data-stu-id="3ad11-182"><span id="ERROR_DS_PROTOCOL_ERROR"></span><span id="error_ds_protocol_error"></span>**ERROR\_DS\_PROTOCOL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-183">8225 (0x2021)</span><span class="sxs-lookup"><span data-stu-id="3ad11-183">8225 (0x2021)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-184">Se ha producido un error de protocolo.</span><span class="sxs-lookup"><span data-stu-id="3ad11-184">A protocol error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-185"><span id="ERROR_DS_TIMELIMIT_EXCEEDED"></span><span id="error_ds_timelimit_exceeded"></span>**ERROR de \_ DS \_ TIMELIMIT \_ superado**</span><span class="sxs-lookup"><span data-stu-id="3ad11-185"><span id="ERROR_DS_TIMELIMIT_EXCEEDED"></span><span id="error_ds_timelimit_exceeded"></span>**ERROR\_DS\_TIMELIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-186">8226 (0x2022)</span><span class="sxs-lookup"><span data-stu-id="3ad11-186">8226 (0x2022)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-187">Se superó el límite de tiempo para esta solicitud.</span><span class="sxs-lookup"><span data-stu-id="3ad11-187">The time limit for this request was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-188"><span id="ERROR_DS_SIZELIMIT_EXCEEDED"></span><span id="error_ds_sizelimit_exceeded"></span>**ERROR de \_ DS \_ SIZELIMIT \_ superado**</span><span class="sxs-lookup"><span data-stu-id="3ad11-188"><span id="ERROR_DS_SIZELIMIT_EXCEEDED"></span><span id="error_ds_sizelimit_exceeded"></span>**ERROR\_DS\_SIZELIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-189">8227 (0x2023)</span><span class="sxs-lookup"><span data-stu-id="3ad11-189">8227 (0x2023)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-190">Se superó el límite de tamaño para esta solicitud.</span><span class="sxs-lookup"><span data-stu-id="3ad11-190">The size limit for this request was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-191"><span id="ERROR_DS_ADMIN_LIMIT_EXCEEDED"></span><span id="error_ds_admin_limit_exceeded"></span>**se \_ \_ \_ superó el límite de administración de DS de error \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-191"><span id="ERROR_DS_ADMIN_LIMIT_EXCEEDED"></span><span id="error_ds_admin_limit_exceeded"></span>**ERROR\_DS\_ADMIN\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-192">8228 (0x2024)</span><span class="sxs-lookup"><span data-stu-id="3ad11-192">8228 (0x2024)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-193">Se superó el límite administrativo para esta solicitud.</span><span class="sxs-lookup"><span data-stu-id="3ad11-193">The administrative limit for this request was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-194"><span id="ERROR_DS_COMPARE_FALSE"></span><span id="error_ds_compare_false"></span>**ERROR \_ de \_ comparación de DS \_ false**</span><span class="sxs-lookup"><span data-stu-id="3ad11-194"><span id="ERROR_DS_COMPARE_FALSE"></span><span id="error_ds_compare_false"></span>**ERROR\_DS\_COMPARE\_FALSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-195">8229 (0x2025)</span><span class="sxs-lookup"><span data-stu-id="3ad11-195">8229 (0x2025)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-196">La respuesta de comparación era falsa.</span><span class="sxs-lookup"><span data-stu-id="3ad11-196">The compare response was false.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-197"><span id="ERROR_DS_COMPARE_TRUE"></span><span id="error_ds_compare_true"></span>**ERROR \_ de \_ comparación de DS \_ true**</span><span class="sxs-lookup"><span data-stu-id="3ad11-197"><span id="ERROR_DS_COMPARE_TRUE"></span><span id="error_ds_compare_true"></span>**ERROR\_DS\_COMPARE\_TRUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-198">8230 (0x2026)</span><span class="sxs-lookup"><span data-stu-id="3ad11-198">8230 (0x2026)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-199">La respuesta de comparación era verdadera.</span><span class="sxs-lookup"><span data-stu-id="3ad11-199">The compare response was true.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-200"><span id="ERROR_DS_AUTH_METHOD_NOT_SUPPORTED"></span><span id="error_ds_auth_method_not_supported"></span>**\_no se \_ admite el \_ método de autenticación DS \_ de error \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-200"><span id="ERROR_DS_AUTH_METHOD_NOT_SUPPORTED"></span><span id="error_ds_auth_method_not_supported"></span>**ERROR\_DS\_AUTH\_METHOD\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-201">8231 (0x2027)</span><span class="sxs-lookup"><span data-stu-id="3ad11-201">8231 (0x2027)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-202">El servidor no admite el método de autenticación solicitado.</span><span class="sxs-lookup"><span data-stu-id="3ad11-202">The requested authentication method is not supported by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-203"><span id="ERROR_DS_STRONG_AUTH_REQUIRED"></span><span id="error_ds_strong_auth_required"></span>**ERROR \_ de \_ DS \_ autenticación segura \_ requerida**</span><span class="sxs-lookup"><span data-stu-id="3ad11-203"><span id="ERROR_DS_STRONG_AUTH_REQUIRED"></span><span id="error_ds_strong_auth_required"></span>**ERROR\_DS\_STRONG\_AUTH\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-204">8232 (0x2028)</span><span class="sxs-lookup"><span data-stu-id="3ad11-204">8232 (0x2028)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-205">Se requiere un método de autenticación más seguro para este servidor.</span><span class="sxs-lookup"><span data-stu-id="3ad11-205">A more secure authentication method is required for this server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-206"><span id="ERROR_DS_INAPPROPRIATE_AUTH"></span><span id="error_ds_inappropriate_auth"></span>**ERROR \_ de \_ autenticación no adecuada de DS \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-206"><span id="ERROR_DS_INAPPROPRIATE_AUTH"></span><span id="error_ds_inappropriate_auth"></span>**ERROR\_DS\_INAPPROPRIATE\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-207">8233 (0x2029)</span><span class="sxs-lookup"><span data-stu-id="3ad11-207">8233 (0x2029)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-208">Autenticación inadecuada.</span><span class="sxs-lookup"><span data-stu-id="3ad11-208">Inappropriate authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-209"><span id="ERROR_DS_AUTH_UNKNOWN"></span><span id="error_ds_auth_unknown"></span>**ERROR \_ de \_ autenticación DS \_ desconocida**</span><span class="sxs-lookup"><span data-stu-id="3ad11-209"><span id="ERROR_DS_AUTH_UNKNOWN"></span><span id="error_ds_auth_unknown"></span>**ERROR\_DS\_AUTH\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-210">8234 (0x202A)</span><span class="sxs-lookup"><span data-stu-id="3ad11-210">8234 (0x202A)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-211">Se desconoce el mecanismo de autenticación.</span><span class="sxs-lookup"><span data-stu-id="3ad11-211">The authentication mechanism is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-212"><span id="ERROR_DS_REFERRAL"></span><span id="error_ds_referral"></span>**\_referencia de DS de error \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-212"><span id="ERROR_DS_REFERRAL"></span><span id="error_ds_referral"></span>**ERROR\_DS\_REFERRAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-213">8235 (0x202B)</span><span class="sxs-lookup"><span data-stu-id="3ad11-213">8235 (0x202B)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-214">El servidor ha devuelto una referencia.</span><span class="sxs-lookup"><span data-stu-id="3ad11-214">A referral was returned from the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-215"><span id="ERROR_DS_UNAVAILABLE_CRIT_EXTENSION"></span><span id="error_ds_unavailable_crit_extension"></span>**ERROR \_ DS \_ \_ extensión de crít no disponible \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-215"><span id="ERROR_DS_UNAVAILABLE_CRIT_EXTENSION"></span><span id="error_ds_unavailable_crit_extension"></span>**ERROR\_DS\_UNAVAILABLE\_CRIT\_EXTENSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-216">8236 (0x202C)</span><span class="sxs-lookup"><span data-stu-id="3ad11-216">8236 (0x202C)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-217">El servidor no admite la extensión crítica solicitada.</span><span class="sxs-lookup"><span data-stu-id="3ad11-217">The server does not support the requested critical extension.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-218"><span id="ERROR_DS_CONFIDENTIALITY_REQUIRED"></span><span id="error_ds_confidentiality_required"></span>**ERROR \_ de \_ confidencialidad de DS \_ requerido**</span><span class="sxs-lookup"><span data-stu-id="3ad11-218"><span id="ERROR_DS_CONFIDENTIALITY_REQUIRED"></span><span id="error_ds_confidentiality_required"></span>**ERROR\_DS\_CONFIDENTIALITY\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-219">8237 (0x202D)</span><span class="sxs-lookup"><span data-stu-id="3ad11-219">8237 (0x202D)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-220">Esta solicitud requiere una conexión segura.</span><span class="sxs-lookup"><span data-stu-id="3ad11-220">This request requires a secure connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-221"><span id="ERROR_DS_INAPPROPRIATE_MATCHING"></span><span id="error_ds_inappropriate_matching"></span>**ERROR \_ de \_ coincidencia incorrecta de DS \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-221"><span id="ERROR_DS_INAPPROPRIATE_MATCHING"></span><span id="error_ds_inappropriate_matching"></span>**ERROR\_DS\_INAPPROPRIATE\_MATCHING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-222">8238 (0x202E)</span><span class="sxs-lookup"><span data-stu-id="3ad11-222">8238 (0x202E)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-223">Coincidencia inadecuada.</span><span class="sxs-lookup"><span data-stu-id="3ad11-223">Inappropriate matching.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-224"><span id="ERROR_DS_CONSTRAINT_VIOLATION"></span><span id="error_ds_constraint_violation"></span>**ERROR \_ de \_ infracción de restricción de DS \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-224"><span id="ERROR_DS_CONSTRAINT_VIOLATION"></span><span id="error_ds_constraint_violation"></span>**ERROR\_DS\_CONSTRAINT\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-225">8239 (0x202F)</span><span class="sxs-lookup"><span data-stu-id="3ad11-225">8239 (0x202F)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-226">Se ha producido una infracción de restricción.</span><span class="sxs-lookup"><span data-stu-id="3ad11-226">A constraint violation occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-227"><span id="ERROR_DS_NO_SUCH_OBJECT"></span><span id="error_ds_no_such_object"></span>**ERROR \_ DS \_ no \_ tal \_ objeto**</span><span class="sxs-lookup"><span data-stu-id="3ad11-227"><span id="ERROR_DS_NO_SUCH_OBJECT"></span><span id="error_ds_no_such_object"></span>**ERROR\_DS\_NO\_SUCH\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-228">8240 (0x2030)</span><span class="sxs-lookup"><span data-stu-id="3ad11-228">8240 (0x2030)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-229">No existe tal objeto en el servidor.</span><span class="sxs-lookup"><span data-stu-id="3ad11-229">There is no such object on the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-230"><span id="ERROR_DS_ALIAS_PROBLEM"></span><span id="error_ds_alias_problem"></span>**\_problema de \_ alias de DS de error \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-230"><span id="ERROR_DS_ALIAS_PROBLEM"></span><span id="error_ds_alias_problem"></span>**ERROR\_DS\_ALIAS\_PROBLEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-231">8241 (0x2031)</span><span class="sxs-lookup"><span data-stu-id="3ad11-231">8241 (0x2031)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-232">Hay un problema de alias.</span><span class="sxs-lookup"><span data-stu-id="3ad11-232">There is an alias problem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-233"><span id="ERROR_DS_INVALID_DN_SYNTAX"></span><span id="error_ds_invalid_dn_syntax"></span>**ERROR \_ DS \_ \_ Sintaxis DN no válida \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-233"><span id="ERROR_DS_INVALID_DN_SYNTAX"></span><span id="error_ds_invalid_dn_syntax"></span>**ERROR\_DS\_INVALID\_DN\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-234">8242 (0x2032)</span><span class="sxs-lookup"><span data-stu-id="3ad11-234">8242 (0x2032)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-235">Se ha especificado una sintaxis DN no válida.</span><span class="sxs-lookup"><span data-stu-id="3ad11-235">An invalid dn syntax has been specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-236"><span id="ERROR_DS_IS_LEAF"></span><span id="error_ds_is_leaf"></span>**el ERROR de \_ DS \_ es \_ hoja**</span><span class="sxs-lookup"><span data-stu-id="3ad11-236"><span id="ERROR_DS_IS_LEAF"></span><span id="error_ds_is_leaf"></span>**ERROR\_DS\_IS\_LEAF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-237">8243 (0x2033)</span><span class="sxs-lookup"><span data-stu-id="3ad11-237">8243 (0x2033)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-238">El objeto es un objeto hoja.</span><span class="sxs-lookup"><span data-stu-id="3ad11-238">The object is a leaf object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-239"><span id="ERROR_DS_ALIAS_DEREF_PROBLEM"></span><span id="error_ds_alias_deref_problem"></span>**problema de alias de DS de ERROR \_ \_ \_ deref \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-239"><span id="ERROR_DS_ALIAS_DEREF_PROBLEM"></span><span id="error_ds_alias_deref_problem"></span>**ERROR\_DS\_ALIAS\_DEREF\_PROBLEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-240">8244 (0x2034)</span><span class="sxs-lookup"><span data-stu-id="3ad11-240">8244 (0x2034)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-241">Hay un problema de desreferenciación de alias.</span><span class="sxs-lookup"><span data-stu-id="3ad11-241">There is an alias dereferencing problem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-242"><span id="ERROR_DS_UNWILLING_TO_PERFORM"></span><span id="error_ds_unwilling_to_perform"></span>**ERROR \_ \_ de DS que no \_ se \_ realizará**</span><span class="sxs-lookup"><span data-stu-id="3ad11-242"><span id="ERROR_DS_UNWILLING_TO_PERFORM"></span><span id="error_ds_unwilling_to_perform"></span>**ERROR\_DS\_UNWILLING\_TO\_PERFORM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-243">8245 (0x2035)</span><span class="sxs-lookup"><span data-stu-id="3ad11-243">8245 (0x2035)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-244">El servidor no va a procesar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3ad11-244">The server is unwilling to process the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-245"><span id="ERROR_DS_LOOP_DETECT"></span><span id="error_ds_loop_detect"></span>**ERROR \_ de \_ detección de bucle DS \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-245"><span id="ERROR_DS_LOOP_DETECT"></span><span id="error_ds_loop_detect"></span>**ERROR\_DS\_LOOP\_DETECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-246">8246 (0x2036)</span><span class="sxs-lookup"><span data-stu-id="3ad11-246">8246 (0x2036)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-247">Se ha detectado un bucle.</span><span class="sxs-lookup"><span data-stu-id="3ad11-247">A loop has been detected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-248"><span id="ERROR_DS_NAMING_VIOLATION"></span><span id="error_ds_naming_violation"></span>**ERROR \_ de \_ infracción de nomenclatura de DS \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-248"><span id="ERROR_DS_NAMING_VIOLATION"></span><span id="error_ds_naming_violation"></span>**ERROR\_DS\_NAMING\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-249">8247 (0x2037)</span><span class="sxs-lookup"><span data-stu-id="3ad11-249">8247 (0x2037)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-250">Existe una infracción de nomenclatura.</span><span class="sxs-lookup"><span data-stu-id="3ad11-250">There is a naming violation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-251"><span id="ERROR_DS_OBJECT_RESULTS_TOO_LARGE"></span><span id="error_ds_object_results_too_large"></span>**\_los resultados del objeto DS de error son \_ \_ \_ demasiado \_ grandes**</span><span class="sxs-lookup"><span data-stu-id="3ad11-251"><span id="ERROR_DS_OBJECT_RESULTS_TOO_LARGE"></span><span id="error_ds_object_results_too_large"></span>**ERROR\_DS\_OBJECT\_RESULTS\_TOO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-252">8248 (0x2038)</span><span class="sxs-lookup"><span data-stu-id="3ad11-252">8248 (0x2038)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-253">El conjunto de resultados es demasiado grande.</span><span class="sxs-lookup"><span data-stu-id="3ad11-253">The result set is too large.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-254"><span id="ERROR_DS_AFFECTS_MULTIPLE_DSAS"></span><span id="error_ds_affects_multiple_dsas"></span>**el ERROR de \_ DS \_ afecta a \_ varios \_ DSA**</span><span class="sxs-lookup"><span data-stu-id="3ad11-254"><span id="ERROR_DS_AFFECTS_MULTIPLE_DSAS"></span><span id="error_ds_affects_multiple_dsas"></span>**ERROR\_DS\_AFFECTS\_MULTIPLE\_DSAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-255">8249 (0x2039)</span><span class="sxs-lookup"><span data-stu-id="3ad11-255">8249 (0x2039)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-256">La operación afecta a varios DSA.</span><span class="sxs-lookup"><span data-stu-id="3ad11-256">The operation affects multiple DSAs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-257"><span id="ERROR_DS_SERVER_DOWN"></span><span id="error_ds_server_down"></span>**ERROR en el \_ servidor de DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-257"><span id="ERROR_DS_SERVER_DOWN"></span><span id="error_ds_server_down"></span>**ERROR\_DS\_SERVER\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-258">8250 (0x203A)</span><span class="sxs-lookup"><span data-stu-id="3ad11-258">8250 (0x203A)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-259">el servidor no es funcional.</span><span class="sxs-lookup"><span data-stu-id="3ad11-259">The server is not operational.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-260"><span id="ERROR_DS_LOCAL_ERROR"></span><span id="error_ds_local_error"></span>**error de \_ DS \_ local \_ error**</span><span class="sxs-lookup"><span data-stu-id="3ad11-260"><span id="ERROR_DS_LOCAL_ERROR"></span><span id="error_ds_local_error"></span>**ERROR\_DS\_LOCAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-261">8251 (0x203B)</span><span class="sxs-lookup"><span data-stu-id="3ad11-261">8251 (0x203B)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-262">Se ha producido un error local.</span><span class="sxs-lookup"><span data-stu-id="3ad11-262">A local error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-263"><span id="ERROR_DS_ENCODING_ERROR"></span><span id="error_ds_encoding_error"></span>**error de \_ codificación de DS de error \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-263"><span id="ERROR_DS_ENCODING_ERROR"></span><span id="error_ds_encoding_error"></span>**ERROR\_DS\_ENCODING\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-264">8252 (0x203C)</span><span class="sxs-lookup"><span data-stu-id="3ad11-264">8252 (0x203C)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-265">Se ha producido un error de codificación.</span><span class="sxs-lookup"><span data-stu-id="3ad11-265">An encoding error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-266"><span id="ERROR_DS_DECODING_ERROR"></span><span id="error_ds_decoding_error"></span>**error \_ de \_ descodificación de DS \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-266"><span id="ERROR_DS_DECODING_ERROR"></span><span id="error_ds_decoding_error"></span>**ERROR\_DS\_DECODING\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-267">8253 (0x203D)</span><span class="sxs-lookup"><span data-stu-id="3ad11-267">8253 (0x203D)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-268">Se ha producido un error de descodificación.</span><span class="sxs-lookup"><span data-stu-id="3ad11-268">A decoding error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-269"><span id="ERROR_DS_FILTER_UNKNOWN"></span><span id="error_ds_filter_unknown"></span>**ERROR \_ de \_ filtro de DS \_ desconocido**</span><span class="sxs-lookup"><span data-stu-id="3ad11-269"><span id="ERROR_DS_FILTER_UNKNOWN"></span><span id="error_ds_filter_unknown"></span>**ERROR\_DS\_FILTER\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-270">8254 (0x203E)</span><span class="sxs-lookup"><span data-stu-id="3ad11-270">8254 (0x203E)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-271">No se reconoce el filtro de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="3ad11-271">The search filter cannot be recognized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-272"><span id="ERROR_DS_PARAM_ERROR"></span><span id="error_ds_param_error"></span>**error \_ de \_ parámetro DS de error \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-272"><span id="ERROR_DS_PARAM_ERROR"></span><span id="error_ds_param_error"></span>**ERROR\_DS\_PARAM\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-273">8255 (0x203F)</span><span class="sxs-lookup"><span data-stu-id="3ad11-273">8255 (0x203F)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-274">Uno o más parámetros no son válidos.</span><span class="sxs-lookup"><span data-stu-id="3ad11-274">One or more parameters are illegal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-275"><span id="ERROR_DS_NOT_SUPPORTED"></span><span id="error_ds_not_supported"></span>**ERROR \_ DS \_ no \_ compatible**</span><span class="sxs-lookup"><span data-stu-id="3ad11-275"><span id="ERROR_DS_NOT_SUPPORTED"></span><span id="error_ds_not_supported"></span>**ERROR\_DS\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-276">8256 (0x2040)</span><span class="sxs-lookup"><span data-stu-id="3ad11-276">8256 (0x2040)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-277">No se admite el método especificado.</span><span class="sxs-lookup"><span data-stu-id="3ad11-277">The specified method is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-278"><span id="ERROR_DS_NO_RESULTS_RETURNED"></span><span id="error_ds_no_results_returned"></span>**ERROR \_ DS \_ no \_ se \_ devolvió ningún resultado**</span><span class="sxs-lookup"><span data-stu-id="3ad11-278"><span id="ERROR_DS_NO_RESULTS_RETURNED"></span><span id="error_ds_no_results_returned"></span>**ERROR\_DS\_NO\_RESULTS\_RETURNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-279">8257 (0x2041)</span><span class="sxs-lookup"><span data-stu-id="3ad11-279">8257 (0x2041)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-280">No se devolvieron resultados.</span><span class="sxs-lookup"><span data-stu-id="3ad11-280">No results were returned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-281"><span id="ERROR_DS_CONTROL_NOT_FOUND"></span><span id="error_ds_control_not_found"></span>**\_ \_ \_ no \_ se encontró el control DS de error**</span><span class="sxs-lookup"><span data-stu-id="3ad11-281"><span id="ERROR_DS_CONTROL_NOT_FOUND"></span><span id="error_ds_control_not_found"></span>**ERROR\_DS\_CONTROL\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-282">8258 (0x2042)</span><span class="sxs-lookup"><span data-stu-id="3ad11-282">8258 (0x2042)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-283">El servidor no admite el control especificado.</span><span class="sxs-lookup"><span data-stu-id="3ad11-283">The specified control is not supported by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-284"><span id="ERROR_DS_CLIENT_LOOP"></span><span id="error_ds_client_loop"></span>**ERROR \_ de \_ bucle de cliente DS \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-284"><span id="ERROR_DS_CLIENT_LOOP"></span><span id="error_ds_client_loop"></span>**ERROR\_DS\_CLIENT\_LOOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-285">8259 (0x2043)</span><span class="sxs-lookup"><span data-stu-id="3ad11-285">8259 (0x2043)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-286">El cliente ha detectado un bucle de referencia.</span><span class="sxs-lookup"><span data-stu-id="3ad11-286">A referral loop was detected by the client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-287"><span id="ERROR_DS_REFERRAL_LIMIT_EXCEEDED"></span><span id="error_ds_referral_limit_exceeded"></span>**se \_ \_ \_ superó el límite de referencia de DS \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-287"><span id="ERROR_DS_REFERRAL_LIMIT_EXCEEDED"></span><span id="error_ds_referral_limit_exceeded"></span>**ERROR\_DS\_REFERRAL\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-288">8260 (0x2044)</span><span class="sxs-lookup"><span data-stu-id="3ad11-288">8260 (0x2044)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-289">Se superó el límite de referencias preestablecidas.</span><span class="sxs-lookup"><span data-stu-id="3ad11-289">The preset referral limit was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-290"><span id="ERROR_DS_SORT_CONTROL_MISSING"></span><span id="error_ds_sort_control_missing"></span>**ERROR \_ \_ no se \_ encuentra el control de ordenación DS \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-290"><span id="ERROR_DS_SORT_CONTROL_MISSING"></span><span id="error_ds_sort_control_missing"></span>**ERROR\_DS\_SORT\_CONTROL\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-291">8261 (0x2045)</span><span class="sxs-lookup"><span data-stu-id="3ad11-291">8261 (0x2045)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-292">La búsqueda requiere un control SORT.</span><span class="sxs-lookup"><span data-stu-id="3ad11-292">The search requires a SORT control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-293"><span id="ERROR_DS_OFFSET_RANGE_ERROR"></span><span id="error_ds_offset_range_error"></span>**error en el intervalo de desplazamiento de \_ DS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-293"><span id="ERROR_DS_OFFSET_RANGE_ERROR"></span><span id="error_ds_offset_range_error"></span>**ERROR\_DS\_OFFSET\_RANGE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-294">8262 (0x2046)</span><span class="sxs-lookup"><span data-stu-id="3ad11-294">8262 (0x2046)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-295">Los resultados de la búsqueda superan el intervalo de desplazamiento especificado.</span><span class="sxs-lookup"><span data-stu-id="3ad11-295">The search results exceed the offset range specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-296"><span id="ERROR_DS_RIDMGR_DISABLED"></span><span id="error_ds_ridmgr_disabled"></span>**ERROR de \_ DS \_ RIDMGR \_ deshabilitado**</span><span class="sxs-lookup"><span data-stu-id="3ad11-296"><span id="ERROR_DS_RIDMGR_DISABLED"></span><span id="error_ds_ridmgr_disabled"></span>**ERROR\_DS\_RIDMGR\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-297">8263 (0x2047)</span><span class="sxs-lookup"><span data-stu-id="3ad11-297">8263 (0x2047)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-298">El servicio de directorio detectó que el subsistema que asigna identificadores relativos está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="3ad11-298">The directory service detected the subsystem that allocates relative identifiers is disabled.</span></span> <span data-ttu-id="3ad11-299">Esto puede ocurrir como un mecanismo de protección cuando el sistema determina que se ha agotado una parte importante de los identificadores relativos (RID).</span><span class="sxs-lookup"><span data-stu-id="3ad11-299">This can occur as a protective mechanism when the system determines a significant portion of relative identifiers (RIDs) have been exhausted.</span></span> <span data-ttu-id="3ad11-300">Consulte <https://go.microsoft.com/fwlink/p/?linkid=228610> para ver los pasos de diagnóstico recomendados y el procedimiento para volver a habilitar la creación de cuentas.</span><span class="sxs-lookup"><span data-stu-id="3ad11-300">Please see <https://go.microsoft.com/fwlink/p/?linkid=228610> for recommended diagnostic steps and the procedure to re-enable account creation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-301"><span id="ERROR_DS_ROOT_MUST_BE_NC"></span><span id="error_ds_root_must_be_nc"></span>**el ERROR de la \_ \_ raíz DS \_ debe \_ ser \_ NC**</span><span class="sxs-lookup"><span data-stu-id="3ad11-301"><span id="ERROR_DS_ROOT_MUST_BE_NC"></span><span id="error_ds_root_must_be_nc"></span>**ERROR\_DS\_ROOT\_MUST\_BE\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-302">8301 (0x206D)</span><span class="sxs-lookup"><span data-stu-id="3ad11-302">8301 (0x206D)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-303">El objeto raíz debe ser el encabezado de un contexto de nomenclatura.</span><span class="sxs-lookup"><span data-stu-id="3ad11-303">The root object must be the head of a naming context.</span></span> <span data-ttu-id="3ad11-304">El objeto raíz no puede tener un elemento primario con instancias.</span><span class="sxs-lookup"><span data-stu-id="3ad11-304">The root object cannot have an instantiated parent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-305"><span id="ERROR_DS_ADD_REPLICA_INHIBITED"></span><span id="error_ds_add_replica_inhibited"></span>**ERROR de la \_ réplica de adición de DS \_ \_ \_ desbloqueado**</span><span class="sxs-lookup"><span data-stu-id="3ad11-305"><span id="ERROR_DS_ADD_REPLICA_INHIBITED"></span><span id="error_ds_add_replica_inhibited"></span>**ERROR\_DS\_ADD\_REPLICA\_INHIBITED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-306">8302 (0x206E)</span><span class="sxs-lookup"><span data-stu-id="3ad11-306">8302 (0x206E)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-307">No se puede realizar la operación de agregar réplica.</span><span class="sxs-lookup"><span data-stu-id="3ad11-307">The add replica operation cannot be performed.</span></span> <span data-ttu-id="3ad11-308">El contexto de nomenclatura debe ser grabable para poder crear la réplica.</span><span class="sxs-lookup"><span data-stu-id="3ad11-308">The naming context must be writeable in order to create the replica.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-309"><span id="ERROR_DS_ATT_NOT_DEF_IN_SCHEMA"></span><span id="error_ds_att_not_def_in_schema"></span>**ERROR \_ DS \_ ATT \_ no \_ Def \_ en el \_ esquema**</span><span class="sxs-lookup"><span data-stu-id="3ad11-309"><span id="ERROR_DS_ATT_NOT_DEF_IN_SCHEMA"></span><span id="error_ds_att_not_def_in_schema"></span>**ERROR\_DS\_ATT\_NOT\_DEF\_IN\_SCHEMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-310">8303 (0x206F)</span><span class="sxs-lookup"><span data-stu-id="3ad11-310">8303 (0x206F)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-311">Se ha producido una referencia a un atributo que no está definido en el esquema.</span><span class="sxs-lookup"><span data-stu-id="3ad11-311">A reference to an attribute that is not defined in the schema occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-312"><span id="ERROR_DS_MAX_OBJ_SIZE_EXCEEDED"></span><span id="error_ds_max_obj_size_exceeded"></span>**se \_ \_ \_ \_ superó el tamaño máximo de obj de DS de error \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-312"><span id="ERROR_DS_MAX_OBJ_SIZE_EXCEEDED"></span><span id="error_ds_max_obj_size_exceeded"></span>**ERROR\_DS\_MAX\_OBJ\_SIZE\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-313">8304 (0x2070)</span><span class="sxs-lookup"><span data-stu-id="3ad11-313">8304 (0x2070)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-314">Se ha superado el tamaño máximo de un objeto.</span><span class="sxs-lookup"><span data-stu-id="3ad11-314">The maximum size of an object has been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-315"><span id="ERROR_DS_OBJ_STRING_NAME_EXISTS"></span><span id="error_ds_obj_string_name_exists"></span>**ERROR \_ DS \_ \_ el nombre de la cadena obj \_ \_ existe**</span><span class="sxs-lookup"><span data-stu-id="3ad11-315"><span id="ERROR_DS_OBJ_STRING_NAME_EXISTS"></span><span id="error_ds_obj_string_name_exists"></span>**ERROR\_DS\_OBJ\_STRING\_NAME\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-316">8305 (0x2071)</span><span class="sxs-lookup"><span data-stu-id="3ad11-316">8305 (0x2071)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-317">Se intentó agregar un objeto al directorio con un nombre que ya está en uso.</span><span class="sxs-lookup"><span data-stu-id="3ad11-317">An attempt was made to add an object to the directory with a name that is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-318"><span id="ERROR_DS_NO_RDN_DEFINED_IN_SCHEMA"></span><span id="error_ds_no_rdn_defined_in_schema"></span>**ERROR \_ DS \_ no \_ se \_ ha definido ningún RDN \_ en el \_ esquema**</span><span class="sxs-lookup"><span data-stu-id="3ad11-318"><span id="ERROR_DS_NO_RDN_DEFINED_IN_SCHEMA"></span><span id="error_ds_no_rdn_defined_in_schema"></span>**ERROR\_DS\_NO\_RDN\_DEFINED\_IN\_SCHEMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-319">8306 (0x2072)</span><span class="sxs-lookup"><span data-stu-id="3ad11-319">8306 (0x2072)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-320">Se intentó agregar un objeto de una clase que no tiene un RDN definido en el esquema.</span><span class="sxs-lookup"><span data-stu-id="3ad11-320">An attempt was made to add an object of a class that does not have an RDN defined in the schema.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-321"><span id="ERROR_DS_RDN_DOESNT_MATCH_SCHEMA"></span><span id="error_ds_rdn_doesnt_match_schema"></span>**esquema de ERROR \_ DS no \_ \_ \_ coincidente de RDN \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-321"><span id="ERROR_DS_RDN_DOESNT_MATCH_SCHEMA"></span><span id="error_ds_rdn_doesnt_match_schema"></span>**ERROR\_DS\_RDN\_DOESNT\_MATCH\_SCHEMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-322">8307 (0x2073)</span><span class="sxs-lookup"><span data-stu-id="3ad11-322">8307 (0x2073)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-323">Se intentó agregar un objeto con un RDN que no es el RDN definido en el esquema.</span><span class="sxs-lookup"><span data-stu-id="3ad11-323">An attempt was made to add an object using an RDN that is not the RDN defined in the schema.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-324"><span id="ERROR_DS_NO_REQUESTED_ATTS_FOUND"></span><span id="error_ds_no_requested_atts_found"></span>**ERROR \_ DS \_ no \_ \_ \_ se ha solicitado ATTS**</span><span class="sxs-lookup"><span data-stu-id="3ad11-324"><span id="ERROR_DS_NO_REQUESTED_ATTS_FOUND"></span><span id="error_ds_no_requested_atts_found"></span>**ERROR\_DS\_NO\_REQUESTED\_ATTS\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-325">8308 (0x2074)</span><span class="sxs-lookup"><span data-stu-id="3ad11-325">8308 (0x2074)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-326">No se encontró ninguno de los atributos solicitados en los objetos.</span><span class="sxs-lookup"><span data-stu-id="3ad11-326">None of the requested attributes were found on the objects.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-327"><span id="ERROR_DS_USER_BUFFER_TO_SMALL"></span><span id="error_ds_user_buffer_to_small"></span>**ERROR \_ \_ \_ \_ de búfer de usuario de DS a \_ pequeño**</span><span class="sxs-lookup"><span data-stu-id="3ad11-327"><span id="ERROR_DS_USER_BUFFER_TO_SMALL"></span><span id="error_ds_user_buffer_to_small"></span>**ERROR\_DS\_USER\_BUFFER\_TO\_SMALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-328">8309 (0x2075)</span><span class="sxs-lookup"><span data-stu-id="3ad11-328">8309 (0x2075)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-329">El búfer del usuario es demasiado pequeño.</span><span class="sxs-lookup"><span data-stu-id="3ad11-329">The user buffer is too small.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-330"><span id="ERROR_DS_ATT_IS_NOT_ON_OBJ"></span><span id="error_ds_att_is_not_on_obj"></span>**ERROR \_ DS \_ ATT \_ \_ no está \_ en \_ obj**</span><span class="sxs-lookup"><span data-stu-id="3ad11-330"><span id="ERROR_DS_ATT_IS_NOT_ON_OBJ"></span><span id="error_ds_att_is_not_on_obj"></span>**ERROR\_DS\_ATT\_IS\_NOT\_ON\_OBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-331">8310 (0x2076)</span><span class="sxs-lookup"><span data-stu-id="3ad11-331">8310 (0x2076)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-332">El atributo especificado en la operación no está presente en el objeto.</span><span class="sxs-lookup"><span data-stu-id="3ad11-332">The attribute specified in the operation is not present on the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-333"><span id="ERROR_DS_ILLEGAL_MOD_OPERATION"></span><span id="error_ds_illegal_mod_operation"></span>**ERROR \_ DS \_ no válido de \_ operación de modificación \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-333"><span id="ERROR_DS_ILLEGAL_MOD_OPERATION"></span><span id="error_ds_illegal_mod_operation"></span>**ERROR\_DS\_ILLEGAL\_MOD\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-334">8311 (0x2077)</span><span class="sxs-lookup"><span data-stu-id="3ad11-334">8311 (0x2077)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-335">Operación de modificación no válida.</span><span class="sxs-lookup"><span data-stu-id="3ad11-335">Illegal modify operation.</span></span> <span data-ttu-id="3ad11-336">Algunos aspectos de la modificación no se permiten.</span><span class="sxs-lookup"><span data-stu-id="3ad11-336">Some aspect of the modification is not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-337"><span id="ERROR_DS_OBJ_TOO_LARGE"></span><span id="error_ds_obj_too_large"></span>**el \_ obj DS de error \_ \_ es demasiado \_ grande**</span><span class="sxs-lookup"><span data-stu-id="3ad11-337"><span id="ERROR_DS_OBJ_TOO_LARGE"></span><span id="error_ds_obj_too_large"></span>**ERROR\_DS\_OBJ\_TOO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-338">8312 (0x2078)</span><span class="sxs-lookup"><span data-stu-id="3ad11-338">8312 (0x2078)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-339">El objeto especificado es demasiado grande.</span><span class="sxs-lookup"><span data-stu-id="3ad11-339">The specified object is too large.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-340"><span id="ERROR_DS_BAD_INSTANCE_TYPE"></span><span id="error_ds_bad_instance_type"></span>**ERROR en el \_ \_ tipo de instancia incorrecta de DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-340"><span id="ERROR_DS_BAD_INSTANCE_TYPE"></span><span id="error_ds_bad_instance_type"></span>**ERROR\_DS\_BAD\_INSTANCE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-341">8313 (0x2079)</span><span class="sxs-lookup"><span data-stu-id="3ad11-341">8313 (0x2079)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-342">El tipo de instancia especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="3ad11-342">The specified instance type is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-343"><span id="ERROR_DS_MASTERDSA_REQUIRED"></span><span id="error_ds_masterdsa_required"></span>**ERROR de \_ DS \_ MASTERDSA \_ requerido**</span><span class="sxs-lookup"><span data-stu-id="3ad11-343"><span id="ERROR_DS_MASTERDSA_REQUIRED"></span><span id="error_ds_masterdsa_required"></span>**ERROR\_DS\_MASTERDSA\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-344">8314 (0x207A)</span><span class="sxs-lookup"><span data-stu-id="3ad11-344">8314 (0x207A)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-345">La operación se debe realizar en un DSA maestro.</span><span class="sxs-lookup"><span data-stu-id="3ad11-345">The operation must be performed at a master DSA.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-346"><span id="ERROR_DS_OBJECT_CLASS_REQUIRED"></span><span id="error_ds_object_class_required"></span>**se \_ \_ requiere la \_ clase de objeto DS de error \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-346"><span id="ERROR_DS_OBJECT_CLASS_REQUIRED"></span><span id="error_ds_object_class_required"></span>**ERROR\_DS\_OBJECT\_CLASS\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-347">8315 (0x207B)</span><span class="sxs-lookup"><span data-stu-id="3ad11-347">8315 (0x207B)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-348">Se debe especificar el atributo de clase de objeto.</span><span class="sxs-lookup"><span data-stu-id="3ad11-348">The object class attribute must be specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-349"><span id="ERROR_DS_MISSING_REQUIRED_ATT"></span><span id="error_ds_missing_required_att"></span>**ERROR \_ DS \_ falta \_ \_ ATT**</span><span class="sxs-lookup"><span data-stu-id="3ad11-349"><span id="ERROR_DS_MISSING_REQUIRED_ATT"></span><span id="error_ds_missing_required_att"></span>**ERROR\_DS\_MISSING\_REQUIRED\_ATT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-350">8316 (0x207C)</span><span class="sxs-lookup"><span data-stu-id="3ad11-350">8316 (0x207C)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-351">Falta un atributo requerido.</span><span class="sxs-lookup"><span data-stu-id="3ad11-351">A required attribute is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-352"><span id="ERROR_DS_ATT_NOT_DEF_FOR_CLASS"></span><span id="error_ds_att_not_def_for_class"></span>**ERROR \_ DS \_ ATT \_ no \_ Def \_ para la \_ clase**</span><span class="sxs-lookup"><span data-stu-id="3ad11-352"><span id="ERROR_DS_ATT_NOT_DEF_FOR_CLASS"></span><span id="error_ds_att_not_def_for_class"></span>**ERROR\_DS\_ATT\_NOT\_DEF\_FOR\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-353">8317 (0x207D)</span><span class="sxs-lookup"><span data-stu-id="3ad11-353">8317 (0x207D)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-354">Se intentó modificar un objeto para incluir un atributo que no es válido para su clase.</span><span class="sxs-lookup"><span data-stu-id="3ad11-354">An attempt was made to modify an object to include an attribute that is not legal for its class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-355"><span id="ERROR_DS_ATT_ALREADY_EXISTS"></span><span id="error_ds_att_already_exists"></span>**el ERROR \_ DS \_ ATT \_ ya \_ existe**</span><span class="sxs-lookup"><span data-stu-id="3ad11-355"><span id="ERROR_DS_ATT_ALREADY_EXISTS"></span><span id="error_ds_att_already_exists"></span>**ERROR\_DS\_ATT\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-356">8318 (0x207E)</span><span class="sxs-lookup"><span data-stu-id="3ad11-356">8318 (0x207E)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-357">El atributo especificado ya está presente en el objeto.</span><span class="sxs-lookup"><span data-stu-id="3ad11-357">The specified attribute is already present on the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-358"><span id="ERROR_DS_CANT_ADD_ATT_VALUES"></span><span id="error_ds_cant_add_att_values"></span>**ERROR DS no se pudo \_ \_ \_ agregar \_ valores de ATT \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-358"><span id="ERROR_DS_CANT_ADD_ATT_VALUES"></span><span id="error_ds_cant_add_att_values"></span>**ERROR\_DS\_CANT\_ADD\_ATT\_VALUES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-359">8320 (0x2080)</span><span class="sxs-lookup"><span data-stu-id="3ad11-359">8320 (0x2080)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-360">El atributo especificado no está presente o no tiene valores.</span><span class="sxs-lookup"><span data-stu-id="3ad11-360">The specified attribute is not present, or has no values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-361"><span id="ERROR_DS_SINGLE_VALUE_CONSTRAINT"></span><span id="error_ds_single_value_constraint"></span>**ERROR \_ de \_ \_ restricción de valor único de DS \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-361"><span id="ERROR_DS_SINGLE_VALUE_CONSTRAINT"></span><span id="error_ds_single_value_constraint"></span>**ERROR\_DS\_SINGLE\_VALUE\_CONSTRAINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-362">8321 (0x2081)</span><span class="sxs-lookup"><span data-stu-id="3ad11-362">8321 (0x2081)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-363">Se especificaron varios valores para un atributo que solo puede tener un valor.</span><span class="sxs-lookup"><span data-stu-id="3ad11-363">Multiple values were specified for an attribute that can have only one value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-364"><span id="ERROR_DS_RANGE_CONSTRAINT"></span><span id="error_ds_range_constraint"></span>**\_restricción de \_ intervalo de DS de error \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-364"><span id="ERROR_DS_RANGE_CONSTRAINT"></span><span id="error_ds_range_constraint"></span>**ERROR\_DS\_RANGE\_CONSTRAINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-365">8322 (0x2082)</span><span class="sxs-lookup"><span data-stu-id="3ad11-365">8322 (0x2082)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-366">Un valor para el atributo no se encontraba en el intervalo aceptable de valores.</span><span class="sxs-lookup"><span data-stu-id="3ad11-366">A value for the attribute was not in the acceptable range of values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-367"><span id="ERROR_DS_ATT_VAL_ALREADY_EXISTS"></span><span id="error_ds_att_val_already_exists"></span>**el ERROR \_ DS \_ ATT \_ Val \_ ya \_ existe**</span><span class="sxs-lookup"><span data-stu-id="3ad11-367"><span id="ERROR_DS_ATT_VAL_ALREADY_EXISTS"></span><span id="error_ds_att_val_already_exists"></span>**ERROR\_DS\_ATT\_VAL\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-368">8323 (0x2083)</span><span class="sxs-lookup"><span data-stu-id="3ad11-368">8323 (0x2083)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-369">El valor especificado ya existe.</span><span class="sxs-lookup"><span data-stu-id="3ad11-369">The specified value already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-370"><span id="ERROR_DS_CANT_REM_MISSING_ATT"></span><span id="error_ds_cant_rem_missing_att"></span>**ERROR \_ DS \_ \_ no se \_ encuentra \_ la**</span><span class="sxs-lookup"><span data-stu-id="3ad11-370"><span id="ERROR_DS_CANT_REM_MISSING_ATT"></span><span id="error_ds_cant_rem_missing_att"></span>**ERROR\_DS\_CANT\_REM\_MISSING\_ATT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-371">8324 (0x2084)</span><span class="sxs-lookup"><span data-stu-id="3ad11-371">8324 (0x2084)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-372">No se puede quitar el atributo porque no está presente en el objeto.</span><span class="sxs-lookup"><span data-stu-id="3ad11-372">The attribute cannot be removed because it is not present on the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-373"><span id="ERROR_DS_CANT_REM_MISSING_ATT_VAL"></span><span id="error_ds_cant_rem_missing_att_val"></span>**ERROR \_ DS \_ \_ no se \_ encuentra \_ el \_ Val de ATT**</span><span class="sxs-lookup"><span data-stu-id="3ad11-373"><span id="ERROR_DS_CANT_REM_MISSING_ATT_VAL"></span><span id="error_ds_cant_rem_missing_att_val"></span>**ERROR\_DS\_CANT\_REM\_MISSING\_ATT\_VAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-374">8325 (0x2085)</span><span class="sxs-lookup"><span data-stu-id="3ad11-374">8325 (0x2085)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-375">No se puede quitar el valor de atributo porque no está presente en el objeto.</span><span class="sxs-lookup"><span data-stu-id="3ad11-375">The attribute value cannot be removed because it is not present on the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-376"><span id="ERROR_DS_ROOT_CANT_BE_SUBREF"></span><span id="error_ds_root_cant_be_subref"></span>**ERROR la \_ raíz de DS no \_ \_ \_ se puede \_ SUBREF**</span><span class="sxs-lookup"><span data-stu-id="3ad11-376"><span id="ERROR_DS_ROOT_CANT_BE_SUBREF"></span><span id="error_ds_root_cant_be_subref"></span>**ERROR\_DS\_ROOT\_CANT\_BE\_SUBREF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-377">8326 (0x2086)</span><span class="sxs-lookup"><span data-stu-id="3ad11-377">8326 (0x2086)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-378">El objeto raíz especificado no puede ser un subref.</span><span class="sxs-lookup"><span data-stu-id="3ad11-378">The specified root object cannot be a subref.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-379"><span id="ERROR_DS_NO_CHAINING"></span><span id="error_ds_no_chaining"></span>**ERROR \_ DS \_ sin \_ encadenamiento**</span><span class="sxs-lookup"><span data-stu-id="3ad11-379"><span id="ERROR_DS_NO_CHAINING"></span><span id="error_ds_no_chaining"></span>**ERROR\_DS\_NO\_CHAINING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-380">8327 (0x2087)</span><span class="sxs-lookup"><span data-stu-id="3ad11-380">8327 (0x2087)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-381">No se permite el encadenamiento.</span><span class="sxs-lookup"><span data-stu-id="3ad11-381">Chaining is not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-382"><span id="ERROR_DS_NO_CHAINED_EVAL"></span><span id="error_ds_no_chained_eval"></span>**ERROR \_ DS \_ sin \_ cadena \_ eval**</span><span class="sxs-lookup"><span data-stu-id="3ad11-382"><span id="ERROR_DS_NO_CHAINED_EVAL"></span><span id="error_ds_no_chained_eval"></span>**ERROR\_DS\_NO\_CHAINED\_EVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-383">8328 (0x2088)</span><span class="sxs-lookup"><span data-stu-id="3ad11-383">8328 (0x2088)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-384">No se permite la evaluación encadenada.</span><span class="sxs-lookup"><span data-stu-id="3ad11-384">Chained evaluation is not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-385"><span id="ERROR_DS_NO_PARENT_OBJECT"></span><span id="error_ds_no_parent_object"></span>**ERROR \_ DS \_ ningún \_ \_ objeto primario**</span><span class="sxs-lookup"><span data-stu-id="3ad11-385"><span id="ERROR_DS_NO_PARENT_OBJECT"></span><span id="error_ds_no_parent_object"></span>**ERROR\_DS\_NO\_PARENT\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-386">8329 (0x2089)</span><span class="sxs-lookup"><span data-stu-id="3ad11-386">8329 (0x2089)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-387">No se puede realizar la operación porque el principal del objeto no se ha instanciado o se ha eliminado.</span><span class="sxs-lookup"><span data-stu-id="3ad11-387">The operation could not be performed because the object's parent is either uninstantiated or deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-388"><span id="ERROR_DS_PARENT_IS_AN_ALIAS"></span><span id="error_ds_parent_is_an_alias"></span>**ERROR \_ DS \_ primario \_ es \_ un \_ alias**</span><span class="sxs-lookup"><span data-stu-id="3ad11-388"><span id="ERROR_DS_PARENT_IS_AN_ALIAS"></span><span id="error_ds_parent_is_an_alias"></span>**ERROR\_DS\_PARENT\_IS\_AN\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-389">8330 (0x208A)</span><span class="sxs-lookup"><span data-stu-id="3ad11-389">8330 (0x208A)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-390">No se permite tener un elemento primario que sea un alias.</span><span class="sxs-lookup"><span data-stu-id="3ad11-390">Having a parent that is an alias is not permitted.</span></span> <span data-ttu-id="3ad11-391">Los alias son objetos hoja.</span><span class="sxs-lookup"><span data-stu-id="3ad11-391">Aliases are leaf objects.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-392"><span id="ERROR_DS_CANT_MIX_MASTER_AND_REPS"></span><span id="error_ds_cant_mix_master_and_reps"></span>**ERROR DS no se pudo \_ \_ \_ mezclar \_ Master \_ y \_ reps**</span><span class="sxs-lookup"><span data-stu-id="3ad11-392"><span id="ERROR_DS_CANT_MIX_MASTER_AND_REPS"></span><span id="error_ds_cant_mix_master_and_reps"></span>**ERROR\_DS\_CANT\_MIX\_MASTER\_AND\_REPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-393">8331 (0x208B)</span><span class="sxs-lookup"><span data-stu-id="3ad11-393">8331 (0x208B)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-394">El objeto y el elemento primario deben ser del mismo tipo, tanto maestros como ambas réplicas.</span><span class="sxs-lookup"><span data-stu-id="3ad11-394">The object and parent must be of the same type, either both masters or both replicas.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-395"><span id="ERROR_DS_CHILDREN_EXIST"></span><span id="error_ds_children_exist"></span>**ERROR \_ DS los \_ elementos secundarios \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-395"><span id="ERROR_DS_CHILDREN_EXIST"></span><span id="error_ds_children_exist"></span>**ERROR\_DS\_CHILDREN\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-396">8332 (0x208C)</span><span class="sxs-lookup"><span data-stu-id="3ad11-396">8332 (0x208C)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-397">No se puede realizar la operación porque existen objetos secundarios.</span><span class="sxs-lookup"><span data-stu-id="3ad11-397">The operation cannot be performed because child objects exist.</span></span> <span data-ttu-id="3ad11-398">Esta operación solo se puede realizar en un objeto hoja.</span><span class="sxs-lookup"><span data-stu-id="3ad11-398">This operation can only be performed on a leaf object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-399"><span id="ERROR_DS_OBJ_NOT_FOUND"></span><span id="error_ds_obj_not_found"></span>**\_ \_ \_ no \_ se encontró el obj del DS de error**</span><span class="sxs-lookup"><span data-stu-id="3ad11-399"><span id="ERROR_DS_OBJ_NOT_FOUND"></span><span id="error_ds_obj_not_found"></span>**ERROR\_DS\_OBJ\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-400">8333 (0x208D)</span><span class="sxs-lookup"><span data-stu-id="3ad11-400">8333 (0x208D)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-401">No se encontró el objeto de directorio.</span><span class="sxs-lookup"><span data-stu-id="3ad11-401">Directory object not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-402"><span id="ERROR_DS_ALIASED_OBJ_MISSING"></span><span id="error_ds_aliased_obj_missing"></span>**\_falta el \_ obj con alias de DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-402"><span id="ERROR_DS_ALIASED_OBJ_MISSING"></span><span id="error_ds_aliased_obj_missing"></span>**ERROR\_DS\_ALIASED\_OBJ\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-403">8334 (0x208E)</span><span class="sxs-lookup"><span data-stu-id="3ad11-403">8334 (0x208E)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-404">Falta el objeto con alias.</span><span class="sxs-lookup"><span data-stu-id="3ad11-404">The aliased object is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-405"><span id="ERROR_DS_BAD_NAME_SYNTAX"></span><span id="error_ds_bad_name_syntax"></span>**ERROR \_ de \_ \_ Sintaxis de nombre incorrecto de DS \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-405"><span id="ERROR_DS_BAD_NAME_SYNTAX"></span><span id="error_ds_bad_name_syntax"></span>**ERROR\_DS\_BAD\_NAME\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-406">8335 (0x208F)</span><span class="sxs-lookup"><span data-stu-id="3ad11-406">8335 (0x208F)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-407">El nombre del objeto tiene una sintaxis incorrecta.</span><span class="sxs-lookup"><span data-stu-id="3ad11-407">The object name has bad syntax.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-408"><span id="ERROR_DS_ALIAS_POINTS_TO_ALIAS"></span><span id="error_ds_alias_points_to_alias"></span>**el \_ alias \_ \_ de DS de error señala \_ a \_ alias**</span><span class="sxs-lookup"><span data-stu-id="3ad11-408"><span id="ERROR_DS_ALIAS_POINTS_TO_ALIAS"></span><span id="error_ds_alias_points_to_alias"></span>**ERROR\_DS\_ALIAS\_POINTS\_TO\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-409">8336 (0x2090)</span><span class="sxs-lookup"><span data-stu-id="3ad11-409">8336 (0x2090)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-410">No se permite que un alias haga referencia a otro alias.</span><span class="sxs-lookup"><span data-stu-id="3ad11-410">It is not permitted for an alias to refer to another alias.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-411"><span id="ERROR_DS_CANT_DEREF_ALIAS"></span><span id="error_ds_cant_deref_alias"></span>**ERROR DS no se pudo \_ \_ \_ deref \_ alias**</span><span class="sxs-lookup"><span data-stu-id="3ad11-411"><span id="ERROR_DS_CANT_DEREF_ALIAS"></span><span id="error_ds_cant_deref_alias"></span>**ERROR\_DS\_CANT\_DEREF\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-412">8337 (0x2091)</span><span class="sxs-lookup"><span data-stu-id="3ad11-412">8337 (0x2091)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-413">No se puede desreferenciar el alias.</span><span class="sxs-lookup"><span data-stu-id="3ad11-413">The alias cannot be dereferenced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-414"><span id="ERROR_DS_OUT_OF_SCOPE"></span><span id="error_ds_out_of_scope"></span>**ERROR \_ \_ de DS fuera \_ del \_ ámbito**</span><span class="sxs-lookup"><span data-stu-id="3ad11-414"><span id="ERROR_DS_OUT_OF_SCOPE"></span><span id="error_ds_out_of_scope"></span>**ERROR\_DS\_OUT\_OF\_SCOPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-415">8338 (0x2092)</span><span class="sxs-lookup"><span data-stu-id="3ad11-415">8338 (0x2092)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-416">La operación está fuera del ámbito.</span><span class="sxs-lookup"><span data-stu-id="3ad11-416">The operation is out of scope.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-417"><span id="ERROR_DS_OBJECT_BEING_REMOVED"></span><span id="error_ds_object_being_removed"></span>**ERROR \_ al \_ quitar el objeto DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-417"><span id="ERROR_DS_OBJECT_BEING_REMOVED"></span><span id="error_ds_object_being_removed"></span>**ERROR\_DS\_OBJECT\_BEING\_REMOVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-418">8339 (0x2093)</span><span class="sxs-lookup"><span data-stu-id="3ad11-418">8339 (0x2093)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-419">La operación no puede continuar porque el objeto está en proceso de eliminación.</span><span class="sxs-lookup"><span data-stu-id="3ad11-419">The operation cannot continue because the object is in the process of being removed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-420"><span id="ERROR_DS_CANT_DELETE_DSA_OBJ"></span><span id="error_ds_cant_delete_dsa_obj"></span>**ERROR DS no se pudo \_ \_ eliminar el \_ \_ DSA \_ obj**</span><span class="sxs-lookup"><span data-stu-id="3ad11-420"><span id="ERROR_DS_CANT_DELETE_DSA_OBJ"></span><span id="error_ds_cant_delete_dsa_obj"></span>**ERROR\_DS\_CANT\_DELETE\_DSA\_OBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-421">8340 (0x2094)</span><span class="sxs-lookup"><span data-stu-id="3ad11-421">8340 (0x2094)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-422">No se puede eliminar el objeto DSA.</span><span class="sxs-lookup"><span data-stu-id="3ad11-422">The DSA object cannot be deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-423"><span id="ERROR_DS_GENERIC_ERROR"></span><span id="error_ds_generic_error"></span>**error de \_ DS \_ genérico \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-423"><span id="ERROR_DS_GENERIC_ERROR"></span><span id="error_ds_generic_error"></span>**ERROR\_DS\_GENERIC\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-424">8341 (0x2095)</span><span class="sxs-lookup"><span data-stu-id="3ad11-424">8341 (0x2095)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-425">Error de servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="3ad11-425">A directory service error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-426"><span id="ERROR_DS_DSA_MUST_BE_INT_MASTER"></span><span id="error_ds_dsa_must_be_int_master"></span>**ERROR \_ DS \_ DSA \_ debe \_ ser \_ un \_ maestro int**</span><span class="sxs-lookup"><span data-stu-id="3ad11-426"><span id="ERROR_DS_DSA_MUST_BE_INT_MASTER"></span><span id="error_ds_dsa_must_be_int_master"></span>**ERROR\_DS\_DSA\_MUST\_BE\_INT\_MASTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-427">8342 (0x2096)</span><span class="sxs-lookup"><span data-stu-id="3ad11-427">8342 (0x2096)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-428">La operación solo se puede realizar en un objeto DSA maestro interno.</span><span class="sxs-lookup"><span data-stu-id="3ad11-428">The operation can only be performed on an internal master DSA object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-429"><span id="ERROR_DS_CLASS_NOT_DSA"></span><span id="error_ds_class_not_dsa"></span>**ERROR \_ de \_ clase DS \_ no \_ DSA**</span><span class="sxs-lookup"><span data-stu-id="3ad11-429"><span id="ERROR_DS_CLASS_NOT_DSA"></span><span id="error_ds_class_not_dsa"></span>**ERROR\_DS\_CLASS\_NOT\_DSA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-430">8343 (0x2097)</span><span class="sxs-lookup"><span data-stu-id="3ad11-430">8343 (0x2097)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-431">El objeto debe ser de la clase DSA.</span><span class="sxs-lookup"><span data-stu-id="3ad11-431">The object must be of class DSA.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-432"><span id="ERROR_DS_INSUFF_ACCESS_RIGHTS"></span><span id="error_ds_insuff_access_rights"></span>**\_derechos de \_ acceso de INSUFF de DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-432"><span id="ERROR_DS_INSUFF_ACCESS_RIGHTS"></span><span id="error_ds_insuff_access_rights"></span>**ERROR\_DS\_INSUFF\_ACCESS\_RIGHTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-433">8344 (0x2098)</span><span class="sxs-lookup"><span data-stu-id="3ad11-433">8344 (0x2098)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-434">Derechos de acceso insuficientes para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="3ad11-434">Insufficient access rights to perform the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-435"><span id="ERROR_DS_ILLEGAL_SUPERIOR"></span><span id="error_ds_illegal_superior"></span>**ERROR \_ DS \_ no válido \_ superior**</span><span class="sxs-lookup"><span data-stu-id="3ad11-435"><span id="ERROR_DS_ILLEGAL_SUPERIOR"></span><span id="error_ds_illegal_superior"></span>**ERROR\_DS\_ILLEGAL\_SUPERIOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-436">8345 (0x2099)</span><span class="sxs-lookup"><span data-stu-id="3ad11-436">8345 (0x2099)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-437">No se puede Agregar el objeto porque el elemento primario no está en la lista de posibles superiores.</span><span class="sxs-lookup"><span data-stu-id="3ad11-437">The object cannot be added because the parent is not on the list of possible superiors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-438"><span id="ERROR_DS_ATTRIBUTE_OWNED_BY_SAM"></span><span id="error_ds_attribute_owned_by_sam"></span>**\_atributo DS \_ \_ de error propiedad \_ de \_ Sam**</span><span class="sxs-lookup"><span data-stu-id="3ad11-438"><span id="ERROR_DS_ATTRIBUTE_OWNED_BY_SAM"></span><span id="error_ds_attribute_owned_by_sam"></span>**ERROR\_DS\_ATTRIBUTE\_OWNED\_BY\_SAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-439">8346 (0x209A)</span><span class="sxs-lookup"><span data-stu-id="3ad11-439">8346 (0x209A)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-440">No se permite el acceso al atributo porque el atributo es propiedad del administrador de cuentas de seguridad (SAM).</span><span class="sxs-lookup"><span data-stu-id="3ad11-440">Access to the attribute is not permitted because the attribute is owned by the Security Accounts Manager (SAM).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-441"><span id="ERROR_DS_NAME_TOO_MANY_PARTS"></span><span id="error_ds_name_too_many_parts"></span>**ERROR \_ de \_ nombre de DS \_ demasiadas \_ \_ partes**</span><span class="sxs-lookup"><span data-stu-id="3ad11-441"><span id="ERROR_DS_NAME_TOO_MANY_PARTS"></span><span id="error_ds_name_too_many_parts"></span>**ERROR\_DS\_NAME\_TOO\_MANY\_PARTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-442">8347 (0x209B)</span><span class="sxs-lookup"><span data-stu-id="3ad11-442">8347 (0x209B)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-443">El nombre tiene demasiadas partes.</span><span class="sxs-lookup"><span data-stu-id="3ad11-443">The name has too many parts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-444"><span id="ERROR_DS_NAME_TOO_LONG"></span><span id="error_ds_name_too_long"></span>**ERROR \_ de \_ nombre de DS \_ demasiado \_ largo**</span><span class="sxs-lookup"><span data-stu-id="3ad11-444"><span id="ERROR_DS_NAME_TOO_LONG"></span><span id="error_ds_name_too_long"></span>**ERROR\_DS\_NAME\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-445">8348 (0x209C)</span><span class="sxs-lookup"><span data-stu-id="3ad11-445">8348 (0x209C)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-446">El nombre es demasiado largo.</span><span class="sxs-lookup"><span data-stu-id="3ad11-446">The name is too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-447"><span id="ERROR_DS_NAME_VALUE_TOO_LONG"></span><span id="error_ds_name_value_too_long"></span>**ERROR \_ : \_ el valor del nombre de DS \_ \_ es demasiado \_ largo**</span><span class="sxs-lookup"><span data-stu-id="3ad11-447"><span id="ERROR_DS_NAME_VALUE_TOO_LONG"></span><span id="error_ds_name_value_too_long"></span>**ERROR\_DS\_NAME\_VALUE\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-448">8349 (0x209D)</span><span class="sxs-lookup"><span data-stu-id="3ad11-448">8349 (0x209D)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-449">El valor del nombre es demasiado largo.</span><span class="sxs-lookup"><span data-stu-id="3ad11-449">The name value is too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-450"><span id="ERROR_DS_NAME_UNPARSEABLE"></span><span id="error_ds_name_unparseable"></span>**ERROR de \_ nombre de DS no \_ \_ analizable**</span><span class="sxs-lookup"><span data-stu-id="3ad11-450"><span id="ERROR_DS_NAME_UNPARSEABLE"></span><span id="error_ds_name_unparseable"></span>**ERROR\_DS\_NAME\_UNPARSEABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-451">8350 (0x209E)</span><span class="sxs-lookup"><span data-stu-id="3ad11-451">8350 (0x209E)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-452">El servicio de directorio encontró un error al analizar un nombre.</span><span class="sxs-lookup"><span data-stu-id="3ad11-452">The directory service encountered an error parsing a name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-453"><span id="ERROR_DS_NAME_TYPE_UNKNOWN"></span><span id="error_ds_name_type_unknown"></span>**ERROR \_ de \_ tipo de nombre de DS \_ \_ desconocido**</span><span class="sxs-lookup"><span data-stu-id="3ad11-453"><span id="ERROR_DS_NAME_TYPE_UNKNOWN"></span><span id="error_ds_name_type_unknown"></span>**ERROR\_DS\_NAME\_TYPE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-454">8351 (0x209F)</span><span class="sxs-lookup"><span data-stu-id="3ad11-454">8351 (0x209F)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-455">El servicio de directorio no puede obtener el tipo de atributo de un nombre.</span><span class="sxs-lookup"><span data-stu-id="3ad11-455">The directory service cannot get the attribute type for a name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-456"><span id="ERROR_DS_NOT_AN_OBJECT"></span><span id="error_ds_not_an_object"></span>**ERROR \_ DS \_ no es \_ un \_ objeto**</span><span class="sxs-lookup"><span data-stu-id="3ad11-456"><span id="ERROR_DS_NOT_AN_OBJECT"></span><span id="error_ds_not_an_object"></span>**ERROR\_DS\_NOT\_AN\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-457">8352 (0x20A0)</span><span class="sxs-lookup"><span data-stu-id="3ad11-457">8352 (0x20A0)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-458">El nombre no identifica un objeto; el nombre identifica una ficticia.</span><span class="sxs-lookup"><span data-stu-id="3ad11-458">The name does not identify an object; the name identifies a phantom.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-459"><span id="ERROR_DS_SEC_DESC_TOO_SHORT"></span><span id="error_ds_sec_desc_too_short"></span>**ERROR \_ DS \_ seg. \_ desc. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-459"><span id="ERROR_DS_SEC_DESC_TOO_SHORT"></span><span id="error_ds_sec_desc_too_short"></span>**ERROR\_DS\_SEC\_DESC\_TOO\_SHORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-460">8353 (0x20A1)</span><span class="sxs-lookup"><span data-stu-id="3ad11-460">8353 (0x20A1)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-461">El descriptor de seguridad es demasiado corto.</span><span class="sxs-lookup"><span data-stu-id="3ad11-461">The security descriptor is too short.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-462"><span id="ERROR_DS_SEC_DESC_INVALID"></span><span id="error_ds_sec_desc_invalid"></span>**ERROR \_ DS \_ s \_ DESC \_ no válido**</span><span class="sxs-lookup"><span data-stu-id="3ad11-462"><span id="ERROR_DS_SEC_DESC_INVALID"></span><span id="error_ds_sec_desc_invalid"></span>**ERROR\_DS\_SEC\_DESC\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-463">8354 (0x20A2)</span><span class="sxs-lookup"><span data-stu-id="3ad11-463">8354 (0x20A2)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-464">El descriptor de seguridad no es válido.</span><span class="sxs-lookup"><span data-stu-id="3ad11-464">The security descriptor is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-465"><span id="ERROR_DS_NO_DELETED_NAME"></span><span id="error_ds_no_deleted_name"></span>**ERROR \_ DS \_ no se \_ eliminó \_ el nombre**</span><span class="sxs-lookup"><span data-stu-id="3ad11-465"><span id="ERROR_DS_NO_DELETED_NAME"></span><span id="error_ds_no_deleted_name"></span>**ERROR\_DS\_NO\_DELETED\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-466">8355 (0x20A3)</span><span class="sxs-lookup"><span data-stu-id="3ad11-466">8355 (0x20A3)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-467">No se pudo crear el nombre para el objeto eliminado.</span><span class="sxs-lookup"><span data-stu-id="3ad11-467">Failed to create name for deleted object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-468"><span id="ERROR_DS_SUBREF_MUST_HAVE_PARENT"></span><span id="error_ds_subref_must_have_parent"></span>**ERROR \_ DS \_ SUBREF \_ debe \_ tener un \_ elemento primario**</span><span class="sxs-lookup"><span data-stu-id="3ad11-468"><span id="ERROR_DS_SUBREF_MUST_HAVE_PARENT"></span><span id="error_ds_subref_must_have_parent"></span>**ERROR\_DS\_SUBREF\_MUST\_HAVE\_PARENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-469">8356 (0x20A4)</span><span class="sxs-lookup"><span data-stu-id="3ad11-469">8356 (0x20A4)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-470">Debe existir el elemento primario de un nuevo subref.</span><span class="sxs-lookup"><span data-stu-id="3ad11-470">The parent of a new subref must exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-471"><span id="ERROR_DS_NCNAME_MUST_BE_NC"></span><span id="error_ds_ncname_must_be_nc"></span>**ERROR \_ DS \_ NCNAME \_ debe \_ ser \_ NC**</span><span class="sxs-lookup"><span data-stu-id="3ad11-471"><span id="ERROR_DS_NCNAME_MUST_BE_NC"></span><span id="error_ds_ncname_must_be_nc"></span>**ERROR\_DS\_NCNAME\_MUST\_BE\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-472">8357 (0x20A5)</span><span class="sxs-lookup"><span data-stu-id="3ad11-472">8357 (0x20A5)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-473">El objeto debe ser un contexto de nomenclatura.</span><span class="sxs-lookup"><span data-stu-id="3ad11-473">The object must be a naming context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-474"><span id="ERROR_DS_CANT_ADD_SYSTEM_ONLY"></span><span id="error_ds_cant_add_system_only"></span>**ERROR DS no se pudo \_ \_ \_ agregar \_ solo el sistema \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-474"><span id="ERROR_DS_CANT_ADD_SYSTEM_ONLY"></span><span id="error_ds_cant_add_system_only"></span>**ERROR\_DS\_CANT\_ADD\_SYSTEM\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-475">8358 (0x20A6)</span><span class="sxs-lookup"><span data-stu-id="3ad11-475">8358 (0x20A6)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-476">No se permite agregar un atributo que sea propiedad del sistema.</span><span class="sxs-lookup"><span data-stu-id="3ad11-476">It is not permitted to add an attribute which is owned by the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-477"><span id="ERROR_DS_CLASS_MUST_BE_CONCRETE"></span><span id="error_ds_class_must_be_concrete"></span>**la \_ clase DS de error \_ \_ debe \_ ser \_ concreta**</span><span class="sxs-lookup"><span data-stu-id="3ad11-477"><span id="ERROR_DS_CLASS_MUST_BE_CONCRETE"></span><span id="error_ds_class_must_be_concrete"></span>**ERROR\_DS\_CLASS\_MUST\_BE\_CONCRETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-478">8359 (0x20A7)</span><span class="sxs-lookup"><span data-stu-id="3ad11-478">8359 (0x20A7)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-479">La clase del objeto debe ser estructural; no se puede crear una instancia de una clase abstracta.</span><span class="sxs-lookup"><span data-stu-id="3ad11-479">The class of the object must be structural; you cannot instantiate an abstract class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-480"><span id="ERROR_DS_INVALID_DMD"></span><span id="error_ds_invalid_dmd"></span>**ERROR \_ DS \_ no válido en el \_ DMD**</span><span class="sxs-lookup"><span data-stu-id="3ad11-480"><span id="ERROR_DS_INVALID_DMD"></span><span id="error_ds_invalid_dmd"></span>**ERROR\_DS\_INVALID\_DMD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-481">8360 (0x20A8)</span><span class="sxs-lookup"><span data-stu-id="3ad11-481">8360 (0x20A8)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-482">No se encontró el objeto de esquema.</span><span class="sxs-lookup"><span data-stu-id="3ad11-482">The schema object could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-483"><span id="ERROR_DS_OBJ_GUID_EXISTS"></span><span id="error_ds_obj_guid_exists"></span>**\_existe el \_ \_ GUID obj de DS \_ de error**</span><span class="sxs-lookup"><span data-stu-id="3ad11-483"><span id="ERROR_DS_OBJ_GUID_EXISTS"></span><span id="error_ds_obj_guid_exists"></span>**ERROR\_DS\_OBJ\_GUID\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-484">8361 (0x20A9)</span><span class="sxs-lookup"><span data-stu-id="3ad11-484">8361 (0x20A9)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-485">Ya existe un objeto local con este GUID (inactivo o activo).</span><span class="sxs-lookup"><span data-stu-id="3ad11-485">A local object with this GUID (dead or alive) already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-486"><span id="ERROR_DS_NOT_ON_BACKLINK"></span><span id="error_ds_not_on_backlink"></span>**ERROR \_ DS \_ no está \_ en \_ BACKLINK**</span><span class="sxs-lookup"><span data-stu-id="3ad11-486"><span id="ERROR_DS_NOT_ON_BACKLINK"></span><span id="error_ds_not_on_backlink"></span>**ERROR\_DS\_NOT\_ON\_BACKLINK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-487">8362 (0x20AA)</span><span class="sxs-lookup"><span data-stu-id="3ad11-487">8362 (0x20AA)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-488">La operación no se puede realizar en un vínculo de retroceso.</span><span class="sxs-lookup"><span data-stu-id="3ad11-488">The operation cannot be performed on a back link.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-489"><span id="ERROR_DS_NO_CROSSREF_FOR_NC"></span><span id="error_ds_no_crossref_for_nc"></span>**ERROR \_ DS \_ no hay ningún \_ CROSSREF \_ para \_ NC**</span><span class="sxs-lookup"><span data-stu-id="3ad11-489"><span id="ERROR_DS_NO_CROSSREF_FOR_NC"></span><span id="error_ds_no_crossref_for_nc"></span>**ERROR\_DS\_NO\_CROSSREF\_FOR\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-490">8363 (0x20AB)</span><span class="sxs-lookup"><span data-stu-id="3ad11-490">8363 (0x20AB)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-491">No se encontró la referencia cruzada para el contexto de nomenclatura especificado.</span><span class="sxs-lookup"><span data-stu-id="3ad11-491">The cross reference for the specified naming context could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-492"><span id="ERROR_DS_SHUTTING_DOWN"></span><span id="error_ds_shutting_down"></span>**ERROR \_ de \_ cierre de \_ DS**</span><span class="sxs-lookup"><span data-stu-id="3ad11-492"><span id="ERROR_DS_SHUTTING_DOWN"></span><span id="error_ds_shutting_down"></span>**ERROR\_DS\_SHUTTING\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-493">8364 (0x20AC)</span><span class="sxs-lookup"><span data-stu-id="3ad11-493">8364 (0x20AC)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-494">No se pudo realizar la operación porque el servicio de directorio se está cerrando.</span><span class="sxs-lookup"><span data-stu-id="3ad11-494">The operation could not be performed because the directory service is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-495"><span id="ERROR_DS_UNKNOWN_OPERATION"></span><span id="error_ds_unknown_operation"></span>**ERROR de \_ DS: \_ \_ operación desconocida**</span><span class="sxs-lookup"><span data-stu-id="3ad11-495"><span id="ERROR_DS_UNKNOWN_OPERATION"></span><span id="error_ds_unknown_operation"></span>**ERROR\_DS\_UNKNOWN\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-496">8365 (0x20AD)</span><span class="sxs-lookup"><span data-stu-id="3ad11-496">8365 (0x20AD)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-497">La solicitud de servicio de directorio no es válida.</span><span class="sxs-lookup"><span data-stu-id="3ad11-497">The directory service request is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-498"><span id="ERROR_DS_INVALID_ROLE_OWNER"></span><span id="error_ds_invalid_role_owner"></span>**ERROR \_ del \_ \_ propietario del rol DS no válido \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-498"><span id="ERROR_DS_INVALID_ROLE_OWNER"></span><span id="error_ds_invalid_role_owner"></span>**ERROR\_DS\_INVALID\_ROLE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-499">8366 (0x20AE)</span><span class="sxs-lookup"><span data-stu-id="3ad11-499">8366 (0x20AE)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-500">No se pudo leer el atributo del propietario del rol.</span><span class="sxs-lookup"><span data-stu-id="3ad11-500">The role owner attribute could not be read.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-501"><span id="ERROR_DS_COULDNT_CONTACT_FSMO"></span><span id="error_ds_couldnt_contact_fsmo"></span>**ERROR de \_ COULDNT de DS de \_ \_ contacto \_ FSMO**</span><span class="sxs-lookup"><span data-stu-id="3ad11-501"><span id="ERROR_DS_COULDNT_CONTACT_FSMO"></span><span id="error_ds_couldnt_contact_fsmo"></span>**ERROR\_DS\_COULDNT\_CONTACT\_FSMO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-502">8367 (0x20AF)</span><span class="sxs-lookup"><span data-stu-id="3ad11-502">8367 (0x20AF)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-503">Error en la operación FSMO solicitada.</span><span class="sxs-lookup"><span data-stu-id="3ad11-503">The requested FSMO operation failed.</span></span> <span data-ttu-id="3ad11-504">No se puede poner en contacto con el titular de FSMO actual.</span><span class="sxs-lookup"><span data-stu-id="3ad11-504">The current FSMO holder could not be contacted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-505"><span id="ERROR_DS_CROSS_NC_DN_RENAME"></span><span id="error_ds_cross_nc_dn_rename"></span>**ERROR de \_ DS \_ Cross \_ NC \_ DN \_ Rename**</span><span class="sxs-lookup"><span data-stu-id="3ad11-505"><span id="ERROR_DS_CROSS_NC_DN_RENAME"></span><span id="error_ds_cross_nc_dn_rename"></span>**ERROR\_DS\_CROSS\_NC\_DN\_RENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-506">8368 (0x20B0)</span><span class="sxs-lookup"><span data-stu-id="3ad11-506">8368 (0x20B0)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-507">No se permite la modificación de un DN en un contexto de nomenclatura.</span><span class="sxs-lookup"><span data-stu-id="3ad11-507">Modification of a DN across a naming context is not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-508"><span id="ERROR_DS_CANT_MOD_SYSTEM_ONLY"></span><span id="error_ds_cant_mod_system_only"></span>**ERROR DS no se pudo \_ \_ \_ MODIF \_ \_ .**</span><span class="sxs-lookup"><span data-stu-id="3ad11-508"><span id="ERROR_DS_CANT_MOD_SYSTEM_ONLY"></span><span id="error_ds_cant_mod_system_only"></span>**ERROR\_DS\_CANT\_MOD\_SYSTEM\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-509">8369 (0x20B1)</span><span class="sxs-lookup"><span data-stu-id="3ad11-509">8369 (0x20B1)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-510">El atributo no se puede modificar porque es propiedad del sistema.</span><span class="sxs-lookup"><span data-stu-id="3ad11-510">The attribute cannot be modified because it is owned by the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-511"><span id="ERROR_DS_REPLICATOR_ONLY"></span><span id="error_ds_replicator_only"></span>**ERROR \_ solo en el duplicador de DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-511"><span id="ERROR_DS_REPLICATOR_ONLY"></span><span id="error_ds_replicator_only"></span>**ERROR\_DS\_REPLICATOR\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-512">8370 (0x20B2)</span><span class="sxs-lookup"><span data-stu-id="3ad11-512">8370 (0x20B2)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-513">Solo el replicador puede realizar esta función.</span><span class="sxs-lookup"><span data-stu-id="3ad11-513">Only the replicator can perform this function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-514"><span id="ERROR_DS_OBJ_CLASS_NOT_DEFINED"></span><span id="error_ds_obj_class_not_defined"></span>**ERROR de la \_ \_ clase obj DS \_ \_ no \_ definida**</span><span class="sxs-lookup"><span data-stu-id="3ad11-514"><span id="ERROR_DS_OBJ_CLASS_NOT_DEFINED"></span><span id="error_ds_obj_class_not_defined"></span>**ERROR\_DS\_OBJ\_CLASS\_NOT\_DEFINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-515">8371 (0x20B3)</span><span class="sxs-lookup"><span data-stu-id="3ad11-515">8371 (0x20B3)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-516">La clase especificada no está definida.</span><span class="sxs-lookup"><span data-stu-id="3ad11-516">The specified class is not defined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-517"><span id="ERROR_DS_OBJ_CLASS_NOT_SUBCLASS"></span><span id="error_ds_obj_class_not_subclass"></span>**ERROR \_ DS \_ \_ clase obj \_ no \_ subclase**</span><span class="sxs-lookup"><span data-stu-id="3ad11-517"><span id="ERROR_DS_OBJ_CLASS_NOT_SUBCLASS"></span><span id="error_ds_obj_class_not_subclass"></span>**ERROR\_DS\_OBJ\_CLASS\_NOT\_SUBCLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-518">8372 (0x20B4)</span><span class="sxs-lookup"><span data-stu-id="3ad11-518">8372 (0x20B4)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-519">La clase especificada no es una subclase.</span><span class="sxs-lookup"><span data-stu-id="3ad11-519">The specified class is not a subclass.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-520"><span id="ERROR_DS_NAME_REFERENCE_INVALID"></span><span id="error_ds_name_reference_invalid"></span>**ERROR de \_ referencia de nombre de DS \_ \_ \_ no válida**</span><span class="sxs-lookup"><span data-stu-id="3ad11-520"><span id="ERROR_DS_NAME_REFERENCE_INVALID"></span><span id="error_ds_name_reference_invalid"></span>**ERROR\_DS\_NAME\_REFERENCE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-521">8373 (0x20B5)</span><span class="sxs-lookup"><span data-stu-id="3ad11-521">8373 (0x20B5)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-522">La referencia de nombre no es válida.</span><span class="sxs-lookup"><span data-stu-id="3ad11-522">The name reference is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-523"><span id="ERROR_DS_CROSS_REF_EXISTS"></span><span id="error_ds_cross_ref_exists"></span>**\_existe una \_ \_ referencia cruzada de DS \_ de error**</span><span class="sxs-lookup"><span data-stu-id="3ad11-523"><span id="ERROR_DS_CROSS_REF_EXISTS"></span><span id="error_ds_cross_ref_exists"></span>**ERROR\_DS\_CROSS\_REF\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-524">8374 (0x20B6)</span><span class="sxs-lookup"><span data-stu-id="3ad11-524">8374 (0x20B6)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-525">Ya existe una referencia cruzada.</span><span class="sxs-lookup"><span data-stu-id="3ad11-525">A cross reference already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-526"><span id="ERROR_DS_CANT_DEL_MASTER_CROSSREF"></span><span id="error_ds_cant_del_master_crossref"></span>**ERROR DS no se pudo \_ \_ \_ del \_ maestro \_ CROSSREF**</span><span class="sxs-lookup"><span data-stu-id="3ad11-526"><span id="ERROR_DS_CANT_DEL_MASTER_CROSSREF"></span><span id="error_ds_cant_del_master_crossref"></span>**ERROR\_DS\_CANT\_DEL\_MASTER\_CROSSREF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-527">8375 (0x20B7)</span><span class="sxs-lookup"><span data-stu-id="3ad11-527">8375 (0x20B7)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-528">No se permite eliminar una referencia cruzada maestra.</span><span class="sxs-lookup"><span data-stu-id="3ad11-528">It is not permitted to delete a master cross reference.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-529"><span id="ERROR_DS_SUBTREE_NOTIFY_NOT_NC_HEAD"></span><span id="error_ds_subtree_notify_not_nc_head"></span>**ERROR \_ el \_ subárbol de DS no se pudo \_ notificar al \_ \_ \_ encabezado NC**</span><span class="sxs-lookup"><span data-stu-id="3ad11-529"><span id="ERROR_DS_SUBTREE_NOTIFY_NOT_NC_HEAD"></span><span id="error_ds_subtree_notify_not_nc_head"></span>**ERROR\_DS\_SUBTREE\_NOTIFY\_NOT\_NC\_HEAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-530">8376 (0x20B8)</span><span class="sxs-lookup"><span data-stu-id="3ad11-530">8376 (0x20B8)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-531">Las notificaciones de subárbol solo se admiten en encabezados de NC.</span><span class="sxs-lookup"><span data-stu-id="3ad11-531">Subtree notifications are only supported on NC heads.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-532"><span id="ERROR_DS_NOTIFY_FILTER_TOO_COMPLEX"></span><span id="error_ds_notify_filter_too_complex"></span>**ERROR de \_ filtro de notificación de DS \_ \_ \_ demasiado \_ complejo**</span><span class="sxs-lookup"><span data-stu-id="3ad11-532"><span id="ERROR_DS_NOTIFY_FILTER_TOO_COMPLEX"></span><span id="error_ds_notify_filter_too_complex"></span>**ERROR\_DS\_NOTIFY\_FILTER\_TOO\_COMPLEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-533">8377 (0x20B9)</span><span class="sxs-lookup"><span data-stu-id="3ad11-533">8377 (0x20B9)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-534">El filtro de notificación es demasiado complejo.</span><span class="sxs-lookup"><span data-stu-id="3ad11-534">Notification filter is too complex.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-535"><span id="ERROR_DS_DUP_RDN"></span><span id="error_ds_dup_rdn"></span>**ERROR \_ de \_ RDN DUP de DS \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-535"><span id="ERROR_DS_DUP_RDN"></span><span id="error_ds_dup_rdn"></span>**ERROR\_DS\_DUP\_RDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-536">8378 (0x20BA)</span><span class="sxs-lookup"><span data-stu-id="3ad11-536">8378 (0x20BA)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-537">No se pudo actualizar el esquema: RDN duplicado.</span><span class="sxs-lookup"><span data-stu-id="3ad11-537">Schema update failed: duplicate RDN.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-538"><span id="ERROR_DS_DUP_OID"></span><span id="error_ds_dup_oid"></span>**\_OID de \_ reduplicación DS de error \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-538"><span id="ERROR_DS_DUP_OID"></span><span id="error_ds_dup_oid"></span>**ERROR\_DS\_DUP\_OID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-539">8379 (0x20BB)</span><span class="sxs-lookup"><span data-stu-id="3ad11-539">8379 (0x20BB)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-540">No se pudo actualizar el esquema: OID duplicado.</span><span class="sxs-lookup"><span data-stu-id="3ad11-540">Schema update failed: duplicate OID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-541"><span id="ERROR_DS_DUP_MAPI_ID"></span><span id="error_ds_dup_mapi_id"></span>**\_ \_ \_ ID. de MAPI \_ DUP de error de DS**</span><span class="sxs-lookup"><span data-stu-id="3ad11-541"><span id="ERROR_DS_DUP_MAPI_ID"></span><span id="error_ds_dup_mapi_id"></span>**ERROR\_DS\_DUP\_MAPI\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-542">8380 (0x20BC)</span><span class="sxs-lookup"><span data-stu-id="3ad11-542">8380 (0x20BC)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-543">Error al actualizar el esquema: identificador de MAPI duplicado.</span><span class="sxs-lookup"><span data-stu-id="3ad11-543">Schema update failed: duplicate MAPI identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-544"><span id="ERROR_DS_DUP_SCHEMA_ID_GUID"></span><span id="error_ds_dup_schema_id_guid"></span>**\_GUID de \_ \_ \_ ID. de esquema duplicado \_ de error de DS**</span><span class="sxs-lookup"><span data-stu-id="3ad11-544"><span id="ERROR_DS_DUP_SCHEMA_ID_GUID"></span><span id="error_ds_dup_schema_id_guid"></span>**ERROR\_DS\_DUP\_SCHEMA\_ID\_GUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-545">8381 (0x20BD)</span><span class="sxs-lookup"><span data-stu-id="3ad11-545">8381 (0x20BD)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-546">Error al actualizar el esquema: GUID de ID. de esquema duplicado.</span><span class="sxs-lookup"><span data-stu-id="3ad11-546">Schema update failed: duplicate schema-id GUID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-547"><span id="ERROR_DS_DUP_LDAP_DISPLAY_NAME"></span><span id="error_ds_dup_ldap_display_name"></span>**ERROR \_ en \_ \_ \_ el nombre para mostrar de LDAP DUP en DS \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-547"><span id="ERROR_DS_DUP_LDAP_DISPLAY_NAME"></span><span id="error_ds_dup_ldap_display_name"></span>**ERROR\_DS\_DUP\_LDAP\_DISPLAY\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-548">8382 (0x20BE)</span><span class="sxs-lookup"><span data-stu-id="3ad11-548">8382 (0x20BE)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-549">Error al actualizar el esquema: nombre para mostrar LDAP duplicado.</span><span class="sxs-lookup"><span data-stu-id="3ad11-549">Schema update failed: duplicate LDAP display name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-550"><span id="ERROR_DS_SEMANTIC_ATT_TEST"></span><span id="error_ds_semantic_att_test"></span>**ERROR de \_ DS semántico de la \_ \_ prueba de ATT \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-550"><span id="ERROR_DS_SEMANTIC_ATT_TEST"></span><span id="error_ds_semantic_att_test"></span>**ERROR\_DS\_SEMANTIC\_ATT\_TEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-551">8383 (0x20BF)</span><span class="sxs-lookup"><span data-stu-id="3ad11-551">8383 (0x20BF)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-552">No se pudo actualizar el esquema: intervalo menor que el intervalo superior.</span><span class="sxs-lookup"><span data-stu-id="3ad11-552">Schema update failed: range-lower less than range upper.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-553"><span id="ERROR_DS_SYNTAX_MISMATCH"></span><span id="error_ds_syntax_mismatch"></span>**ERROR \_ de \_ coincidencia de sintaxis de DS \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-553"><span id="ERROR_DS_SYNTAX_MISMATCH"></span><span id="error_ds_syntax_mismatch"></span>**ERROR\_DS\_SYNTAX\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-554">8384 (0x20C0)</span><span class="sxs-lookup"><span data-stu-id="3ad11-554">8384 (0x20C0)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-555">Error al actualizar el esquema: no coincide la sintaxis.</span><span class="sxs-lookup"><span data-stu-id="3ad11-555">Schema update failed: syntax mismatch.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-556"><span id="ERROR_DS_EXISTS_IN_MUST_HAVE"></span><span id="error_ds_exists_in_must_have"></span>**el ERROR \_ DS \_ existe \_ en \_ debe \_ tener**</span><span class="sxs-lookup"><span data-stu-id="3ad11-556"><span id="ERROR_DS_EXISTS_IN_MUST_HAVE"></span><span id="error_ds_exists_in_must_have"></span>**ERROR\_DS\_EXISTS\_IN\_MUST\_HAVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-557">8385 (0x20C1)</span><span class="sxs-lookup"><span data-stu-id="3ad11-557">8385 (0x20C1)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-558">No se pudo eliminar el esquema: el atributo se utiliza en debe contener.</span><span class="sxs-lookup"><span data-stu-id="3ad11-558">Schema deletion failed: attribute is used in must-contain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-559"><span id="ERROR_DS_EXISTS_IN_MAY_HAVE"></span><span id="error_ds_exists_in_may_have"></span>**el ERROR \_ DS \_ existe \_ en \_ puede \_ tener**</span><span class="sxs-lookup"><span data-stu-id="3ad11-559"><span id="ERROR_DS_EXISTS_IN_MAY_HAVE"></span><span id="error_ds_exists_in_may_have"></span>**ERROR\_DS\_EXISTS\_IN\_MAY\_HAVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-560">8386 (0x20C2)</span><span class="sxs-lookup"><span data-stu-id="3ad11-560">8386 (0x20C2)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-561">No se pudo eliminar el esquema: el atributo se usa en puede contener.</span><span class="sxs-lookup"><span data-stu-id="3ad11-561">Schema deletion failed: attribute is used in may-contain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-562"><span id="ERROR_DS_NONEXISTENT_MAY_HAVE"></span><span id="error_ds_nonexistent_may_have"></span>**el ERROR \_ DS \_ inexistente \_ puede \_ tener**</span><span class="sxs-lookup"><span data-stu-id="3ad11-562"><span id="ERROR_DS_NONEXISTENT_MAY_HAVE"></span><span id="error_ds_nonexistent_may_have"></span>**ERROR\_DS\_NONEXISTENT\_MAY\_HAVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-563">8387 (0x20C3)</span><span class="sxs-lookup"><span data-stu-id="3ad11-563">8387 (0x20C3)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-564">Error al actualizar el esquema: el atributo de puede contener no existe.</span><span class="sxs-lookup"><span data-stu-id="3ad11-564">Schema update failed: attribute in may-contain does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-565"><span id="ERROR_DS_NONEXISTENT_MUST_HAVE"></span><span id="error_ds_nonexistent_must_have"></span>**el ERROR \_ DS no \_ existente \_ debe \_ tener**</span><span class="sxs-lookup"><span data-stu-id="3ad11-565"><span id="ERROR_DS_NONEXISTENT_MUST_HAVE"></span><span id="error_ds_nonexistent_must_have"></span>**ERROR\_DS\_NONEXISTENT\_MUST\_HAVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-566">8388 (0x20C4)</span><span class="sxs-lookup"><span data-stu-id="3ad11-566">8388 (0x20C4)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-567">Error al actualizar el esquema: el atributo de debe contener no existe.</span><span class="sxs-lookup"><span data-stu-id="3ad11-567">Schema update failed: attribute in must-contain does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-568"><span id="ERROR_DS_AUX_CLS_TEST_FAIL"></span><span id="error_ds_aux_cls_test_fail"></span>**ERROR \_ de \_ \_ prueba de CLS de AUX \_ de DS \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-568"><span id="ERROR_DS_AUX_CLS_TEST_FAIL"></span><span id="error_ds_aux_cls_test_fail"></span>**ERROR\_DS\_AUX\_CLS\_TEST\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-569">8389 (0x20C5)</span><span class="sxs-lookup"><span data-stu-id="3ad11-569">8389 (0x20C5)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-570">Error al actualizar el esquema: la clase de la lista de clases auxiliares no existe o no es una clase auxiliar.</span><span class="sxs-lookup"><span data-stu-id="3ad11-570">Schema update failed: class in aux-class list does not exist or is not an auxiliary class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-571"><span id="ERROR_DS_NONEXISTENT_POSS_SUP"></span><span id="error_ds_nonexistent_poss_sup"></span>**ERROR \_ de \_ \_ Poss SUP inexistente de DS \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-571"><span id="ERROR_DS_NONEXISTENT_POSS_SUP"></span><span id="error_ds_nonexistent_poss_sup"></span>**ERROR\_DS\_NONEXISTENT\_POSS\_SUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-572">8390 (0x20C6)</span><span class="sxs-lookup"><span data-stu-id="3ad11-572">8390 (0x20C6)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-573">No se pudo actualizar el esquema: la clase en Poss no existe.</span><span class="sxs-lookup"><span data-stu-id="3ad11-573">Schema update failed: class in poss-superiors does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-574"><span id="ERROR_DS_SUB_CLS_TEST_FAIL"></span><span id="error_ds_sub_cls_test_fail"></span>**ERROR en la \_ \_ prueba de sub \_ CLS de \_ DS \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-574"><span id="ERROR_DS_SUB_CLS_TEST_FAIL"></span><span id="error_ds_sub_cls_test_fail"></span>**ERROR\_DS\_SUB\_CLS\_TEST\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-575">8391 (0x20C7)</span><span class="sxs-lookup"><span data-stu-id="3ad11-575">8391 (0x20C7)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-576">Error al actualizar el esquema: la clase en la lista de subclases no existe o no cumple las reglas de jerarquía.</span><span class="sxs-lookup"><span data-stu-id="3ad11-576">Schema update failed: class in subclassof list does not exist or does not satisfy hierarchy rules.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-577"><span id="ERROR_DS_BAD_RDN_ATT_ID_SYNTAX"></span><span id="error_ds_bad_rdn_att_id_syntax"></span>**ERROR en la \_ \_ \_ Sintaxis de \_ \_ ID. de RDN RDN erróneo de DS \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-577"><span id="ERROR_DS_BAD_RDN_ATT_ID_SYNTAX"></span><span id="error_ds_bad_rdn_att_id_syntax"></span>**ERROR\_DS\_BAD\_RDN\_ATT\_ID\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-578">8392 (0x20C8)</span><span class="sxs-lookup"><span data-stu-id="3ad11-578">8392 (0x20C8)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-579">No se pudo actualizar el esquema: el ID. de RDN-ATT-ID tiene una sintaxis incorrecta.</span><span class="sxs-lookup"><span data-stu-id="3ad11-579">Schema update failed: Rdn-Att-Id has wrong syntax.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-580"><span id="ERROR_DS_EXISTS_IN_AUX_CLS"></span><span id="error_ds_exists_in_aux_cls"></span>**el ERROR \_ DS \_ existe \_ en \_ AUX \_ CLS**</span><span class="sxs-lookup"><span data-stu-id="3ad11-580"><span id="ERROR_DS_EXISTS_IN_AUX_CLS"></span><span id="error_ds_exists_in_aux_cls"></span>**ERROR\_DS\_EXISTS\_IN\_AUX\_CLS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-581">8393 (0x20C9)</span><span class="sxs-lookup"><span data-stu-id="3ad11-581">8393 (0x20C9)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-582">No se pudo eliminar el esquema: la clase se usa como clase auxiliar.</span><span class="sxs-lookup"><span data-stu-id="3ad11-582">Schema deletion failed: class is used as auxiliary class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-583"><span id="ERROR_DS_EXISTS_IN_SUB_CLS"></span><span id="error_ds_exists_in_sub_cls"></span>**el \_ error \_ DS \_ existe \_ en \_ subcls**</span><span class="sxs-lookup"><span data-stu-id="3ad11-583"><span id="ERROR_DS_EXISTS_IN_SUB_CLS"></span><span id="error_ds_exists_in_sub_cls"></span>**ERROR\_DS\_EXISTS\_IN\_SUB\_CLS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-584">8394 (0x20CA)</span><span class="sxs-lookup"><span data-stu-id="3ad11-584">8394 (0x20CA)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-585">No se pudo eliminar el esquema: la clase se usa como subclase.</span><span class="sxs-lookup"><span data-stu-id="3ad11-585">Schema deletion failed: class is used as sub class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-586"><span id="ERROR_DS_EXISTS_IN_POSS_SUP"></span><span id="error_ds_exists_in_poss_sup"></span>**el ERROR \_ DS \_ existe en el \_ SUP de \_ Poss \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-586"><span id="ERROR_DS_EXISTS_IN_POSS_SUP"></span><span id="error_ds_exists_in_poss_sup"></span>**ERROR\_DS\_EXISTS\_IN\_POSS\_SUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-587">8395 (0x20CB)</span><span class="sxs-lookup"><span data-stu-id="3ad11-587">8395 (0x20CB)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-588">No se pudo eliminar el esquema: se usa la clase como Poss superior.</span><span class="sxs-lookup"><span data-stu-id="3ad11-588">Schema deletion failed: class is used as poss superior.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-589"><span id="ERROR_DS_RECALCSCHEMA_FAILED"></span><span id="error_ds_recalcschema_failed"></span>**ERROR \_ de \_ RECALCSCHEMA de DS \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-589"><span id="ERROR_DS_RECALCSCHEMA_FAILED"></span><span id="error_ds_recalcschema_failed"></span>**ERROR\_DS\_RECALCSCHEMA\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-590">8396 (0x20CC)</span><span class="sxs-lookup"><span data-stu-id="3ad11-590">8396 (0x20CC)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-591">No se pudo actualizar el esquema al recalcular la caché de validación.</span><span class="sxs-lookup"><span data-stu-id="3ad11-591">Schema update failed in recalculating validation cache.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-592"><span id="ERROR_DS_TREE_DELETE_NOT_FINISHED"></span><span id="error_ds_tree_delete_not_finished"></span>**ERROR \_ al \_ eliminar el árbol de DS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-592"><span id="ERROR_DS_TREE_DELETE_NOT_FINISHED"></span><span id="error_ds_tree_delete_not_finished"></span>**ERROR\_DS\_TREE\_DELETE\_NOT\_FINISHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-593">8397 (0x20CD)</span><span class="sxs-lookup"><span data-stu-id="3ad11-593">8397 (0x20CD)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-594">No se ha terminado de eliminar el árbol.</span><span class="sxs-lookup"><span data-stu-id="3ad11-594">The tree deletion is not finished.</span></span> <span data-ttu-id="3ad11-595">La solicitud se debe volver a realizar para continuar con la eliminación del árbol.</span><span class="sxs-lookup"><span data-stu-id="3ad11-595">The request must be made again to continue deleting the tree.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-596"><span id="ERROR_DS_CANT_DELETE"></span><span id="error_ds_cant_delete"></span>**ERROR DS no se pudo \_ \_ \_ eliminar**</span><span class="sxs-lookup"><span data-stu-id="3ad11-596"><span id="ERROR_DS_CANT_DELETE"></span><span id="error_ds_cant_delete"></span>**ERROR\_DS\_CANT\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-597">8398 (0x20CE)</span><span class="sxs-lookup"><span data-stu-id="3ad11-597">8398 (0x20CE)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-598">No se pudo realizar la operación de eliminación solicitada.</span><span class="sxs-lookup"><span data-stu-id="3ad11-598">The requested delete operation could not be performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-599"><span id="ERROR_DS_ATT_SCHEMA_REQ_ID"></span><span id="error_ds_att_schema_req_id"></span>**\_ \_ \_ \_ ID. de solicitud de esquema DS ATT de error \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-599"><span id="ERROR_DS_ATT_SCHEMA_REQ_ID"></span><span id="error_ds_att_schema_req_id"></span>**ERROR\_DS\_ATT\_SCHEMA\_REQ\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-600">8399 (0x20CF)</span><span class="sxs-lookup"><span data-stu-id="3ad11-600">8399 (0x20CF)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-601">No se puede leer el identificador de clase de control para el registro de esquema.</span><span class="sxs-lookup"><span data-stu-id="3ad11-601">Cannot read the governs class identifier for the schema record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-602"><span id="ERROR_DS_BAD_ATT_SCHEMA_SYNTAX"></span><span id="error_ds_bad_att_schema_syntax"></span>**ERROR \_ de \_ \_ Sintaxis de \_ esquema de ATT \_ de DS incorrecta**</span><span class="sxs-lookup"><span data-stu-id="3ad11-602"><span id="ERROR_DS_BAD_ATT_SCHEMA_SYNTAX"></span><span id="error_ds_bad_att_schema_syntax"></span>**ERROR\_DS\_BAD\_ATT\_SCHEMA\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-603">8400 (0x20D0)</span><span class="sxs-lookup"><span data-stu-id="3ad11-603">8400 (0x20D0)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-604">El esquema de atributo tiene una sintaxis incorrecta.</span><span class="sxs-lookup"><span data-stu-id="3ad11-604">The attribute schema has bad syntax.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-605"><span id="ERROR_DS_CANT_CACHE_ATT"></span><span id="error_ds_cant_cache_att"></span>**ERROR de caché de ERROR de \_ DS \_ \_ \_ ATT**</span><span class="sxs-lookup"><span data-stu-id="3ad11-605"><span id="ERROR_DS_CANT_CACHE_ATT"></span><span id="error_ds_cant_cache_att"></span>**ERROR\_DS\_CANT\_CACHE\_ATT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-606">8401 (0x20D1)</span><span class="sxs-lookup"><span data-stu-id="3ad11-606">8401 (0x20D1)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-607">No se pudo almacenar en caché el atributo.</span><span class="sxs-lookup"><span data-stu-id="3ad11-607">The attribute could not be cached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-608"><span id="ERROR_DS_CANT_CACHE_CLASS"></span><span id="error_ds_cant_cache_class"></span>**ERROR de la \_ \_ \_ \_ clase caché no se pudo DS**</span><span class="sxs-lookup"><span data-stu-id="3ad11-608"><span id="ERROR_DS_CANT_CACHE_CLASS"></span><span id="error_ds_cant_cache_class"></span>**ERROR\_DS\_CANT\_CACHE\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-609">8402 (0x20D2)</span><span class="sxs-lookup"><span data-stu-id="3ad11-609">8402 (0x20D2)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-610">No se pudo almacenar en caché la clase.</span><span class="sxs-lookup"><span data-stu-id="3ad11-610">The class could not be cached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-611"><span id="ERROR_DS_CANT_REMOVE_ATT_CACHE"></span><span id="error_ds_cant_remove_att_cache"></span>**ERROR DS no se pudo \_ \_ quitar la \_ \_ caché de ATT \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-611"><span id="ERROR_DS_CANT_REMOVE_ATT_CACHE"></span><span id="error_ds_cant_remove_att_cache"></span>**ERROR\_DS\_CANT\_REMOVE\_ATT\_CACHE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-612">8403 (0x20D3)</span><span class="sxs-lookup"><span data-stu-id="3ad11-612">8403 (0x20D3)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-613">No se pudo quitar el atributo de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="3ad11-613">The attribute could not be removed from the cache.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-614"><span id="ERROR_DS_CANT_REMOVE_CLASS_CACHE"></span><span id="error_ds_cant_remove_class_cache"></span>**ERROR DS no se pudo \_ \_ quitar la \_ \_ caché de clases \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-614"><span id="ERROR_DS_CANT_REMOVE_CLASS_CACHE"></span><span id="error_ds_cant_remove_class_cache"></span>**ERROR\_DS\_CANT\_REMOVE\_CLASS\_CACHE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-615">8404 (0x20D4)</span><span class="sxs-lookup"><span data-stu-id="3ad11-615">8404 (0x20D4)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-616">No se pudo quitar la clase de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="3ad11-616">The class could not be removed from the cache.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-617"><span id="ERROR_DS_CANT_RETRIEVE_DN"></span><span id="error_ds_cant_retrieve_dn"></span>**ERROR DS no se pudo \_ \_ \_ recuperar \_ DN**</span><span class="sxs-lookup"><span data-stu-id="3ad11-617"><span id="ERROR_DS_CANT_RETRIEVE_DN"></span><span id="error_ds_cant_retrieve_dn"></span>**ERROR\_DS\_CANT\_RETRIEVE\_DN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-618">8405 (0x20D5)</span><span class="sxs-lookup"><span data-stu-id="3ad11-618">8405 (0x20D5)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-619">No se pudo leer el atributo de nombre distintivo.</span><span class="sxs-lookup"><span data-stu-id="3ad11-619">The distinguished name attribute could not be read.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-620"><span id="ERROR_DS_MISSING_SUPREF"></span><span id="error_ds_missing_supref"></span>**ERROR de \_ DS \_ que falta \_ SUPREF**</span><span class="sxs-lookup"><span data-stu-id="3ad11-620"><span id="ERROR_DS_MISSING_SUPREF"></span><span id="error_ds_missing_supref"></span>**ERROR\_DS\_MISSING\_SUPREF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-621">8406 (0x20D6)</span><span class="sxs-lookup"><span data-stu-id="3ad11-621">8406 (0x20D6)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-622">No se configuró ninguna referencia superior para el servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="3ad11-622">No superior reference has been configured for the directory service.</span></span> <span data-ttu-id="3ad11-623">Por tanto, el servicio de directorio no puede emitir referencias a los objetos fuera de este bosque.</span><span class="sxs-lookup"><span data-stu-id="3ad11-623">The directory service is therefore unable to issue referrals to objects outside this forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-624"><span id="ERROR_DS_CANT_RETRIEVE_INSTANCE"></span><span id="error_ds_cant_retrieve_instance"></span>**ERROR DS no se pudo \_ \_ recuperar la \_ \_ instancia**</span><span class="sxs-lookup"><span data-stu-id="3ad11-624"><span id="ERROR_DS_CANT_RETRIEVE_INSTANCE"></span><span id="error_ds_cant_retrieve_instance"></span>**ERROR\_DS\_CANT\_RETRIEVE\_INSTANCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-625">8407 (0x20D7)</span><span class="sxs-lookup"><span data-stu-id="3ad11-625">8407 (0x20D7)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-626">No se pudo recuperar el atributo de tipo de instancia.</span><span class="sxs-lookup"><span data-stu-id="3ad11-626">The instance type attribute could not be retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-627"><span id="ERROR_DS_CODE_INCONSISTENCY"></span><span id="error_ds_code_inconsistency"></span>**ERROR \_ de \_ incoherencia de código DS \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-627"><span id="ERROR_DS_CODE_INCONSISTENCY"></span><span id="error_ds_code_inconsistency"></span>**ERROR\_DS\_CODE\_INCONSISTENCY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-628">8408 (0x20D8)</span><span class="sxs-lookup"><span data-stu-id="3ad11-628">8408 (0x20D8)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-629">Se ha producido un error interno.</span><span class="sxs-lookup"><span data-stu-id="3ad11-629">An internal error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-630"><span id="ERROR_DS_DATABASE_ERROR"></span><span id="error_ds_database_error"></span>**error \_ de \_ base de datos de DS \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-630"><span id="ERROR_DS_DATABASE_ERROR"></span><span id="error_ds_database_error"></span>**ERROR\_DS\_DATABASE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-631">8409 (0x20D9)</span><span class="sxs-lookup"><span data-stu-id="3ad11-631">8409 (0x20D9)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-632">Error de base de datos.</span><span class="sxs-lookup"><span data-stu-id="3ad11-632">A database error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-633"><span id="ERROR_DS_GOVERNSID_MISSING"></span><span id="error_ds_governsid_missing"></span>**ERROR \_ DS \_ GOVERNSID \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-633"><span id="ERROR_DS_GOVERNSID_MISSING"></span><span id="error_ds_governsid_missing"></span>**ERROR\_DS\_GOVERNSID\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-634">8410 (0x20DA)</span><span class="sxs-lookup"><span data-stu-id="3ad11-634">8410 (0x20DA)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-635">Falta el atributo GOVERNSID.</span><span class="sxs-lookup"><span data-stu-id="3ad11-635">The attribute GOVERNSID is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-636"><span id="ERROR_DS_MISSING_EXPECTED_ATT"></span><span id="error_ds_missing_expected_att"></span>**ERROR \_ DS \_ falta \_ \_ ATT esperado**</span><span class="sxs-lookup"><span data-stu-id="3ad11-636"><span id="ERROR_DS_MISSING_EXPECTED_ATT"></span><span id="error_ds_missing_expected_att"></span>**ERROR\_DS\_MISSING\_EXPECTED\_ATT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-637">8411 (0x20DB)</span><span class="sxs-lookup"><span data-stu-id="3ad11-637">8411 (0x20DB)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-638">Falta un atributo esperado.</span><span class="sxs-lookup"><span data-stu-id="3ad11-638">An expected attribute is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-639"><span id="ERROR_DS_NCNAME_MISSING_CR_REF"></span><span id="error_ds_ncname_missing_cr_ref"></span>**ERROR \_ DS \_ \_ falta la \_ \_ referencia CR de NCNAME**</span><span class="sxs-lookup"><span data-stu-id="3ad11-639"><span id="ERROR_DS_NCNAME_MISSING_CR_REF"></span><span id="error_ds_ncname_missing_cr_ref"></span>**ERROR\_DS\_NCNAME\_MISSING\_CR\_REF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-640">8412 (0x20DC)</span><span class="sxs-lookup"><span data-stu-id="3ad11-640">8412 (0x20DC)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-641">Falta una referencia cruzada en el contexto de nomenclatura especificado.</span><span class="sxs-lookup"><span data-stu-id="3ad11-641">The specified naming context is missing a cross reference.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-642"><span id="ERROR_DS_SECURITY_CHECKING_ERROR"></span><span id="error_ds_security_checking_error"></span>**error \_ de \_ comprobación de seguridad de DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-642"><span id="ERROR_DS_SECURITY_CHECKING_ERROR"></span><span id="error_ds_security_checking_error"></span>**ERROR\_DS\_SECURITY\_CHECKING\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-643">8413 (0x20DD)</span><span class="sxs-lookup"><span data-stu-id="3ad11-643">8413 (0x20DD)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-644">Se ha producido un error de comprobación de seguridad.</span><span class="sxs-lookup"><span data-stu-id="3ad11-644">A security checking error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-645"><span id="ERROR_DS_SCHEMA_NOT_LOADED"></span><span id="error_ds_schema_not_loaded"></span>**\_no se \_ cargó el esquema DS de \_ error \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-645"><span id="ERROR_DS_SCHEMA_NOT_LOADED"></span><span id="error_ds_schema_not_loaded"></span>**ERROR\_DS\_SCHEMA\_NOT\_LOADED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-646">8414 (0x20DE)</span><span class="sxs-lookup"><span data-stu-id="3ad11-646">8414 (0x20DE)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-647">No se ha cargado el esquema.</span><span class="sxs-lookup"><span data-stu-id="3ad11-647">The schema is not loaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-648"><span id="ERROR_DS_SCHEMA_ALLOC_FAILED"></span><span id="error_ds_schema_alloc_failed"></span>**ERROR \_ de \_ asignación de esquema de DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-648"><span id="ERROR_DS_SCHEMA_ALLOC_FAILED"></span><span id="error_ds_schema_alloc_failed"></span>**ERROR\_DS\_SCHEMA\_ALLOC\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-649">8415 (0x20DF)</span><span class="sxs-lookup"><span data-stu-id="3ad11-649">8415 (0x20DF)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-650">No se pudo asignar el esquema.</span><span class="sxs-lookup"><span data-stu-id="3ad11-650">Schema allocation failed.</span></span> <span data-ttu-id="3ad11-651">Compruebe si el equipo se está quedando sin memoria.</span><span class="sxs-lookup"><span data-stu-id="3ad11-651">Please check if the machine is running low on memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-652"><span id="ERROR_DS_ATT_SCHEMA_REQ_SYNTAX"></span><span id="error_ds_att_schema_req_syntax"></span>**ERROR en la \_ Sintaxis de REQ de esquema de DS \_ ATT \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-652"><span id="ERROR_DS_ATT_SCHEMA_REQ_SYNTAX"></span><span id="error_ds_att_schema_req_syntax"></span>**ERROR\_DS\_ATT\_SCHEMA\_REQ\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-653">8416 (0x20E0)</span><span class="sxs-lookup"><span data-stu-id="3ad11-653">8416 (0x20E0)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-654">No se pudo obtener la sintaxis necesaria para el esquema de atributo.</span><span class="sxs-lookup"><span data-stu-id="3ad11-654">Failed to obtain the required syntax for the attribute schema.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-655"><span id="ERROR_DS_GCVERIFY_ERROR"></span><span id="error_ds_gcverify_error"></span>**error \_ \_ GCVERIFY DS \_ error**</span><span class="sxs-lookup"><span data-stu-id="3ad11-655"><span id="ERROR_DS_GCVERIFY_ERROR"></span><span id="error_ds_gcverify_error"></span>**ERROR\_DS\_GCVERIFY\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-656">8417 (0x20E1)</span><span class="sxs-lookup"><span data-stu-id="3ad11-656">8417 (0x20E1)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-657">No se pudo comprobar el catálogo global.</span><span class="sxs-lookup"><span data-stu-id="3ad11-657">The global catalog verification failed.</span></span> <span data-ttu-id="3ad11-658">El catálogo global no está disponible o no es compatible con la operación.</span><span class="sxs-lookup"><span data-stu-id="3ad11-658">The global catalog is not available or does not support the operation.</span></span> <span data-ttu-id="3ad11-659">Parte del directorio no está disponible actualmente.</span><span class="sxs-lookup"><span data-stu-id="3ad11-659">Some part of the directory is currently not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-660"><span id="ERROR_DS_DRA_SCHEMA_MISMATCH"></span><span id="error_ds_dra_schema_mismatch"></span>**ERROR \_ de \_ \_ coincidencia de esquema \_ de DS Dra**</span><span class="sxs-lookup"><span data-stu-id="3ad11-660"><span id="ERROR_DS_DRA_SCHEMA_MISMATCH"></span><span id="error_ds_dra_schema_mismatch"></span>**ERROR\_DS\_DRA\_SCHEMA\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-661">8418 (0x20E2)</span><span class="sxs-lookup"><span data-stu-id="3ad11-661">8418 (0x20E2)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-662">No se pudo realizar la operación de replicación debido a un error de coincidencia de esquema entre los servidores implicados.</span><span class="sxs-lookup"><span data-stu-id="3ad11-662">The replication operation failed because of a schema mismatch between the servers involved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-663"><span id="ERROR_DS_CANT_FIND_DSA_OBJ"></span><span id="error_ds_cant_find_dsa_obj"></span>**ERROR \_ DS no se \_ encuentra el \_ \_ DSA \_ obj**</span><span class="sxs-lookup"><span data-stu-id="3ad11-663"><span id="ERROR_DS_CANT_FIND_DSA_OBJ"></span><span id="error_ds_cant_find_dsa_obj"></span>**ERROR\_DS\_CANT\_FIND\_DSA\_OBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-664">8419 (0x20E3)</span><span class="sxs-lookup"><span data-stu-id="3ad11-664">8419 (0x20E3)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-665">No se encontró el objeto DSA.</span><span class="sxs-lookup"><span data-stu-id="3ad11-665">The DSA object could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-666"><span id="ERROR_DS_CANT_FIND_EXPECTED_NC"></span><span id="error_ds_cant_find_expected_nc"></span>**ERROR \_ DS \_ no \_ se encuentra el \_ \_ NC esperado**</span><span class="sxs-lookup"><span data-stu-id="3ad11-666"><span id="ERROR_DS_CANT_FIND_EXPECTED_NC"></span><span id="error_ds_cant_find_expected_nc"></span>**ERROR\_DS\_CANT\_FIND\_EXPECTED\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-667">8420 (0x20E4)</span><span class="sxs-lookup"><span data-stu-id="3ad11-667">8420 (0x20E4)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-668">No se encontró el contexto de nomenclatura.</span><span class="sxs-lookup"><span data-stu-id="3ad11-668">The naming context could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-669"><span id="ERROR_DS_CANT_FIND_NC_IN_CACHE"></span><span id="error_ds_cant_find_nc_in_cache"></span>**ERROR \_ DS no se \_ \_ encuentra \_ NC \_ en la \_ memoria caché**</span><span class="sxs-lookup"><span data-stu-id="3ad11-669"><span id="ERROR_DS_CANT_FIND_NC_IN_CACHE"></span><span id="error_ds_cant_find_nc_in_cache"></span>**ERROR\_DS\_CANT\_FIND\_NC\_IN\_CACHE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-670">8421 (0x20E5)</span><span class="sxs-lookup"><span data-stu-id="3ad11-670">8421 (0x20E5)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-671">No se encontró el contexto de nomenclatura en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="3ad11-671">The naming context could not be found in the cache.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-672"><span id="ERROR_DS_CANT_RETRIEVE_CHILD"></span><span id="error_ds_cant_retrieve_child"></span>**ERROR DS no se pudo \_ \_ recuperar el \_ \_ elemento secundario**</span><span class="sxs-lookup"><span data-stu-id="3ad11-672"><span id="ERROR_DS_CANT_RETRIEVE_CHILD"></span><span id="error_ds_cant_retrieve_child"></span>**ERROR\_DS\_CANT\_RETRIEVE\_CHILD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-673">8422 (0x20E6)</span><span class="sxs-lookup"><span data-stu-id="3ad11-673">8422 (0x20E6)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-674">No se pudo recuperar el objeto secundario.</span><span class="sxs-lookup"><span data-stu-id="3ad11-674">The child object could not be retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-675"><span id="ERROR_DS_SECURITY_ILLEGAL_MODIFY"></span><span id="error_ds_security_illegal_modify"></span>**ERROR \_ de \_ seguridad de DS \_ modificación no válida \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-675"><span id="ERROR_DS_SECURITY_ILLEGAL_MODIFY"></span><span id="error_ds_security_illegal_modify"></span>**ERROR\_DS\_SECURITY\_ILLEGAL\_MODIFY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-676">8423 (0x20E7)</span><span class="sxs-lookup"><span data-stu-id="3ad11-676">8423 (0x20E7)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-677">No se permitió la modificación por motivos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="3ad11-677">The modification was not permitted for security reasons.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-678"><span id="ERROR_DS_CANT_REPLACE_HIDDEN_REC"></span><span id="error_ds_cant_replace_hidden_rec"></span>**ERROR DS no se pudo \_ \_ reemplazar el \_ \_ \_ rec oculto**</span><span class="sxs-lookup"><span data-stu-id="3ad11-678"><span id="ERROR_DS_CANT_REPLACE_HIDDEN_REC"></span><span id="error_ds_cant_replace_hidden_rec"></span>**ERROR\_DS\_CANT\_REPLACE\_HIDDEN\_REC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-679">8424 (0x20E8)</span><span class="sxs-lookup"><span data-stu-id="3ad11-679">8424 (0x20E8)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-680">La operación no puede reemplazar el registro oculto.</span><span class="sxs-lookup"><span data-stu-id="3ad11-680">The operation cannot replace the hidden record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-681"><span id="ERROR_DS_BAD_HIERARCHY_FILE"></span><span id="error_ds_bad_hierarchy_file"></span>**ERROR en el \_ \_ archivo de jerarquía incorrecta de DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-681"><span id="ERROR_DS_BAD_HIERARCHY_FILE"></span><span id="error_ds_bad_hierarchy_file"></span>**ERROR\_DS\_BAD\_HIERARCHY\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-682">8425 (0x20E9)</span><span class="sxs-lookup"><span data-stu-id="3ad11-682">8425 (0x20E9)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-683">El archivo de jerarquía no es válido.</span><span class="sxs-lookup"><span data-stu-id="3ad11-683">The hierarchy file is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-684"><span id="ERROR_DS_BUILD_HIERARCHY_TABLE_FAILED"></span><span id="error_ds_build_hierarchy_table_failed"></span>**ERROR en la \_ tabla de jerarquía de compilación de DS \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-684"><span id="ERROR_DS_BUILD_HIERARCHY_TABLE_FAILED"></span><span id="error_ds_build_hierarchy_table_failed"></span>**ERROR\_DS\_BUILD\_HIERARCHY\_TABLE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-685">8426 (0x20EA)</span><span class="sxs-lookup"><span data-stu-id="3ad11-685">8426 (0x20EA)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-686">Error al tratar de generar la tabla de jerarquías.</span><span class="sxs-lookup"><span data-stu-id="3ad11-686">The attempt to build the hierarchy table failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-687"><span id="ERROR_DS_CONFIG_PARAM_MISSING"></span><span id="error_ds_config_param_missing"></span>**ERROR \_ \_ falta el \_ parámetro de configuración de DS \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-687"><span id="ERROR_DS_CONFIG_PARAM_MISSING"></span><span id="error_ds_config_param_missing"></span>**ERROR\_DS\_CONFIG\_PARAM\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-688">8427 (0x20EB)</span><span class="sxs-lookup"><span data-stu-id="3ad11-688">8427 (0x20EB)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-689">Falta el parámetro de configuración de directorio en el registro.</span><span class="sxs-lookup"><span data-stu-id="3ad11-689">The directory configuration parameter is missing from the registry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-690"><span id="ERROR_DS_COUNTING_AB_INDICES_FAILED"></span><span id="error_ds_counting_ab_indices_failed"></span>**ERROR \_ DS \_ \_ al contar \_ índices AB \_ con errores**</span><span class="sxs-lookup"><span data-stu-id="3ad11-690"><span id="ERROR_DS_COUNTING_AB_INDICES_FAILED"></span><span id="error_ds_counting_ab_indices_failed"></span>**ERROR\_DS\_COUNTING\_AB\_INDICES\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-691">8428 (0x20EC)</span><span class="sxs-lookup"><span data-stu-id="3ad11-691">8428 (0x20EC)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-692">Error al intentar contar los índices de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="3ad11-692">The attempt to count the address book indices failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-693"><span id="ERROR_DS_HIERARCHY_TABLE_MALLOC_FAILED"></span><span id="error_ds_hierarchy_table_malloc_failed"></span>**ERROR en la \_ tabla de jerarquía de DS \_ \_ \_ MALLOC \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-693"><span id="ERROR_DS_HIERARCHY_TABLE_MALLOC_FAILED"></span><span id="error_ds_hierarchy_table_malloc_failed"></span>**ERROR\_DS\_HIERARCHY\_TABLE\_MALLOC\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-694">8429 (0x20ED)</span><span class="sxs-lookup"><span data-stu-id="3ad11-694">8429 (0x20ED)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-695">Error en la asignación de la tabla de jerarquía.</span><span class="sxs-lookup"><span data-stu-id="3ad11-695">The allocation of the hierarchy table failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-696"><span id="ERROR_DS_INTERNAL_FAILURE"></span><span id="error_ds_internal_failure"></span>**ERROR \_ interno de DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-696"><span id="ERROR_DS_INTERNAL_FAILURE"></span><span id="error_ds_internal_failure"></span>**ERROR\_DS\_INTERNAL\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-697">8430 (0x20EE)</span><span class="sxs-lookup"><span data-stu-id="3ad11-697">8430 (0x20EE)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-698">El servicio de directorio encontró un error interno.</span><span class="sxs-lookup"><span data-stu-id="3ad11-698">The directory service encountered an internal failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-699"><span id="ERROR_DS_UNKNOWN_ERROR"></span><span id="error_ds_unknown_error"></span>**error de \_ DS \_ desconocido \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-699"><span id="ERROR_DS_UNKNOWN_ERROR"></span><span id="error_ds_unknown_error"></span>**ERROR\_DS\_UNKNOWN\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-700">8431 (0x20EF)</span><span class="sxs-lookup"><span data-stu-id="3ad11-700">8431 (0x20EF)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-701">El servicio de directorio encontró un error desconocido.</span><span class="sxs-lookup"><span data-stu-id="3ad11-701">The directory service encountered an unknown failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-702"><span id="ERROR_DS_ROOT_REQUIRES_CLASS_TOP"></span><span id="error_ds_root_requires_class_top"></span>**el ERROR de la \_ raíz de DS \_ requiere la \_ \_ clase \_ Top**</span><span class="sxs-lookup"><span data-stu-id="3ad11-702"><span id="ERROR_DS_ROOT_REQUIRES_CLASS_TOP"></span><span id="error_ds_root_requires_class_top"></span>**ERROR\_DS\_ROOT\_REQUIRES\_CLASS\_TOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-703">8432 (0x20F0)</span><span class="sxs-lookup"><span data-stu-id="3ad11-703">8432 (0x20F0)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-704">Un objeto raíz requiere una clase de ' Top '.</span><span class="sxs-lookup"><span data-stu-id="3ad11-704">A root object requires a class of 'top'.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-705"><span id="ERROR_DS_REFUSING_FSMO_ROLES"></span><span id="error_ds_refusing_fsmo_roles"></span>**ERROR de \_ DS al \_ rechazar los \_ \_ roles FSMO**</span><span class="sxs-lookup"><span data-stu-id="3ad11-705"><span id="ERROR_DS_REFUSING_FSMO_ROLES"></span><span id="error_ds_refusing_fsmo_roles"></span>**ERROR\_DS\_REFUSING\_FSMO\_ROLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-706">8433 (0x20F1)</span><span class="sxs-lookup"><span data-stu-id="3ad11-706">8433 (0x20F1)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-707">Este servidor de directorio se está cerrando y no puede tomar posesión de los nuevos roles de operación de maestro único flotante.</span><span class="sxs-lookup"><span data-stu-id="3ad11-707">This directory server is shutting down, and cannot take ownership of new floating single-master operation roles.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-708"><span id="ERROR_DS_MISSING_FSMO_SETTINGS"></span><span id="error_ds_missing_fsmo_settings"></span>**ERROR \_ DS \_ falta \_ la \_ configuración de FSMO**</span><span class="sxs-lookup"><span data-stu-id="3ad11-708"><span id="ERROR_DS_MISSING_FSMO_SETTINGS"></span><span id="error_ds_missing_fsmo_settings"></span>**ERROR\_DS\_MISSING\_FSMO\_SETTINGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-709">8434 (0x20F2)</span><span class="sxs-lookup"><span data-stu-id="3ad11-709">8434 (0x20F2)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-710">Falta información de configuración obligatoria en el servicio de directorio y no puede determinar la propiedad de los roles de operación de un solo maestro flotante.</span><span class="sxs-lookup"><span data-stu-id="3ad11-710">The directory service is missing mandatory configuration information, and is unable to determine the ownership of floating single-master operation roles.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-711"><span id="ERROR_DS_UNABLE_TO_SURRENDER_ROLES"></span><span id="error_ds_unable_to_surrender_roles"></span>**ERROR \_ DS \_ no se pueden ceder \_ \_ \_ roles**</span><span class="sxs-lookup"><span data-stu-id="3ad11-711"><span id="ERROR_DS_UNABLE_TO_SURRENDER_ROLES"></span><span id="error_ds_unable_to_surrender_roles"></span>**ERROR\_DS\_UNABLE\_TO\_SURRENDER\_ROLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-712">8435 (0x20F3)</span><span class="sxs-lookup"><span data-stu-id="3ad11-712">8435 (0x20F3)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-713">El servicio de directorio no pudo transferir la propiedad de uno o varios roles de operación de maestro único flotante a otros servidores.</span><span class="sxs-lookup"><span data-stu-id="3ad11-713">The directory service was unable to transfer ownership of one or more floating single-master operation roles to other servers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-714"><span id="ERROR_DS_DRA_GENERIC"></span><span id="error_ds_dra_generic"></span>**ERROR de \_ DS \_ Dra \_ genérico**</span><span class="sxs-lookup"><span data-stu-id="3ad11-714"><span id="ERROR_DS_DRA_GENERIC"></span><span id="error_ds_dra_generic"></span>**ERROR\_DS\_DRA\_GENERIC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-715">8436 (0x20F4)</span><span class="sxs-lookup"><span data-stu-id="3ad11-715">8436 (0x20F4)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-716">No se pudo realizar la operación de replicación.</span><span class="sxs-lookup"><span data-stu-id="3ad11-716">The replication operation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-717"><span id="ERROR_DS_DRA_INVALID_PARAMETER"></span><span id="error_ds_dra_invalid_parameter"></span>**ERROR en el \_ \_ \_ parámetro no válido del Dra DS \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-717"><span id="ERROR_DS_DRA_INVALID_PARAMETER"></span><span id="error_ds_dra_invalid_parameter"></span>**ERROR\_DS\_DRA\_INVALID\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-718">8437 (0x20F5)</span><span class="sxs-lookup"><span data-stu-id="3ad11-718">8437 (0x20F5)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-719">Se especificó un parámetro no válido para esta operación de replicación.</span><span class="sxs-lookup"><span data-stu-id="3ad11-719">An invalid parameter was specified for this replication operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-720"><span id="ERROR_DS_DRA_BUSY"></span><span id="error_ds_dra_busy"></span>**ERROR de \_ DS \_ Dra \_ ocupado**</span><span class="sxs-lookup"><span data-stu-id="3ad11-720"><span id="ERROR_DS_DRA_BUSY"></span><span id="error_ds_dra_busy"></span>**ERROR\_DS\_DRA\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-721">8438 (0x20F6)</span><span class="sxs-lookup"><span data-stu-id="3ad11-721">8438 (0x20F6)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-722">El servicio de directorio está demasiado ocupado para completar la operación de replicación en este momento.</span><span class="sxs-lookup"><span data-stu-id="3ad11-722">The directory service is too busy to complete the replication operation at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-723"><span id="ERROR_DS_DRA_BAD_DN"></span><span id="error_ds_dra_bad_dn"></span>**ERROR \_ DS \_ Dra \_ \_ DN erróneo**</span><span class="sxs-lookup"><span data-stu-id="3ad11-723"><span id="ERROR_DS_DRA_BAD_DN"></span><span id="error_ds_dra_bad_dn"></span>**ERROR\_DS\_DRA\_BAD\_DN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-724">8439 (0x20F7)</span><span class="sxs-lookup"><span data-stu-id="3ad11-724">8439 (0x20F7)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-725">El nombre distintivo especificado para esta operación de replicación no es válido.</span><span class="sxs-lookup"><span data-stu-id="3ad11-725">The distinguished name specified for this replication operation is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-726"><span id="ERROR_DS_DRA_BAD_NC"></span><span id="error_ds_dra_bad_nc"></span>**ERROR de \_ DS no válido de DS \_ Dra \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-726"><span id="ERROR_DS_DRA_BAD_NC"></span><span id="error_ds_dra_bad_nc"></span>**ERROR\_DS\_DRA\_BAD\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-727">8440 (0x20F8)</span><span class="sxs-lookup"><span data-stu-id="3ad11-727">8440 (0x20F8)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-728">El contexto de nomenclatura especificado para esta operación de replicación no es válido.</span><span class="sxs-lookup"><span data-stu-id="3ad11-728">The naming context specified for this replication operation is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-729"><span id="ERROR_DS_DRA_DN_EXISTS"></span><span id="error_ds_dra_dn_exists"></span>**ERROR \_ \_ DN Dra \_ DN \_ existe**</span><span class="sxs-lookup"><span data-stu-id="3ad11-729"><span id="ERROR_DS_DRA_DN_EXISTS"></span><span id="error_ds_dra_dn_exists"></span>**ERROR\_DS\_DRA\_DN\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-730">8441 (0x20F9)</span><span class="sxs-lookup"><span data-stu-id="3ad11-730">8441 (0x20F9)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-731">El nombre distintivo especificado para esta operación de replicación ya existe.</span><span class="sxs-lookup"><span data-stu-id="3ad11-731">The distinguished name specified for this replication operation already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-732"><span id="ERROR_DS_DRA_INTERNAL_ERROR"></span><span id="error_ds_dra_internal_error"></span>**error \_ \_ interno de Dra de DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-732"><span id="ERROR_DS_DRA_INTERNAL_ERROR"></span><span id="error_ds_dra_internal_error"></span>**ERROR\_DS\_DRA\_INTERNAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-733">8442 (0x20FA)</span><span class="sxs-lookup"><span data-stu-id="3ad11-733">8442 (0x20FA)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-734">El sistema de replicación encontró un error interno.</span><span class="sxs-lookup"><span data-stu-id="3ad11-734">The replication system encountered an internal error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-735"><span id="ERROR_DS_DRA_INCONSISTENT_DIT"></span><span id="error_ds_dra_inconsistent_dit"></span>**ERROR en el \_ \_ \_ DIT Dra incoherente de DS \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-735"><span id="ERROR_DS_DRA_INCONSISTENT_DIT"></span><span id="error_ds_dra_inconsistent_dit"></span>**ERROR\_DS\_DRA\_INCONSISTENT\_DIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-736">8443 (0x20FB)</span><span class="sxs-lookup"><span data-stu-id="3ad11-736">8443 (0x20FB)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-737">La operación de replicación encontró una incoherencia en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="3ad11-737">The replication operation encountered a database inconsistency.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-738"><span id="ERROR_DS_DRA_CONNECTION_FAILED"></span><span id="error_ds_dra_connection_failed"></span>**ERROR en la \_ \_ \_ conexión \_ Dra de DS**</span><span class="sxs-lookup"><span data-stu-id="3ad11-738"><span id="ERROR_DS_DRA_CONNECTION_FAILED"></span><span id="error_ds_dra_connection_failed"></span>**ERROR\_DS\_DRA\_CONNECTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-739">8444 (0x20FC)</span><span class="sxs-lookup"><span data-stu-id="3ad11-739">8444 (0x20FC)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-740">No se pudo establecer contacto con el servidor especificado para esta operación de replicación.</span><span class="sxs-lookup"><span data-stu-id="3ad11-740">The server specified for this replication operation could not be contacted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-741"><span id="ERROR_DS_DRA_BAD_INSTANCE_TYPE"></span><span id="error_ds_dra_bad_instance_type"></span>**ERROR \_ de \_ \_ tipo de \_ instancia \_ incorrecta de Dra DS**</span><span class="sxs-lookup"><span data-stu-id="3ad11-741"><span id="ERROR_DS_DRA_BAD_INSTANCE_TYPE"></span><span id="error_ds_dra_bad_instance_type"></span>**ERROR\_DS\_DRA\_BAD\_INSTANCE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-742">8445 (0x20FD)</span><span class="sxs-lookup"><span data-stu-id="3ad11-742">8445 (0x20FD)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-743">La operación de replicación encontró un objeto con un tipo de instancia no válido.</span><span class="sxs-lookup"><span data-stu-id="3ad11-743">The replication operation encountered an object with an invalid instance type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-744"><span id="ERROR_DS_DRA_OUT_OF_MEM"></span><span id="error_ds_dra_out_of_mem"></span>**ERROR \_ \_ de DS \_ Dra \_ de \_ memoria insuficiente**</span><span class="sxs-lookup"><span data-stu-id="3ad11-744"><span id="ERROR_DS_DRA_OUT_OF_MEM"></span><span id="error_ds_dra_out_of_mem"></span>**ERROR\_DS\_DRA\_OUT\_OF\_MEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-745">8446 (0x20FE)</span><span class="sxs-lookup"><span data-stu-id="3ad11-745">8446 (0x20FE)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-746">La operación de replicación no pudo asignar memoria.</span><span class="sxs-lookup"><span data-stu-id="3ad11-746">The replication operation failed to allocate memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-747"><span id="ERROR_DS_DRA_MAIL_PROBLEM"></span><span id="error_ds_dra_mail_problem"></span>**ERROR \_ de \_ correo Dra de DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-747"><span id="ERROR_DS_DRA_MAIL_PROBLEM"></span><span id="error_ds_dra_mail_problem"></span>**ERROR\_DS\_DRA\_MAIL\_PROBLEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-748">8447 (0x20FF)</span><span class="sxs-lookup"><span data-stu-id="3ad11-748">8447 (0x20FF)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-749">La operación de replicación encontró un error con el sistema de correo.</span><span class="sxs-lookup"><span data-stu-id="3ad11-749">The replication operation encountered an error with the mail system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-750"><span id="ERROR_DS_DRA_REF_ALREADY_EXISTS"></span><span id="error_ds_dra_ref_already_exists"></span>**el ERROR \_ DS \_ Dra \_ ref \_ ya \_ existe**</span><span class="sxs-lookup"><span data-stu-id="3ad11-750"><span id="ERROR_DS_DRA_REF_ALREADY_EXISTS"></span><span id="error_ds_dra_ref_already_exists"></span>**ERROR\_DS\_DRA\_REF\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-751">8448 (0x2100)</span><span class="sxs-lookup"><span data-stu-id="3ad11-751">8448 (0x2100)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-752">La información de referencia de replicación para el servidor de destino ya existe.</span><span class="sxs-lookup"><span data-stu-id="3ad11-752">The replication reference information for the target server already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-753"><span id="ERROR_DS_DRA_REF_NOT_FOUND"></span><span id="error_ds_dra_ref_not_found"></span>**ERROR \_ de \_ referencia Dra de DS \_ \_ no \_ encontrada**</span><span class="sxs-lookup"><span data-stu-id="3ad11-753"><span id="ERROR_DS_DRA_REF_NOT_FOUND"></span><span id="error_ds_dra_ref_not_found"></span>**ERROR\_DS\_DRA\_REF\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-754">8449 (0x2101)</span><span class="sxs-lookup"><span data-stu-id="3ad11-754">8449 (0x2101)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-755">La información de referencia de replicación para el servidor de destino no existe.</span><span class="sxs-lookup"><span data-stu-id="3ad11-755">The replication reference information for the target server does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-756"><span id="ERROR_DS_DRA_OBJ_IS_REP_SOURCE"></span><span id="error_ds_dra_obj_is_rep_source"></span>**ERROR \_ DS \_ Dra \_ obj \_ es \_ origen de REP \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-756"><span id="ERROR_DS_DRA_OBJ_IS_REP_SOURCE"></span><span id="error_ds_dra_obj_is_rep_source"></span>**ERROR\_DS\_DRA\_OBJ\_IS\_REP\_SOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-757">8450 (0x2102)</span><span class="sxs-lookup"><span data-stu-id="3ad11-757">8450 (0x2102)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-758">No se puede quitar el contexto de nomenclatura porque se replica en otro servidor.</span><span class="sxs-lookup"><span data-stu-id="3ad11-758">The naming context cannot be removed because it is replicated to another server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-759"><span id="ERROR_DS_DRA_DB_ERROR"></span><span id="error_ds_dra_db_error"></span>**error \_ DS \_ BD de Dra \_ \_ error**</span><span class="sxs-lookup"><span data-stu-id="3ad11-759"><span id="ERROR_DS_DRA_DB_ERROR"></span><span id="error_ds_dra_db_error"></span>**ERROR\_DS\_DRA\_DB\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-760">8451 (0x2103)</span><span class="sxs-lookup"><span data-stu-id="3ad11-760">8451 (0x2103)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-761">La operación de replicación encontró un error de base de datos.</span><span class="sxs-lookup"><span data-stu-id="3ad11-761">The replication operation encountered a database error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-762"><span id="ERROR_DS_DRA_NO_REPLICA"></span><span id="error_ds_dra_no_replica"></span>**ERROR \_ DS \_ Dra \_ sin \_ réplica**</span><span class="sxs-lookup"><span data-stu-id="3ad11-762"><span id="ERROR_DS_DRA_NO_REPLICA"></span><span id="error_ds_dra_no_replica"></span>**ERROR\_DS\_DRA\_NO\_REPLICA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-763">8452 (0x2104)</span><span class="sxs-lookup"><span data-stu-id="3ad11-763">8452 (0x2104)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-764">El contexto de nomenclatura se está quitando o no se ha replicado desde el servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="3ad11-764">The naming context is in the process of being removed or is not replicated from the specified server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-765"><span id="ERROR_DS_DRA_ACCESS_DENIED"></span><span id="error_ds_dra_access_denied"></span>**ERROR \_ de \_ acceso de Dra DS \_ \_ denegado**</span><span class="sxs-lookup"><span data-stu-id="3ad11-765"><span id="ERROR_DS_DRA_ACCESS_DENIED"></span><span id="error_ds_dra_access_denied"></span>**ERROR\_DS\_DRA\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-766">8453 (0x2105)</span><span class="sxs-lookup"><span data-stu-id="3ad11-766">8453 (0x2105)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-767">Se denegó el acceso a la replicación.</span><span class="sxs-lookup"><span data-stu-id="3ad11-767">Replication access was denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-768"><span id="ERROR_DS_DRA_NOT_SUPPORTED"></span><span id="error_ds_dra_not_supported"></span>**ERROR \_ DS \_ Dra \_ no \_ compatible**</span><span class="sxs-lookup"><span data-stu-id="3ad11-768"><span id="ERROR_DS_DRA_NOT_SUPPORTED"></span><span id="error_ds_dra_not_supported"></span>**ERROR\_DS\_DRA\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-769">8454 (0x2106)</span><span class="sxs-lookup"><span data-stu-id="3ad11-769">8454 (0x2106)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-770">La operación solicitada no es compatible con esta versión del servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="3ad11-770">The requested operation is not supported by this version of the directory service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-771"><span id="ERROR_DS_DRA_RPC_CANCELLED"></span><span id="error_ds_dra_rpc_cancelled"></span>**ERROR \_ de \_ RPC Dra de DS \_ \_ cancelado**</span><span class="sxs-lookup"><span data-stu-id="3ad11-771"><span id="ERROR_DS_DRA_RPC_CANCELLED"></span><span id="error_ds_dra_rpc_cancelled"></span>**ERROR\_DS\_DRA\_RPC\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-772">8455 (0x2107)</span><span class="sxs-lookup"><span data-stu-id="3ad11-772">8455 (0x2107)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-773">Se canceló la llamada a procedimiento remoto de replicación.</span><span class="sxs-lookup"><span data-stu-id="3ad11-773">The replication remote procedure call was cancelled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-774"><span id="ERROR_DS_DRA_SOURCE_DISABLED"></span><span id="error_ds_dra_source_disabled"></span>**origen Dra de ERROR de \_ DS \_ \_ \_ deshabilitado**</span><span class="sxs-lookup"><span data-stu-id="3ad11-774"><span id="ERROR_DS_DRA_SOURCE_DISABLED"></span><span id="error_ds_dra_source_disabled"></span>**ERROR\_DS\_DRA\_SOURCE\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-775">8456 (0x2108)</span><span class="sxs-lookup"><span data-stu-id="3ad11-775">8456 (0x2108)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-776">El servidor de origen está rechazando actualmente las solicitudes de replicación.</span><span class="sxs-lookup"><span data-stu-id="3ad11-776">The source server is currently rejecting replication requests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-777"><span id="ERROR_DS_DRA_SINK_DISABLED"></span><span id="error_ds_dra_sink_disabled"></span>**ERROR \_ de \_ receptor Dra de DS \_ \_ deshabilitado**</span><span class="sxs-lookup"><span data-stu-id="3ad11-777"><span id="ERROR_DS_DRA_SINK_DISABLED"></span><span id="error_ds_dra_sink_disabled"></span>**ERROR\_DS\_DRA\_SINK\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-778">8457 (0x2109)</span><span class="sxs-lookup"><span data-stu-id="3ad11-778">8457 (0x2109)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-779">El servidor de destino está rechazando actualmente las solicitudes de replicación.</span><span class="sxs-lookup"><span data-stu-id="3ad11-779">The destination server is currently rejecting replication requests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-780"><span id="ERROR_DS_DRA_NAME_COLLISION"></span><span id="error_ds_dra_name_collision"></span>**\_conflicto de \_ nombres de Dra de DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-780"><span id="ERROR_DS_DRA_NAME_COLLISION"></span><span id="error_ds_dra_name_collision"></span>**ERROR\_DS\_DRA\_NAME\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-781">8458 (0x210A)</span><span class="sxs-lookup"><span data-stu-id="3ad11-781">8458 (0x210A)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-782">No se pudo realizar la operación de replicación debido a una colisión de nombres de objetos.</span><span class="sxs-lookup"><span data-stu-id="3ad11-782">The replication operation failed due to a collision of object names.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-783"><span id="ERROR_DS_DRA_SOURCE_REINSTALLED"></span><span id="error_ds_dra_source_reinstalled"></span>**ERROR \_ de \_ origen Dra de DS \_ \_ reinstalado**</span><span class="sxs-lookup"><span data-stu-id="3ad11-783"><span id="ERROR_DS_DRA_SOURCE_REINSTALLED"></span><span id="error_ds_dra_source_reinstalled"></span>**ERROR\_DS\_DRA\_SOURCE\_REINSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-784">8459 (0x210B)</span><span class="sxs-lookup"><span data-stu-id="3ad11-784">8459 (0x210B)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-785">Se ha reinstalado el origen de replicación.</span><span class="sxs-lookup"><span data-stu-id="3ad11-785">The replication source has been reinstalled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-786"><span id="ERROR_DS_DRA_MISSING_PARENT"></span><span id="error_ds_dra_missing_parent"></span>**ERROR \_ : \_ no se encuentra el \_ elemento primario de Dra DS \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-786"><span id="ERROR_DS_DRA_MISSING_PARENT"></span><span id="error_ds_dra_missing_parent"></span>**ERROR\_DS\_DRA\_MISSING\_PARENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-787">8460 (0x210C)</span><span class="sxs-lookup"><span data-stu-id="3ad11-787">8460 (0x210C)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-788">No se pudo realizar la operación de replicación porque falta un objeto primario necesario.</span><span class="sxs-lookup"><span data-stu-id="3ad11-788">The replication operation failed because a required parent object is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-789"><span id="ERROR_DS_DRA_PREEMPTED"></span><span id="error_ds_dra_preempted"></span>**ERROR \_ de \_ Dra DS \_ cambiado**</span><span class="sxs-lookup"><span data-stu-id="3ad11-789"><span id="ERROR_DS_DRA_PREEMPTED"></span><span id="error_ds_dra_preempted"></span>**ERROR\_DS\_DRA\_PREEMPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-790">8461 (0x210D)</span><span class="sxs-lookup"><span data-stu-id="3ad11-790">8461 (0x210D)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-791">Se ha adelantado la operación de replicación.</span><span class="sxs-lookup"><span data-stu-id="3ad11-791">The replication operation was preempted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-792"><span id="ERROR_DS_DRA_ABANDON_SYNC"></span><span id="error_ds_dra_abandon_sync"></span>**ERROR \_ DS: salir de la \_ \_ \_ sincronización**</span><span class="sxs-lookup"><span data-stu-id="3ad11-792"><span id="ERROR_DS_DRA_ABANDON_SYNC"></span><span id="error_ds_dra_abandon_sync"></span>**ERROR\_DS\_DRA\_ABANDON\_SYNC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-793">8462 (0x210E)</span><span class="sxs-lookup"><span data-stu-id="3ad11-793">8462 (0x210E)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-794">Se abandonó el intento de sincronización de la replicación debido a una falta de actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="3ad11-794">The replication synchronization attempt was abandoned because of a lack of updates.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-795"><span id="ERROR_DS_DRA_SHUTDOWN"></span><span id="error_ds_dra_shutdown"></span>**ERROR \_ de \_ cierre de Dra de DS \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-795"><span id="ERROR_DS_DRA_SHUTDOWN"></span><span id="error_ds_dra_shutdown"></span>**ERROR\_DS\_DRA\_SHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-796">8463 (0x210F)</span><span class="sxs-lookup"><span data-stu-id="3ad11-796">8463 (0x210F)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-797">La operación de replicación finalizó porque el sistema se está cerrando.</span><span class="sxs-lookup"><span data-stu-id="3ad11-797">The replication operation was terminated because the system is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-798"><span id="ERROR_DS_DRA_INCOMPATIBLE_PARTIAL_SET"></span><span id="error_ds_dra_incompatible_partial_set"></span>**ERROR en el \_ \_ \_ \_ \_ conjunto parcial de Dra no compatible DS**</span><span class="sxs-lookup"><span data-stu-id="3ad11-798"><span id="ERROR_DS_DRA_INCOMPATIBLE_PARTIAL_SET"></span><span id="error_ds_dra_incompatible_partial_set"></span>**ERROR\_DS\_DRA\_INCOMPATIBLE\_PARTIAL\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-799">8464 (0x2110)</span><span class="sxs-lookup"><span data-stu-id="3ad11-799">8464 (0x2110)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-800">No se pudo realizar el intento de sincronización porque el controlador de dominio de destino está esperando sincronizar nuevos atributos parciales desde el origen.</span><span class="sxs-lookup"><span data-stu-id="3ad11-800">Synchronization attempt failed because the destination DC is currently waiting to synchronize new partial attributes from source.</span></span> <span data-ttu-id="3ad11-801">Esta condición es normal si un cambio de esquema reciente modificó el conjunto de atributos parcial.</span><span class="sxs-lookup"><span data-stu-id="3ad11-801">This condition is normal if a recent schema change modified the partial attribute set.</span></span> <span data-ttu-id="3ad11-802">El conjunto de atributos parciales de destino no es un subconjunto del conjunto de atributos parciales de origen.</span><span class="sxs-lookup"><span data-stu-id="3ad11-802">The destination partial attribute set is not a subset of source partial attribute set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-803"><span id="ERROR_DS_DRA_SOURCE_IS_PARTIAL_REPLICA"></span><span id="error_ds_dra_source_is_partial_replica"></span>**el \_ origen Dra DS de error \_ \_ es una \_ \_ \_ réplica parcial**</span><span class="sxs-lookup"><span data-stu-id="3ad11-803"><span id="ERROR_DS_DRA_SOURCE_IS_PARTIAL_REPLICA"></span><span id="error_ds_dra_source_is_partial_replica"></span>**ERROR\_DS\_DRA\_SOURCE\_IS\_PARTIAL\_REPLICA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-804">8465 (0x2111)</span><span class="sxs-lookup"><span data-stu-id="3ad11-804">8465 (0x2111)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-805">No se pudo realizar el intento de sincronización de replicación porque una réplica maestra intentó realizar la sincronización desde una réplica parcial.</span><span class="sxs-lookup"><span data-stu-id="3ad11-805">The replication synchronization attempt failed because a master replica attempted to sync from a partial replica.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-806"><span id="ERROR_DS_DRA_EXTN_CONNECTION_FAILED"></span><span id="error_ds_dra_extn_connection_failed"></span>**ERROR \_ de \_ \_ conexión de EXTN Dra \_ de DS \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-806"><span id="ERROR_DS_DRA_EXTN_CONNECTION_FAILED"></span><span id="error_ds_dra_extn_connection_failed"></span>**ERROR\_DS\_DRA\_EXTN\_CONNECTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-807">8466 (0x2112)</span><span class="sxs-lookup"><span data-stu-id="3ad11-807">8466 (0x2112)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-808">Se ha establecido contacto con el servidor especificado para esta operación de replicación, pero el servidor no pudo ponerse en contacto con un servidor adicional necesario para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="3ad11-808">The server specified for this replication operation was contacted, but that server was unable to contact an additional server needed to complete the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-809"><span id="ERROR_DS_INSTALL_SCHEMA_MISMATCH"></span><span id="error_ds_install_schema_mismatch"></span>**ERROR \_ de \_ \_ coincidencia de esquema de instalación de DS \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-809"><span id="ERROR_DS_INSTALL_SCHEMA_MISMATCH"></span><span id="error_ds_install_schema_mismatch"></span>**ERROR\_DS\_INSTALL\_SCHEMA\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-810">8467 (0x2113)</span><span class="sxs-lookup"><span data-stu-id="3ad11-810">8467 (0x2113)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-811">La versión del esquema del servicio de directorio del bosque de origen no es compatible con la versión del servicio de directorio de este equipo.</span><span class="sxs-lookup"><span data-stu-id="3ad11-811">The version of the directory service schema of the source forest is not compatible with the version of directory service on this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-812"><span id="ERROR_DS_DUP_LINK_ID"></span><span id="error_ds_dup_link_id"></span>**\_identificador de \_ \_ vínculo DUP de DS \_ de error**</span><span class="sxs-lookup"><span data-stu-id="3ad11-812"><span id="ERROR_DS_DUP_LINK_ID"></span><span id="error_ds_dup_link_id"></span>**ERROR\_DS\_DUP\_LINK\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-813">8468 (0x2114)</span><span class="sxs-lookup"><span data-stu-id="3ad11-813">8468 (0x2114)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-814">No se pudo actualizar el esquema: ya existe un atributo con el mismo identificador de vínculo.</span><span class="sxs-lookup"><span data-stu-id="3ad11-814">Schema update failed: An attribute with the same link identifier already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-815"><span id="ERROR_DS_NAME_ERROR_RESOLVING"></span><span id="error_ds_name_error_resolving"></span>**ERROR \_ al \_ resolver el nombre de DS \_ error \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-815"><span id="ERROR_DS_NAME_ERROR_RESOLVING"></span><span id="error_ds_name_error_resolving"></span>**ERROR\_DS\_NAME\_ERROR\_RESOLVING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-816">8469 (0x2115)</span><span class="sxs-lookup"><span data-stu-id="3ad11-816">8469 (0x2115)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-817">Traducción de nombres: error de procesamiento genérico.</span><span class="sxs-lookup"><span data-stu-id="3ad11-817">Name translation: Generic processing error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-818"><span id="ERROR_DS_NAME_ERROR_NOT_FOUND"></span><span id="error_ds_name_error_not_found"></span>**error \_ de \_ nombre de DS \_ \_ no \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="3ad11-818"><span id="ERROR_DS_NAME_ERROR_NOT_FOUND"></span><span id="error_ds_name_error_not_found"></span>**ERROR\_DS\_NAME\_ERROR\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-819">8470 (0x2116)</span><span class="sxs-lookup"><span data-stu-id="3ad11-819">8470 (0x2116)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-820">Traducción de nombres: no se encontró el nombre o no es suficiente para ver el nombre.</span><span class="sxs-lookup"><span data-stu-id="3ad11-820">Name translation: Could not find the name or insufficient right to see name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-821"><span id="ERROR_DS_NAME_ERROR_NOT_UNIQUE"></span><span id="error_ds_name_error_not_unique"></span>**ERROR \_ de \_ nombre de DS \_ error \_ no \_ único**</span><span class="sxs-lookup"><span data-stu-id="3ad11-821"><span id="ERROR_DS_NAME_ERROR_NOT_UNIQUE"></span><span id="error_ds_name_error_not_unique"></span>**ERROR\_DS\_NAME\_ERROR\_NOT\_UNIQUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-822">8471 (0x2117)</span><span class="sxs-lookup"><span data-stu-id="3ad11-822">8471 (0x2117)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-823">Traducción de nombres: nombre de entrada asignado a más de un nombre de salida.</span><span class="sxs-lookup"><span data-stu-id="3ad11-823">Name translation: Input name mapped to more than one output name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-824"><span id="ERROR_DS_NAME_ERROR_NO_MAPPING"></span><span id="error_ds_name_error_no_mapping"></span>**ERROR \_ \_ el nombre de DS \_ error \_ no \_ asignación**</span><span class="sxs-lookup"><span data-stu-id="3ad11-824"><span id="ERROR_DS_NAME_ERROR_NO_MAPPING"></span><span id="error_ds_name_error_no_mapping"></span>**ERROR\_DS\_NAME\_ERROR\_NO\_MAPPING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-825">8472 (0x2118)</span><span class="sxs-lookup"><span data-stu-id="3ad11-825">8472 (0x2118)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-826">Traducción de nombres: se encontró el nombre de entrada, pero no el formato de salida asociado.</span><span class="sxs-lookup"><span data-stu-id="3ad11-826">Name translation: Input name found, but not the associated output format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-827"><span id="ERROR_DS_NAME_ERROR_DOMAIN_ONLY"></span><span id="error_ds_name_error_domain_only"></span>**ERROR \_ nombre de DS \_ \_ error \_ \_ solo dominio**</span><span class="sxs-lookup"><span data-stu-id="3ad11-827"><span id="ERROR_DS_NAME_ERROR_DOMAIN_ONLY"></span><span id="error_ds_name_error_domain_only"></span>**ERROR\_DS\_NAME\_ERROR\_DOMAIN\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-828">8473 (0x2119)</span><span class="sxs-lookup"><span data-stu-id="3ad11-828">8473 (0x2119)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-829">Traducción de nombres: no se puede resolver completamente, solo se encontró el dominio.</span><span class="sxs-lookup"><span data-stu-id="3ad11-829">Name translation: Unable to resolve completely, only the domain was found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-830"><span id="ERROR_DS_NAME_ERROR_NO_SYNTACTICAL_MAPPING"></span><span id="error_ds_name_error_no_syntactical_mapping"></span>**ERROR \_ \_ el nombre de DS \_ error \_ no \_ \_ asignación sintáctica**</span><span class="sxs-lookup"><span data-stu-id="3ad11-830"><span id="ERROR_DS_NAME_ERROR_NO_SYNTACTICAL_MAPPING"></span><span id="error_ds_name_error_no_syntactical_mapping"></span>**ERROR\_DS\_NAME\_ERROR\_NO\_SYNTACTICAL\_MAPPING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-831">8474 (0x211A)</span><span class="sxs-lookup"><span data-stu-id="3ad11-831">8474 (0x211A)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-832">Traducción de nombres: no se puede realizar una asignación puramente sintáctica en el cliente sin pasar a la conexión.</span><span class="sxs-lookup"><span data-stu-id="3ad11-832">Name translation: Unable to perform purely syntactical mapping at the client without going out to the wire.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-833"><span id="ERROR_DS_CONSTRUCTED_ATT_MOD"></span><span id="error_ds_constructed_att_mod"></span>**ERROR de \_ DS construido en el \_ \_ \_ módulo**</span><span class="sxs-lookup"><span data-stu-id="3ad11-833"><span id="ERROR_DS_CONSTRUCTED_ATT_MOD"></span><span id="error_ds_constructed_att_mod"></span>**ERROR\_DS\_CONSTRUCTED\_ATT\_MOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-834">8475 (0x211B)</span><span class="sxs-lookup"><span data-stu-id="3ad11-834">8475 (0x211B)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-835">No se permite la modificación de un atributo construido.</span><span class="sxs-lookup"><span data-stu-id="3ad11-835">Modification of a constructed attribute is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-836"><span id="ERROR_DS_WRONG_OM_OBJ_CLASS"></span><span id="error_ds_wrong_om_obj_class"></span>**ERROR \_ DS \_ \_ clase obj de OM incorrecta \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-836"><span id="ERROR_DS_WRONG_OM_OBJ_CLASS"></span><span id="error_ds_wrong_om_obj_class"></span>**ERROR\_DS\_WRONG\_OM\_OBJ\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-837">8476 (0x211C)</span><span class="sxs-lookup"><span data-stu-id="3ad11-837">8476 (0x211C)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-838">El objeto OM-Object-Class especificado no es correcto para un atributo con la sintaxis especificada.</span><span class="sxs-lookup"><span data-stu-id="3ad11-838">The OM-Object-Class specified is incorrect for an attribute with the specified syntax.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-839"><span id="ERROR_DS_DRA_REPL_PENDING"></span><span id="error_ds_dra_repl_pending"></span>**ERROR \_ de \_ REPL de Dra de DS \_ \_ pendiente**</span><span class="sxs-lookup"><span data-stu-id="3ad11-839"><span id="ERROR_DS_DRA_REPL_PENDING"></span><span id="error_ds_dra_repl_pending"></span>**ERROR\_DS\_DRA\_REPL\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-840">8477 (0x211D)</span><span class="sxs-lookup"><span data-stu-id="3ad11-840">8477 (0x211D)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-841">Se ha publicado la solicitud de replicación; esperando respuesta.</span><span class="sxs-lookup"><span data-stu-id="3ad11-841">The replication request has been posted; waiting for reply.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-842"><span id="ERROR_DS_DS_REQUIRED"></span><span id="error_ds_ds_required"></span>**ERROR \_ DS \_ DS \_ requerido**</span><span class="sxs-lookup"><span data-stu-id="3ad11-842"><span id="ERROR_DS_DS_REQUIRED"></span><span id="error_ds_ds_required"></span>**ERROR\_DS\_DS\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-843">8478 (0x211E)</span><span class="sxs-lookup"><span data-stu-id="3ad11-843">8478 (0x211E)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-844">La operación solicitada requiere un servicio de directorio y no hay ninguna disponible.</span><span class="sxs-lookup"><span data-stu-id="3ad11-844">The requested operation requires a directory service, and none was available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-845"><span id="ERROR_DS_INVALID_LDAP_DISPLAY_NAME"></span><span id="error_ds_invalid_ldap_display_name"></span>**ERROR \_ DS \_ \_ nombre para \_ Mostrar \_ LDAP no válido**</span><span class="sxs-lookup"><span data-stu-id="3ad11-845"><span id="ERROR_DS_INVALID_LDAP_DISPLAY_NAME"></span><span id="error_ds_invalid_ldap_display_name"></span>**ERROR\_DS\_INVALID\_LDAP\_DISPLAY\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-846">8479 (0x211F)</span><span class="sxs-lookup"><span data-stu-id="3ad11-846">8479 (0x211F)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-847">El nombre LDAP para mostrar de la clase o el atributo contiene caracteres que no son ASCII.</span><span class="sxs-lookup"><span data-stu-id="3ad11-847">The LDAP display name of the class or attribute contains non-ASCII characters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-848"><span id="ERROR_DS_NON_BASE_SEARCH"></span><span id="error_ds_non_base_search"></span>**ERROR \_ de \_ \_ búsqueda no \_ base de DS**</span><span class="sxs-lookup"><span data-stu-id="3ad11-848"><span id="ERROR_DS_NON_BASE_SEARCH"></span><span id="error_ds_non_base_search"></span>**ERROR\_DS\_NON\_BASE\_SEARCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-849">8480 (0x2120)</span><span class="sxs-lookup"><span data-stu-id="3ad11-849">8480 (0x2120)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-850">La operación de búsqueda solicitada solo se admite para las búsquedas base.</span><span class="sxs-lookup"><span data-stu-id="3ad11-850">The requested search operation is only supported for base searches.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-851"><span id="ERROR_DS_CANT_RETRIEVE_ATTS"></span><span id="error_ds_cant_retrieve_atts"></span>**ERROR DS no se pudo \_ \_ \_ recuperar \_ ATTS**</span><span class="sxs-lookup"><span data-stu-id="3ad11-851"><span id="ERROR_DS_CANT_RETRIEVE_ATTS"></span><span id="error_ds_cant_retrieve_atts"></span>**ERROR\_DS\_CANT\_RETRIEVE\_ATTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-852">8481 (0x2121)</span><span class="sxs-lookup"><span data-stu-id="3ad11-852">8481 (0x2121)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-853">La búsqueda no pudo recuperar los atributos de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="3ad11-853">The search failed to retrieve attributes from the database.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-854"><span id="ERROR_DS_BACKLINK_WITHOUT_LINK"></span><span id="error_ds_backlink_without_link"></span>**ERROR de \_ DS \_ BACKLINK \_ sin \_ vínculo**</span><span class="sxs-lookup"><span data-stu-id="3ad11-854"><span id="ERROR_DS_BACKLINK_WITHOUT_LINK"></span><span id="error_ds_backlink_without_link"></span>**ERROR\_DS\_BACKLINK\_WITHOUT\_LINK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-855">8482 (0x2122)</span><span class="sxs-lookup"><span data-stu-id="3ad11-855">8482 (0x2122)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-856">La operación de actualización del esquema intentó agregar un atributo de vínculo hacia atrás que no tiene un vínculo de avance correspondiente.</span><span class="sxs-lookup"><span data-stu-id="3ad11-856">The schema update operation tried to add a backward link attribute that has no corresponding forward link.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-857"><span id="ERROR_DS_EPOCH_MISMATCH"></span><span id="error_ds_epoch_mismatch"></span>**ERROR \_ de \_ coincidencia de tiempo de DS \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-857"><span id="ERROR_DS_EPOCH_MISMATCH"></span><span id="error_ds_epoch_mismatch"></span>**ERROR\_DS\_EPOCH\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-858">8483 (0x2123)</span><span class="sxs-lookup"><span data-stu-id="3ad11-858">8483 (0x2123)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-859">El origen y el destino de un movimiento entre dominios no coinciden con el número de tiempo del objeto.</span><span class="sxs-lookup"><span data-stu-id="3ad11-859">Source and destination of a cross-domain move do not agree on the object's epoch number.</span></span> <span data-ttu-id="3ad11-860">El origen o el destino no tienen la versión más reciente del objeto.</span><span class="sxs-lookup"><span data-stu-id="3ad11-860">Either source or destination does not have the latest version of the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-861"><span id="ERROR_DS_SRC_NAME_MISMATCH"></span><span id="error_ds_src_name_mismatch"></span>**ERROR \_ de \_ \_ coincidencia de nombre de origen de DS \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-861"><span id="ERROR_DS_SRC_NAME_MISMATCH"></span><span id="error_ds_src_name_mismatch"></span>**ERROR\_DS\_SRC\_NAME\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-862">8484 (0x2124)</span><span class="sxs-lookup"><span data-stu-id="3ad11-862">8484 (0x2124)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-863">El origen y el destino de un movimiento entre dominios no coinciden con el nombre actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="3ad11-863">Source and destination of a cross-domain move do not agree on the object's current name.</span></span> <span data-ttu-id="3ad11-864">El origen o el destino no tienen la versión más reciente del objeto.</span><span class="sxs-lookup"><span data-stu-id="3ad11-864">Either source or destination does not have the latest version of the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-865"><span id="ERROR_DS_SRC_AND_DST_NC_IDENTICAL"></span><span id="error_ds_src_and_dst_nc_identical"></span>**ERROR \_ DS \_ src \_ y \_ DST \_ NC \_ idénticos**</span><span class="sxs-lookup"><span data-stu-id="3ad11-865"><span id="ERROR_DS_SRC_AND_DST_NC_IDENTICAL"></span><span id="error_ds_src_and_dst_nc_identical"></span>**ERROR\_DS\_SRC\_AND\_DST\_NC\_IDENTICAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-866">8485 (0x2125)</span><span class="sxs-lookup"><span data-stu-id="3ad11-866">8485 (0x2125)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-867">El origen y el destino de la operación de movimiento entre dominios son idénticos.</span><span class="sxs-lookup"><span data-stu-id="3ad11-867">Source and destination for the cross-domain move operation are identical.</span></span> <span data-ttu-id="3ad11-868">El autor de la llamada debe usar la operación de movimiento local en lugar de la operación de movimiento entre dominios.</span><span class="sxs-lookup"><span data-stu-id="3ad11-868">Caller should use local move operation instead of cross-domain move operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-869"><span id="ERROR_DS_DST_NC_MISMATCH"></span><span id="error_ds_dst_nc_mismatch"></span>**ERROR de \_ DS \_ DST \_ NC \_ no coincidente**</span><span class="sxs-lookup"><span data-stu-id="3ad11-869"><span id="ERROR_DS_DST_NC_MISMATCH"></span><span id="error_ds_dst_nc_mismatch"></span>**ERROR\_DS\_DST\_NC\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-870">8486 (0x2126)</span><span class="sxs-lookup"><span data-stu-id="3ad11-870">8486 (0x2126)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-871">El origen y el destino de un movimiento entre dominios no están en acuerdo con los contextos de nomenclatura del bosque.</span><span class="sxs-lookup"><span data-stu-id="3ad11-871">Source and destination for a cross-domain move are not in agreement on the naming contexts in the forest.</span></span> <span data-ttu-id="3ad11-872">El origen o el destino no tienen la versión más reciente del contenedor de particiones.</span><span class="sxs-lookup"><span data-stu-id="3ad11-872">Either source or destination does not have the latest version of the Partitions container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-873"><span id="ERROR_DS_NOT_AUTHORITIVE_FOR_DST_NC"></span><span id="error_ds_not_authoritive_for_dst_nc"></span>**ERROR \_ DS \_ no \_ AUTHORITIVE \_ para \_ DST \_ NC**</span><span class="sxs-lookup"><span data-stu-id="3ad11-873"><span id="ERROR_DS_NOT_AUTHORITIVE_FOR_DST_NC"></span><span id="error_ds_not_authoritive_for_dst_nc"></span>**ERROR\_DS\_NOT\_AUTHORITIVE\_FOR\_DST\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-874">8487 (0x2127)</span><span class="sxs-lookup"><span data-stu-id="3ad11-874">8487 (0x2127)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-875">El destino de un movimiento entre dominios no es autoritativo para el contexto de nomenclatura de destino.</span><span class="sxs-lookup"><span data-stu-id="3ad11-875">Destination of a cross-domain move is not authoritative for the destination naming context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-876"><span id="ERROR_DS_SRC_GUID_MISMATCH"></span><span id="error_ds_src_guid_mismatch"></span>**ERROR \_ de \_ \_ coincidencia de GUID de src de DS \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-876"><span id="ERROR_DS_SRC_GUID_MISMATCH"></span><span id="error_ds_src_guid_mismatch"></span>**ERROR\_DS\_SRC\_GUID\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-877">8488 (0x2128)</span><span class="sxs-lookup"><span data-stu-id="3ad11-877">8488 (0x2128)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-878">El origen y el destino de un movimiento entre dominios no coinciden con la identidad del objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="3ad11-878">Source and destination of a cross-domain move do not agree on the identity of the source object.</span></span> <span data-ttu-id="3ad11-879">El origen o el destino no tienen la versión más reciente del objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="3ad11-879">Either source or destination does not have the latest version of the source object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-880"><span id="ERROR_DS_CANT_MOVE_DELETED_OBJECT"></span><span id="error_ds_cant_move_deleted_object"></span>**ERROR DS no se pudo \_ \_ quitar el \_ \_ \_ objeto eliminado**</span><span class="sxs-lookup"><span data-stu-id="3ad11-880"><span id="ERROR_DS_CANT_MOVE_DELETED_OBJECT"></span><span id="error_ds_cant_move_deleted_object"></span>**ERROR\_DS\_CANT\_MOVE\_DELETED\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-881">8489 (0x2129)</span><span class="sxs-lookup"><span data-stu-id="3ad11-881">8489 (0x2129)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-882">El servidor de destino ya sabe que el objeto que se está moviendo entre dominios se ha eliminado.</span><span class="sxs-lookup"><span data-stu-id="3ad11-882">Object being moved across-domains is already known to be deleted by the destination server.</span></span> <span data-ttu-id="3ad11-883">El servidor de origen no tiene la versión más reciente del objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="3ad11-883">The source server does not have the latest version of the source object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-884"><span id="ERROR_DS_PDC_OPERATION_IN_PROGRESS"></span><span id="error_ds_pdc_operation_in_progress"></span>**ERROR \_ \_ en la \_ operación \_ de PDC de DS en \_ curso**</span><span class="sxs-lookup"><span data-stu-id="3ad11-884"><span id="ERROR_DS_PDC_OPERATION_IN_PROGRESS"></span><span id="error_ds_pdc_operation_in_progress"></span>**ERROR\_DS\_PDC\_OPERATION\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-885">8490 (0x212A)</span><span class="sxs-lookup"><span data-stu-id="3ad11-885">8490 (0x212A)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-886">Otra operación que requiere acceso exclusivo al PDC FSMO ya está en curso.</span><span class="sxs-lookup"><span data-stu-id="3ad11-886">Another operation which requires exclusive access to the PDC FSMO is already in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-887"><span id="ERROR_DS_CROSS_DOMAIN_CLEANUP_REQD"></span><span id="error_ds_cross_domain_cleanup_reqd"></span>**ERROR \_ de \_ limpieza entre dominios de DS \_ \_ \_ REQD**</span><span class="sxs-lookup"><span data-stu-id="3ad11-887"><span id="ERROR_DS_CROSS_DOMAIN_CLEANUP_REQD"></span><span id="error_ds_cross_domain_cleanup_reqd"></span>**ERROR\_DS\_CROSS\_DOMAIN\_CLEANUP\_REQD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-888">8491 (0x212B)</span><span class="sxs-lookup"><span data-stu-id="3ad11-888">8491 (0x212B)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-889">No se pudo realizar una operación de movimiento entre dominios, de modo que existen dos versiones del objeto movido: una en los dominios de origen y de destino.</span><span class="sxs-lookup"><span data-stu-id="3ad11-889">A cross-domain move operation failed such that two versions of the moved object exist - one each in the source and destination domains.</span></span> <span data-ttu-id="3ad11-890">Es necesario quitar el objeto de destino para restaurar el sistema a un estado coherente.</span><span class="sxs-lookup"><span data-stu-id="3ad11-890">The destination object needs to be removed to restore the system to a consistent state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-891"><span id="ERROR_DS_ILLEGAL_XDOM_MOVE_OPERATION"></span><span id="error_ds_illegal_xdom_move_operation"></span>**ERROR de \_ DS \_ XDOM de \_ \_ operación de traslado \_ no válida**</span><span class="sxs-lookup"><span data-stu-id="3ad11-891"><span id="ERROR_DS_ILLEGAL_XDOM_MOVE_OPERATION"></span><span id="error_ds_illegal_xdom_move_operation"></span>**ERROR\_DS\_ILLEGAL\_XDOM\_MOVE\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-892">8492 (0x212C)</span><span class="sxs-lookup"><span data-stu-id="3ad11-892">8492 (0x212C)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-893">Es posible que este objeto no se mueva entre los límites del dominio porque no se permiten los movimientos entre dominios para esta clase, o bien el objeto tiene algunas características especiales, por ejemplo: cuenta de confianza o RID restringida, que impiden su movimiento.</span><span class="sxs-lookup"><span data-stu-id="3ad11-893">This object may not be moved across domain boundaries either because cross-domain moves for this class are disallowed, or the object has some special characteristics, e.g.: trust account or restricted RID, which prevent its move.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-894"><span id="ERROR_DS_CANT_WITH_ACCT_GROUP_MEMBERSHPS"></span><span id="error_ds_cant_with_acct_group_membershps"></span>**ERROR \_ DS \_ peralte \_ con el \_ grupo de acct \_ \_ MEMBERSHPS**</span><span class="sxs-lookup"><span data-stu-id="3ad11-894"><span id="ERROR_DS_CANT_WITH_ACCT_GROUP_MEMBERSHPS"></span><span id="error_ds_cant_with_acct_group_membershps"></span>**ERROR\_DS\_CANT\_WITH\_ACCT\_GROUP\_MEMBERSHPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-895">8493 (0x212D)</span><span class="sxs-lookup"><span data-stu-id="3ad11-895">8493 (0x212D)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-896">No se pueden trasladar objetos con pertenencias a los límites del dominio como una vez movidos, lo que infringiría las condiciones de pertenencia del grupo de cuentas.</span><span class="sxs-lookup"><span data-stu-id="3ad11-896">Can't move objects with memberships across domain boundaries as once moved, this would violate the membership conditions of the account group.</span></span> <span data-ttu-id="3ad11-897">Quite el objeto de cualquier pertenencia a grupos de cuentas e inténtelo de nuevo.</span><span class="sxs-lookup"><span data-stu-id="3ad11-897">Remove the object from any account group memberships and retry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-898"><span id="ERROR_DS_NC_MUST_HAVE_NC_PARENT"></span><span id="error_ds_nc_must_have_nc_parent"></span>**el \_ NC DS de error \_ \_ debe \_ tener el \_ \_ elemento primario NC**</span><span class="sxs-lookup"><span data-stu-id="3ad11-898"><span id="ERROR_DS_NC_MUST_HAVE_NC_PARENT"></span><span id="error_ds_nc_must_have_nc_parent"></span>**ERROR\_DS\_NC\_MUST\_HAVE\_NC\_PARENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-899">8494 (0x212E)</span><span class="sxs-lookup"><span data-stu-id="3ad11-899">8494 (0x212E)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-900">Un encabezado de contexto de nomenclatura debe ser el elemento secundario inmediato de otro encabezado de contexto de nomenclatura, no de un nodo interior.</span><span class="sxs-lookup"><span data-stu-id="3ad11-900">A naming context head must be the immediate child of another naming context head, not of an interior node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-901"><span id="ERROR_DS_CR_IMPOSSIBLE_TO_VALIDATE"></span><span id="error_ds_cr_impossible_to_validate"></span>**ERROR \_ DS \_ CR \_ imposible \_ \_ validar**</span><span class="sxs-lookup"><span data-stu-id="3ad11-901"><span id="ERROR_DS_CR_IMPOSSIBLE_TO_VALIDATE"></span><span id="error_ds_cr_impossible_to_validate"></span>**ERROR\_DS\_CR\_IMPOSSIBLE\_TO\_VALIDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-902">8495 (0x212F)</span><span class="sxs-lookup"><span data-stu-id="3ad11-902">8495 (0x212F)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-903">El directorio no puede validar el nombre del contexto de nomenclatura propuesto porque no contiene una réplica del contexto de nomenclatura por encima del contexto de nomenclatura propuesto.</span><span class="sxs-lookup"><span data-stu-id="3ad11-903">The directory cannot validate the proposed naming context name because it does not hold a replica of the naming context above the proposed naming context.</span></span> <span data-ttu-id="3ad11-904">Asegúrese de que el rol de maestro de nomenclatura de dominios está incluido en un servidor que está configurado como un servidor de catálogo global y que el servidor está actualizado con sus asociados de replicación.</span><span class="sxs-lookup"><span data-stu-id="3ad11-904">Please ensure that the domain naming master role is held by a server that is configured as a global catalog server, and that the server is up to date with its replication partners.</span></span> <span data-ttu-id="3ad11-905">(Se aplica solo a los maestros de nomenclatura de dominios de Windows 2000).</span><span class="sxs-lookup"><span data-stu-id="3ad11-905">(Applies only to Windows 2000 Domain Naming masters.)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-906"><span id="ERROR_DS_DST_DOMAIN_NOT_NATIVE"></span><span id="error_ds_dst_domain_not_native"></span>**ERROR de \_ dominio de DST de DS \_ \_ \_ no \_ nativo**</span><span class="sxs-lookup"><span data-stu-id="3ad11-906"><span id="ERROR_DS_DST_DOMAIN_NOT_NATIVE"></span><span id="error_ds_dst_domain_not_native"></span>**ERROR\_DS\_DST\_DOMAIN\_NOT\_NATIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-907">8496 (0x2130)</span><span class="sxs-lookup"><span data-stu-id="3ad11-907">8496 (0x2130)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-908">El dominio de destino debe estar en modo nativo.</span><span class="sxs-lookup"><span data-stu-id="3ad11-908">Destination domain must be in native mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-909"><span id="ERROR_DS_MISSING_INFRASTRUCTURE_CONTAINER"></span><span id="error_ds_missing_infrastructure_container"></span>**ERROR \_ DS \_ falta \_ el \_ contenedor de infraestructura**</span><span class="sxs-lookup"><span data-stu-id="3ad11-909"><span id="ERROR_DS_MISSING_INFRASTRUCTURE_CONTAINER"></span><span id="error_ds_missing_infrastructure_container"></span>**ERROR\_DS\_MISSING\_INFRASTRUCTURE\_CONTAINER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-910">8497 (0x2131)</span><span class="sxs-lookup"><span data-stu-id="3ad11-910">8497 (0x2131)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-911">No se puede realizar la operación porque el servidor no tiene un contenedor de infraestructura en el dominio de interés.</span><span class="sxs-lookup"><span data-stu-id="3ad11-911">The operation cannot be performed because the server does not have an infrastructure container in the domain of interest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-912"><span id="ERROR_DS_CANT_MOVE_ACCOUNT_GROUP"></span><span id="error_ds_cant_move_account_group"></span>**ERROR DS no se pudo \_ \_ quitar el \_ \_ grupo de cuentas \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-912"><span id="ERROR_DS_CANT_MOVE_ACCOUNT_GROUP"></span><span id="error_ds_cant_move_account_group"></span>**ERROR\_DS\_CANT\_MOVE\_ACCOUNT\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-913">8498 (0x2132)</span><span class="sxs-lookup"><span data-stu-id="3ad11-913">8498 (0x2132)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-914">No se permite el movimiento entre dominios de grupos de cuentas que no estén vacíos.</span><span class="sxs-lookup"><span data-stu-id="3ad11-914">Cross-domain move of non-empty account groups is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-915"><span id="ERROR_DS_CANT_MOVE_RESOURCE_GROUP"></span><span id="error_ds_cant_move_resource_group"></span>**ERROR DS no se pudo \_ \_ quitar el \_ \_ grupo de recursos \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-915"><span id="ERROR_DS_CANT_MOVE_RESOURCE_GROUP"></span><span id="error_ds_cant_move_resource_group"></span>**ERROR\_DS\_CANT\_MOVE\_RESOURCE\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-916">8499 (0x2133)</span><span class="sxs-lookup"><span data-stu-id="3ad11-916">8499 (0x2133)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-917">No se permite el movimiento entre dominios de grupos de recursos no vacíos.</span><span class="sxs-lookup"><span data-stu-id="3ad11-917">Cross-domain move of non-empty resource groups is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-918"><span id="ERROR_DS_INVALID_SEARCH_FLAG"></span><span id="error_ds_invalid_search_flag"></span>**ERROR \_ de \_ \_ marca de búsqueda no válida DS \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-918"><span id="ERROR_DS_INVALID_SEARCH_FLAG"></span><span id="error_ds_invalid_search_flag"></span>**ERROR\_DS\_INVALID\_SEARCH\_FLAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-919">8500 (0x2134)</span><span class="sxs-lookup"><span data-stu-id="3ad11-919">8500 (0x2134)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-920">Las marcas de búsqueda para el atributo no son válidas.</span><span class="sxs-lookup"><span data-stu-id="3ad11-920">The search flags for the attribute are invalid.</span></span> <span data-ttu-id="3ad11-921">El bit de ANR solo es válido en atributos de cadenas Unicode o teletexto.</span><span class="sxs-lookup"><span data-stu-id="3ad11-921">The ANR bit is valid only on attributes of Unicode or Teletex strings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-922"><span id="ERROR_DS_NO_TREE_DELETE_ABOVE_NC"></span><span id="error_ds_no_tree_delete_above_nc"></span>**ERROR \_ DS \_ no \_ se \_ eliminó el árbol \_ antes de \_ NC**</span><span class="sxs-lookup"><span data-stu-id="3ad11-922"><span id="ERROR_DS_NO_TREE_DELETE_ABOVE_NC"></span><span id="error_ds_no_tree_delete_above_nc"></span>**ERROR\_DS\_NO\_TREE\_DELETE\_ABOVE\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-923">8501 (0x2135)</span><span class="sxs-lookup"><span data-stu-id="3ad11-923">8501 (0x2135)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-924">No se permiten las eliminaciones de árbol a partir de un objeto que tiene un encabezado NC como descendiente.</span><span class="sxs-lookup"><span data-stu-id="3ad11-924">Tree deletions starting at an object which has an NC head as a descendant are not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-925"><span id="ERROR_DS_COULDNT_LOCK_TREE_FOR_DELETE"></span><span id="error_ds_couldnt_lock_tree_for_delete"></span>**ERROR \_ DS \_ COULDNT \_ \_ árbol \_ de bloqueo para \_ eliminar**</span><span class="sxs-lookup"><span data-stu-id="3ad11-925"><span id="ERROR_DS_COULDNT_LOCK_TREE_FOR_DELETE"></span><span id="error_ds_couldnt_lock_tree_for_delete"></span>**ERROR\_DS\_COULDNT\_LOCK\_TREE\_FOR\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-926">8502 (0x2136)</span><span class="sxs-lookup"><span data-stu-id="3ad11-926">8502 (0x2136)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-927">El servicio de directorio no pudo bloquear un árbol para preparar una eliminación de árbol porque el árbol estaba en uso.</span><span class="sxs-lookup"><span data-stu-id="3ad11-927">The directory service failed to lock a tree in preparation for a tree deletion because the tree was in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-928"><span id="ERROR_DS_COULDNT_IDENTIFY_OBJECTS_FOR_TREE_DELETE"></span><span id="error_ds_couldnt_identify_objects_for_tree_delete"></span>**ERROR \_ DS \_ COULDNT \_ identificar \_ objetos \_ para \_ la \_ eliminación de árbol**</span><span class="sxs-lookup"><span data-stu-id="3ad11-928"><span id="ERROR_DS_COULDNT_IDENTIFY_OBJECTS_FOR_TREE_DELETE"></span><span id="error_ds_couldnt_identify_objects_for_tree_delete"></span>**ERROR\_DS\_COULDNT\_IDENTIFY\_OBJECTS\_FOR\_TREE\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-929">8503 (0x2137)</span><span class="sxs-lookup"><span data-stu-id="3ad11-929">8503 (0x2137)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-930">El servicio de directorio no pudo identificar la lista de objetos que se van a eliminar al intentar una eliminación de árbol.</span><span class="sxs-lookup"><span data-stu-id="3ad11-930">The directory service failed to identify the list of objects to delete while attempting a tree deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-931"><span id="ERROR_DS_SAM_INIT_FAILURE"></span><span id="error_ds_sam_init_failure"></span>**ERROR de \_ DS de \_ \_ inicialización de Sam \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-931"><span id="ERROR_DS_SAM_INIT_FAILURE"></span><span id="error_ds_sam_init_failure"></span>**ERROR\_DS\_SAM\_INIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-932">8504 (0x2138)</span><span class="sxs-lookup"><span data-stu-id="3ad11-932">8504 (0x2138)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-933">No se pudo inicializar el administrador de cuentas de seguridad debido al siguiente error: %1.</span><span class="sxs-lookup"><span data-stu-id="3ad11-933">Security Accounts Manager initialization failed because of the following error: %1.</span></span> <span data-ttu-id="3ad11-934">Estado de error: 0x %2.</span><span class="sxs-lookup"><span data-stu-id="3ad11-934">Error Status: 0x%2.</span></span> <span data-ttu-id="3ad11-935">Apague este sistema y reinicie en Modo de restauración de servicios de directorio, compruebe el registro de eventos para obtener información más detallada.</span><span class="sxs-lookup"><span data-stu-id="3ad11-935">Please shutdown this system and reboot into Directory Services Restore Mode, check the event log for more detailed information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-936"><span id="ERROR_DS_SENSITIVE_GROUP_VIOLATION"></span><span id="error_ds_sensitive_group_violation"></span>**ERROR \_ de \_ \_ infracción de grupo sensible a DS \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-936"><span id="ERROR_DS_SENSITIVE_GROUP_VIOLATION"></span><span id="error_ds_sensitive_group_violation"></span>**ERROR\_DS\_SENSITIVE\_GROUP\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-937">8505 (0x2139)</span><span class="sxs-lookup"><span data-stu-id="3ad11-937">8505 (0x2139)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-938">Solo un administrador puede modificar la lista de miembros de un grupo administrativo.</span><span class="sxs-lookup"><span data-stu-id="3ad11-938">Only an administrator can modify the membership list of an administrative group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-939"><span id="ERROR_DS_CANT_MOD_PRIMARYGROUPID"></span><span id="error_ds_cant_mod_primarygroupid"></span>**ERROR DS no se pudo \_ \_ \_ mod \_ PRIMARYGROUPID**</span><span class="sxs-lookup"><span data-stu-id="3ad11-939"><span id="ERROR_DS_CANT_MOD_PRIMARYGROUPID"></span><span id="error_ds_cant_mod_primarygroupid"></span>**ERROR\_DS\_CANT\_MOD\_PRIMARYGROUPID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-940">8506 (0x213A)</span><span class="sxs-lookup"><span data-stu-id="3ad11-940">8506 (0x213A)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-941">No se puede cambiar el identificador de grupo principal de una cuenta de controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="3ad11-941">Cannot change the primary group ID of a domain controller account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-942"><span id="ERROR_DS_ILLEGAL_BASE_SCHEMA_MOD"></span><span id="error_ds_illegal_base_schema_mod"></span>**ERROR \_ de \_ \_ modificación de \_ esquema de base no válido de DS \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-942"><span id="ERROR_DS_ILLEGAL_BASE_SCHEMA_MOD"></span><span id="error_ds_illegal_base_schema_mod"></span>**ERROR\_DS\_ILLEGAL\_BASE\_SCHEMA\_MOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-943">8507 (0x213B)</span><span class="sxs-lookup"><span data-stu-id="3ad11-943">8507 (0x213B)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-944">Se ha intentado modificar el esquema base.</span><span class="sxs-lookup"><span data-stu-id="3ad11-944">An attempt is made to modify the base schema.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-945"><span id="ERROR_DS_NONSAFE_SCHEMA_CHANGE"></span><span id="error_ds_nonsafe_schema_change"></span>**ERROR \_ de \_ esquema no seguro de DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-945"><span id="ERROR_DS_NONSAFE_SCHEMA_CHANGE"></span><span id="error_ds_nonsafe_schema_change"></span>**ERROR\_DS\_NONSAFE\_SCHEMA\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-946">8508 (0x213C)</span><span class="sxs-lookup"><span data-stu-id="3ad11-946">8508 (0x213C)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-947">No se permite agregar un nuevo atributo obligatorio a una clase existente, eliminar un atributo obligatorio de una clase existente o agregar un atributo opcional a la clase especial superior que no es un atributo backlink (directamente o a través de la herencia, por ejemplo, mediante la adición o eliminación de una clase auxiliar).</span><span class="sxs-lookup"><span data-stu-id="3ad11-947">Adding a new mandatory attribute to an existing class, deleting a mandatory attribute from an existing class, or adding an optional attribute to the special class Top that is not a backlink attribute (directly or through inheritance, for example, by adding or deleting an auxiliary class) is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-948"><span id="ERROR_DS_SCHEMA_UPDATE_DISALLOWED"></span><span id="error_ds_schema_update_disallowed"></span>**ERROR: no se \_ permite la actualización del esquema de DS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-948"><span id="ERROR_DS_SCHEMA_UPDATE_DISALLOWED"></span><span id="error_ds_schema_update_disallowed"></span>**ERROR\_DS\_SCHEMA\_UPDATE\_DISALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-949">8509 (0x213D)</span><span class="sxs-lookup"><span data-stu-id="3ad11-949">8509 (0x213D)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-950">No se permite la actualización de esquemas en este controlador de dominio porque el controlador de dominio no es el propietario del rol FSMO del esquema.</span><span class="sxs-lookup"><span data-stu-id="3ad11-950">Schema update is not allowed on this DC because the DC is not the schema FSMO Role Owner.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-951"><span id="ERROR_DS_CANT_CREATE_UNDER_SCHEMA"></span><span id="error_ds_cant_create_under_schema"></span>**ERROR DS no se pudo \_ \_ \_ crear \_ en el \_ esquema**</span><span class="sxs-lookup"><span data-stu-id="3ad11-951"><span id="ERROR_DS_CANT_CREATE_UNDER_SCHEMA"></span><span id="error_ds_cant_create_under_schema"></span>**ERROR\_DS\_CANT\_CREATE\_UNDER\_SCHEMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-952">8510 (0x213E)</span><span class="sxs-lookup"><span data-stu-id="3ad11-952">8510 (0x213E)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-953">No se puede crear un objeto de esta clase en el contenedor de esquemas.</span><span class="sxs-lookup"><span data-stu-id="3ad11-953">An object of this class cannot be created under the schema container.</span></span> <span data-ttu-id="3ad11-954">En el contenedor de esquemas solo se pueden crear objetos Attribute-Schema y Class-Schema.</span><span class="sxs-lookup"><span data-stu-id="3ad11-954">You can only create attribute-schema and class-schema objects under the schema container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-955"><span id="ERROR_DS_INSTALL_NO_SRC_SCH_VERSION"></span><span id="error_ds_install_no_src_sch_version"></span>**ERROR \_ DS \_ \_ no instalar ninguna \_ versión de src \_ SCH \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-955"><span id="ERROR_DS_INSTALL_NO_SRC_SCH_VERSION"></span><span id="error_ds_install_no_src_sch_version"></span>**ERROR\_DS\_INSTALL\_NO\_SRC\_SCH\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-956">8511 (0x213F)</span><span class="sxs-lookup"><span data-stu-id="3ad11-956">8511 (0x213F)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-957">La instalación de la réplica o el elemento secundario no pudo obtener el atributo objectVersion en el contenedor de esquema en el controlador de dominio de origen.</span><span class="sxs-lookup"><span data-stu-id="3ad11-957">The replica/child install failed to get the objectVersion attribute on the schema container on the source DC.</span></span> <span data-ttu-id="3ad11-958">Falta el atributo en el contenedor de esquema o las credenciales proporcionadas no tienen permiso para leerlo.</span><span class="sxs-lookup"><span data-stu-id="3ad11-958">Either the attribute is missing on the schema container or the credentials supplied do not have permission to read it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-959"><span id="ERROR_DS_INSTALL_NO_SCH_VERSION_IN_INIFILE"></span><span id="error_ds_install_no_sch_version_in_inifile"></span>**ERROR \_ DS \_ instalar \_ no \_ \_ versión SCH \_ en \_ INIFILE**</span><span class="sxs-lookup"><span data-stu-id="3ad11-959"><span id="ERROR_DS_INSTALL_NO_SCH_VERSION_IN_INIFILE"></span><span id="error_ds_install_no_sch_version_in_inifile"></span>**ERROR\_DS\_INSTALL\_NO\_SCH\_VERSION\_IN\_INIFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-960">8512 (0x2140)</span><span class="sxs-lookup"><span data-stu-id="3ad11-960">8512 (0x2140)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-961">La instalación de la réplica o el elemento secundario no pudo leer el atributo objectVersion en la sección SCHEMA del archivo schema.ini en el directorio system32.</span><span class="sxs-lookup"><span data-stu-id="3ad11-961">The replica/child install failed to read the objectVersion attribute in the SCHEMA section of the file schema.ini in the system32 directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-962"><span id="ERROR_DS_INVALID_GROUP_TYPE"></span><span id="error_ds_invalid_group_type"></span>**ERROR \_ DS \_ \_ tipo de grupo no válido \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-962"><span id="ERROR_DS_INVALID_GROUP_TYPE"></span><span id="error_ds_invalid_group_type"></span>**ERROR\_DS\_INVALID\_GROUP\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-963">8513 (0x2141)</span><span class="sxs-lookup"><span data-stu-id="3ad11-963">8513 (0x2141)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-964">El tipo de grupo especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="3ad11-964">The specified group type is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-965"><span id="ERROR_DS_NO_NEST_GLOBALGROUP_IN_MIXEDDOMAIN"></span><span id="error_ds_no_nest_globalgroup_in_mixeddomain"></span>**ERROR \_ DS \_ no \_ anidado \_ GLOBALGROUP \_ en \_ MIXEDDOMAIN**</span><span class="sxs-lookup"><span data-stu-id="3ad11-965"><span id="ERROR_DS_NO_NEST_GLOBALGROUP_IN_MIXEDDOMAIN"></span><span id="error_ds_no_nest_globalgroup_in_mixeddomain"></span>**ERROR\_DS\_NO\_NEST\_GLOBALGROUP\_IN\_MIXEDDOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-966">8514 (0x2142)</span><span class="sxs-lookup"><span data-stu-id="3ad11-966">8514 (0x2142)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-967">No se pueden anidar grupos globales en un dominio mixto si el grupo tiene habilitada la seguridad.</span><span class="sxs-lookup"><span data-stu-id="3ad11-967">You cannot nest global groups in a mixed domain if the group is security-enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-968"><span id="ERROR_DS_NO_NEST_LOCALGROUP_IN_MIXEDDOMAIN"></span><span id="error_ds_no_nest_localgroup_in_mixeddomain"></span>**ERROR \_ DS \_ no \_ anidar el \_ LOCALGROUP \_ en \_ MIXEDDOMAIN**</span><span class="sxs-lookup"><span data-stu-id="3ad11-968"><span id="ERROR_DS_NO_NEST_LOCALGROUP_IN_MIXEDDOMAIN"></span><span id="error_ds_no_nest_localgroup_in_mixeddomain"></span>**ERROR\_DS\_NO\_NEST\_LOCALGROUP\_IN\_MIXEDDOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-969">8515 (0x2143)</span><span class="sxs-lookup"><span data-stu-id="3ad11-969">8515 (0x2143)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-970">No se pueden anidar grupos locales en un dominio mixto si el grupo tiene habilitada la seguridad.</span><span class="sxs-lookup"><span data-stu-id="3ad11-970">You cannot nest local groups in a mixed domain if the group is security-enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-971"><span id="ERROR_DS_GLOBAL_CANT_HAVE_LOCAL_MEMBER"></span><span id="error_ds_global_cant_have_local_member"></span>**ERROR \_ DS \_ global no se \_ \_ tiene \_ \_ miembro local**</span><span class="sxs-lookup"><span data-stu-id="3ad11-971"><span id="ERROR_DS_GLOBAL_CANT_HAVE_LOCAL_MEMBER"></span><span id="error_ds_global_cant_have_local_member"></span>**ERROR\_DS\_GLOBAL\_CANT\_HAVE\_LOCAL\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-972">8516 (0x2144)</span><span class="sxs-lookup"><span data-stu-id="3ad11-972">8516 (0x2144)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-973">Un grupo global no puede tener un grupo local como miembro.</span><span class="sxs-lookup"><span data-stu-id="3ad11-973">A global group cannot have a local group as a member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-974"><span id="ERROR_DS_GLOBAL_CANT_HAVE_UNIVERSAL_MEMBER"></span><span id="error_ds_global_cant_have_universal_member"></span>**ERROR \_ DS \_ global no se \_ \_ tiene \_ \_ miembro universal**</span><span class="sxs-lookup"><span data-stu-id="3ad11-974"><span id="ERROR_DS_GLOBAL_CANT_HAVE_UNIVERSAL_MEMBER"></span><span id="error_ds_global_cant_have_universal_member"></span>**ERROR\_DS\_GLOBAL\_CANT\_HAVE\_UNIVERSAL\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-975">8517 (0x2145)</span><span class="sxs-lookup"><span data-stu-id="3ad11-975">8517 (0x2145)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-976">Un grupo global no puede tener un grupo universal como miembro.</span><span class="sxs-lookup"><span data-stu-id="3ad11-976">A global group cannot have a universal group as a member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-977"><span id="ERROR_DS_UNIVERSAL_CANT_HAVE_LOCAL_MEMBER"></span><span id="error_ds_universal_cant_have_local_member"></span>**ERROR \_ DS \_ universal \_ peralte \_ tiene \_ \_ miembro local**</span><span class="sxs-lookup"><span data-stu-id="3ad11-977"><span id="ERROR_DS_UNIVERSAL_CANT_HAVE_LOCAL_MEMBER"></span><span id="error_ds_universal_cant_have_local_member"></span>**ERROR\_DS\_UNIVERSAL\_CANT\_HAVE\_LOCAL\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-978">8518 (0x2146)</span><span class="sxs-lookup"><span data-stu-id="3ad11-978">8518 (0x2146)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-979">Un grupo universal no puede tener un grupo local como miembro.</span><span class="sxs-lookup"><span data-stu-id="3ad11-979">A universal group cannot have a local group as a member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-980"><span id="ERROR_DS_GLOBAL_CANT_HAVE_CROSSDOMAIN_MEMBER"></span><span id="error_ds_global_cant_have_crossdomain_member"></span>**ERROR \_ DS \_ global no se \_ \_ tiene \_ miembro de CROSSDOMAIN \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-980"><span id="ERROR_DS_GLOBAL_CANT_HAVE_CROSSDOMAIN_MEMBER"></span><span id="error_ds_global_cant_have_crossdomain_member"></span>**ERROR\_DS\_GLOBAL\_CANT\_HAVE\_CROSSDOMAIN\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-981">8519 (0x2147)</span><span class="sxs-lookup"><span data-stu-id="3ad11-981">8519 (0x2147)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-982">Un grupo global no puede tener un miembro entre dominios.</span><span class="sxs-lookup"><span data-stu-id="3ad11-982">A global group cannot have a cross-domain member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-983"><span id="ERROR_DS_LOCAL_CANT_HAVE_CROSSDOMAIN_LOCAL_MEMBER"></span><span id="error_ds_local_cant_have_crossdomain_local_member"></span>**ERROR \_ DS \_ local no se tiene un \_ \_ \_ \_ miembro local de CROSSDOMAIN \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-983"><span id="ERROR_DS_LOCAL_CANT_HAVE_CROSSDOMAIN_LOCAL_MEMBER"></span><span id="error_ds_local_cant_have_crossdomain_local_member"></span>**ERROR\_DS\_LOCAL\_CANT\_HAVE\_CROSSDOMAIN\_LOCAL\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-984">8520 (0x2148)</span><span class="sxs-lookup"><span data-stu-id="3ad11-984">8520 (0x2148)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-985">Un grupo local no puede tener otro grupo local entre dominios como miembro.</span><span class="sxs-lookup"><span data-stu-id="3ad11-985">A local group cannot have another cross domain local group as a member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-986"><span id="ERROR_DS_HAVE_PRIMARY_MEMBERS"></span><span id="error_ds_have_primary_members"></span>**el \_ error \_ DS \_ tiene \_ miembros principales**</span><span class="sxs-lookup"><span data-stu-id="3ad11-986"><span id="ERROR_DS_HAVE_PRIMARY_MEMBERS"></span><span id="error_ds_have_primary_members"></span>**ERROR\_DS\_HAVE\_PRIMARY\_MEMBERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-987">8521 (0x2149)</span><span class="sxs-lookup"><span data-stu-id="3ad11-987">8521 (0x2149)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-988">Un grupo con miembros principales no puede cambiar a un grupo deshabilitado para la seguridad.</span><span class="sxs-lookup"><span data-stu-id="3ad11-988">A group with primary members cannot change to a security-disabled group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-989"><span id="ERROR_DS_STRING_SD_CONVERSION_FAILED"></span><span id="error_ds_string_sd_conversion_failed"></span>**ERROR en la \_ \_ \_ \_ conversión SD \_ de la cadena DS**</span><span class="sxs-lookup"><span data-stu-id="3ad11-989"><span id="ERROR_DS_STRING_SD_CONVERSION_FAILED"></span><span id="error_ds_string_sd_conversion_failed"></span>**ERROR\_DS\_STRING\_SD\_CONVERSION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-990">8522 (0x214A)</span><span class="sxs-lookup"><span data-stu-id="3ad11-990">8522 (0x214A)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-991">La carga de la caché de esquema no pudo convertir el SD predeterminado de la cadena en un objeto de esquema de clase.</span><span class="sxs-lookup"><span data-stu-id="3ad11-991">The schema cache load failed to convert the string default SD on a class-schema object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-992"><span id="ERROR_DS_NAMING_MASTER_GC"></span><span id="error_ds_naming_master_gc"></span>**ERROR \_ DS de \_ nomenclatura del \_ \_ GC maestro**</span><span class="sxs-lookup"><span data-stu-id="3ad11-992"><span id="ERROR_DS_NAMING_MASTER_GC"></span><span id="error_ds_naming_master_gc"></span>**ERROR\_DS\_NAMING\_MASTER\_GC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-993">8523 (0x214B)</span><span class="sxs-lookup"><span data-stu-id="3ad11-993">8523 (0x214B)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-994">Solo se debe permitir que los DSA configurados como servidores de catálogo global contengan el rol FSMO del maestro de nomenclatura de dominios.</span><span class="sxs-lookup"><span data-stu-id="3ad11-994">Only DSAs configured to be Global Catalog servers should be allowed to hold the Domain Naming Master FSMO role.</span></span> <span data-ttu-id="3ad11-995">(Sólo se aplica a los servidores de Windows 2000).</span><span class="sxs-lookup"><span data-stu-id="3ad11-995">(Applies only to Windows 2000 servers.)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-996"><span id="ERROR_DS_DNS_LOOKUP_FAILURE"></span><span id="error_ds_dns_lookup_failure"></span>**ERROR \_ de \_ búsqueda de DNS de DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-996"><span id="ERROR_DS_DNS_LOOKUP_FAILURE"></span><span id="error_ds_dns_lookup_failure"></span>**ERROR\_DS\_DNS\_LOOKUP\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-997">8524 (0x214C)</span><span class="sxs-lookup"><span data-stu-id="3ad11-997">8524 (0x214C)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-998">La operación DSA no puede continuar debido a un error de búsqueda DNS.</span><span class="sxs-lookup"><span data-stu-id="3ad11-998">The DSA operation is unable to proceed because of a DNS lookup failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-999"><span id="ERROR_DS_COULDNT_UPDATE_SPNS"></span><span id="error_ds_couldnt_update_spns"></span>**SPN de ERROR de \_ \_ COULDNT de \_ actualización de DS \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-999"><span id="ERROR_DS_COULDNT_UPDATE_SPNS"></span><span id="error_ds_couldnt_update_spns"></span>**ERROR\_DS\_COULDNT\_UPDATE\_SPNS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1000">8525 (0x214D)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1000">8525 (0x214D)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1001">Al procesar un cambio en el nombre de host DNS de un objeto, los valores de nombre de entidad de seguridad de servicio no se pueden mantener sincronizados.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1001">While processing a change to the DNS Host Name for an object, the Service Principal Name values could not be kept in sync.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1002"><span id="ERROR_DS_CANT_RETRIEVE_SD"></span><span id="error_ds_cant_retrieve_sd"></span>**ERROR DS no se pudo \_ \_ \_ recuperar \_ SD**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1002"><span id="ERROR_DS_CANT_RETRIEVE_SD"></span><span id="error_ds_cant_retrieve_sd"></span>**ERROR\_DS\_CANT\_RETRIEVE\_SD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1003">8526 (0x214E)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1003">8526 (0x214E)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1004">No se pudo leer el atributo de descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1004">The Security Descriptor attribute could not be read.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1005"><span id="ERROR_DS_KEY_NOT_UNIQUE"></span><span id="error_ds_key_not_unique"></span>**ERROR de la \_ \_ clave DS no es \_ \_ única**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1005"><span id="ERROR_DS_KEY_NOT_UNIQUE"></span><span id="error_ds_key_not_unique"></span>**ERROR\_DS\_KEY\_NOT\_UNIQUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1006">8527 (0x214F)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1006">8527 (0x214F)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1007">No se encontró el objeto solicitado, pero se encontró un objeto con esa clave.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1007">The object requested was not found, but an object with that key was found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1008"><span id="ERROR_DS_WRONG_LINKED_ATT_SYNTAX"></span><span id="error_ds_wrong_linked_att_syntax"></span>**ERROR \_ de \_ DS \_ \_ Sintaxis de ATT vinculada incorrecta \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1008"><span id="ERROR_DS_WRONG_LINKED_ATT_SYNTAX"></span><span id="error_ds_wrong_linked_att_syntax"></span>**ERROR\_DS\_WRONG\_LINKED\_ATT\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1009">8528 (0x2150)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1009">8528 (0x2150)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1010">La sintaxis del atributo vinculado que se va a agregar es incorrecta.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1010">The syntax of the linked attribute being added is incorrect.</span></span> <span data-ttu-id="3ad11-1011">Los vínculos hacia delante solo pueden tener la sintaxis 2.5.5.1, 2.5.5.7 y 2.5.5.14, y los vínculos posteriores solo pueden tener la sintaxis 2.5.5.1.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1011">Forward links can only have syntax 2.5.5.1, 2.5.5.7, and 2.5.5.14, and backlinks can only have syntax 2.5.5.1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1012"><span id="ERROR_DS_SAM_NEED_BOOTKEY_PASSWORD"></span><span id="error_ds_sam_need_bootkey_password"></span>**ERROR \_ DS \_ Sam \_ necesito \_ BOOTKEY \_ contraseña**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1012"><span id="ERROR_DS_SAM_NEED_BOOTKEY_PASSWORD"></span><span id="error_ds_sam_need_bootkey_password"></span>**ERROR\_DS\_SAM\_NEED\_BOOTKEY\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1013">8529 (0x2151)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1013">8529 (0x2151)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1014">El administrador de cuentas de seguridad debe obtener la contraseña de arranque.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1014">Security Account Manager needs to get the boot password.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1015"><span id="ERROR_DS_SAM_NEED_BOOTKEY_FLOPPY"></span><span id="error_ds_sam_need_bootkey_floppy"></span>**ERROR \_ DS \_ Sam \_ necesito \_ \_ disquete BOOTKEY**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1015"><span id="ERROR_DS_SAM_NEED_BOOTKEY_FLOPPY"></span><span id="error_ds_sam_need_bootkey_floppy"></span>**ERROR\_DS\_SAM\_NEED\_BOOTKEY\_FLOPPY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1016">8530 (0x2152)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1016">8530 (0x2152)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1017">El administrador de cuentas de seguridad debe obtener la clave de arranque desde el disquete.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1017">Security Account Manager needs to get the boot key from floppy disk.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1018"><span id="ERROR_DS_CANT_START"></span><span id="error_ds_cant_start"></span>**ERROR DS no se pudo \_ \_ \_ iniciar**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1018"><span id="ERROR_DS_CANT_START"></span><span id="error_ds_cant_start"></span>**ERROR\_DS\_CANT\_START**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1019">8531 (0x2153)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1019">8531 (0x2153)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1020">No se puede iniciar el servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1020">Directory Service cannot start.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1021"><span id="ERROR_DS_INIT_FAILURE"></span><span id="error_ds_init_failure"></span>**ERROR \_ de \_ inicialización de DS \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1021"><span id="ERROR_DS_INIT_FAILURE"></span><span id="error_ds_init_failure"></span>**ERROR\_DS\_INIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1022">8532 (0x2154)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1022">8532 (0x2154)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1023">No se pudieron iniciar los servicios de directorio.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1023">Directory Services could not start.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1024"><span id="ERROR_DS_NO_PKT_PRIVACY_ON_CONNECTION"></span><span id="error_ds_no_pkt_privacy_on_connection"></span>**ERROR \_ \_ de DS \_ sin \_ Privacidad \_ en la \_ conexión**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1024"><span id="ERROR_DS_NO_PKT_PRIVACY_ON_CONNECTION"></span><span id="error_ds_no_pkt_privacy_on_connection"></span>**ERROR\_DS\_NO\_PKT\_PRIVACY\_ON\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1025">8533 (0x2155)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1025">8533 (0x2155)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1026">La conexión entre el cliente y el servidor requiere privacidad del paquete o mejor.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1026">The connection between client and server requires packet privacy or better.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1027"><span id="ERROR_DS_SOURCE_DOMAIN_IN_FOREST"></span><span id="error_ds_source_domain_in_forest"></span>**ERROR \_ \_ \_ de dominio de origen DS \_ en el \_ bosque**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1027"><span id="ERROR_DS_SOURCE_DOMAIN_IN_FOREST"></span><span id="error_ds_source_domain_in_forest"></span>**ERROR\_DS\_SOURCE\_DOMAIN\_IN\_FOREST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1028">8534 (0x2156)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1028">8534 (0x2156)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1029">Es posible que el dominio de origen no esté en el mismo bosque que el destino.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1029">The source domain may not be in the same forest as destination.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1030"><span id="ERROR_DS_DESTINATION_DOMAIN_NOT_IN_FOREST"></span><span id="error_ds_destination_domain_not_in_forest"></span>**ERROR \_ el \_ \_ dominio de destino DS no está en el \_ \_ \_ bosque**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1030"><span id="ERROR_DS_DESTINATION_DOMAIN_NOT_IN_FOREST"></span><span id="error_ds_destination_domain_not_in_forest"></span>**ERROR\_DS\_DESTINATION\_DOMAIN\_NOT\_IN\_FOREST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1031">8535 (0x2157)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1031">8535 (0x2157)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1032">El dominio de destino debe estar en el bosque.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1032">The destination domain must be in the forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1033"><span id="ERROR_DS_DESTINATION_AUDITING_NOT_ENABLED"></span><span id="error_ds_destination_auditing_not_enabled"></span>**ERROR de \_ Auditoría de destino de DS \_ \_ \_ no \_ habilitada**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1033"><span id="ERROR_DS_DESTINATION_AUDITING_NOT_ENABLED"></span><span id="error_ds_destination_auditing_not_enabled"></span>**ERROR\_DS\_DESTINATION\_AUDITING\_NOT\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1034">8536 (0x2158)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1034">8536 (0x2158)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1035">La operación requiere que esté habilitada la auditoría de dominio de destino.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1035">The operation requires that destination domain auditing be enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1036"><span id="ERROR_DS_CANT_FIND_DC_FOR_SRC_DOMAIN"></span><span id="error_ds_cant_find_dc_for_src_domain"></span>**ERROR \_ DS no se \_ encuentra el \_ \_ controlador \_ de dominio para el \_ \_ dominio src**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1036"><span id="ERROR_DS_CANT_FIND_DC_FOR_SRC_DOMAIN"></span><span id="error_ds_cant_find_dc_for_src_domain"></span>**ERROR\_DS\_CANT\_FIND\_DC\_FOR\_SRC\_DOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1037">8537 (0x2159)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1037">8537 (0x2159)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1038">La operación no pudo encontrar un DC para el dominio de origen.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1038">The operation couldn't locate a DC for the source domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1039"><span id="ERROR_DS_SRC_OBJ_NOT_GROUP_OR_USER"></span><span id="error_ds_src_obj_not_group_or_user"></span>**ERROR \_ DS \_ src \_ obj \_ not \_ Group \_ or \_ User**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1039"><span id="ERROR_DS_SRC_OBJ_NOT_GROUP_OR_USER"></span><span id="error_ds_src_obj_not_group_or_user"></span>**ERROR\_DS\_SRC\_OBJ\_NOT\_GROUP\_OR\_USER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1040">8538 (0x215A)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1040">8538 (0x215A)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1041">El objeto de origen debe ser un grupo o un usuario.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1041">The source object must be a group or user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1042"><span id="ERROR_DS_SRC_SID_EXISTS_IN_FOREST"></span><span id="error_ds_src_sid_exists_in_forest"></span>**ERROR \_ DS \_ src \_ SID \_ exist \_ in \_ Forest**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1042"><span id="ERROR_DS_SRC_SID_EXISTS_IN_FOREST"></span><span id="error_ds_src_sid_exists_in_forest"></span>**ERROR\_DS\_SRC\_SID\_EXISTS\_IN\_FOREST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1043">8539 (0x215B)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1043">8539 (0x215B)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1044">El SID del objeto de origen ya existe en el bosque de destino.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1044">The source object's SID already exists in destination forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1045"><span id="ERROR_DS_SRC_AND_DST_OBJECT_CLASS_MISMATCH"></span><span id="error_ds_src_and_dst_object_class_mismatch"></span>**ERROR \_ DS \_ src \_ y \_ la \_ clase de objeto DST \_ \_ no coinciden**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1045"><span id="ERROR_DS_SRC_AND_DST_OBJECT_CLASS_MISMATCH"></span><span id="error_ds_src_and_dst_object_class_mismatch"></span>**ERROR\_DS\_SRC\_AND\_DST\_OBJECT\_CLASS\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1046">8540 (0x215C)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1046">8540 (0x215C)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1047">El objeto de origen y el de destino deben ser del mismo tipo.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1047">The source and destination object must be of the same type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1048"><span id="ERROR_SAM_INIT_FAILURE"></span><span id="error_sam_init_failure"></span>**ERROR \_ Sam \_ init \_ error**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1048"><span id="ERROR_SAM_INIT_FAILURE"></span><span id="error_sam_init_failure"></span>**ERROR\_SAM\_INIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1049">8541 (0x215D)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1049">8541 (0x215D)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1050">No se pudo inicializar el administrador de cuentas de seguridad debido al siguiente error: %1.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1050">Security Accounts Manager initialization failed because of the following error: %1.</span></span> <span data-ttu-id="3ad11-1051">Estado de error: 0x %2.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1051">Error Status: 0x%2.</span></span> <span data-ttu-id="3ad11-1052">Haga clic en Aceptar para apagar el sistema y reiniciar en modo seguro.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1052">Click OK to shut down the system and reboot into Safe Mode.</span></span> <span data-ttu-id="3ad11-1053">Compruebe el registro de eventos para obtener información detallada.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1053">Check the event log for detailed information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1054"><span id="ERROR_DS_DRA_SCHEMA_INFO_SHIP"></span><span id="error_ds_dra_schema_info_ship"></span>**ERROR \_ de \_ \_ envío de \_ información de esquema \_ de DS Dra**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1054"><span id="ERROR_DS_DRA_SCHEMA_INFO_SHIP"></span><span id="error_ds_dra_schema_info_ship"></span>**ERROR\_DS\_DRA\_SCHEMA\_INFO\_SHIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1055">8542 (0x215E)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1055">8542 (0x215E)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1056">No se pudo incluir la información de esquema en la solicitud de replicación.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1056">Schema information could not be included in the replication request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1057"><span id="ERROR_DS_DRA_SCHEMA_CONFLICT"></span><span id="error_ds_dra_schema_conflict"></span>**\_conflicto de esquema de DS Dra de error \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1057"><span id="ERROR_DS_DRA_SCHEMA_CONFLICT"></span><span id="error_ds_dra_schema_conflict"></span>**ERROR\_DS\_DRA\_SCHEMA\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1058">8543 (0x215F)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1058">8543 (0x215F)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1059">No se pudo completar la operación de replicación debido a una incompatibilidad de esquemas.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1059">The replication operation could not be completed due to a schema incompatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1060"><span id="ERROR_DS_DRA_EARLIER_SCHEMA_CONFLICT"></span><span id="error_ds_dra_earlier_schema_conflict"></span>**\_conflicto de \_ \_ \_ esquemas Dra \_ anteriores de error de DS**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1060"><span id="ERROR_DS_DRA_EARLIER_SCHEMA_CONFLICT"></span><span id="error_ds_dra_earlier_schema_conflict"></span>**ERROR\_DS\_DRA\_EARLIER\_SCHEMA\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1061">8544 (0x2160)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1061">8544 (0x2160)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1062">No se pudo completar la operación de replicación debido a una incompatibilidad de esquema anterior.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1062">The replication operation could not be completed due to a previous schema incompatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1063"><span id="ERROR_DS_DRA_OBJ_NC_MISMATCH"></span><span id="error_ds_dra_obj_nc_mismatch"></span>**ERROR de \_ DS. \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1063"><span id="ERROR_DS_DRA_OBJ_NC_MISMATCH"></span><span id="error_ds_dra_obj_nc_mismatch"></span>**ERROR\_DS\_DRA\_OBJ\_NC\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1064">8545 (0x2161)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1064">8545 (0x2161)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1065">No se pudo aplicar la actualización de replicación porque el origen o el destino no han recibido todavía información relacionada con una operación de movimiento entre dominios reciente.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1065">The replication update could not be applied because either the source or the destination has not yet received information regarding a recent cross-domain move operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1066"><span id="ERROR_DS_NC_STILL_HAS_DSAS"></span><span id="error_ds_nc_still_has_dsas"></span>**el \_ NC DS de error \_ \_ sigue teniendo \_ \_ DSA**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1066"><span id="ERROR_DS_NC_STILL_HAS_DSAS"></span><span id="error_ds_nc_still_has_dsas"></span>**ERROR\_DS\_NC\_STILL\_HAS\_DSAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1067">8546 (0x2162)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1067">8546 (0x2162)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1068">No se pudo eliminar el dominio solicitado porque existen controladores de dominio que todavía hospedan este dominio.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1068">The requested domain could not be deleted because there exist domain controllers that still host this domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1069"><span id="ERROR_DS_GC_REQUIRED"></span><span id="error_ds_gc_required"></span>**ERROR \_ DS \_ GC \_ requerido**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1069"><span id="ERROR_DS_GC_REQUIRED"></span><span id="error_ds_gc_required"></span>**ERROR\_DS\_GC\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1070">8547 (0x2163)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1070">8547 (0x2163)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1071">La operación solicitada solo se puede realizar en un servidor de catálogo global.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1071">The requested operation can be performed only on a global catalog server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1072"><span id="ERROR_DS_LOCAL_MEMBER_OF_LOCAL_ONLY"></span><span id="error_ds_local_member_of_local_only"></span>**ERROR \_ DS \_ local \_ miembro \_ de \_ \_ solo local**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1072"><span id="ERROR_DS_LOCAL_MEMBER_OF_LOCAL_ONLY"></span><span id="error_ds_local_member_of_local_only"></span>**ERROR\_DS\_LOCAL\_MEMBER\_OF\_LOCAL\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1073">8548 (0x2164)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1073">8548 (0x2164)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1074">Un grupo local solo puede ser miembro de otros grupos locales del mismo dominio.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1074">A local group can only be a member of other local groups in the same domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1075"><span id="ERROR_DS_NO_FPO_IN_UNIVERSAL_GROUPS"></span><span id="error_ds_no_fpo_in_universal_groups"></span>**ERROR \_ DS \_ no \_ FPO \_ en \_ grupos universales \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1075"><span id="ERROR_DS_NO_FPO_IN_UNIVERSAL_GROUPS"></span><span id="error_ds_no_fpo_in_universal_groups"></span>**ERROR\_DS\_NO\_FPO\_IN\_UNIVERSAL\_GROUPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1076">8549 (0x2165)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1076">8549 (0x2165)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1077">Las entidades de seguridad externas no pueden ser miembros de grupos universales.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1077">Foreign security principals cannot be members of universal groups.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1078"><span id="ERROR_DS_CANT_ADD_TO_GC"></span><span id="error_ds_cant_add_to_gc"></span>**ERROR \_ DS \_ no \_ se pudo agregar \_ al \_ GC**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1078"><span id="ERROR_DS_CANT_ADD_TO_GC"></span><span id="error_ds_cant_add_to_gc"></span>**ERROR\_DS\_CANT\_ADD\_TO\_GC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1079">8550 (0x2166)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1079">8550 (0x2166)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1080">El atributo no se puede replicar en el GC por motivos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1080">The attribute is not allowed to be replicated to the GC because of security reasons.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1081"><span id="ERROR_DS_NO_CHECKPOINT_WITH_PDC"></span><span id="error_ds_no_checkpoint_with_pdc"></span>**ERROR \_ DS \_ no \_ Checkpoint \_ con \_ PDC**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1081"><span id="ERROR_DS_NO_CHECKPOINT_WITH_PDC"></span><span id="error_ds_no_checkpoint_with_pdc"></span>**ERROR\_DS\_NO\_CHECKPOINT\_WITH\_PDC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1082">8551 (0x2167)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1082">8551 (0x2167)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1083">No se pudo realizar el punto de control con el PDC porque actualmente se están procesando demasiadas modificaciones.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1083">The checkpoint with the PDC could not be taken because there too many modifications being processed currently.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1084"><span id="ERROR_DS_SOURCE_AUDITING_NOT_ENABLED"></span><span id="error_ds_source_auditing_not_enabled"></span>**ERROR de \_ Auditoría de origen de DS \_ \_ \_ no \_ habilitada**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1084"><span id="ERROR_DS_SOURCE_AUDITING_NOT_ENABLED"></span><span id="error_ds_source_auditing_not_enabled"></span>**ERROR\_DS\_SOURCE\_AUDITING\_NOT\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1085">8552 (0x2168)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1085">8552 (0x2168)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1086">La operación requiere que esté habilitada la auditoría de dominio de origen.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1086">The operation requires that source domain auditing be enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1087"><span id="ERROR_DS_CANT_CREATE_IN_NONDOMAIN_NC"></span><span id="error_ds_cant_create_in_nondomain_nc"></span>**ERROR DS no se pudo \_ \_ \_ crear \_ en el NC del no \_ dominio \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1087"><span id="ERROR_DS_CANT_CREATE_IN_NONDOMAIN_NC"></span><span id="error_ds_cant_create_in_nondomain_nc"></span>**ERROR\_DS\_CANT\_CREATE\_IN\_NONDOMAIN\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1088">8553 (0x2169)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1088">8553 (0x2169)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1089">Los objetos de entidad de seguridad solo se pueden crear dentro de los contextos de nomenclatura de dominio.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1089">Security principal objects can only be created inside domain naming contexts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1090"><span id="ERROR_DS_INVALID_NAME_FOR_SPN"></span><span id="error_ds_invalid_name_for_spn"></span>**ERROR \_ DS \_ nombre no válido \_ \_ para el \_ SPN**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1090"><span id="ERROR_DS_INVALID_NAME_FOR_SPN"></span><span id="error_ds_invalid_name_for_spn"></span>**ERROR\_DS\_INVALID\_NAME\_FOR\_SPN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1091">8554 (0x216A)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1091">8554 (0x216A)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1092">No se pudo construir un nombre principal de servicio (SPN) porque el nombre de host proporcionado no tiene el formato necesario.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1092">A Service Principal Name (SPN) could not be constructed because the provided hostname is not in the necessary format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1093"><span id="ERROR_DS_FILTER_USES_CONTRUCTED_ATTRS"></span><span id="error_ds_filter_uses_contructed_attrs"></span>**el \_ filtro DS de error \_ \_ utiliza \_ construye \_ attrs**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1093"><span id="ERROR_DS_FILTER_USES_CONTRUCTED_ATTRS"></span><span id="error_ds_filter_uses_contructed_attrs"></span>**ERROR\_DS\_FILTER\_USES\_CONTRUCTED\_ATTRS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1094">8555 (0x216B)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1094">8555 (0x216B)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1095">Se pasó un filtro que utiliza atributos construidos.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1095">A Filter was passed that uses constructed attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1096"><span id="ERROR_DS_UNICODEPWD_NOT_IN_QUOTES"></span><span id="error_ds_unicodepwd_not_in_quotes"></span>**ERROR \_ DS \_ UNICODEPWD \_ no \_ entre \_ comillas**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1096"><span id="ERROR_DS_UNICODEPWD_NOT_IN_QUOTES"></span><span id="error_ds_unicodepwd_not_in_quotes"></span>**ERROR\_DS\_UNICODEPWD\_NOT\_IN\_QUOTES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1097">8556 (0x216C)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1097">8556 (0x216C)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1098">El valor del atributo unicodePwd debe ir entre comillas dobles.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1098">The unicodePwd attribute value must be enclosed in double quotes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1099"><span id="ERROR_DS_MACHINE_ACCOUNT_QUOTA_EXCEEDED"></span><span id="error_ds_machine_account_quota_exceeded"></span>**ERROR al superar la cuota de la \_ cuenta del \_ equipo DS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1099"><span id="ERROR_DS_MACHINE_ACCOUNT_QUOTA_EXCEEDED"></span><span id="error_ds_machine_account_quota_exceeded"></span>**ERROR\_DS\_MACHINE\_ACCOUNT\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1100">8557 (0x216D)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1100">8557 (0x216D)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1101">No se pudo unir el equipo al dominio.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1101">Your computer could not be joined to the domain.</span></span> <span data-ttu-id="3ad11-1102">Ha superado el número máximo de cuentas de equipo que se permite crear en este dominio.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1102">You have exceeded the maximum number of computer accounts you are allowed to create in this domain.</span></span> <span data-ttu-id="3ad11-1103">Póngase en contacto con el administrador del sistema para que este límite se restablezca o aumente.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1103">Contact your system administrator to have this limit reset or increased.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1104"><span id="ERROR_DS_MUST_BE_RUN_ON_DST_DC"></span><span id="error_ds_must_be_run_on_dst_dc"></span>**el \_ error \_ DS \_ debe \_ ejecutarse \_ en el \_ controlador de dominio de DST \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1104"><span id="ERROR_DS_MUST_BE_RUN_ON_DST_DC"></span><span id="error_ds_must_be_run_on_dst_dc"></span>**ERROR\_DS\_MUST\_BE\_RUN\_ON\_DST\_DC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1105">8558 (0x216E)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1105">8558 (0x216E)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1106">Por motivos de seguridad, la operación se debe ejecutar en el controlador de dominio de destino.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1106">For security reasons, the operation must be run on the destination DC.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1107"><span id="ERROR_DS_SRC_DC_MUST_BE_SP4_OR_GREATER"></span><span id="error_ds_src_dc_must_be_sp4_or_greater"></span>**ERROR \_ DS \_ src \_ DC \_ debe \_ ser \_ SP4 \_ o \_ superior**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1107"><span id="ERROR_DS_SRC_DC_MUST_BE_SP4_OR_GREATER"></span><span id="error_ds_src_dc_must_be_sp4_or_greater"></span>**ERROR\_DS\_SRC\_DC\_MUST\_BE\_SP4\_OR\_GREATER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1108">8559 (0x216F)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1108">8559 (0x216F)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1109">Por motivos de seguridad, el controlador de dominio de origen debe ser NT4SP4 o superior.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1109">For security reasons, the source DC must be NT4SP4 or greater.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1110"><span id="ERROR_DS_CANT_TREE_DELETE_CRITICAL_OBJ"></span><span id="error_ds_cant_tree_delete_critical_obj"></span>**ERROR DS no se pudo \_ \_ eliminar el \_ árbol \_ \_ imprescindible \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1110"><span id="ERROR_DS_CANT_TREE_DELETE_CRITICAL_OBJ"></span><span id="error_ds_cant_tree_delete_critical_obj"></span>**ERROR\_DS\_CANT\_TREE\_DELETE\_CRITICAL\_OBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1111">8560 (0x2170)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1111">8560 (0x2170)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1112">No se pueden eliminar objetos críticos del sistema de servicios de directorio durante las operaciones de eliminación de árboles.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1112">Critical Directory Service System objects cannot be deleted during tree delete operations.</span></span> <span data-ttu-id="3ad11-1113">Es posible que se haya realizado parcialmente la eliminación de árboles.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1113">The tree delete may have been partially performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1114"><span id="ERROR_DS_INIT_FAILURE_CONSOLE"></span><span id="error_ds_init_failure_console"></span>**ERROR en la consola de error de \_ DS \_ init \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1114"><span id="ERROR_DS_INIT_FAILURE_CONSOLE"></span><span id="error_ds_init_failure_console"></span>**ERROR\_DS\_INIT\_FAILURE\_CONSOLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1115">8561 (0x2171)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1115">8561 (0x2171)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1116">No se pudieron iniciar los servicios de directorio debido al siguiente error: %1.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1116">Directory Services could not start because of the following error: %1.</span></span> <span data-ttu-id="3ad11-1117">Estado de error: 0x %2.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1117">Error Status: 0x%2.</span></span> <span data-ttu-id="3ad11-1118">Haga clic en Aceptar para cerrar el sistema.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1118">Please click OK to shutdown the system.</span></span> <span data-ttu-id="3ad11-1119">Puede usar la consola de recuperación para examinar el sistema más a fondo.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1119">You can use the recovery console to diagnose the system further.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1120"><span id="ERROR_DS_SAM_INIT_FAILURE_CONSOLE"></span><span id="error_ds_sam_init_failure_console"></span>**ERROR \_ DS \_ Sam \_ init \_ error \_ Console**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1120"><span id="ERROR_DS_SAM_INIT_FAILURE_CONSOLE"></span><span id="error_ds_sam_init_failure_console"></span>**ERROR\_DS\_SAM\_INIT\_FAILURE\_CONSOLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1121">8562 (0x2172)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1121">8562 (0x2172)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1122">No se pudo inicializar el administrador de cuentas de seguridad debido al siguiente error: %1.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1122">Security Accounts Manager initialization failed because of the following error: %1.</span></span> <span data-ttu-id="3ad11-1123">Estado de error: 0x %2.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1123">Error Status: 0x%2.</span></span> <span data-ttu-id="3ad11-1124">Haga clic en Aceptar para cerrar el sistema.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1124">Please click OK to shutdown the system.</span></span> <span data-ttu-id="3ad11-1125">Puede usar la consola de recuperación para examinar el sistema más a fondo.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1125">You can use the recovery console to diagnose the system further.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1126"><span id="ERROR_DS_FOREST_VERSION_TOO_HIGH"></span><span id="error_ds_forest_version_too_high"></span>**ERROR en la \_ \_ versión del bosque DS \_ \_ demasiado \_ alta**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1126"><span id="ERROR_DS_FOREST_VERSION_TOO_HIGH"></span><span id="error_ds_forest_version_too_high"></span>**ERROR\_DS\_FOREST\_VERSION\_TOO\_HIGH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1127">8563 (0x2173)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1127">8563 (0x2173)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1128">La versión del sistema operativo no es compatible con el nivel funcional del bosque de AD DS actual o AD LDS nivel funcional del conjunto de configuración.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1128">The version of the operating system is incompatible with the current AD DS forest functional level or AD LDS Configuration Set functional level.</span></span> <span data-ttu-id="3ad11-1129">Debe actualizar a una nueva versión del sistema operativo para que este servidor pueda convertirse en un controlador de dominio de AD DS o agregar una instancia de AD LDS en este AD DS bosque o AD LDS conjunto de configuración.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1129">You must upgrade to a new version of the operating system before this server can become an AD DS Domain Controller or add an AD LDS Instance in this AD DS Forest or AD LDS Configuration Set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1130"><span id="ERROR_DS_DOMAIN_VERSION_TOO_HIGH"></span><span id="error_ds_domain_version_too_high"></span>**ERROR de \_ versión de dominio de DS \_ \_ \_ demasiado \_ alto**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1130"><span id="ERROR_DS_DOMAIN_VERSION_TOO_HIGH"></span><span id="error_ds_domain_version_too_high"></span>**ERROR\_DS\_DOMAIN\_VERSION\_TOO\_HIGH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1131">8564 (0x2174)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1131">8564 (0x2174)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1132">La versión del sistema operativo instalada es incompatible con el nivel funcional del dominio actual.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1132">The version of the operating system installed is incompatible with the current domain functional level.</span></span> <span data-ttu-id="3ad11-1133">Debe actualizar a una nueva versión del sistema operativo para que este servidor pueda convertirse en un controlador de dominio en este dominio.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1133">You must upgrade to a new version of the operating system before this server can become a domain controller in this domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1134"><span id="ERROR_DS_FOREST_VERSION_TOO_LOW"></span><span id="error_ds_forest_version_too_low"></span>**ERROR: la \_ \_ versión del bosque DS \_ \_ es demasiado \_ baja**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1134"><span id="ERROR_DS_FOREST_VERSION_TOO_LOW"></span><span id="error_ds_forest_version_too_low"></span>**ERROR\_DS\_FOREST\_VERSION\_TOO\_LOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1135">8565 (0x2175)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1135">8565 (0x2175)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1136">La versión del sistema operativo instalado en este servidor ya no es compatible con el nivel funcional del bosque de AD DS actual o AD LDS nivel funcional del conjunto de configuración.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1136">The version of the operating system installed on this server no longer supports the current AD DS Forest functional level or AD LDS Configuration Set functional level.</span></span> <span data-ttu-id="3ad11-1137">Debe elevar el nivel funcional del bosque de AD DS o AD LDS nivel funcional del conjunto de configuración antes de que este servidor pueda convertirse en un controlador de dominio de AD DS o en una instancia de AD LDS en este bosque o conjunto de configuración.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1137">You must raise the AD DS Forest functional level or AD LDS Configuration Set functional level before this server can become an AD DS Domain Controller or an AD LDS Instance in this Forest or Configuration Set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1138"><span id="ERROR_DS_DOMAIN_VERSION_TOO_LOW"></span><span id="error_ds_domain_version_too_low"></span>**ERROR en la \_ versión de dominio de DS \_ \_ \_ demasiado \_ baja**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1138"><span id="ERROR_DS_DOMAIN_VERSION_TOO_LOW"></span><span id="error_ds_domain_version_too_low"></span>**ERROR\_DS\_DOMAIN\_VERSION\_TOO\_LOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1139">8566 (0x2176)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1139">8566 (0x2176)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1140">La versión del sistema operativo instalado en este servidor ya no es compatible con el nivel funcional del dominio actual.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1140">The version of the operating system installed on this server no longer supports the current domain functional level.</span></span> <span data-ttu-id="3ad11-1141">Debe elevar el nivel funcional del dominio para que este servidor pueda convertirse en un controlador de dominio en este dominio.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1141">You must raise the domain functional level before this server can become a domain controller in this domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1142"><span id="ERROR_DS_INCOMPATIBLE_VERSION"></span><span id="error_ds_incompatible_version"></span>**ERROR \_ de \_ versión de DS compatible \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1142"><span id="ERROR_DS_INCOMPATIBLE_VERSION"></span><span id="error_ds_incompatible_version"></span>**ERROR\_DS\_INCOMPATIBLE\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1143">8567 (0x2177)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1143">8567 (0x2177)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1144">La versión del sistema operativo instalado en este servidor no es compatible con el nivel funcional del dominio o bosque.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1144">The version of the operating system installed on this server is incompatible with the functional level of the domain or forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1145"><span id="ERROR_DS_LOW_DSA_VERSION"></span><span id="error_ds_low_dsa_version"></span>**ERROR \_ DS \_ \_ versión de DSA inferior \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1145"><span id="ERROR_DS_LOW_DSA_VERSION"></span><span id="error_ds_low_dsa_version"></span>**ERROR\_DS\_LOW\_DSA\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1146">8568 (0x2178)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1146">8568 (0x2178)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1147">No se puede elevar el nivel funcional del dominio (o bosque) al valor solicitado porque existen uno o más controladores de dominio en el dominio (o bosque) que están en un nivel funcional inferior incompatible.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1147">The functional level of the domain (or forest) cannot be raised to the requested value, because there exist one or more domain controllers in the domain (or forest) that are at a lower incompatible functional level.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1148"><span id="ERROR_DS_NO_BEHAVIOR_VERSION_IN_MIXEDDOMAIN"></span><span id="error_ds_no_behavior_version_in_mixeddomain"></span>**ERROR \_ DS \_ \_ \_ versión de comportamiento no \_ en \_ MIXEDDOMAIN**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1148"><span id="ERROR_DS_NO_BEHAVIOR_VERSION_IN_MIXEDDOMAIN"></span><span id="error_ds_no_behavior_version_in_mixeddomain"></span>**ERROR\_DS\_NO\_BEHAVIOR\_VERSION\_IN\_MIXEDDOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1149">8569 (0x2179)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1149">8569 (0x2179)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1150">No se puede elevar el nivel funcional del bosque al valor solicitado porque uno o varios dominios todavía están en modo de dominio mixto.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1150">The forest functional level cannot be raised to the requested value since one or more domains are still in mixed domain mode.</span></span> <span data-ttu-id="3ad11-1151">Todos los dominios del bosque deben estar en modo nativo para elevar el nivel funcional del bosque.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1151">All domains in the forest must be in native mode, for you to raise the forest functional level.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1152"><span id="ERROR_DS_NOT_SUPPORTED_SORT_ORDER"></span><span id="error_ds_not_supported_sort_order"></span>**ERROR \_ DS \_ no \_ compatible con el criterio de \_ ordenación \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1152"><span id="ERROR_DS_NOT_SUPPORTED_SORT_ORDER"></span><span id="error_ds_not_supported_sort_order"></span>**ERROR\_DS\_NOT\_SUPPORTED\_SORT\_ORDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1153">8570 (0x217A)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1153">8570 (0x217A)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1154">No se admite el criterio de ordenación solicitado.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1154">The sort order requested is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1155"><span id="ERROR_DS_NAME_NOT_UNIQUE"></span><span id="error_ds_name_not_unique"></span>**ERROR \_ de \_ nombre de DS \_ no \_ único**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1155"><span id="ERROR_DS_NAME_NOT_UNIQUE"></span><span id="error_ds_name_not_unique"></span>**ERROR\_DS\_NAME\_NOT\_UNIQUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1156">8571 (0x217B)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1156">8571 (0x217B)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1157">El nombre solicitado ya existe como identificador único.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1157">The requested name already exists as a unique identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1158"><span id="ERROR_DS_MACHINE_ACCOUNT_CREATED_PRENT4"></span><span id="error_ds_machine_account_created_prent4"></span>**ERROR en la \_ \_ cuenta de equipo DS \_ \_ creada \_ PRENT4**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1158"><span id="ERROR_DS_MACHINE_ACCOUNT_CREATED_PRENT4"></span><span id="error_ds_machine_account_created_prent4"></span>**ERROR\_DS\_MACHINE\_ACCOUNT\_CREATED\_PRENT4**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1159">8572 (0x217C)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1159">8572 (0x217C)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1160">La cuenta de equipo se creó antes de NT4.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1160">The machine account was created pre-NT4.</span></span> <span data-ttu-id="3ad11-1161">Es necesario volver a crear la cuenta.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1161">The account needs to be recreated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1162"><span id="ERROR_DS_OUT_OF_VERSION_STORE"></span><span id="error_ds_out_of_version_store"></span>**ERROR \_ \_ de DS \_ fuera \_ del \_ almacén de versiones**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1162"><span id="ERROR_DS_OUT_OF_VERSION_STORE"></span><span id="error_ds_out_of_version_store"></span>**ERROR\_DS\_OUT\_OF\_VERSION\_STORE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1163">8573 (0x217D)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1163">8573 (0x217D)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1164">La base de datos está fuera del almacén de versiones.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1164">The database is out of version store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1165"><span id="ERROR_DS_INCOMPATIBLE_CONTROLS_USED"></span><span id="error_ds_incompatible_controls_used"></span>**ERROR \_ en \_ \_ los controles \_ no compatibles de DS**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1165"><span id="ERROR_DS_INCOMPATIBLE_CONTROLS_USED"></span><span id="error_ds_incompatible_controls_used"></span>**ERROR\_DS\_INCOMPATIBLE\_CONTROLS\_USED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1166">8574 (0x217E)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1166">8574 (0x217E)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1167">No se puede continuar la operación porque se usaron varios controles conflictivos.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1167">Unable to continue operation because multiple conflicting controls were used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1168"><span id="ERROR_DS_NO_REF_DOMAIN"></span><span id="error_ds_no_ref_domain"></span>**ERROR \_ DS \_ sin \_ dominio de referencia \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1168"><span id="ERROR_DS_NO_REF_DOMAIN"></span><span id="error_ds_no_ref_domain"></span>**ERROR\_DS\_NO\_REF\_DOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1169">8575 (0x217F)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1169">8575 (0x217F)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1170">No se encuentra un dominio de referencia de descriptor de seguridad válido para esta partición.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1170">Unable to find a valid security descriptor reference domain for this partition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1171"><span id="ERROR_DS_RESERVED_LINK_ID"></span><span id="error_ds_reserved_link_id"></span>**\_ \_ \_ ID. de vínculo \_ reservado de DS de error**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1171"><span id="ERROR_DS_RESERVED_LINK_ID"></span><span id="error_ds_reserved_link_id"></span>**ERROR\_DS\_RESERVED\_LINK\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1172">8576 (0x2180)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1172">8576 (0x2180)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1173">Error al actualizar el esquema: el identificador del vínculo está reservado.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1173">Schema update failed: The link identifier is reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1174"><span id="ERROR_DS_LINK_ID_NOT_AVAILABLE"></span><span id="error_ds_link_id_not_available"></span>**ERROR \_ de \_ ID. de vínculo de DS \_ \_ no \_ disponible**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1174"><span id="ERROR_DS_LINK_ID_NOT_AVAILABLE"></span><span id="error_ds_link_id_not_available"></span>**ERROR\_DS\_LINK\_ID\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1175">8577 (0x2181)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1175">8577 (0x2181)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1176">No se pudo actualizar el esquema: no hay identificadores de vínculo disponibles.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1176">Schema update failed: There are no link identifiers available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1177"><span id="ERROR_DS_AG_CANT_HAVE_UNIVERSAL_MEMBER"></span><span id="error_ds_ag_cant_have_universal_member"></span>**ERROR \_ DS \_ AG no se \_ \_ tiene \_ \_ miembro universal**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1177"><span id="ERROR_DS_AG_CANT_HAVE_UNIVERSAL_MEMBER"></span><span id="error_ds_ag_cant_have_universal_member"></span>**ERROR\_DS\_AG\_CANT\_HAVE\_UNIVERSAL\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1178">8578 (0x2182)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1178">8578 (0x2182)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1179">Un grupo de cuentas no puede tener un grupo universal como miembro.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1179">An account group cannot have a universal group as a member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1180"><span id="ERROR_DS_MODIFYDN_DISALLOWED_BY_INSTANCE_TYPE"></span><span id="error_ds_modifydn_disallowed_by_instance_type"></span>**ERROR \_ \_ de MODIFYDN \_ de DS no \_ permitido \_ por \_ tipo de instancia**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1180"><span id="ERROR_DS_MODIFYDN_DISALLOWED_BY_INSTANCE_TYPE"></span><span id="error_ds_modifydn_disallowed_by_instance_type"></span>**ERROR\_DS\_MODIFYDN\_DISALLOWED\_BY\_INSTANCE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1181">8579 (0x2183)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1181">8579 (0x2183)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1182">No se permiten las operaciones de cambio de nombre o movimiento en encabezados de contexto de nomenclatura o en objetos de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1182">Rename or move operations on naming context heads or read-only objects are not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1183"><span id="ERROR_DS_NO_OBJECT_MOVE_IN_SCHEMA_NC"></span><span id="error_ds_no_object_move_in_schema_nc"></span>**ERROR \_ DS \_ no \_ se \_ mueve ningún objeto en el \_ \_ esquema \_ NC**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1183"><span id="ERROR_DS_NO_OBJECT_MOVE_IN_SCHEMA_NC"></span><span id="error_ds_no_object_move_in_schema_nc"></span>**ERROR\_DS\_NO\_OBJECT\_MOVE\_IN\_SCHEMA\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1184">8580 (0x2184)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1184">8580 (0x2184)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1185">No se permiten las operaciones de movimiento en objetos en el contexto de nomenclatura de esquemas.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1185">Move operations on objects in the schema naming context are not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1186"><span id="ERROR_DS_MODIFYDN_DISALLOWED_BY_FLAG"></span><span id="error_ds_modifydn_disallowed_by_flag"></span>**ERROR \_ \_ de DS MODIFYDN no \_ permitido \_ por la \_ marca**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1186"><span id="ERROR_DS_MODIFYDN_DISALLOWED_BY_FLAG"></span><span id="error_ds_modifydn_disallowed_by_flag"></span>**ERROR\_DS\_MODIFYDN\_DISALLOWED\_BY\_FLAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1187">8581 (0x2185)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1187">8581 (0x2185)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1188">Se ha establecido una marca de sistema en el objeto y no permite que el objeto se mueva o cambie de nombre.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1188">A system flag has been set on the object and does not allow the object to be moved or renamed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1189"><span id="ERROR_DS_MODIFYDN_WRONG_GRANDPARENT"></span><span id="error_ds_modifydn_wrong_grandparent"></span>**ERROR de \_ DS \_ MODIFYDN de \_ \_ padre incorrecto**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1189"><span id="ERROR_DS_MODIFYDN_WRONG_GRANDPARENT"></span><span id="error_ds_modifydn_wrong_grandparent"></span>**ERROR\_DS\_MODIFYDN\_WRONG\_GRANDPARENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1190">8582 (0x2186)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1190">8582 (0x2186)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1191">Este objeto no tiene permiso para cambiar su contenedor principal.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1191">This object is not allowed to change its grandparent container.</span></span> <span data-ttu-id="3ad11-1192">Los movimientos no están prohibidos en este objeto, pero están restringidos a contenedores relacionados.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1192">Moves are not forbidden on this object, but are restricted to sibling containers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1193"><span id="ERROR_DS_NAME_ERROR_TRUST_REFERRAL"></span><span id="error_ds_name_error_trust_referral"></span>**ERROR \_ de \_ nombre de DS error de \_ \_ referencia de confianza \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1193"><span id="ERROR_DS_NAME_ERROR_TRUST_REFERRAL"></span><span id="error_ds_name_error_trust_referral"></span>**ERROR\_DS\_NAME\_ERROR\_TRUST\_REFERRAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1194">8583 (0x2187)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1194">8583 (0x2187)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1195">No se puede resolver por completo, se genera una referencia a otro bosque.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1195">Unable to resolve completely, a referral to another forest is generated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1196"><span id="ERROR_NOT_SUPPORTED_ON_STANDARD_SERVER"></span><span id="error_not_supported_on_standard_server"></span>**ERROR \_ no \_ admitido \_ en el \_ \_ servidor estándar**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1196"><span id="ERROR_NOT_SUPPORTED_ON_STANDARD_SERVER"></span><span id="error_not_supported_on_standard_server"></span>**ERROR\_NOT\_SUPPORTED\_ON\_STANDARD\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1197">8584 (0x2188)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1197">8584 (0x2188)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1198">La acción solicitada no se admite en el servidor estándar.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1198">The requested action is not supported on standard server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1199"><span id="ERROR_DS_CANT_ACCESS_REMOTE_PART_OF_AD"></span><span id="error_ds_cant_access_remote_part_of_ad"></span>**ERROR \_ DS no se \_ \_ puede acceder a la \_ \_ parte remota \_ de \_ ad**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1199"><span id="ERROR_DS_CANT_ACCESS_REMOTE_PART_OF_AD"></span><span id="error_ds_cant_access_remote_part_of_ad"></span>**ERROR\_DS\_CANT\_ACCESS\_REMOTE\_PART\_OF\_AD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1200">8585 (0x2189)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1200">8585 (0x2189)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1201">No se pudo obtener acceso a una partición del servicio de directorio ubicada en un servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1201">Could not access a partition of the directory service located on a remote server.</span></span> <span data-ttu-id="3ad11-1202">Asegúrese de que se está ejecutando al menos un servidor para la partición en cuestión.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1202">Make sure at least one server is running for the partition in question.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1203"><span id="ERROR_DS_CR_IMPOSSIBLE_TO_VALIDATE_V2"></span><span id="error_ds_cr_impossible_to_validate_v2"></span>**ERROR \_ DS \_ CR \_ imposible \_ \_ validar \_ V2**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1203"><span id="ERROR_DS_CR_IMPOSSIBLE_TO_VALIDATE_V2"></span><span id="error_ds_cr_impossible_to_validate_v2"></span>**ERROR\_DS\_CR\_IMPOSSIBLE\_TO\_VALIDATE\_V2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1204">8586 (0x218A)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1204">8586 (0x218A)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1205">El directorio no puede validar el nombre de contexto de nomenclatura propuesto (o partición) porque no contiene una réplica ni puede ponerse en contacto con una réplica del contexto de nomenclatura por encima del contexto de nomenclatura propuesto.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1205">The directory cannot validate the proposed naming context (or partition) name because it does not hold a replica nor can it contact a replica of the naming context above the proposed naming context.</span></span> <span data-ttu-id="3ad11-1206">Asegúrese de que el contexto de nomenclatura principal esté registrado correctamente en DNS y de que el maestro de nombres de dominio pueda tener acceso al menos a una réplica de este contexto de nomenclatura.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1206">Please ensure that the parent naming context is properly registered in DNS, and at least one replica of this naming context is reachable by the Domain Naming master.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1207"><span id="ERROR_DS_THREAD_LIMIT_EXCEEDED"></span><span id="error_ds_thread_limit_exceeded"></span>**se \_ \_ \_ superó el límite de subprocesos de DS \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1207"><span id="ERROR_DS_THREAD_LIMIT_EXCEEDED"></span><span id="error_ds_thread_limit_exceeded"></span>**ERROR\_DS\_THREAD\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1208">8587 (0x218B)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1208">8587 (0x218B)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1209">Se superó el límite de subprocesos para esta solicitud.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1209">The thread limit for this request was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1210"><span id="ERROR_DS_NOT_CLOSEST"></span><span id="error_ds_not_closest"></span>**ERROR \_ DS \_ no \_ más cercano**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1210"><span id="ERROR_DS_NOT_CLOSEST"></span><span id="error_ds_not_closest"></span>**ERROR\_DS\_NOT\_CLOSEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1211">8588 (0x218C)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1211">8588 (0x218C)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1212">El servidor de catálogo global no está en el sitio más cercano.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1212">The Global catalog server is not in the closest site.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1213"><span id="ERROR_DS_CANT_DERIVE_SPN_WITHOUT_SERVER_REF"></span><span id="error_ds_cant_derive_spn_without_server_ref"></span>**ERROR \_ DS \_ no se pudo \_ derivar \_ SPN \_ sin \_ referencia de servidor \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1213"><span id="ERROR_DS_CANT_DERIVE_SPN_WITHOUT_SERVER_REF"></span><span id="error_ds_cant_derive_spn_without_server_ref"></span>**ERROR\_DS\_CANT\_DERIVE\_SPN\_WITHOUT\_SERVER\_REF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1214">8589 (0x218D)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1214">8589 (0x218D)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1215">El DS no puede derivar un nombre principal de servicio (SPN) con el que autenticar mutuamente el servidor de destino porque el objeto de servidor correspondiente en la base de datos de DS local no tiene ningún atributo serverReference.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1215">The DS cannot derive a service principal name (SPN) with which to mutually authenticate the target server because the corresponding server object in the local DS database has no serverReference attribute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1216"><span id="ERROR_DS_SINGLE_USER_MODE_FAILED"></span><span id="error_ds_single_user_mode_failed"></span>**ERROR en el \_ \_ \_ modo de usuario único \_ de DS \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1216"><span id="ERROR_DS_SINGLE_USER_MODE_FAILED"></span><span id="error_ds_single_user_mode_failed"></span>**ERROR\_DS\_SINGLE\_USER\_MODE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1217">8590 (0x218E)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1217">8590 (0x218E)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1218">El servicio de directorio no pudo entrar en el modo de usuario único.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1218">The Directory Service failed to enter single user mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1219"><span id="ERROR_DS_NTDSCRIPT_SYNTAX_ERROR"></span><span id="error_ds_ntdscript_syntax_error"></span>**error \_ de \_ Sintaxis de NTDSCRIPT de DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1219"><span id="ERROR_DS_NTDSCRIPT_SYNTAX_ERROR"></span><span id="error_ds_ntdscript_syntax_error"></span>**ERROR\_DS\_NTDSCRIPT\_SYNTAX\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1220">8591 (0x218F)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1220">8591 (0x218F)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1221">El servicio de directorio no puede analizar el script debido a un error de sintaxis.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1221">The Directory Service cannot parse the script because of a syntax error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1222"><span id="ERROR_DS_NTDSCRIPT_PROCESS_ERROR"></span><span id="error_ds_ntdscript_process_error"></span>**error \_ de \_ proceso NTDSCRIPT de DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1222"><span id="ERROR_DS_NTDSCRIPT_PROCESS_ERROR"></span><span id="error_ds_ntdscript_process_error"></span>**ERROR\_DS\_NTDSCRIPT\_PROCESS\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1223">8592 (0x2190)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1223">8592 (0x2190)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1224">El servicio de directorio no puede procesar el script debido a un error.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1224">The Directory Service cannot process the script because of an error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1225"><span id="ERROR_DS_DIFFERENT_REPL_EPOCHS"></span><span id="error_ds_different_repl_epochs"></span>**\_tiempo de \_ \_ réplica diferente \_ de error de DS**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1225"><span id="ERROR_DS_DIFFERENT_REPL_EPOCHS"></span><span id="error_ds_different_repl_epochs"></span>**ERROR\_DS\_DIFFERENT\_REPL\_EPOCHS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1226">8593 (0x2191)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1226">8593 (0x2191)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1227">El servicio de directorio no puede realizar la operación solicitada porque los servidores implicados tienen tiempos de replicación diferentes (que suelen estar relacionados con un cambio de nombre de dominio que está en curso).</span><span class="sxs-lookup"><span data-stu-id="3ad11-1227">The directory service cannot perform the requested operation because the servers involved are of different replication epochs (which is usually related to a domain rename that is in progress).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1228"><span id="ERROR_DS_DRS_EXTENSIONS_CHANGED"></span><span id="error_ds_drs_extensions_changed"></span>**se \_ \_ \_ cambiaron las extensiones de DS DRS \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1228"><span id="ERROR_DS_DRS_EXTENSIONS_CHANGED"></span><span id="error_ds_drs_extensions_changed"></span>**ERROR\_DS\_DRS\_EXTENSIONS\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1229">8594 (0x2192)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1229">8594 (0x2192)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1230">El enlace del servicio de directorio se debe volver a negociar debido a un cambio en la información de las extensiones del servidor.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1230">The directory service binding must be renegotiated due to a change in the server extensions information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1231"><span id="ERROR_DS_REPLICA_SET_CHANGE_NOT_ALLOWED_ON_DISABLED_CR"></span><span id="error_ds_replica_set_change_not_allowed_on_disabled_cr"></span>**ERROR \_ \_ \_ \_ de cambio de conjunto de réplicas DS \_ no \_ permitido \_ en \_ CR deshabilitado \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1231"><span id="ERROR_DS_REPLICA_SET_CHANGE_NOT_ALLOWED_ON_DISABLED_CR"></span><span id="error_ds_replica_set_change_not_allowed_on_disabled_cr"></span>**ERROR\_DS\_REPLICA\_SET\_CHANGE\_NOT\_ALLOWED\_ON\_DISABLED\_CR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1232">8595 (0x2193)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1232">8595 (0x2193)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1233">Operación no permitida en una referencia cruzada deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1233">Operation not allowed on a disabled cross ref.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1234"><span id="ERROR_DS_NO_MSDS_INTID"></span><span id="error_ds_no_msds_intid"></span>**ERROR \_ DS \_ no \_ MSDS \_ INtId**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1234"><span id="ERROR_DS_NO_MSDS_INTID"></span><span id="error_ds_no_msds_intid"></span>**ERROR\_DS\_NO\_MSDS\_INTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1235">8596 (0x2194)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1235">8596 (0x2194)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1236">No se pudo actualizar el esquema: no hay valores disponibles para msDS-IntId.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1236">Schema update failed: No values for msDS-IntId are available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1237"><span id="ERROR_DS_DUP_MSDS_INTID"></span><span id="error_ds_dup_msds_intid"></span>**ERROR \_ de \_ atributo DUP de DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1237"><span id="ERROR_DS_DUP_MSDS_INTID"></span><span id="error_ds_dup_msds_intid"></span>**ERROR\_DS\_DUP\_MSDS\_INTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1238">8597 (0x2195)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1238">8597 (0x2195)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1239">No se pudo actualizar el esquema: se ha duplicado msDS-INtId.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1239">Schema update failed: Duplicate msDS-INtId.</span></span> <span data-ttu-id="3ad11-1240">Vuelva a intentar la operación.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1240">Retry the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1241"><span id="ERROR_DS_EXISTS_IN_RDNATTID"></span><span id="error_ds_exists_in_rdnattid"></span>**el \_ DS \_ de error existe \_ en \_ RDNATTID**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1241"><span id="ERROR_DS_EXISTS_IN_RDNATTID"></span><span id="error_ds_exists_in_rdnattid"></span>**ERROR\_DS\_EXISTS\_IN\_RDNATTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1242">8598 (0x2196)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1242">8598 (0x2196)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1243">No se pudo eliminar el esquema: el atributo se usa en rDNAttID.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1243">Schema deletion failed: attribute is used in rDNAttID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1244"><span id="ERROR_DS_AUTHORIZATION_FAILED"></span><span id="error_ds_authorization_failed"></span>**ERROR \_ de \_ autorización de DS \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1244"><span id="ERROR_DS_AUTHORIZATION_FAILED"></span><span id="error_ds_authorization_failed"></span>**ERROR\_DS\_AUTHORIZATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1245">8599 (0x2197)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1245">8599 (0x2197)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1246">El servicio de directorio no pudo autorizar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1246">The directory service failed to authorize the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1247"><span id="ERROR_DS_INVALID_SCRIPT"></span><span id="error_ds_invalid_script"></span>**ERROR \_ de \_ script DS no válido \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1247"><span id="ERROR_DS_INVALID_SCRIPT"></span><span id="error_ds_invalid_script"></span>**ERROR\_DS\_INVALID\_SCRIPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1248">8600 (0x2198)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1248">8600 (0x2198)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1249">El servicio de directorio no puede procesar el script porque no es válido.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1249">The Directory Service cannot process the script because it is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1250"><span id="ERROR_DS_REMOTE_CROSSREF_OP_FAILED"></span><span id="error_ds_remote_crossref_op_failed"></span>**ERROR \_ de \_ OP remota de \_ CROSSREF de \_ DS \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1250"><span id="ERROR_DS_REMOTE_CROSSREF_OP_FAILED"></span><span id="error_ds_remote_crossref_op_failed"></span>**ERROR\_DS\_REMOTE\_CROSSREF\_OP\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1251">8601 (0x2199)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1251">8601 (0x2199)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1252">No se pudo realizar la operación de referencia cruzada de creación remota en el FSMO del maestro de nomenclatura de dominios.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1252">The remote create cross reference operation failed on the Domain Naming Master FSMO.</span></span> <span data-ttu-id="3ad11-1253">El error de la operación se encuentra en los datos extendidos.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1253">The operation's error is in the extended data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1254"><span id="ERROR_DS_CROSS_REF_BUSY"></span><span id="error_ds_cross_ref_busy"></span>**ERROR en la \_ \_ \_ referencia \_ cruzada de DS**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1254"><span id="ERROR_DS_CROSS_REF_BUSY"></span><span id="error_ds_cross_ref_busy"></span>**ERROR\_DS\_CROSS\_REF\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1255">8602 (0x219A)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1255">8602 (0x219A)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1256">Una referencia cruzada está en uso localmente con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1256">A cross reference is in use locally with the same name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1257"><span id="ERROR_DS_CANT_DERIVE_SPN_FOR_DELETED_DOMAIN"></span><span id="error_ds_cant_derive_spn_for_deleted_domain"></span>**ERROR DS no se pudo \_ \_ \_ derivar \_ SPN \_ para el \_ \_ dominio eliminado**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1257"><span id="ERROR_DS_CANT_DERIVE_SPN_FOR_DELETED_DOMAIN"></span><span id="error_ds_cant_derive_spn_for_deleted_domain"></span>**ERROR\_DS\_CANT\_DERIVE\_SPN\_FOR\_DELETED\_DOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1258">8603 (0x219B)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1258">8603 (0x219B)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1259">El DS no puede derivar un nombre principal de servicio (SPN) con el que autenticar mutuamente el servidor de destino porque el dominio del servidor se ha eliminado del bosque.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1259">The DS cannot derive a service principal name (SPN) with which to mutually authenticate the target server because the server's domain has been deleted from the forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1260"><span id="ERROR_DS_CANT_DEMOTE_WITH_WRITEABLE_NC"></span><span id="error_ds_cant_demote_with_writeable_nc"></span>**ERROR DS no se pudo \_ \_ \_ disminuir \_ de nivel con el \_ \_ NC grabable**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1260"><span id="ERROR_DS_CANT_DEMOTE_WITH_WRITEABLE_NC"></span><span id="error_ds_cant_demote_with_writeable_nc"></span>**ERROR\_DS\_CANT\_DEMOTE\_WITH\_WRITEABLE\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1261">8604 (0x219C)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1261">8604 (0x219C)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1262">Los NC grabable impiden que este controlador de dominio se degrade.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1262">Writeable NCs prevent this DC from demoting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1263"><span id="ERROR_DS_DUPLICATE_ID_FOUND"></span><span id="error_ds_duplicate_id_found"></span>**ERROR \_ de \_ ID. de DS duplicado \_ \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1263"><span id="ERROR_DS_DUPLICATE_ID_FOUND"></span><span id="error_ds_duplicate_id_found"></span>**ERROR\_DS\_DUPLICATE\_ID\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1264">8605 (0x219D)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1264">8605 (0x219D)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1265">El objeto solicitado tiene un identificador no único y no se puede recuperar.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1265">The requested object has a non-unique identifier and cannot be retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1266"><span id="ERROR_DS_INSUFFICIENT_ATTR_TO_CREATE_OBJECT"></span><span id="error_ds_insufficient_attr_to_create_object"></span>**ERROR \_ DS \_ atributo insuficiente \_ \_ para \_ crear el \_ objeto**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1266"><span id="ERROR_DS_INSUFFICIENT_ATTR_TO_CREATE_OBJECT"></span><span id="error_ds_insufficient_attr_to_create_object"></span>**ERROR\_DS\_INSUFFICIENT\_ATTR\_TO\_CREATE\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1267">8606 (0x219E)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1267">8606 (0x219E)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1268">Se asignaron atributos insuficientes para crear un objeto.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1268">Insufficient attributes were given to create an object.</span></span> <span data-ttu-id="3ad11-1269">Es posible que este objeto no exista porque puede que se haya eliminado y ya se haya recolectado el elemento no utilizado.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1269">This object may not exist because it may have been deleted and already garbage collected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1270"><span id="ERROR_DS_GROUP_CONVERSION_ERROR"></span><span id="error_ds_group_conversion_error"></span>**error \_ de \_ conversión de grupo DS \_ de error \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1270"><span id="ERROR_DS_GROUP_CONVERSION_ERROR"></span><span id="error_ds_group_conversion_error"></span>**ERROR\_DS\_GROUP\_CONVERSION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1271">8607 (0x219F)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1271">8607 (0x219F)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1272">No se puede convertir el grupo debido a restricciones de atributo en el tipo de grupo solicitado.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1272">The group cannot be converted due to attribute restrictions on the requested group type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1273"><span id="ERROR_DS_CANT_MOVE_APP_BASIC_GROUP"></span><span id="error_ds_cant_move_app_basic_group"></span>**ERROR DS no se pudo \_ \_ cambiar el \_ \_ \_ \_ grupo básico de la aplicación**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1273"><span id="ERROR_DS_CANT_MOVE_APP_BASIC_GROUP"></span><span id="error_ds_cant_move_app_basic_group"></span>**ERROR\_DS\_CANT\_MOVE\_APP\_BASIC\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1274">8608 (0x21A0)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1274">8608 (0x21A0)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1275">No se permite el movimiento entre dominios de grupos de aplicaciones básicas no vacías.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1275">Cross-domain move of non-empty basic application groups is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1276"><span id="ERROR_DS_CANT_MOVE_APP_QUERY_GROUP"></span><span id="error_ds_cant_move_app_query_group"></span>**ERROR DS no se pudo \_ \_ \_ migrar el \_ \_ grupo de consultas \_ de la aplicación**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1276"><span id="ERROR_DS_CANT_MOVE_APP_QUERY_GROUP"></span><span id="error_ds_cant_move_app_query_group"></span>**ERROR\_DS\_CANT\_MOVE\_APP\_QUERY\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1277">8609 (0x21A1)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1277">8609 (0x21A1)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1278">No se permite el movimiento entre dominios de grupos de aplicaciones basados en consultas no vacías.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1278">Cross-domain move of non-empty query based application groups is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1279"><span id="ERROR_DS_ROLE_NOT_VERIFIED"></span><span id="error_ds_role_not_verified"></span>**\_no se \_ \_ ha \_ comprobado el rol DS de error**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1279"><span id="ERROR_DS_ROLE_NOT_VERIFIED"></span><span id="error_ds_role_not_verified"></span>**ERROR\_DS\_ROLE\_NOT\_VERIFIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1280">8610 (0x21A2)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1280">8610 (0x21A2)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1281">No se pudo comprobar la propiedad del rol FSMO porque su partición de directorio no se ha replicado correctamente con al menos un asociado de replicación.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1281">The FSMO role ownership could not be verified because its directory partition has not replicated successfully with at least one replication partner.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1282"><span id="ERROR_DS_WKO_CONTAINER_CANNOT_BE_SPECIAL"></span><span id="error_ds_wko_container_cannot_be_special"></span>**el \_ contenedor WKO de DS de error \_ \_ \_ no puede \_ ser \_ especial**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1282"><span id="ERROR_DS_WKO_CONTAINER_CANNOT_BE_SPECIAL"></span><span id="error_ds_wko_container_cannot_be_special"></span>**ERROR\_DS\_WKO\_CONTAINER\_CANNOT\_BE\_SPECIAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1283">8611 (0x21A3)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1283">8611 (0x21A3)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1284">El contenedor de destino para una redirección de un contenedor de objetos conocido no puede ser ya un contenedor especial.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1284">The target container for a redirection of a well known object container cannot already be a special container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1285"><span id="ERROR_DS_DOMAIN_RENAME_IN_PROGRESS"></span><span id="error_ds_domain_rename_in_progress"></span>**ERROR \_ \_ \_ de cambio de nombre \_ de dominio de DS en \_ curso**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1285"><span id="ERROR_DS_DOMAIN_RENAME_IN_PROGRESS"></span><span id="error_ds_domain_rename_in_progress"></span>**ERROR\_DS\_DOMAIN\_RENAME\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1286">8612 (0x21A4)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1286">8612 (0x21A4)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1287">El servicio de directorio no puede realizar la operación solicitada porque hay una operación de cambio de nombre de dominio en curso.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1287">The Directory Service cannot perform the requested operation because a domain rename operation is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1288"><span id="ERROR_DS_EXISTING_AD_CHILD_NC"></span><span id="error_ds_existing_ad_child_nc"></span>**ERROR \_ DS \_ \_ ad \_ Child \_ NC existente**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1288"><span id="ERROR_DS_EXISTING_AD_CHILD_NC"></span><span id="error_ds_existing_ad_child_nc"></span>**ERROR\_DS\_EXISTING\_AD\_CHILD\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1289">8613 (0x21A5)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1289">8613 (0x21A5)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1290">El servicio de directorio detectó una partición secundaria debajo del nombre de partición solicitado.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1290">The directory service detected a child partition below the requested partition name.</span></span> <span data-ttu-id="3ad11-1291">La jerarquía de particiones se debe crear en un método de arriba abajo.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1291">The partition hierarchy must be created in a top down method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1292"><span id="ERROR_DS_REPL_LIFETIME_EXCEEDED"></span><span id="error_ds_repl_lifetime_exceeded"></span>**ERROR en la \_ duración de REPL de DS \_ \_ \_ superada**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1292"><span id="ERROR_DS_REPL_LIFETIME_EXCEEDED"></span><span id="error_ds_repl_lifetime_exceeded"></span>**ERROR\_DS\_REPL\_LIFETIME\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1293">8614 (0x21A6)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1293">8614 (0x21A6)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1294">El servicio de directorio no se puede replicar con este servidor porque el tiempo transcurrido desde la última replicación con este servidor superó la duración del desecho.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1294">The directory service cannot replicate with this server because the time since the last replication with this server has exceeded the tombstone lifetime.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1295"><span id="ERROR_DS_DISALLOWED_IN_SYSTEM_CONTAINER"></span><span id="error_ds_disallowed_in_system_container"></span>**ERROR \_ de DS no \_ permitido \_ en \_ el \_ contenedor del sistema**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1295"><span id="ERROR_DS_DISALLOWED_IN_SYSTEM_CONTAINER"></span><span id="error_ds_disallowed_in_system_container"></span>**ERROR\_DS\_DISALLOWED\_IN\_SYSTEM\_CONTAINER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1296">8615 (0x21A7)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1296">8615 (0x21A7)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1297">La operación solicitada no se permite en un objeto en el contenedor del sistema.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1297">The requested operation is not allowed on an object under the system container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1298"><span id="ERROR_DS_LDAP_SEND_QUEUE_FULL"></span><span id="error_ds_ldap_send_queue_full"></span>**ERROR \_ \_ en la \_ cola de envío LDAP \_ DS \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1298"><span id="ERROR_DS_LDAP_SEND_QUEUE_FULL"></span><span id="error_ds_ldap_send_queue_full"></span>**ERROR\_DS\_LDAP\_SEND\_QUEUE\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1299">8616 (0x21A8)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1299">8616 (0x21A8)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1300">La cola de envío de red de servidores LDAP se ha rellenado porque el cliente no está procesando los resultados de sus solicitudes con la rapidez suficiente.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1300">The LDAP servers network send queue has filled up because the client is not processing the results of its requests fast enough.</span></span> <span data-ttu-id="3ad11-1301">No se procesarán más solicitudes hasta que el cliente se ponga al día.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1301">No more requests will be processed until the client catches up.</span></span> <span data-ttu-id="3ad11-1302">Si el cliente no se pone al día, se desconectará.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1302">If the client does not catch up then it will be disconnected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1303"><span id="ERROR_DS_DRA_OUT_SCHEDULE_WINDOW"></span><span id="error_ds_dra_out_schedule_window"></span>**ERROR de la \_ \_ \_ ventana de \_ programación Dra \_ de DS**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1303"><span id="ERROR_DS_DRA_OUT_SCHEDULE_WINDOW"></span><span id="error_ds_dra_out_schedule_window"></span>**ERROR\_DS\_DRA\_OUT\_SCHEDULE\_WINDOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1304">8617 (0x21A9)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1304">8617 (0x21A9)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1305">No se pudo realizar la replicación programada porque el sistema estaba demasiado ocupado para ejecutar la solicitud en la ventana de programación.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1305">The scheduled replication did not take place because the system was too busy to execute the request within the schedule window.</span></span> <span data-ttu-id="3ad11-1306">La cola de replicación está sobrecargada.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1306">The replication queue is overloaded.</span></span> <span data-ttu-id="3ad11-1307">Considere la posibilidad de reducir el número de asociados o disminuir la frecuencia de replicación programada.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1307">Consider reducing the number of partners or decreasing the scheduled replication frequency.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1308"><span id="ERROR_DS_POLICY_NOT_KNOWN"></span><span id="error_ds_policy_not_known"></span>**ERROR \_ de \_ Directiva de DS \_ \_ desconocida**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1308"><span id="ERROR_DS_POLICY_NOT_KNOWN"></span><span id="error_ds_policy_not_known"></span>**ERROR\_DS\_POLICY\_NOT\_KNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1309">8618 (0x21AA)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1309">8618 (0x21AA)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1310">En este momento, no se puede determinar si la Directiva de replicación de la rama está disponible en el controlador de dominio del concentrador.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1310">At this time, it cannot be determined if the branch replication policy is available on the hub domain controller.</span></span> <span data-ttu-id="3ad11-1311">Vuelva a intentarlo más tarde para tener en cuenta las latencias de replicación.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1311">Please retry at a later time to account for replication latencies.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1312"><span id="ERROR_NO_SITE_SETTINGS_OBJECT"></span><span id="error_no_site_settings_object"></span>**ERROR: \_ no hay ningún \_ objeto de configuración de sitio \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1312"><span id="ERROR_NO_SITE_SETTINGS_OBJECT"></span><span id="error_no_site_settings_object"></span>**ERROR\_NO\_SITE\_SETTINGS\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1313">8619 (0x21AB)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1313">8619 (0x21AB)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1314">No existe el objeto de configuración del sitio para el sitio especificado.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1314">The site settings object for the specified site does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1315"><span id="ERROR_NO_SECRETS"></span><span id="error_no_secrets"></span>**ERROR \_ sin \_ secretos**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1315"><span id="ERROR_NO_SECRETS"></span><span id="error_no_secrets"></span>**ERROR\_NO\_SECRETS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1316">8620 (0x21AC)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1316">8620 (0x21AC)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1317">El almacén de cuentas local no contiene el material secreto de la cuenta especificada.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1317">The local account store does not contain secret material for the specified account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1318"><span id="ERROR_NO_WRITABLE_DC_FOUND"></span><span id="error_no_writable_dc_found"></span>**ERROR \_ : \_ no \_ \_ se encontró un DC grabable**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1318"><span id="ERROR_NO_WRITABLE_DC_FOUND"></span><span id="error_no_writable_dc_found"></span>**ERROR\_NO\_WRITABLE\_DC\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1319">8621 (0x21AD)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1319">8621 (0x21AD)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1320">No se pudo encontrar un controlador de dominio grabable en el dominio.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1320">Could not find a writable domain controller in the domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1321"><span id="ERROR_DS_NO_SERVER_OBJECT"></span><span id="error_ds_no_server_object"></span>**ERROR \_ DS \_ no \_ hay \_ objeto de servidor**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1321"><span id="ERROR_DS_NO_SERVER_OBJECT"></span><span id="error_ds_no_server_object"></span>**ERROR\_DS\_NO\_SERVER\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1322">8622 (0x21AE)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1322">8622 (0x21AE)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1323">El objeto de servidor para el controlador de dominio no existe.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1323">The server object for the domain controller does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1324"><span id="ERROR_DS_NO_NTDSA_OBJECT"></span><span id="error_ds_no_ntdsa_object"></span>**ERROR \_ DS \_ no \_ NTDSA \_ objeto**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1324"><span id="ERROR_DS_NO_NTDSA_OBJECT"></span><span id="error_ds_no_ntdsa_object"></span>**ERROR\_DS\_NO\_NTDSA\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1325">8623 (0x21AF)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1325">8623 (0x21AF)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1326">No existe el objeto de configuración NTDS para el controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1326">The NTDS Settings object for the domain controller does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1327"><span id="ERROR_DS_NON_ASQ_SEARCH"></span><span id="error_ds_non_asq_search"></span>**ERROR de \_ búsqueda de DS \_ no \_ ASQ \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1327"><span id="ERROR_DS_NON_ASQ_SEARCH"></span><span id="error_ds_non_asq_search"></span>**ERROR\_DS\_NON\_ASQ\_SEARCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1328">8624 (0x21B0)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1328">8624 (0x21B0)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1329">La operación de búsqueda solicitada no se admite para las búsquedas de ASQ.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1329">The requested search operation is not supported for ASQ searches.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1330"><span id="ERROR_DS_AUDIT_FAILURE"></span><span id="error_ds_audit_failure"></span>**ERROR \_ de \_ Auditoría de DS \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1330"><span id="ERROR_DS_AUDIT_FAILURE"></span><span id="error_ds_audit_failure"></span>**ERROR\_DS\_AUDIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1331">8625 (0x21B1)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1331">8625 (0x21B1)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1332">No se pudo generar un evento de auditoría necesario para la operación.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1332">A required audit event could not be generated for the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1333"><span id="ERROR_DS_INVALID_SEARCH_FLAG_SUBTREE"></span><span id="error_ds_invalid_search_flag_subtree"></span>**ERROR \_ DS \_ de \_ marca de búsqueda no válida \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1333"><span id="ERROR_DS_INVALID_SEARCH_FLAG_SUBTREE"></span><span id="error_ds_invalid_search_flag_subtree"></span>**ERROR\_DS\_INVALID\_SEARCH\_FLAG\_SUBTREE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1334">8626 (0x21B2)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1334">8626 (0x21B2)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1335">Las marcas de búsqueda para el atributo no son válidas.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1335">The search flags for the attribute are invalid.</span></span> <span data-ttu-id="3ad11-1336">El bit de índice de subárbol solo es válido en atributos de valor único.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1336">The subtree index bit is valid only on single valued attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1337"><span id="ERROR_DS_INVALID_SEARCH_FLAG_TUPLE"></span><span id="error_ds_invalid_search_flag_tuple"></span>**ERROR de la \_ tupla de marca de \_ búsqueda no válida de DS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1337"><span id="ERROR_DS_INVALID_SEARCH_FLAG_TUPLE"></span><span id="error_ds_invalid_search_flag_tuple"></span>**ERROR\_DS\_INVALID\_SEARCH\_FLAG\_TUPLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1338">8627 (0x21B3)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1338">8627 (0x21B3)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1339">Las marcas de búsqueda para el atributo no son válidas.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1339">The search flags for the attribute are invalid.</span></span> <span data-ttu-id="3ad11-1340">El bit de índice de tupla solo es válido en atributos de cadenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1340">The tuple index bit is valid only on attributes of Unicode strings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1341"><span id="ERROR_DS_HIERARCHY_TABLE_TOO_DEEP"></span><span id="error_ds_hierarchy_table_too_deep"></span>**ERROR en la \_ tabla de jerarquía de DS \_ \_ \_ demasiado \_ profunda**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1341"><span id="ERROR_DS_HIERARCHY_TABLE_TOO_DEEP"></span><span id="error_ds_hierarchy_table_too_deep"></span>**ERROR\_DS\_HIERARCHY\_TABLE\_TOO\_DEEP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1342">8628 (0x21B4)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1342">8628 (0x21B4)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1343">Las libretas de direcciones tienen un anidamiento demasiado profundo.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1343">The address books are nested too deeply.</span></span> <span data-ttu-id="3ad11-1344">No se pudo generar la tabla de jerarquía.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1344">Failed to build the hierarchy table.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1345"><span id="ERROR_DS_DRA_CORRUPT_UTD_VECTOR"></span><span id="error_ds_dra_corrupt_utd_vector"></span>**ERROR \_ DS \_ Dra \_ dañado \_ UTD \_ Vector**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1345"><span id="ERROR_DS_DRA_CORRUPT_UTD_VECTOR"></span><span id="error_ds_dra_corrupt_utd_vector"></span>**ERROR\_DS\_DRA\_CORRUPT\_UTD\_VECTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1346">8629 (0x21B5)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1346">8629 (0x21B5)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1347">El vector de actualización especificado está dañado.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1347">The specified up-to-date-ness vector is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1348"><span id="ERROR_DS_DRA_SECRETS_DENIED"></span><span id="error_ds_dra_secrets_denied"></span>**ERROR de los \_ secretos de Dra de DS \_ \_ \_ denegados**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1348"><span id="ERROR_DS_DRA_SECRETS_DENIED"></span><span id="error_ds_dra_secrets_denied"></span>**ERROR\_DS\_DRA\_SECRETS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1349">8630 (0x21B6)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1349">8630 (0x21B6)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1350">Se denegó la solicitud de replicación de secretos.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1350">The request to replicate secrets is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1351"><span id="ERROR_DS_RESERVED_MAPI_ID"></span><span id="error_ds_reserved_mapi_id"></span>**ERROR \_ de \_ \_ ID. de MAPI reservado de DS \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1351"><span id="ERROR_DS_RESERVED_MAPI_ID"></span><span id="error_ds_reserved_mapi_id"></span>**ERROR\_DS\_RESERVED\_MAPI\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1352">8631 (0x21B7)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1352">8631 (0x21B7)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1353">No se pudo actualizar el esquema: el identificador de MAPI está reservado.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1353">Schema update failed: The MAPI identifier is reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1354"><span id="ERROR_DS_MAPI_ID_NOT_AVAILABLE"></span><span id="error_ds_mapi_id_not_available"></span>**ERROR \_ de \_ ID. de MAPI de DS \_ \_ no \_ disponible**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1354"><span id="ERROR_DS_MAPI_ID_NOT_AVAILABLE"></span><span id="error_ds_mapi_id_not_available"></span>**ERROR\_DS\_MAPI\_ID\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1355">8632 (0x21B8)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1355">8632 (0x21B8)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1356">No se pudo actualizar el esquema: no hay identificadores de MAPI disponibles.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1356">Schema update failed: There are no MAPI identifiers available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1357"><span id="ERROR_DS_DRA_MISSING_KRBTGT_SECRET"></span><span id="error_ds_dra_missing_krbtgt_secret"></span>**ERROR \_ DS \_ Dra \_ falta \_ el \_ secreto de KRBTGT**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1357"><span id="ERROR_DS_DRA_MISSING_KRBTGT_SECRET"></span><span id="error_ds_dra_missing_krbtgt_secret"></span>**ERROR\_DS\_DRA\_MISSING\_KRBTGT\_SECRET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1358">8633 (0x21B9)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1358">8633 (0x21B9)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1359">No se pudo realizar la operación de replicación porque faltan los atributos necesarios del objeto krbtgt local.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1359">The replication operation failed because the required attributes of the local krbtgt object are missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1360"><span id="ERROR_DS_DOMAIN_NAME_EXISTS_IN_FOREST"></span><span id="error_ds_domain_name_exists_in_forest"></span>**ERROR \_ \_ \_ el nombre \_ de dominio \_ de DS existe en el \_ bosque**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1360"><span id="ERROR_DS_DOMAIN_NAME_EXISTS_IN_FOREST"></span><span id="error_ds_domain_name_exists_in_forest"></span>**ERROR\_DS\_DOMAIN\_NAME\_EXISTS\_IN\_FOREST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1361">8634 (0x21BA)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1361">8634 (0x21BA)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1362">El nombre de dominio del dominio de confianza ya existe en el bosque.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1362">The domain name of the trusted domain already exists in the forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1363"><span id="ERROR_DS_FLAT_NAME_EXISTS_IN_FOREST"></span><span id="error_ds_flat_name_exists_in_forest"></span>**ERROR \_ DS \_ \_ el nombre plano \_ existe en el \_ \_ bosque**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1363"><span id="ERROR_DS_FLAT_NAME_EXISTS_IN_FOREST"></span><span id="error_ds_flat_name_exists_in_forest"></span>**ERROR\_DS\_FLAT\_NAME\_EXISTS\_IN\_FOREST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1364">8635 (0x21BB)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1364">8635 (0x21BB)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1365">El nombre plano del dominio de confianza ya existe en el bosque.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1365">The flat name of the trusted domain already exists in the forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1366"><span id="ERROR_INVALID_USER_PRINCIPAL_NAME"></span><span id="error_invalid_user_principal_name"></span>**ERROR \_ de \_ \_ nombre principal de usuario no válido \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1366"><span id="ERROR_INVALID_USER_PRINCIPAL_NAME"></span><span id="error_invalid_user_principal_name"></span>**ERROR\_INVALID\_USER\_PRINCIPAL\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1367">8636 (0x21BC)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1367">8636 (0x21BC)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1368">El nombre principal de usuario (UPN) no es válido.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1368">The User Principal Name (UPN) is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1369"><span id="ERROR_DS_OID_MAPPED_GROUP_CANT_HAVE_MEMBERS"></span><span id="error_ds_oid_mapped_group_cant_have_members"></span>**ERROR \_ DS \_ OID \_ el \_ grupo asignado no \_ \_ tiene \_ miembros**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1369"><span id="ERROR_DS_OID_MAPPED_GROUP_CANT_HAVE_MEMBERS"></span><span id="error_ds_oid_mapped_group_cant_have_members"></span>**ERROR\_DS\_OID\_MAPPED\_GROUP\_CANT\_HAVE\_MEMBERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1370">8637 (0x21BD)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1370">8637 (0x21BD)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1371">Los grupos asignados OID no pueden tener miembros.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1371">OID mapped groups cannot have members.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1372"><span id="ERROR_DS_OID_NOT_FOUND"></span><span id="error_ds_oid_not_found"></span>**ERROR \_ DS \_ OID \_ no \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1372"><span id="ERROR_DS_OID_NOT_FOUND"></span><span id="error_ds_oid_not_found"></span>**ERROR\_DS\_OID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1373">8638 (0x21BE)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1373">8638 (0x21BE)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1374">No se encuentra el OID especificado.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1374">The specified OID cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1375"><span id="ERROR_DS_DRA_RECYCLED_TARGET"></span><span id="error_ds_dra_recycled_target"></span>**\_destino de \_ Dra \_ reciclado de DS de error \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1375"><span id="ERROR_DS_DRA_RECYCLED_TARGET"></span><span id="error_ds_dra_recycled_target"></span>**ERROR\_DS\_DRA\_RECYCLED\_TARGET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1376">8639 (0x21BF)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1376">8639 (0x21BF)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1377">No se pudo realizar la operación de replicación porque se recicla el objeto de destino al que hace referencia un valor de vínculo.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1377">The replication operation failed because the target object referred by a link value is recycled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1378"><span id="ERROR_DS_DISALLOWED_NC_REDIRECT"></span><span id="error_ds_disallowed_nc_redirect"></span>**ERROR \_ DS no \_ permitido \_ \_ redirección de NC**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1378"><span id="ERROR_DS_DISALLOWED_NC_REDIRECT"></span><span id="error_ds_disallowed_nc_redirect"></span>**ERROR\_DS\_DISALLOWED\_NC\_REDIRECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1379">8640 (0x21C0)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1379">8640 (0x21C0)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1380">No se pudo realizar la operación de redirección porque el objeto de destino está en un NC diferente del NC de dominio del controlador de dominio actual.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1380">The redirect operation failed because the target object is in a NC different from the domain NC of the current domain controller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1381"><span id="ERROR_DS_HIGH_ADLDS_FFL"></span><span id="error_ds_high_adlds_ffl"></span>**ERROR de \_ DS de \_ alta calidad \_ \_ FFL**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1381"><span id="ERROR_DS_HIGH_ADLDS_FFL"></span><span id="error_ds_high_adlds_ffl"></span>**ERROR\_DS\_HIGH\_ADLDS\_FFL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1382">8641 (0x21C1)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1382">8641 (0x21C1)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1383">El nivel funcional del conjunto de configuración AD LDS no puede reducirse al valor solicitado.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1383">The functional level of the AD LDS configuration set cannot be lowered to the requested value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1384"><span id="ERROR_DS_HIGH_DSA_VERSION"></span><span id="error_ds_high_dsa_version"></span>**ERROR \_ de \_ DS \_ versión de DSA alta \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1384"><span id="ERROR_DS_HIGH_DSA_VERSION"></span><span id="error_ds_high_dsa_version"></span>**ERROR\_DS\_HIGH\_DSA\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1385">8642 (0x21C2)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1385">8642 (0x21C2)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1386">El nivel funcional del dominio (o bosque) no puede reducirse al valor solicitado.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1386">The functional level of the domain (or forest) cannot be lowered to the requested value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1387"><span id="ERROR_DS_LOW_ADLDS_FFL"></span><span id="error_ds_low_adlds_ffl"></span>**ERROR \_ DS \_ Low-ad \_ \_ FFL**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1387"><span id="ERROR_DS_LOW_ADLDS_FFL"></span><span id="error_ds_low_adlds_ffl"></span>**ERROR\_DS\_LOW\_ADLDS\_FFL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1388">8643 (0x21C3)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1388">8643 (0x21C3)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1389">No se puede elevar el nivel funcional del conjunto de configuración AD LDS al valor solicitado porque existe una o más instancias de la instancia de este que se encuentran en un nivel funcional inferior incompatible.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1389">The functional level of the AD LDS configuration set cannot be raised to the requested value, because there exist one or more ADLDS instances that are at a lower incompatible functional level.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1390"><span id="ERROR_DOMAIN_SID_SAME_AS_LOCAL_WORKSTATION"></span><span id="error_domain_sid_same_as_local_workstation"></span>**\_ \_ SID de dominio \_ de error igual \_ que la \_ estación de \_ trabajo local**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1390"><span id="ERROR_DOMAIN_SID_SAME_AS_LOCAL_WORKSTATION"></span><span id="error_domain_sid_same_as_local_workstation"></span>**ERROR\_DOMAIN\_SID\_SAME\_AS\_LOCAL\_WORKSTATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1391">8644 (0x21C4)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1391">8644 (0x21C4)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1392">No se puede completar la Unión al dominio porque el SID del dominio al que intentó unirse era idéntico al SID de esta máquina.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1392">The domain join cannot be completed because the SID of the domain you attempted to join was identical to the SID of this machine.</span></span> <span data-ttu-id="3ad11-1393">Esto es un síntoma de una instalación de sistema operativo clonada incorrectamente.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1393">This is a symptom of an improperly cloned operating system install.</span></span> <span data-ttu-id="3ad11-1394">Debe ejecutar Sysprep en este equipo para poder generar un nuevo SID de equipo.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1394">You should run sysprep on this machine in order to generate a new machine SID.</span></span> <span data-ttu-id="3ad11-1395">Consulte <https://go.microsoft.com/fwlink/p/?linkid=168895> para más información.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1395">Please see <https://go.microsoft.com/fwlink/p/?linkid=168895> for more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1396"><span id="ERROR_DS_UNDELETE_SAM_VALIDATION_FAILED"></span><span id="error_ds_undelete_sam_validation_failed"></span>**ERROR de \_ validación de DS de \_ eliminación de \_ Sam \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1396"><span id="ERROR_DS_UNDELETE_SAM_VALIDATION_FAILED"></span><span id="error_ds_undelete_sam_validation_failed"></span>**ERROR\_DS\_UNDELETE\_SAM\_VALIDATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1397">8645 (0x21C5)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1397">8645 (0x21C5)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1398">No se pudo realizar la operación de eliminación porque el nombre de cuenta SAM o el nombre de cuenta SAM adicional del objeto que se va a recuperar entra en conflicto con un objeto activo existente.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1398">The undelete operation failed because the Sam Account Name or Additional Sam Account Name of the object being undeleted conflicts with an existing live object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ad11-1399"><span id="ERROR_INCORRECT_ACCOUNT_TYPE"></span><span id="error_incorrect_account_type"></span>**ERROR \_ de \_ tipo de cuenta incorrecto \_**</span><span class="sxs-lookup"><span data-stu-id="3ad11-1399"><span id="ERROR_INCORRECT_ACCOUNT_TYPE"></span><span id="error_incorrect_account_type"></span>**ERROR\_INCORRECT\_ACCOUNT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad11-1400">8646 (0x21C6)</span><span class="sxs-lookup"><span data-stu-id="3ad11-1400">8646 (0x21C6)</span></span>
</dt> <dt>



<span data-ttu-id="3ad11-1401">El sistema no es autoritativo para la cuenta especificada y, por lo tanto, no puede completar la operación.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1401">The system is not authoritative for the specified account and therefore cannot complete the operation.</span></span> <span data-ttu-id="3ad11-1402">Vuelva a intentar la operación con el proveedor asociado a esta cuenta.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1402">Please retry the operation using the provider associated with this account.</span></span> <span data-ttu-id="3ad11-1403">Si se trata de un proveedor en línea, use el sitio en línea del proveedor.</span><span class="sxs-lookup"><span data-stu-id="3ad11-1403">If this is an online provider please use the provider's online site.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="3ad11-1404">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ad11-1404">Requirements</span></span>



| <span data-ttu-id="3ad11-1405">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ad11-1405">Requirement</span></span> | <span data-ttu-id="3ad11-1406">Value</span><span class="sxs-lookup"><span data-stu-id="3ad11-1406">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3ad11-1407">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ad11-1407">Minimum supported client</span></span><br/> | <span data-ttu-id="3ad11-1408">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="3ad11-1408">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3ad11-1409">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ad11-1409">Minimum supported server</span></span><br/> | <span data-ttu-id="3ad11-1410">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="3ad11-1410">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3ad11-1411">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3ad11-1411">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ad11-1412"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ad11-1412"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ad11-1413">Vea también</span><span class="sxs-lookup"><span data-stu-id="3ad11-1413">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ad11-1414">Códigos de error del sistema</span><span class="sxs-lookup"><span data-stu-id="3ad11-1414">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




