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
ms.openlocfilehash: 41acab19f83fdcc88a384c0407b666a7f641a598
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074173"
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



## <a name="members"></a>Members

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

## <a name="remarks"></a>Observaciones

Use esta estructura como parte del proceso de construcción del filtro de captura. Para obtener más información sobre cómo implementar esta estructura, vea [Capturar filtros](capture-filters.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

 




