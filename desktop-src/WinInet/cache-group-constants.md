---
title: Constantes de grupo de caché (Wininet. h)
description: La lista siguiente contiene las constantes utilizadas por las funciones de grupo de caché.
ms.assetid: 9ca2069e-497d-4747-acf4-d5b8020b8ab7
topic_type:
- apiref
api_name:
- CACHEGROUP_ATTRIBUTE_BASIC
- CACHEGROUP_ATTRIBUTE_FLAG
- CACHEGROUP_ATTRIBUTE_GET_ALL
- CACHEGROUP_ATTRIBUTE_GROUPNAME
- CACHEGROUP_ATTRIBUTE_QUOTA
- CACHEGROUP_ATTRIBUTE_STORAGE
- CACHEGROUP_ATTRIBUTE_TYPE
- CACHEGROUP_FLAG_FLUSHURL_ONDELETE
- CACHEGROUP_FLAG_GIDONLY
- CACHEGROUP_FLAG_NONPURGEABLE
- CACHEGROUP_READWRITE_MASK
- CACHEGROUP_SEARCH_ALL
- CACHEGROUP_SEARCH_BYURL
- CACHEGROUP_TYPE_INVALID
- GROUP_OWNER_STORAGE_SIZE
- GROUPNAME_MAX_LENGTH
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a08efa37ad78fa3351d12fa43491c7b62ee64af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714617"
---
# <a name="cache-group-constants"></a><span data-ttu-id="f073e-103">Constantes de grupo de caché</span><span class="sxs-lookup"><span data-stu-id="f073e-103">Cache Group Constants</span></span>

<span data-ttu-id="f073e-104">La lista siguiente contiene las constantes utilizadas por las funciones de grupo de caché.</span><span class="sxs-lookup"><span data-stu-id="f073e-104">The following list contains the constants used by the cache group functions.</span></span>

<dl> <dt>

