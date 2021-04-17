---
description: La estructura ADDRESSPAIR crea un filtro de captura.
ms.assetid: 0dd2bcaa-5e0f-448f-969e-14b923a01a2f
title: Estructura ADDRESSPAIR (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDRESSPAIR
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 7960a8bb1c3ed1b2fc86c93f371b2f05d299b97b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667744"
---
# <a name="addresspair-structure"></a>Estructura ADDRESSPAIR

La estructura **ADDRESSPAIR** crea un filtro de captura.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _ADDRESSPAIR {
  WORD    AddressFlags;
  WORD    NalReserved;
  ADDRESS DstAddress;
  ADDRESS SrcAddress;
} ADDRESSPAIR, *LPADDRESSPAIR;
```



## <a name="members"></a>Miembros

<dl> <dt>

**AddressFlags**
</dt> <dd>

Marcas que describen las direcciones utilizadas por un filtro de captura. Vea Comentarios para obtener más información.



| Value                                                                                                                                                                                                         | Significado                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="ADDRESS_FLAGS_MATCH_DST"></span><span id="address_flags_match_dst"></span><dl> <dt>**marcas de dirección \_ \_ Match \_ DST**</dt> </dl>                 | Coincide con la dirección de destino.<br/>                              |
| <span id="ADDRESS_FLAGS_MATCH_SRC"></span><span id="address_flags_match_src"></span><dl> <dt>**coincidencia de marcas de dirección \_ \_ \_ src**</dt> </dl>                 | Coincide con la dirección de origen.<br/>                                   |
| <span id="ADDRESS_FLAGS_EXCLUDED"></span><span id="address_flags_excluded"></span><dl> <dt>**marcas de dirección \_ \_ excluidas**</dt> </dl>                     | Excluye el marco si se encuentra esta dirección.<br/>                  |
| <span id="ADDRESS_FLAGS_DST_GROUP_ADDR"></span><span id="address_flags_dst_group_addr"></span><dl> <dt>**marcas de dirección \_ \_ grupo de DST \_ \_**</dt> </dl> | Coincide solo con el bit de grupo. Utilice esto para los mensajes de tipo difusión.<br/> |
| <span id="ADDRESS_FLAGS_MATCH_BOTH"></span><span id="address_flags_match_both"></span><dl> <dt>**las \_ marcas de dirección \_ coinciden con \_ ambas**</dt> </dl>              | Coincide con las direcciones de destino y de origen.<br/>                     |



 

</dd> <dt>

**NalReserved**
</dt> <dd>

Está reservada.

</dd> <dt>

**DstAddress**
</dt> <dd>

Dirección de destino del elemento de par de direcciones.

</dd> <dt>

**SrcAddress**
</dt> <dd>

Dirección de origen del elemento de par de direcciones.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las marcas del miembro **AddressFlags** se pueden combinar. Por ejemplo, la siguiente configuración excluye el marco si se detecta la dirección de origen especificada.

``` syntax
ADDRESS_FLAGS_MATCH_SOURCE|ADDRESS_FLAGS_EXCLUDED
```

Para obtener más información sobre la implementación de esta estructura, vea [Capture filters](capture-filters.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[CAPTUREFILTER](capturefilter.md)
</dt> </dl>

 

 




