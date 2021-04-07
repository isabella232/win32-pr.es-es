---
description: La \_ estructura PF PARSERDLLINFO define los analizadores ubicados en el archivo DLL del analizador.
ms.assetid: a7473b58-7767-4224-be3b-e96132d98adf
title: Estructura de PF_PARSERDLLINFO (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_PARSERDLLINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: ab4a3673c567a72cb5d0284a07d5603913e77550
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002357"
---
# <a name="pf_parserdllinfo-structure"></a>\_Estructura PF PARSERDLLINFO

La estructura **PF \_ PARSERDLLINFO** define los analizadores ubicados en el archivo DLL del analizador.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PF_PARSERDLLINFO {
  DWORD         nParsers;
  PF_PARSERINFO ParserInfo[];
} PF_PARSERDLLINFO, *PPF_PARSERDLLINFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**nParsers**
</dt> <dd>

Número de analizadores en el archivo DLL del analizador.

</dd> <dt>

**ParserInfo**
</dt> <dd>

Matriz de estructuras [PF \_ PARSERINFO](pf-parserinfo.md) que describen cada analizador en el archivo DLL del analizador.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La función de exportación [ParserAutoInstallInfo](parserautoinstallinfo.md) que se implementa en el archivo DLL del analizador devuelve la estructura **PF \_ PARSERDLLINFO** . La función **ParserAutoInstallInfo** identifica el número de analizadores en el archivo dll y utiliza una matriz de estructuras [PF \_ PARSERINFO](pf-parserinfo.md) para describir cada analizador.

La \_ estructura PF PARSERDLLINFO debe estar asignada mediante **HeapAlloc**.



| Para obtener información acerca de                                               | Vea                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------|
| Qué son los analizadores y cómo funcionan con Monitor de red.        | [Analizadores](parsers.md)                                                      |
| Qué puntos de entrada se incluyen en el archivo DLL del analizador.               | [Arquitectura de DLL de analizador](parser-dll-architecture.md)                      |
| Cómo implementar **ParserAutoInstallInfo**  incluye un ejemplo. | [Implementación de ParserAutoIstallInfo](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[PF \_ PARSERINFO](pf-parserinfo.md)
</dt> <dt>

[ParserAutoInstallInfo](parserautoinstallinfo.md)
</dt> </dl>

 

 




