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
# <a name="cache-group-constants"></a>Constantes de grupo de caché

La lista siguiente contiene las constantes utilizadas por las funciones de grupo de caché.

<dl> <dt>

<span id="CACHEGROUP_ATTRIBUTE_BASIC"></span><span id="cachegroup_attribute_basic"></span>**\_atributo CACHEGROUP \_ básico**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Recupera las marcas, el tipo y los atributos de cuota de disco del grupo de caché. Lo utiliza la función [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) .


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_FLAG"></span><span id="cachegroup_attribute_flag"></span>**\_marca de atributo CACHEGROUP \_**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Establece o recupera las marcas asociadas al grupo de caché. Lo usan las funciones [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) y [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_GET_ALL"></span><span id="cachegroup_attribute_get_all"></span>**CACHEGROUP el \_ atributo \_ Get \_ All**
</dt> <dd> <dl> <dt>

0xFFFFFFFF
</dt> <dt>



Recupera todos los atributos del grupo de caché. Lo utiliza la función [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) .


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_GROUPNAME"></span><span id="cachegroup_attribute_groupname"></span>**CACHEGROUP \_ atributo \_ GROUPNAME**
</dt> <dd> <dl> <dt>

0x000000010
</dt> <dt>



Establece o recupera el nombre de grupo del grupo de caché. Lo usan las funciones [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) y [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_QUOTA"></span><span id="cachegroup_attribute_quota"></span>**\_cuota de atributo CACHEGROUP \_**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Establece o recupera la cuota de disco asociada con el grupo de caché. Lo usan las funciones [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) y [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_STORAGE"></span><span id="cachegroup_attribute_storage"></span>**\_almacenamiento de atributos de CACHEGROUP \_**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Establece o recupera el almacenamiento del propietario del grupo asociado al grupo de caché. Lo usan las funciones [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) y [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_TYPE"></span><span id="cachegroup_attribute_type"></span>**\_tipo de atributo CACHEGROUP \_**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Establece o recupera el tipo de grupo de caché. Lo usan las funciones [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) y [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_FLAG_FLUSHURL_ONDELETE"></span><span id="cachegroup_flag_flushurl_ondelete"></span>**\_marca CACHEGROUP \_ FLUSHURL \_ aleliminar**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Indica que se deben eliminar todas las entradas de caché asociadas al grupo de caché, a menos que la entrada pertenezca a otro grupo de caché.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_FLAG_GIDONLY"></span><span id="cachegroup_flag_gidonly"></span>**CACHEGROUP \_ marca \_ GIDONLY**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Indica que la función solo debe crear un GROUPID único para el grupo de caché y no crear el grupo real.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_FLAG_NONPURGEABLE"></span><span id="cachegroup_flag_nonpurgeable"></span>**marca CACHEGROUP no \_ \_ purgable**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Indica que no se puede purgar el grupo de caché.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_READWRITE_MASK"></span><span id="cachegroup_readwrite_mask"></span>**\_máscara ReadWrite de CACHEGROUP \_**
</dt> <dd> <dl> <dt>

0x0000003c
</dt> <dt>



Establece el tipo, la cuota de disco, el nombre de grupo y los atributos de almacenamiento propietario del grupo de caché. Lo utiliza la función [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_SEARCH_ALL"></span><span id="cachegroup_search_all"></span>**CACHEGROUP \_ Buscar \_ todo**
</dt> <dd> <dl> <dt>

0x00000000
</dt> <dt>



Indica que se deben enumerar todos los grupos de caché del sistema del usuario.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_SEARCH_BYURL"></span><span id="cachegroup_search_byurl"></span>**CACHEGROUP \_ Search \_ BYURL**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



No implementado actualmente.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_TYPE_INVALID"></span><span id="cachegroup_type_invalid"></span>**tipo de CACHEGROUP \_ \_ no válido**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Indica que el tipo de grupo de caché no es válido.


</dt> </dl> </dd> <dt>

<span id="GROUP_OWNER_STORAGE_SIZE"></span><span id="group_owner_storage_size"></span>**\_tamaño de \_ almacenamiento del propietario del grupo \_**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Longitud de la matriz de almacenamiento del propietario del grupo.


</dt> </dl> </dd> <dt>

<span id="GROUPNAME_MAX_LENGTH"></span><span id="groupname_max_length"></span>**\_longitud máxima de nombre_grupo \_**
</dt> <dd> <dl> <dt>

0x00000078
</dt> <dt>



Número máximo de caracteres permitidos para un nombre de grupo de caché.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

> [!Note]  
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Wininet. h</dt> </dl> |



 

