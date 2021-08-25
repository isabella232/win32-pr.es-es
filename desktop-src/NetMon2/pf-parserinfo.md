---
description: La estructura \_ PF PARSERINFO define un analizador a la vez. En la estructura PF PARSERINFO, la información sobre el protocolo que detecta el analizador define \_ un analizador.
ms.assetid: e1180952-9560-4386-9320-919dfb8171b3
title: PF_PARSERINFO estructura (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_PARSERINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 533e8dae6a009488998acd3232b062b423553b9df10f14ec97ef9ae2f8c55bea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889945"
---
# <a name="pf_parserinfo-structure"></a>Pf \_ PARSERINFO (estructura)

La **estructura \_ PF PARSERINFO** define un analizador a la vez. En la **estructura PF \_ PARSERINFO,** la información sobre el protocolo que detecta el analizador define un analizador.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PF_PARSERINFO {
  char           szProtocolName[MAX_PROTOCOL_NAME_LEN];
  char           szComment[MAX_PROTOCOL_COMMENT_LEN];
  char           szHelpFile[MAX_PATH];
  PPF_FOLLOWSET  pWhoCanPrecedeMe;
  PPF_FOLLOWSET  pWhoCanFollowMe;
  PPF_HANDOFFSET pWhoHandsOffToMe;
  PPF_HANDOFFSET pWhoDoIHandOffTo;
} PF_PARSERINFO, *PPF_PARSERINFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**szProtocolName**
</dt> <dd>

Nombre del protocolo que detecta el analizador.

</dd> <dt>

**szComment**
</dt> <dd>

Breve descripción del protocolo.

</dd> <dt>

**szHelpFile**
</dt> <dd>

Nombre del archivo de Ayuda del protocolo, si lo hubiera.

</dd> <dt>

**pWhoCanPrecedeMe**
</dt> <dd>

Puntero a una [estructura \_ PF FOLLOWSET](pf-followset.md) que enumera los protocolos que pueden preceder al protocolo que describe la estructura **PF \_ PARSERINFO.** Monitor de red agrega el protocolo del analizador al [*siguiente*](f.md) conjunto de todos los protocolos del conjunto.

</dd> <dt>

**pWhoCanFollowMe**
</dt> <dd>

Puntero a una [estructura \_ PF FOLLOWSET](pf-followset.md) que enumera el protocolo que puede seguir el protocolo que describe la estructura **PF \_ PARSERINFO.** Monitor de red agrega los protocolos del conjunto al [*siguiente*](f.md) conjunto del protocolo de analizador.

</dd> <dt>

**pHandHandsOffToMe**
</dt> <dd>

Puntero a una [estructura \_ HANDOFFSET PF](pf-handoffset.md) que se entrega al protocolo que describe la estructura **PF \_ PARSERINFO.** Monitor de red agrega el protocolo de analizador a los [*conjuntos de entrega*](h.md) de todos los protocolos del conjunto.

</dd> <dt>

**pHandDoIHandOffTo**
</dt> <dd>

Puntero a una [estructura \_ HANDOFFSET PF](pf-handoffset.md) que enumera los protocolos a los que entrega el protocolo de analizador. Monitor de red agrega los protocolos de este conjunto al [*conjunto de entrega*](h.md) del protocolo de analizador.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **estructura \_ PF PARSERINFO** se usa en la estructura **PF \_ PARSERDLLINFO** para proporcionar una descripción de un analizador. Monitor de red usa la descripción del analizador para actualizar el archivo [*Parser.ini*](p.md) y los archivos INI de los analizadores que preceden y siguen el protocolo descrito en la estructura **PF \_ PARSERINFO.**

Un conjunto de seguimiento especifica los protocolos que siguen a un protocolo. Monitor de red utiliza un conjunto de seguimiento cuando el analizador no puede identificar el siguiente protocolo a partir de los datos de una instancia de protocolo. Un conjunto de seguimiento se almacena en el [*Parser.ini*](p.md) siguiente. Cuando el analizador se instala por primera vez, Monitor de red actualiza el siguiente conjunto de los protocolos de analizador que se enumeran en **pWhoCanPrecedeMe** y **pLowCanFollowMe**.

Un conjunto de entrega especifica los protocolos que siguen a un protocolo. El analizador usa un conjunto de entrega solo cuando el analizador puede identificar el siguiente protocolo a partir de los datos de una instancia de protocolo. Un conjunto de entregas se almacena en los archivos INI de cada analizador. Cuando el analizador se instala por primera vez, Monitor de red actualiza el conjunto de entrega de los protocolos de analizador que aparecen en **pHandHandsOffToMe** y **pHandDoIHandOffTo.**



| Para obtener información acerca de                                               | Vea                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------|
| Qué son los analizadores y cómo funcionan con Monitor de red.        | [Analizadores](parsers.md)                                                       |
| Qué contienen los siguientes conjuntos.                                        | [Especificar un conjunto de seguimiento](specifying-a-follow-set.md)                       |
| Qué conjuntos de entrega contienen.                                       | [Especificar un conjunto de entrega](specifying-a-handoff-set.md)                     |
| Qué puntos de entrada se incluyen en el archivo DLL del analizador.                | [Arquitectura dll del analizador](parser-dll-architecture.md)                       |
| Cómo implementar **ParserAutoInstallInfo incluye**  un ejemplo. | [Implementación de ParserAutoInstallInfo](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ParserAutoInstallInfo](parserautoinstallinfo.md)
</dt> <dt>

[PF \_ FOLLOWSET](pf-followset.md)
</dt> <dt>

[PF \_ HANDOFFSET](pf-handoffset.md)
</dt> <dt>

[PF \_ PARSERDLLINFO](pf-parserdllinfo.md)
</dt> </dl>

 

 