<span data-ttu-id="f073e-105"><span id="CACHEGROUP_ATTRIBUTE_BASIC"></span><span id="cachegroup_attribute_basic"></span>**\_atributo CACHEGROUP \_ básico**</span><span class="sxs-lookup"><span data-stu-id="f073e-105"><span id="CACHEGROUP_ATTRIBUTE_BASIC"></span><span id="cachegroup_attribute_basic"></span>**CACHEGROUP\_ATTRIBUTE\_BASIC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f073e-106">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f073e-106">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="f073e-107">Recupera las marcas, el tipo y los atributos de cuota de disco del grupo de caché.</span><span class="sxs-lookup"><span data-stu-id="f073e-107">Retrieves the flags, type, and disk quota attributes of the cache group.</span></span> <span data-ttu-id="f073e-108">Lo utiliza la función [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) .</span><span class="sxs-lookup"><span data-stu-id="f073e-108">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f073e-109"><span id="CACHEGROUP_ATTRIBUTE_FLAG"></span><span id="cachegroup_attribute_flag"></span>**\_marca de atributo CACHEGROUP \_**</span><span class="sxs-lookup"><span data-stu-id="f073e-109"><span id="CACHEGROUP_ATTRIBUTE_FLAG"></span><span id="cachegroup_attribute_flag"></span>**CACHEGROUP\_ATTRIBUTE\_FLAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f073e-110">0x00000002</span><span class="sxs-lookup"><span data-stu-id="f073e-110">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="f073e-111">Establece o recupera las marcas asociadas al grupo de caché.</span><span class="sxs-lookup"><span data-stu-id="f073e-111">Sets or retrieves the flags associated with the cache group.</span></span> <span data-ttu-id="f073e-112">Lo usan las funciones [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) y [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .</span><span class="sxs-lookup"><span data-stu-id="f073e-112">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) and [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f073e-113"><span id="CACHEGROUP_ATTRIBUTE_GET_ALL"></span><span id="cachegroup_attribute_get_all"></span>**CACHEGROUP el \_ atributo \_ Get \_ All**</span><span class="sxs-lookup"><span data-stu-id="f073e-113"><span id="CACHEGROUP_ATTRIBUTE_GET_ALL"></span><span id="cachegroup_attribute_get_all"></span>**CACHEGROUP\_ATTRIBUTE\_GET\_ALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f073e-114">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="f073e-114">0xffffffff</span></span>
</dt> <dt>



<span data-ttu-id="f073e-115">Recupera todos los atributos del grupo de caché.</span><span class="sxs-lookup"><span data-stu-id="f073e-115">Retrieves all the attributes of the cache group.</span></span> <span data-ttu-id="f073e-116">Lo utiliza la función [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) .</span><span class="sxs-lookup"><span data-stu-id="f073e-116">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f073e-117"><span id="CACHEGROUP_ATTRIBUTE_GROUPNAME"></span><span id="cachegroup_attribute_groupname"></span>**CACHEGROUP \_ atributo \_ GROUPNAME**</span><span class="sxs-lookup"><span data-stu-id="f073e-117"><span id="CACHEGROUP_ATTRIBUTE_GROUPNAME"></span><span id="cachegroup_attribute_groupname"></span>**CACHEGROUP\_ATTRIBUTE\_GROUPNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f073e-118">0x000000010</span><span class="sxs-lookup"><span data-stu-id="f073e-118">0x000000010</span></span>
</dt> <dt>



<span data-ttu-id="f073e-119">Establece o recupera el nombre de grupo del grupo de caché.</span><span class="sxs-lookup"><span data-stu-id="f073e-119">Sets or retrieves the group name of the cache group.</span></span> <span data-ttu-id="f073e-120">Lo usan las funciones [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) y [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .</span><span class="sxs-lookup"><span data-stu-id="f073e-120">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) and [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f073e-121"><span id="CACHEGROUP_ATTRIBUTE_QUOTA"></span><span id="cachegroup_attribute_quota"></span>**\_cuota de atributo CACHEGROUP \_**</span><span class="sxs-lookup"><span data-stu-id="f073e-121"><span id="CACHEGROUP_ATTRIBUTE_QUOTA"></span><span id="cachegroup_attribute_quota"></span>**CACHEGROUP\_ATTRIBUTE\_QUOTA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f073e-122">0x00000008</span><span class="sxs-lookup"><span data-stu-id="f073e-122">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="f073e-123">Establece o recupera la cuota de disco asociada con el grupo de caché.</span><span class="sxs-lookup"><span data-stu-id="f073e-123">Sets or retrieves the disk quota associated with the cache group.</span></span> <span data-ttu-id="f073e-124">Lo usan las funciones [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) y [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .</span><span class="sxs-lookup"><span data-stu-id="f073e-124">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) and [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f073e-125"><span id="CACHEGROUP_ATTRIBUTE_STORAGE"></span><span id="cachegroup_attribute_storage"></span>**\_almacenamiento de atributos de CACHEGROUP \_**</span><span class="sxs-lookup"><span data-stu-id="f073e-125"><span id="CACHEGROUP_ATTRIBUTE_STORAGE"></span><span id="cachegroup_attribute_storage"></span>**CACHEGROUP\_ATTRIBUTE\_STORAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f073e-126">0x00000020</span><span class="sxs-lookup"><span data-stu-id="f073e-126">0x00000020</span></span>
</dt> <dt>



<span data-ttu-id="f073e-127">Establece o recupera el almacenamiento del propietario del grupo asociado al grupo de caché.</span><span class="sxs-lookup"><span data-stu-id="f073e-127">Sets or retrieves the group owner storage associated with the cache group.</span></span> <span data-ttu-id="f073e-128">Lo usan las funciones [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) y [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .</span><span class="sxs-lookup"><span data-stu-id="f073e-128">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) and [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f073e-129"><span id="CACHEGROUP_ATTRIBUTE_TYPE"></span><span id="cachegroup_attribute_type"></span>**\_tipo de atributo CACHEGROUP \_**</span><span class="sxs-lookup"><span data-stu-id="f073e-129"><span id="CACHEGROUP_ATTRIBUTE_TYPE"></span><span id="cachegroup_attribute_type"></span>**CACHEGROUP\_ATTRIBUTE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f073e-130">0x00000004</span><span class="sxs-lookup"><span data-stu-id="f073e-130">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="f073e-131">Establece o recupera el tipo de grupo de caché.</span><span class="sxs-lookup"><span data-stu-id="f073e-131">Sets or retrieves the cache group type.</span></span> <span data-ttu-id="f073e-132">Lo usan las funciones [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) y [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .</span><span class="sxs-lookup"><span data-stu-id="f073e-132">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) and [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f073e-133"><span id="CACHEGROUP_FLAG_FLUSHURL_ONDELETE"></span><span id="cachegroup_flag_flushurl_ondelete"></span>**\_marca CACHEGROUP \_ FLUSHURL \_ aleliminar**</span><span class="sxs-lookup"><span data-stu-id="f073e-133"><span id="CACHEGROUP_FLAG_FLUSHURL_ONDELETE"></span><span id="cachegroup_flag_flushurl_ondelete"></span>**CACHEGROUP\_FLAG\_FLUSHURL\_ONDELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f073e-134">0x00000002</span><span class="sxs-lookup"><span data-stu-id="f073e-134">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="f073e-135">Indica que se deben eliminar todas las entradas de caché asociadas al grupo de caché, a menos que la entrada pertenezca a otro grupo de caché.</span><span class="sxs-lookup"><span data-stu-id="f073e-135">Indicates that all the cache entries associated with the cache group should be deleted, unless the entry belongs to another cache group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f073e-136"><span id="CACHEGROUP_FLAG_GIDONLY"></span><span id="cachegroup_flag_gidonly"></span>**CACHEGROUP \_ marca \_ GIDONLY**</span><span class="sxs-lookup"><span data-stu-id="f073e-136"><span id="CACHEGROUP_FLAG_GIDONLY"></span><span id="cachegroup_flag_gidonly"></span>**CACHEGROUP\_FLAG\_GIDONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f073e-137">0x00000004</span><span class="sxs-lookup"><span data-stu-id="f073e-137">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="f073e-138">Indica que la función solo debe crear un GROUPID único para el grupo de caché y no crear el grupo real.</span><span class="sxs-lookup"><span data-stu-id="f073e-138">Indicates that the function should only create a unique GROUPID for the cache group and not create the actual group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f073e-139"><span id="CACHEGROUP_FLAG_NONPURGEABLE"></span><span id="cachegroup_flag_nonpurgeable"></span>**marca CACHEGROUP no \_ \_ purgable**</span><span class="sxs-lookup"><span data-stu-id="f073e-139"><span id="CACHEGROUP_FLAG_NONPURGEABLE"></span><span id="cachegroup_flag_nonpurgeable"></span>**CACHEGROUP\_FLAG\_NONPURGEABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f073e-140">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f073e-140">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="f073e-141">Indica que no se puede purgar el grupo de caché.</span><span class="sxs-lookup"><span data-stu-id="f073e-141">Indicates that the cache group cannot be purged.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f073e-142"><span id="CACHEGROUP_READWRITE_MASK"></span><span id="cachegroup_readwrite_mask"></span>**\_máscara ReadWrite de CACHEGROUP \_**</span><span class="sxs-lookup"><span data-stu-id="f073e-142"><span id="CACHEGROUP_READWRITE_MASK"></span><span id="cachegroup_readwrite_mask"></span>**CACHEGROUP\_READWRITE\_MASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f073e-143">0x0000003c</span><span class="sxs-lookup"><span data-stu-id="f073e-143">0x0000003c</span></span>
</dt> <dt>



<span data-ttu-id="f073e-144">Establece el tipo, la cuota de disco, el nombre de grupo y los atributos de almacenamiento propietario del grupo de caché.</span><span class="sxs-lookup"><span data-stu-id="f073e-144">Sets the type, disk quota, group name, and owner storage attributes of the cache group.</span></span> <span data-ttu-id="f073e-145">Lo utiliza la función [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .</span><span class="sxs-lookup"><span data-stu-id="f073e-145">This is used by the [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f073e-146"><span id="CACHEGROUP_SEARCH_ALL"></span><span id="cachegroup_search_all"></span>**CACHEGROUP \_ Buscar \_ todo**</span><span class="sxs-lookup"><span data-stu-id="f073e-146"><span id="CACHEGROUP_SEARCH_ALL"></span><span id="cachegroup_search_all"></span>**CACHEGROUP\_SEARCH\_ALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f073e-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f073e-147">0x00000000</span></span>
</dt> <dt>



<span data-ttu-id="f073e-148">Indica que se deben enumerar todos los grupos de caché del sistema del usuario.</span><span class="sxs-lookup"><span data-stu-id="f073e-148">Indicates that all of the cache groups in the user's system should be enumerated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f073e-149"><span id="CACHEGROUP_SEARCH_BYURL"></span><span id="cachegroup_search_byurl"></span>**CACHEGROUP \_ Search \_ BYURL**</span><span class="sxs-lookup"><span data-stu-id="f073e-149"><span id="CACHEGROUP_SEARCH_BYURL"></span><span id="cachegroup_search_byurl"></span>**CACHEGROUP\_SEARCH\_BYURL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f073e-150">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f073e-150">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="f073e-151">No implementado actualmente.</span><span class="sxs-lookup"><span data-stu-id="f073e-151">Not currently implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f073e-152"><span id="CACHEGROUP_TYPE_INVALID"></span><span id="cachegroup_type_invalid"></span>**tipo de CACHEGROUP \_ \_ no válido**</span><span class="sxs-lookup"><span data-stu-id="f073e-152"><span id="CACHEGROUP_TYPE_INVALID"></span><span id="cachegroup_type_invalid"></span>**CACHEGROUP\_TYPE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f073e-153">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f073e-153">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="f073e-154">Indica que el tipo de grupo de caché no es válido.</span><span class="sxs-lookup"><span data-stu-id="f073e-154">Indicates that the cache group type is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f073e-155"><span id="GROUP_OWNER_STORAGE_SIZE"></span><span id="group_owner_storage_size"></span>**\_tamaño de \_ almacenamiento del propietario del grupo \_**</span><span class="sxs-lookup"><span data-stu-id="f073e-155"><span id="GROUP_OWNER_STORAGE_SIZE"></span><span id="group_owner_storage_size"></span>**GROUP\_OWNER\_STORAGE\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f073e-156">0x00000004</span><span class="sxs-lookup"><span data-stu-id="f073e-156">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="f073e-157">Longitud de la matriz de almacenamiento del propietario del grupo.</span><span class="sxs-lookup"><span data-stu-id="f073e-157">Length of the group owner storage array.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f073e-158"><span id="GROUPNAME_MAX_LENGTH"></span><span id="groupname_max_length"></span>**\_longitud máxima de nombre_grupo \_**</span><span class="sxs-lookup"><span data-stu-id="f073e-158"><span id="GROUPNAME_MAX_LENGTH"></span><span id="groupname_max_length"></span>**GROUPNAME\_MAX\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f073e-159">0x00000078</span><span class="sxs-lookup"><span data-stu-id="f073e-159">0x00000078</span></span>
</dt> <dt>



<span data-ttu-id="f073e-160">Número máximo de caracteres permitidos para un nombre de grupo de caché.</span><span class="sxs-lookup"><span data-stu-id="f073e-160">Maximum number of characters allowed for a cache group name.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f073e-161">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f073e-161">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f073e-162">WinINet no admite implementaciones de servidor.</span><span class="sxs-lookup"><span data-stu-id="f073e-162">WinINet does not support server implementations.</span></span> <span data-ttu-id="f073e-163">Además, no se debe usar desde un servicio.</span><span class="sxs-lookup"><span data-stu-id="f073e-163">In addition, it should not be used from a service.</span></span> <span data-ttu-id="f073e-164">En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="f073e-164">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f073e-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f073e-165">Requirements</span></span>



| <span data-ttu-id="f073e-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="f073e-166">Requirement</span></span> | <span data-ttu-id="f073e-167">Value</span><span class="sxs-lookup"><span data-stu-id="f073e-167">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f073e-168">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f073e-168">Minimum supported client</span></span><br/> | <span data-ttu-id="f073e-169">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f073e-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f073e-170">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f073e-170">Minimum supported server</span></span><br/> | <span data-ttu-id="f073e-171">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f073e-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f073e-172">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f073e-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="f073e-173"><dt>Wininet. h</dt></span><span class="sxs-lookup"><span data-stu-id="f073e-173"><dt>Wininet.h</dt></span></span> </dl> |



 

