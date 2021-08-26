---
description: La estructura \_ PF PARSERDLLINFO define los analizadores ubicados en el archivo DLL del analizador.
ms.assetid: a7473b58-7767-4224-be3b-e96132d98adf
title: PF_PARSERDLLINFO estructura (Netmon.h)
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
ms.openlocfilehash: caaafeb9883ad514366f91f3834354fbd5ac0850400e61594a5307c4533e0960
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962855"
---
# <a name="pf_parserdllinfo-structure"></a>Estructura \_ PF PARSERDLLINFO

La **estructura \_ PF PARSERDLLINFO** define los analizadores ubicados en el archivo DLL del analizador.

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

Número de analizadores del archivo DLL del analizador.

</dd> <dt>

**ParserInfo**
</dt> <dd>

Matriz [de estructuras PF \_ PARSERINFO](pf-parserinfo.md) que describen cada analizador en el archivo DLL del analizador.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La función de exportación [ParserAutoInstallInfo](parserautoinstallinfo.md) que se implementa en el archivo DLL del analizador devuelve la estructura **PF \_ PARSERDLLINFO.** La **función ParserAutoInstallInfo** identifica el número de analizadores del archivo DLL y usa una matriz de estructuras [PF \_ PARSERINFO](pf-parserinfo.md) para describir cada analizador.

La estructura \_ PF PARSERDLLINFO debe asignarse mediante **HeapAlloc**.



| Para obtener información acerca de                                               | Vea                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------|
| Qué son los analizadores y cómo funcionan con Monitor de red.        | [Analizadores](parsers.md)                                                      |
| Qué puntos de entrada se incluyen en el archivo DLL del analizador.               | [Arquitectura dll del analizador](parser-dll-architecture.md)                      |
| Cómo implementar **ParserAutoInstallInfo incluye**  un ejemplo. | [Implementación de ParserAutoIstallInfo](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[PF \_ PARSERINFO](pf-parserinfo.md)
</dt> <dt>

[ParserAutoInstallInfo](parserautoinstallinfo.md)
</dt> </dl>

 

 




