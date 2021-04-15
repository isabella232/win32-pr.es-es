---
description: Contiene información que utiliza el administrador de archivos para agregar una cadena de ayuda para un elemento de comando de menú o barra de herramientas.
title: FMS_HELPSTRING estructura (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_HELPSTRING
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: b3ae7f86-5d58-47fa-87bd-e4e6a3541a93
ms.openlocfilehash: c934409712ae740797eb3b5af0b55c50ff125342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997737"
---
# <a name="fms_helpstring-structure"></a>FMS \_ HELPSTRING (estructura)

Contiene información que utiliza el administrador de archivos para agregar una cadena de ayuda para un elemento de comando de menú o barra de herramientas.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _FMS_HELPSTRING {
  INT       idCommand;
  HMENU     hMenu;
  __wchar_t szHelp[128];
} FMS_HELPSTRING;
```



## <a name="members"></a>Miembros

<dl> <dt>

**idCommand**
</dt> <dd>

Tipo: **int**

</dd> <dd>

Identificador del elemento de comando.

</dd> <dt>

**hMenu**
</dt> <dd>

Tipo: **HMENU**

</dd> <dd>

Identificador de la barra de menús.

</dd> <dt>

**szHelp**
</dt> <dd>

Tipo: **\_ \_ WCHAR \_ t \[ 128 \]**

</dd> <dd>

Cadena terminada en null que recibe el texto de ayuda.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> <dt>

[**FMEVENT \_ HELPMENUITEM**](fmevent-helpmenuitem.md)
</dt> </dl>

 

 




