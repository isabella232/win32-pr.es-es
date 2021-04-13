---
description: Códigos de retorno de WMI que indican el estado y no indican un error.
ms.assetid: 36faa3fb-9496-47ca-bdba-f8eb52a06ff7
ms.tgt_platform: multiple
title: Constantes que no son de error de WMI (WbemCli. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0880c9fda00f03c1fa8b174242bfc84ed9d75ad8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276251"
---
# <a name="wmi-non-error-constants"></a><span data-ttu-id="2f106-103">Constantes que no son de error de WMI</span><span class="sxs-lookup"><span data-stu-id="2f106-103">WMI Non-Error Constants</span></span>

<span data-ttu-id="2f106-104">Códigos de retorno de WMI que indican el estado y no indican un error.</span><span class="sxs-lookup"><span data-stu-id="2f106-104">WMI return codes that indicate status and do not indicate an error.</span></span>

<span data-ttu-id="2f106-105">Si una operación no produce un error, WMI devuelve uno de los códigos siguientes como **HRESULT** que indica el estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="2f106-105">If an operation does not result in an error, WMI returns one of the following codes as an **HRESULT** that indicates the status of the operation.</span></span>

> [!Note]  
> <span data-ttu-id="2f106-106">Algunos métodos de las clases WMI pueden devolver códigos de error del sistema y de la red (por ejemplo, 64).</span><span class="sxs-lookup"><span data-stu-id="2f106-106">Some methods in WMI classes can return system and network error codes (64 for example).</span></span> <span data-ttu-id="2f106-107">Puede comprobar la definición de estos tipos de códigos de error mediante el comando **net helpmsg** en la ventana del símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="2f106-107">You can check the definition of these types of error codes by using the **net helpmsg** command in the command prompt window.</span></span> <span data-ttu-id="2f106-108">Por ejemplo, el comando **net helpmsg 64** devuelve el mensaje: el nombre de red especificado ya no está disponible.</span><span class="sxs-lookup"><span data-stu-id="2f106-108">For example, the command **net helpmsg 64** returns the message: The specified network name is no longer available.</span></span>

 

<span data-ttu-id="2f106-109">En C++, puede llamar a [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) y especificar **C: \\ Windows \\ system32 \\ WBEM \\wmiutils.dll** como el módulo de mensajes.</span><span class="sxs-lookup"><span data-stu-id="2f106-109">In C++, you can call [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) and specify **C:\\Windows\\System32\\wbem\\wmiutils.dll** as the message module.</span></span>

<dl> <dt>

<span data-ttu-id="2f106-110"><span id="WBEM_S_NO_ERROR"></span><span id="wbem_s_no_error"></span>**NO se ha podido obtener \_ \_ un \_ error de WBEM**</span><span class="sxs-lookup"><span data-stu-id="2f106-110"><span id="WBEM_S_NO_ERROR"></span><span id="wbem_s_no_error"></span>**WBEM\_S\_NO\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f106-111">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="2f106-111">0 (0x0)</span></span>
</dt> <dt>



<span data-ttu-id="2f106-112">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="2f106-112">The operation was successful.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2f106-113"><span id="WBEM_S_FALSE"></span><span id="wbem_s_false"></span>**WBEM \_ S \_ falso**</span><span class="sxs-lookup"><span data-stu-id="2f106-113"><span id="WBEM_S_FALSE"></span><span id="wbem_s_false"></span>**WBEM\_S\_FALSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f106-114">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="2f106-114">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="2f106-115">No hay más objetos disponibles, el número de objetos devueltos es menor que el número solicitado o es el final de una enumeración.</span><span class="sxs-lookup"><span data-stu-id="2f106-115">No more objects are available, the number of objects returned is less than the number requested, or this is the end of an enumeration.</span></span> <span data-ttu-id="2f106-116">También se devuelve este valor cuando se llama a este método con un valor de 0 para el parámetro *uCount* .</span><span class="sxs-lookup"><span data-stu-id="2f106-116">This value is also returned when this method is called with a value of 0 for the *uCount* parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2f106-117"><span id="WBEM_S_ALREADY_EXISTS"></span><span id="wbem_s_already_exists"></span>**WBEM \_ S \_ ya \_ existe**</span><span class="sxs-lookup"><span data-stu-id="2f106-117"><span id="WBEM_S_ALREADY_EXISTS"></span><span id="wbem_s_already_exists"></span>**WBEM\_S\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f106-118">262145 (0x40001)</span><span class="sxs-lookup"><span data-stu-id="2f106-118">262145 (0x40001)</span></span>
</dt> <dt>



<span data-ttu-id="2f106-119">Se intentó crear un objeto o una clase que ya existe.</span><span class="sxs-lookup"><span data-stu-id="2f106-119">An attempt was made to create an object or class that already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2f106-120"><span id="WBEM_S_RESET_TO_DEFAULT"></span><span id="wbem_s_reset_to_default"></span>**\_ \_ \_ configuración predeterminada de WBEM \_ S**</span><span class="sxs-lookup"><span data-stu-id="2f106-120"><span id="WBEM_S_RESET_TO_DEFAULT"></span><span id="wbem_s_reset_to_default"></span>**WBEM\_S\_RESET\_TO\_DEFAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f106-121">262146 (0x40002)</span><span class="sxs-lookup"><span data-stu-id="2f106-121">262146 (0x40002)</span></span>
</dt> <dt>



<span data-ttu-id="2f106-122">Se eliminó una propiedad reemplazada.</span><span class="sxs-lookup"><span data-stu-id="2f106-122">An overridden property was deleted.</span></span> <span data-ttu-id="2f106-123">Se devuelve este valor para indicar que se ha restaurado el valor original no reemplazado como resultado de la eliminación.</span><span class="sxs-lookup"><span data-stu-id="2f106-123">This value is returned to signal that the original non-overridden value has been restored as a result of the deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2f106-124"><span id="WBEM_S_DIFFERENT"></span><span id="wbem_s_different"></span>**WBEM \_ S \_ diferente**</span><span class="sxs-lookup"><span data-stu-id="2f106-124"><span id="WBEM_S_DIFFERENT"></span><span id="wbem_s_different"></span>**WBEM\_S\_DIFFERENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f106-125">262147 (0x40003)</span><span class="sxs-lookup"><span data-stu-id="2f106-125">262147 (0x40003)</span></span>
</dt> <dt>



<span data-ttu-id="2f106-126">Los elementos (objetos, clases, etc.) que se están comparando no son idénticos.</span><span class="sxs-lookup"><span data-stu-id="2f106-126">The items (objects, classes, and so on) that are being compared are not identical.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2f106-127"><span id="WBEM_S_TIMEDOUT"></span><span id="wbem_s_timedout"></span>**\_S. \_**</span><span class="sxs-lookup"><span data-stu-id="2f106-127"><span id="WBEM_S_TIMEDOUT"></span><span id="wbem_s_timedout"></span>**WBEM\_S\_TIMEDOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f106-128">262148 (0x40004)</span><span class="sxs-lookup"><span data-stu-id="2f106-128">262148 (0x40004)</span></span>
</dt> <dt>



<span data-ttu-id="2f106-129">Se agotó el tiempo de espera de una llamada. No se trata de una condición de error.</span><span class="sxs-lookup"><span data-stu-id="2f106-129">A call timed out. This is not an error condition.</span></span> <span data-ttu-id="2f106-130">Por lo tanto, es posible que también se hayan devuelto algunos resultados.</span><span class="sxs-lookup"><span data-stu-id="2f106-130">Therefore, some results may have also been returned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2f106-131"><span id="WBEM_S_NO_MORE_DATA"></span><span id="wbem_s_no_more_data"></span>**WBEM \_ S \_ no hay \_ más \_ datos**</span><span class="sxs-lookup"><span data-stu-id="2f106-131"><span id="WBEM_S_NO_MORE_DATA"></span><span id="wbem_s_no_more_data"></span>**WBEM\_S\_NO\_MORE\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f106-132">262149 (0x40005)</span><span class="sxs-lookup"><span data-stu-id="2f106-132">262149 (0x40005)</span></span>
</dt> <dt>



<span data-ttu-id="2f106-133">No hay más datos disponibles en la enumeración y el usuario debe finalizar la enumeración.</span><span class="sxs-lookup"><span data-stu-id="2f106-133">No more data is available from the enumeration, and the user must terminate the enumeration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2f106-134"><span id="WBEM_S_OPERATION_CANCELLED"></span><span id="wbem_s_operation_cancelled"></span>**\_operación S de WBEM \_ \_ cancelada**</span><span class="sxs-lookup"><span data-stu-id="2f106-134"><span id="WBEM_S_OPERATION_CANCELLED"></span><span id="wbem_s_operation_cancelled"></span>**WBEM\_S\_OPERATION\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f106-135">262150 (0x40006)</span><span class="sxs-lookup"><span data-stu-id="2f106-135">262150 (0x40006)</span></span>
</dt> <dt>



<span data-ttu-id="2f106-136">La operación se canceló de manera intencionada o accidental.</span><span class="sxs-lookup"><span data-stu-id="2f106-136">The operation was intentionally or unintentionally canceled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2f106-137"><span id="WBEM_S_PENDING"></span><span id="wbem_s_pending"></span>**WBEM \_ S \_ pendientes**</span><span class="sxs-lookup"><span data-stu-id="2f106-137"><span id="WBEM_S_PENDING"></span><span id="wbem_s_pending"></span>**WBEM\_S\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f106-138">262151 (0x40007)</span><span class="sxs-lookup"><span data-stu-id="2f106-138">262151 (0x40007)</span></span>
</dt> <dt>



<span data-ttu-id="2f106-139">Todavía hay una solicitud en curso y los resultados aún no están disponibles.</span><span class="sxs-lookup"><span data-stu-id="2f106-139">A request is still in progress, and the results are not yet available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2f106-140"><span id="WBEM_S_DUPLICATE_OBJECTS"></span><span id="wbem_s_duplicate_objects"></span>**\_ \_ objetos duplicados de WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="2f106-140"><span id="WBEM_S_DUPLICATE_OBJECTS"></span><span id="wbem_s_duplicate_objects"></span>**WBEM\_S\_DUPLICATE\_OBJECTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f106-141">262152 (0x40008)</span><span class="sxs-lookup"><span data-stu-id="2f106-141">262152 (0x40008)</span></span>
</dt> <dt>



<span data-ttu-id="2f106-142">Se detectó más de una copia del mismo objeto en el conjunto de resultados de una enumeración.</span><span class="sxs-lookup"><span data-stu-id="2f106-142">More than one copy of the same object was detected in the result set of an enumeration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2f106-143"><span id="WBEM_S_ACCESS_DENIED"></span><span id="wbem_s_access_denied"></span>**\_ \_ acceso \_ denegado a WBEM**</span><span class="sxs-lookup"><span data-stu-id="2f106-143"><span id="WBEM_S_ACCESS_DENIED"></span><span id="wbem_s_access_denied"></span>**WBEM\_S\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f106-144">262153 (0x40009)</span><span class="sxs-lookup"><span data-stu-id="2f106-144">262153 (0x40009)</span></span>
</dt> <dt>



<span data-ttu-id="2f106-145">Al usuario se le denegó el acceso a algunos, pero no a todos los recursos.</span><span class="sxs-lookup"><span data-stu-id="2f106-145">The user was denied access to some but not all resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2f106-146"><span id="WBEM_S_PARTIAL_RESULTS"></span><span id="wbem_s_partial_results"></span>**\_ \_ resultados parciales de WBEM S \_**</span><span class="sxs-lookup"><span data-stu-id="2f106-146"><span id="WBEM_S_PARTIAL_RESULTS"></span><span id="wbem_s_partial_results"></span>**WBEM\_S\_PARTIAL\_RESULTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f106-147">262160 (0x40010)</span><span class="sxs-lookup"><span data-stu-id="2f106-147">262160 (0x40010)</span></span>
</dt> <dt>



<span data-ttu-id="2f106-148">El usuario no recibió todos los objetos solicitados debido a recursos inaccesibles (distintos de las infracciones de seguridad).</span><span class="sxs-lookup"><span data-stu-id="2f106-148">The user did not receive all of the objects requested due to inaccessible resources (other than security violations).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2f106-149"><span id="WBEM_S_LIMITED_SERVICE"></span><span id="wbem_s_limited_service"></span>**\_ \_ servicio limitado de WBEM S \_**</span><span class="sxs-lookup"><span data-stu-id="2f106-149"><span id="WBEM_S_LIMITED_SERVICE"></span><span id="wbem_s_limited_service"></span>**WBEM\_S\_LIMITED\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f106-150">274433 (0x43001)</span><span class="sxs-lookup"><span data-stu-id="2f106-150">274433 (0x43001)</span></span>
</dt> <dt>



<span data-ttu-id="2f106-151">El proveedor es capaz de ofrecer un servicio limitado.</span><span class="sxs-lookup"><span data-stu-id="2f106-151">The provider is capable of limited service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2f106-152"><span id="WBEM_S_INDIRECTLY_UPDATED"></span><span id="wbem_s_indirectly_updated"></span>**WBEM \_ S \_ actualizado indirectamente \_**</span><span class="sxs-lookup"><span data-stu-id="2f106-152"><span id="WBEM_S_INDIRECTLY_UPDATED"></span><span id="wbem_s_indirectly_updated"></span>**WBEM\_S\_INDIRECTLY\_UPDATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f106-153">274434 (0x43002)</span><span class="sxs-lookup"><span data-stu-id="2f106-153">274434 (0x43002)</span></span>
</dt> <dt>



<span data-ttu-id="2f106-154">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="2f106-154">Reserved for future use.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2f106-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f106-155">Requirements</span></span>



| <span data-ttu-id="2f106-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f106-156">Requirement</span></span> | <span data-ttu-id="2f106-157">Value</span><span class="sxs-lookup"><span data-stu-id="2f106-157">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f106-158">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f106-158">Minimum supported client</span></span><br/> | <span data-ttu-id="2f106-159">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2f106-159">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="2f106-160">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f106-160">Minimum supported server</span></span><br/> | <span data-ttu-id="2f106-161">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2f106-161">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="2f106-162">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2f106-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f106-163"><dt>WbemCli. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f106-163"><dt>WbemCli.h</dt></span></span> </dl>   |
| <span data-ttu-id="2f106-164">IDL</span><span class="sxs-lookup"><span data-stu-id="2f106-164">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2f106-165"><dt>WbemCli. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2f106-165"><dt>WbemCli.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f106-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f106-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f106-167">Códigos de retorno de WMI</span><span class="sxs-lookup"><span data-stu-id="2f106-167">WMI Return Codes</span></span>](wmi-return-codes.md)
</dt> </dl>

 

