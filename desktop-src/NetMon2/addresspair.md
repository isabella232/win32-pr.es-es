---
description: La estructura ADDRESSPAIR crea un filtro de captura.
ms.assetid: 0dd2bcaa-5e0f-448f-969e-14b923a01a2f
title: Estructura ADDRESSPAIR (Netmon.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074176"
---
# <a name="addresspair-structure"></a>AddressPAIR (estructura)

La **estructura ADDRESSPAIR** crea un filtro de captura.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _ADDRESSPAIR {
  WORD    AddressFlags;
  WORD    NalReserved;
  ADDRESS DstAddress;
  ADDRESS SrcAddress;
} ADDRESSPAIR, *LPADDRESSPAIR;
```



## <a name="members"></a>Members

<dl> <dt>

**AddressFlags**
</dt> <dd>

Marcas que describen las direcciones usadas por un filtro de captura. Vea Comentarios para obtener más información.



| Value                                                                                                                                                                                                         | Significado                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="ADDRESS_FLAGS_MATCH_DST"></span><span id="address_flags_match_dst"></span><dl> <dt>**LAS \_ MARCAS DE DIRECCIÓN COINCIDEN CON \_ \_ DST**</dt> </dl>                 | Coincide con la dirección de destino.<br/>                              |
| <span id="ADDRESS_FLAGS_MATCH_SRC"></span><span id="address_flags_match_src"></span><dl> <dt>**LAS \_ MARCAS DE DIRECCIÓN COINCIDEN CON \_ \_ SRC**</dt> </dl>                 | Coincide con la dirección de origen.<br/>                                   |
| <span id="ADDRESS_FLAGS_EXCLUDED"></span><span id="address_flags_excluded"></span><dl> <dt>**MARCAS \_ DE DIRECCIÓN \_ EXCLUIDAS**</dt> </dl>                     | Excluye el marco si se encuentra esta dirección.<br/>                  |
| <span id="ADDRESS_FLAGS_DST_GROUP_ADDR"></span><span id="address_flags_dst_group_addr"></span><dl> <dt>**MARCADOR \_ DE DIRECCIÓN \_ ADDR DE GRUPO \_ \_ DST**</dt> </dl> | Coincide solo con el bit de grupo. Úselo para los mensajes de tipo de difusión.<br/> |
| <span id="ADDRESS_FLAGS_MATCH_BOTH"></span><span id="address_flags_match_both"></span><dl> <dt>**LAS \_ MARCAS DE DIRECCIÓN COINCIDEN CON \_ \_ AMBAS**</dt> </dl>              | Coincide con las direcciones de destino y de origen.<br/>                     |



 

</dd> <dt>

**NalReserved**
</dt> <dd>

Esto está reservado.

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

Se pueden combinar las **marcas del miembro AddressFlags.** Por ejemplo, la siguiente configuración excluye el marco si se detecta la dirección de origen especificada.

``` syntax
ADDRESS_FLAGS_MATCH_SOURCE|ADDRESS_FLAGS_EXCLUDED
```

Para obtener más información sobre cómo implementar esta estructura, vea [Capturar filtros](capture-filters.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[CAPTUREFILTER](capturefilter.md)
</dt> </dl>

 

 




