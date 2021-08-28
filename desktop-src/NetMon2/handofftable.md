---
description: La estructura HANDOFFTABLE define los protocolos de una tabla de entrega.
ms.assetid: 6bb7465b-c1ba-4ffe-aecf-8125993c309a
title: Estructura HANDOFFTABLE (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HANDOFFTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 533d69b198ecff24dc48926669cbd0476ae1ce1f73abfc76ba711a30456e43ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117981428"
---
# <a name="handofftable-structure"></a>HANDOFFTABLE (estructura)

La **estructura HANDOFFTABLE** define los protocolos de una tabla de entrega.

Esta estructura se rellena mediante Monitor de red en función de la información de un archivo de .ini proporcionado por el usuario al llamar a la [**función CreateHandoffTable.**](createhandofftable.md)

## <a name="syntax"></a>Sintaxis


```C++
typedef struct HANDOFFTABLE {
  DWORD          hot_sig;
  DWORD          hot_NumEntries;
  LPHANDOFFENTRY hot_Entries;
} HANDOFFTABLE, *LPHANDOFFTABLE;
```



## <a name="members"></a>Miembros

<dl> <dt>

**hot \_ sig**
</dt> <dd>

Firma que identifica esta tabla como una tabla de entrega.

</dd> <dt>

**hot \_ NumEntries**
</dt> <dd>

Número de entradas que Monitor de red a la tabla de entrega.

</dd> <dt>

**entradas \_ de acceso de acceso**
</dt> <dd>

Tabla handoff.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta estructura y sus estructuras HANDOFFENTRY asociadas se rellenan mediante Monitor de red cuando Monitor de red crea una tabla de entrega.

La información de protocolo que se usa al crear una tabla de entrega se proporciona en un archivo .ini proporcionado por la aplicación cuando se llama a [**CreateHandoffTable.**](createhandofftable.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[HANDOFFENTRY](handoffentry.md)
</dt> <dt>

[CreateHandoffTable](createhandofftable.md)
</dt> </dl>

 

 




