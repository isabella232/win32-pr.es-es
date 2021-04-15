---
description: La estructura ADDRESSTABLE contiene una tabla de pares de direcciones.
ms.assetid: 84577b6c-9d43-4e53-9f8d-33685329b11d
title: Estructura ADDRESSTABLE (Netmon. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497806"
---
# <a name="addresstable-structure"></a>Estructura ADDRESSTABLE

La estructura **ADDRESSTABLE** contiene una tabla de pares de direcciones.

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

Número de pares de direcciones en la matriz **AddressPair** .

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

Use esta estructura como parte del proceso de construcción del filtro de captura. Para obtener más información sobre la implementación de esta estructura, vea [Capture filters](capture-filters.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ADDRESSPAIR](addresspair.md)
</dt> <dt>

[CAPTUREFILTER](capturefilter.md)
</dt> </dl>

 

 




