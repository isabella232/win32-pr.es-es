---
description: Contiene información sobre un botón que un archivo DLL de extensión del administrador de archivos agrega a la barra de herramientas del administrador de archivos.
title: EXT_BUTTON estructura (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXT_BUTTON
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 8cd29a06-0f38-4285-9092-647a391b72d7
ms.openlocfilehash: 5eabb9f5e958b1e0bd15a6412dfbfa276d23f255
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809410"
---
# <a name="ext_button-structure"></a>\_Estructura del botón ext

Contiene información sobre un botón que un archivo DLL de extensión del administrador de archivos agrega a la barra de herramientas del administrador de archivos.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagEXT_BUTTON {
  WORD idCommand;
  WORD idsHelp;
  WORD fsStyle;
} EXT_BUTTON, *LPEXT_BUTTON;
```



## <a name="members"></a>Miembros

<dl> <dt>

**idCommand**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Identificador de comando para el botón.

</dd> <dt>

**idsHelp**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Identificador de la cadena de ayuda para el botón.

</dd> <dt>

**fsStyle**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Estilo del botón.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**FMEVENT \_ TOOLBARLOAD**](fmevent-toolbarload.md)
</dt> <dt>

[**TOOLBARLOAD de FMS \_**](fms-toolbarload.md)
</dt> </dl>

 

 




