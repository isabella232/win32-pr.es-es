---
title: Estructura POPUPMENUITEM
description: Contiene información sobre los elementos de menú en un recurso de menú que abre un menú o un submenú. La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.
ms.assetid: cb8faeb2-bca9-4ff5-8f80-d273c3fca504
keywords:
- Menús de la estructura POPUPMENUITEM y otros recursos
topic_type:
- apiref
api_name:
- POPUPMENUITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: faa755c2ec7a2b9eeb2f123d7fd3e169b2df1be1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996066"
---
# <a name="popupmenuitem-structure"></a>Estructura POPUPMENUITEM

Contiene información sobre los elementos de menú en un recurso de menú que abre un menú o un submenú. La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.

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

Además de los valores mostrados, este miembro también puede ser una combinación de los valores de tipo enumerados con el miembro **fType** de la estructura [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) . Los valores de tipo son los que comienzan por MFT \_ . Para usar estos valores predefinidos \_ \* de tipo MFT, incluya la siguiente instrucción en el archivo. RC:

`#include "winuser.h"`



| Value                                                                                                                                                                                                    | Significado                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="MF_END"></span><span id="mf_end"></span><dl> <dt>**MF \_ FINALIZAR**</dt> <dt>0x80</dt> </dl>       | El elemento de menú es el último en el menú; el sistema utiliza internamente la marca. <br/>   |
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <dt>**MF \_ EMERGENTE**</dt> <dt>0x01</dt> </dl> | El elemento de menú abre un menú o un submenú; el sistema utiliza internamente la marca. <br/> |



 

</dd> <dt>

**state**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Describe el elemento de menú. Este miembro puede ser una combinación de los valores de estado enumerados con el miembro **dwState** de la estructura [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) . Los valores de estado son los que comienzan por MFS \_ . Para usar estos \_ \* valores de estado de MFS predefinidos, incluya la siguiente instrucción en el archivo. RC:

`#include "winuser.h"`

</dd> <dt>

**id**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Expresión numérica que identifica el elemento de menú que se pasa en el mensaje del [**\_ comando de WM**](wm-command.md) .

</dd> <dt>

**resInfo**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Un conjunto de marcadores de bits que especifican el tipo de elemento de menú. Este miembro puede ser uno de los valores siguientes.



| Value                                                                                                                                                                                                       | Significado                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MFR_END"></span><span id="mfr_end"></span><dl> <dt>**MFR \_ FINALIZAR**</dt> <dt>0x80</dt> </dl>       | El elemento de menú es el último de este recurso de menú o submenú; Este marcador lo utiliza internamente el sistema.<br/> |
| <span id="MFR_POPUP"></span><span id="mfr_popup"></span><dl> <dt>**MFR \_ EMERGENTE**</dt> <dt>0x01</dt> </dl> | El elemento de menú abre un menú o un submenú; el sistema utiliza internamente la marca.<br/>                     |



 

</dd> <dt>

**menuText**
</dt> <dd>

Tipo: **szOrOrd**

</dd> <dd>

Una cadena Unicode terminada en null que contiene el texto de este elemento de menú. No hay ningún límite fijo en el tamaño de esta cadena.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Hay una estructura **POPUPMENUITEM** para cada elemento de menú que abre un menú o un submenú. Identifique este tipo de elemento de menú estableciendo el miembro de **tipo** en el **\_ elemento emergente MF** y estableciendo el bit **\_ emergente MFR** en el miembro **resInfo** en 0x0001. En este caso, los datos finales escritos en el recurso de [**\_ menú RT**](/windows/desktop/menurc/resource-types) para el menú o el submenú son la estructura [**MENUHELPID**](menuhelpid.md) . **MENUHELPID** contiene una expresión numérica que identifica el menú durante el procesamiento de la [**\_ ayuda de WM**](../shell/wm-help.md) .

Además, cada estructura de **POPUPMENUITEM** que tenga el bit de **\_ menú emergente MFR** establecido en el miembro **ResInfo** irá seguida de una estructura [**MENUHELPID**](menuhelpid.md) más un número adicional de estructuras **POPUPMENUITEM** , una para cada elemento de menú de ese submenú. La última estructura **POPUPMENUITEM** del submenú tendrá el bit de **\_ final MFR** establecido en el miembro **resInfo** . Para buscar el final del recurso, busque un **\_ extremo MFR** coincidente para cada **\_ elemento popup MFR** más un **\_ extremo MFR** adicional que coincida con el conjunto más externo de elementos de menú.

Indique el último elemento de menú estableciendo el miembro de **tipo** en **MF \_ End**. Dado que puede anidar submenús, puede haber varios niveles de **MF \_ End**. En estos casos, los elementos de menú son secuenciales.

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

**Vista**
</dt> <dt>

[Recursos](resources.md)
</dt> </dl>

 

