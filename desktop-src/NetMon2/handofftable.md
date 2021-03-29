---
description: La estructura HANDOFFTABLE define los protocolos de una tabla de entrega.
ms.assetid: 6bb7465b-c1ba-4ffe-aecf-8125993c309a
title: Estructura HANDOFFTABLE (Netmon. h)
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
ms.openlocfilehash: 842ef9fde56ff6b4c420034b861aa8c151e7e6b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666271"
---
# <a name="handofftable-structure"></a>Estructura HANDOFFTABLE

La estructura **HANDOFFTABLE** define los protocolos de una tabla de entrega.

Esta estructura se rellena mediante Monitor de red en función de la información del archivo. ini proporcionado por el usuario que se proporciona al llamar a la función [**CreateHandoffTable**](createhandofftable.md) .

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

**\_SIG activo**
</dt> <dd>

Firma que identifica esta tabla como una tabla de entrega.

</dd> <dt>

**NumEntries en caliente \_**
</dt> <dd>

Número de entradas que Monitor de red agregaron a la tabla de entrega.

</dd> <dt>

**\_entradas activas**
</dt> <dd>

Tabla de entrega.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura y sus estructuras HANDOFFENTRY asociadas se rellenan mediante Monitor de red cuando Monitor de red crea una tabla de entrega.

La información del protocolo que se usa al crear una tabla de entrega se proporciona en un archivo. ini proporcionado por la aplicación cuando se llama a [**CreateHandoffTable**](createhandofftable.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[HANDOFFENTRY](handoffentry.md)
</dt> <dt>

[CreateHandoffTable](createhandofftable.md)
</dt> </dl>

 

 




