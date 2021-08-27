---
title: PopupMENUITEM (estructura)
description: Contiene información sobre los elementos de menú de un recurso de menú que abren un menú o un submenú. La definición de estructura que se proporciona aquí es solo para una explicación; no está presente en ningún archivo de encabezado estándar.
ms.assetid: cb8faeb2-bca9-4ff5-8f80-d273c3fca504
keywords:
- Menús de estructura POPUPMENUITEM y otros recursos
topic_type:
- apiref
api_name:
- POPUPMENUITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 62d769e9756f0d15e7377a79f9aa94802a469746807e3a32b5ba329f76484b82
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011705"
---
# <a name="popupmenuitem-structure"></a>PopupMENUITEM (estructura)

Contiene información sobre los elementos de menú de un recurso de menú que abren un menú o un submenú. La definición de estructura que se proporciona aquí es solo para una explicación; no está presente en ningún archivo de encabezado estándar.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  DWORD   type;
  DWORD   state;
  DWORD   id;
  WORD    resInfo;
  szOrOrd menuText;
} POPUPMENUITEM;
```



## <a name="members"></a>Miembros

<dl> <dt>

**type**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Describe el elemento de menú. Algunos de los valores que este miembro puede tener incluyen los que se muestran en la lista siguiente.

Además de los valores mostrados, este miembro también puede ser una combinación de los valores de tipo enumerados con el **miembro fType** de la [**estructura MENUITEMINFO.**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) Los valores de tipo son los que comienzan por \_ MFT. Para usar estos valores de tipo de MFT \_ \* predefinidos, incluya la siguiente instrucción en el archivo .rc:

`#include "winuser.h"`



| Value                                                                                                                                                                                                    | Significado                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="MF_END"></span><span id="mf_end"></span><dl> <dt>**MF \_ End**</dt> <dt>0x80</dt> </dl>       | El elemento de menú es el último del menú; el sistema usa internamente la marca . <br/>   |
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <dt>**MF \_ Ventana emergente**</dt> <dt>0x01</dt> </dl> | El elemento de menú abre un menú o un submenú; el sistema usa internamente la marca . <br/> |



 

</dd> <dt>

**state**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Describe el elemento de menú. Este miembro puede ser una combinación de los valores de estado enumerados con el **miembro dwState** de la [**estructura MENUITEMINFO.**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) Los valores de estado son los que comienzan por \_ MFS. Para usar estos valores de estado MFS \_ \* predefinidos, incluya la siguiente instrucción en el archivo .rc:

`#include "winuser.h"`

</dd> <dt>

**identificador**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Expresión numérica que identifica el elemento de menú que se pasa en el [**mensaje WM \_ COMMAND.**](wm-command.md)

</dd> <dt>

**resInfo**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Conjunto de marcas de bits que especifican el tipo de elemento de menú. Este miembro puede ser uno de los siguientes valores.



| Value                                                                                                                                                                                                       | Significado                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MFR_END"></span><span id="mfr_end"></span><dl> <dt>**MFR \_ End**</dt> <dt>0x80</dt> </dl>       | El elemento de menú es el último de este submenú o recurso de menú; el sistema usa internamente esta marca.<br/> |
| <span id="MFR_POPUP"></span><span id="mfr_popup"></span><dl> <dt>**MFR \_ Ventana emergente**</dt> <dt>0x01</dt> </dl> | El elemento de menú abre un menú o un submenú; el sistema usa internamente la marca .<br/>                     |



 

</dd> <dt>

**menuText**
</dt> <dd>

Tipo: **szOrOrd**

</dd> <dd>

Cadena Unicode terminada en NULL que contiene el texto de este elemento de menú. No hay ningún límite fijo en el tamaño de esta cadena.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Hay una estructura **POPUPMENUITEM** para cada elemento de menú que abre un menú o un submenú. Identifique este tipo de elemento  de menú estableciendo el miembro de tipo en **MF \_ POPUP** y estableciendo el bit **MFR \_ POPUP** en el **miembro resInfo** en 0x0001. En este caso, los datos finales escritos en el recurso [**\_ RT MENU**](/windows/desktop/menurc/resource-types) para el menú o submenú son la estructura [**MENUHELPID.**](menuhelpid.md) **MENUHELPID contiene** una expresión numérica que identifica el menú durante el [**procesamiento de WM \_ HELP.**](../shell/wm-help.md)

Además, cada estructura **POPUPMENUITEM** que tenga el bit POPUP de **\_ MFR** establecido en el miembro **resInfo** va seguido de una estructura [**MENUHELPID**](menuhelpid.md) más un número adicional de estructuras **POPUPMENUITEM,** una para cada elemento de menú de ese submenú. La última **estructura POPUPMENUITEM** del submenú tendrá el bit **MFR \_ END** establecido en el **miembro resInfo.** Para buscar el final del recurso, busque un **MFR \_ END** correspondiente para cada **MFR \_ POPUP** más un **MFR \_ END** adicional que coincida con el conjunto más externo de elementos de menú.

Indique el último elemento de menú estableciendo el **miembro de tipo** en MF **\_ END**. Dado que puede anidar submenús, puede haber varios niveles de **MF \_ END.** En estos casos, los elementos de menú son secuenciales.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**MENUHEADER**](menuheader.md)
</dt> <dt>

[**MENUHELPID**](menuhelpid.md)
</dt> <dt>

[**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)
</dt> <dt>

[**NORMALMENUITEM**](normalmenuitem.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Recursos](resources.md)
</dt> </dl>

 

