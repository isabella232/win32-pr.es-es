---
description: La \_ estructura PF PARSERINFO define un analizador cada vez. En la \_ estructura PF PARSERINFO, se define un analizador mediante la información sobre el protocolo que detecta el analizador.
ms.assetid: e1180952-9560-4386-9320-919dfb8171b3
title: Estructura de PF_PARSERINFO (Netmon. h)
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
ms.openlocfilehash: 28ebeaad31e6f40ceb961d8c303a22590966947f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678131"
---
# <a name="pf_parserinfo-structure"></a>\_Estructura PF PARSERINFO

La estructura **PF \_ PARSERINFO** define un analizador cada vez. En la estructura **PF \_ PARSERINFO** , se define un analizador mediante la información sobre el protocolo que detecta el analizador.

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

Nombre del archivo de ayuda del Protocolo, si existe.

</dd> <dt>

**pWhoCanPrecedeMe**
</dt> <dd>

Puntero a una estructura [PF \_ FOLLOWSET](pf-followset.md) que enumera los protocolos que pueden preceder al protocolo que describe la estructura **PF \_ PARSERINFO** . Monitor de red agrega el protocolo del analizador al [*siguiente conjunto*](f.md) de todos los protocolos del conjunto.

</dd> <dt>

**pWhoCanFollowMe**
</dt> <dd>

Puntero a una estructura de [PF \_ FOLLOWSET](pf-followset.md) que muestra el protocolo que puede seguir el protocolo que describe la estructura **PF \_ PARSERINFO** . Monitor de red agrega los protocolos del conjunto al [*siguiente conjunto*](f.md) del protocolo del analizador.

</dd> <dt>

**pWhoHandsOffToMe**
</dt> <dd>

Puntero a una estructura [PF \_ HANDOFFSET](pf-handoffset.md) que se describa en el protocolo que describe la estructura **PF \_ PARSERINFO** . Monitor de red agrega el protocolo del analizador a los [*conjuntos de entrega*](h.md) de todos los protocolos del conjunto.

</dd> <dt>

**pWhoDoIHandOffTo**
</dt> <dd>

Puntero a una estructura de [PF \_ HANDOFFSET](pf-handoffset.md) que enumera los protocolos a los que el protocolo del analizador se entrega. Monitor de red agrega los protocolos de este conjunto al [*conjunto de entrega*](h.md) del protocolo del analizador.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La estructura **PF \_ PARSERINFO** se usa en la estructura **PF \_ PARSERDLLINFO** para proporcionar una descripción de un analizador. Monitor de red usa la descripción del analizador para actualizar el archivo [*Parser.ini*](p.md) y los archivos INI de los analizadores que preceden y siguen al protocolo descrito en la estructura **PF \_ PARSERINFO** .

Un conjunto siguiente especifica los protocolos que siguen a un protocolo. Monitor de red usa un conjunto de seguimiento cuando el analizador no puede identificar el protocolo siguiente a partir de los datos de una instancia de protocolo. En el archivo [*Parser.ini*](p.md) se almacena un conjunto de seguimiento. Cuando el analizador se instala por primera vez, Monitor de red actualiza el siguiente conjunto de protocolos de analizador que se enumeran en **pWhoCanPrecedeMe** y **pWhoCanFollowMe**.

Un conjunto de entrega especifica los protocolos que siguen a un protocolo. El analizador utiliza un conjunto de entrega solo cuando el analizador puede identificar el protocolo siguiente a partir de los datos de una instancia de protocolo. Un conjunto de entrega se almacena en los archivos INI de cada analizador. Cuando el analizador se instala por primera vez, Monitor de red actualiza el conjunto de entrega de los protocolos de analizador que se enumeran en **pWhoHandsOffToMe** y **pWhoDoIHandOffTo**.



| Para obtener información acerca de                                               | Vea                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------|
| Qué son los analizadores y cómo funcionan con Monitor de red.        | [Analizadores](parsers.md)                                                       |
| Qué incluyen los conjuntos siguientes.                                        | [Especificar un conjunto de seguimiento](specifying-a-follow-set.md)                       |
| Qué contienen los conjuntos de entrega.                                       | [Especificar un conjunto de entrega](specifying-a-handoff-set.md)                     |
| Qué puntos de entrada se incluyen en el archivo DLL del analizador.                | [Arquitectura de DLL de analizador](parser-dll-architecture.md)                       |
| Cómo implementar **ParserAutoInstallInfo**  incluye un ejemplo. | [Implementación de ParserAutoInstallInfo](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



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

 

 




