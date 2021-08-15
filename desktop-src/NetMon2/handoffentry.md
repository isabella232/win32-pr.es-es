---
description: La estructura HANDOFFENTRY define una entrada de protocolo específica en una estructura HANDOFFTABLE.
ms.assetid: 85793326-3007-4dd9-9325-3447d6e09883
title: Estructura HANDOFFENTRY (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HANDOFFENTRY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 692b9e925442920a67434f74c9e8a8ebd225fc417cbbf419b6eb568aa9eee2df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117981418"
---
# <a name="handoffentry-structure"></a>HANDOFFENTRY (estructura)

La **estructura HANDOFFENTRY** define una entrada de protocolo específica en una **estructura HANDOFFTABLE.**

Esta estructura se rellena mediante Monitor de red en función de la información de un archivo .ini proporcionado por el usuario al llamar a la [**función CreateHandoffTable.**](createhandofftable.md) Una aplicación nunca debe modificar explícitamente esta estructura.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _SESSIONSTATS {
  DWORD      hoe_sig;
  DWORD      hoe_ProtIdentNumber;
  HPPROTOCOL hoe_ProtocolHandle;
  DWORD      hoe_ProtocolData;
} HANDOFFENTRY, *LPHANDOFFENTRY;
```



## <a name="members"></a>Miembros

<dl> <dt>

**para \_ sig**
</dt> <dd>

Firma que identifica esta entrada como una entrada de tabla de entrega.

</dd> <dt>

**number \_ ProtIdentNumber**
</dt> <dd>

Número de protocolo proporcionado por el usuario .ini archivo.

</dd> <dt>

**routing \_ ProtocolHandle**
</dt> <dd>

Identificador del protocolo creado con el nombre de protocolo proporcionado por el usuario .ini archivo.

</dd> <dt>

**routing \_ ProtocolData**
</dt> <dd>

Datos de instancia de protocolo proporcionados por el usuario .ini archivo.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta estructura se rellena mediante Monitor de red cuando Monitor de red crea una tabla de entrega.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[HANDOFFTABLE](handofftable.md)
</dt> </dl>

 

 




