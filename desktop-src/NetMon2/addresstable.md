---
description: La estructura ADDRESSTABLE contiene una tabla de pares de direcciones.
ms.assetid: 84577b6c-9d43-4e53-9f8d-33685329b11d
title: Estructura ADDRESSTABLE (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDRESSTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: c1c766e29033136954abab69755e1231e610983314cdaa01da3957889af5eb33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064285"
---
# <a name="addresstable-structure"></a>AddressTABLE (estructura)

La **estructura ADDRESSTABLE** contiene una tabla de pares de direcciones.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _ADDRESSTABLE {
  DWORD       nAddressPairs;
  DWORD       nNonMacAddressPairs;
  ADDRESSPAIR AddressPair[MAX_ADDRESS_PAIRS];
} ADDRESSTABLE, *LPADDRESSTABLE;
```



## <a name="members"></a>Miembros

<dl> <dt>

**nAddressPairs**
</dt> <dd>

Número de pares de direcciones en la **matriz AddressPair.**

</dd> <dt>

**nNonMacAddressPairs**
</dt> <dd>

Número de pares de direcciones que no son MAC.

</dd> <dt>

**AddressPair**
</dt> <dd>

Matriz de pares de direcciones. Tenga en cuenta que solo puede almacenar hasta ocho pares de direcciones por estructura ADDRESSTABLE.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Use esta estructura como parte del proceso de construcción del filtro de captura. Para obtener más información sobre cómo implementar esta estructura, vea [Capturar filtros](capture-filters.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ADDRESSPAIR](addresspair.md)
</dt> <dt>

[CAPTUREFILTER](capturefilter.md)
</dt> </dl>

 

 




