---
description: Contiene información que el Administrador de archivos usa para agregar una cadena de Ayuda para un elemento de comando de menú o barra de herramientas.
title: FMS_HELPSTRING estructura (Wfext.h)
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
ms.openlocfilehash: 4e9521df91619d108c7a03b6574926147fc2b04a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572541"
---
# <a name="fms_helpstring-structure"></a>Estructura \_ HELPSTRING de FMS

Contiene información que el Administrador de archivos usa para agregar una cadena de Ayuda para un elemento de comando de menú o barra de herramientas.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _FMS_HELPSTRING {
  INT       idCommand;
  HMENU     hMenu;
  __wchar_t szHelp[128];
} FMS_HELPSTRING;
```



## <a name="members"></a>Members

<dl> <dt>

**idCommand**
</dt> <dd>

Tipo: **INT**

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

Tipo: **\_ \_ wchar \_ t \[ 128 \]**

</dd> <dd>

Cadena terminada en NULL que recibe el texto de ayuda.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> <dt>

[**FMEVENT \_ HELPMENUITEM**](fmevent-helpmenuitem.md)
</dt> </dl>

 

 




