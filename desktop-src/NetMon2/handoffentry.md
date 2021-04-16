---
description: La estructura HANDOFFENTRY define una entrada de protocolo específica en una estructura HANDOFFTABLE.
ms.assetid: 85793326-3007-4dd9-9325-3447d6e09883
title: Estructura HANDOFFENTRY (Netmon. h)
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
ms.openlocfilehash: 7c04c7bc90fdd0f36beb6aed26a6b84c077eff5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540195"
---
# <a name="handoffentry-structure"></a>Estructura HANDOFFENTRY

La estructura **HANDOFFENTRY** define una entrada de protocolo específica en una estructura **HANDOFFTABLE** .

Esta estructura se rellena mediante Monitor de red en función de la información del archivo. ini proporcionado por el usuario que se proporciona al llamar a la función [**CreateHandoffTable**](createhandofftable.md) . Una aplicación nunca debe modificar explícitamente esta estructura.

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

**Cómo \_ SIG**
</dt> <dd>

Firma que identifica esta entrada como una entrada de la tabla de entrega.

</dd> <dt>

**Cómo \_ ProtIdentNumber**
</dt> <dd>

Número de protocolo proporcionado por el archivo. ini proporcionado por el usuario.

</dd> <dt>

**Cómo \_ ProtocolHandle**
</dt> <dd>

Identificador del protocolo creado con el nombre de protocolo proporcionado por el archivo. ini proporcionado por el usuario.

</dd> <dt>

**Cómo \_ ProtocolData**
</dt> <dd>

Datos de instancia de protocolo proporcionados por el archivo. ini proporcionado por el usuario.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura se rellena por Monitor de red cuando Monitor de red crea una tabla de entrega.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[HANDOFFTABLE](handofftable.md)
</dt> </dl>

 

 




