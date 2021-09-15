---
description: Contiene información sobre un botón que un archivo DLL de extensión del Administrador de archivos está agregando a la barra de herramientas del Administrador de archivos.
title: EXT_BUTTON estructura (Wfext.h)
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
ms.openlocfilehash: 6d1505ef7b330f0e935136eacaf808da3add8cd8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468252"
---
# <a name="ext_button-structure"></a>EXT \_ BUTTON (estructura)

Contiene información sobre un botón que un archivo DLL de extensión del Administrador de archivos está agregando a la barra de herramientas del Administrador de archivos.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagEXT_BUTTON {
  WORD idCommand;
  WORD idsHelp;
  WORD fsStyle;
} EXT_BUTTON, *LPEXT_BUTTON;
```



## <a name="members"></a>Members

<dl> <dt>

**idCommand**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Identificador de comando para el botón.

</dd> <dt>

**idsHelp**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Identificador de la cadena de Ayuda del botón.

</dd> <dt>

**fsStyle**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Estilo del botón.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**FMEVENT \_ TOOLBARLOAD**](fmevent-toolbarload.md)
</dt> <dt>

[**FMS \_ TOOLBARLOAD**](fms-toolbarload.md)
</dt> </dl>

 

 




