---
title: NORMALMENUITEM (estructura)
description: Contiene información sobre cada elemento de un recurso de menú que no abre un menú o un submenú. La definición de estructura que se proporciona aquí es solo para explicación; no está presente en ningún archivo de encabezado estándar.
ms.assetid: c1b84264-2d7f-4bc3-8e74-7b921a0bfe30
keywords:
- Menús de estructura NORMALMENUITEM y otros recursos
topic_type:
- apiref
api_name:
- NORMALMENUITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f47fef5e1481d56671cd525061f1a5fcf88481213671bac45c923cfbae0ebbd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118733695"
---
# <a name="normalmenuitem-structure"></a>NORMALMENUITEM (estructura)

Contiene información sobre cada elemento de un recurso de menú que no abre un menú o un submenú. La definición de estructura que se proporciona aquí es solo para explicación; no está presente en ningún archivo de encabezado estándar.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  WORD    resInfo;
  szOrOrd menuText;
} NORMALMENUITEM;
```



## <a name="members"></a>Miembros

<dl> <dt>

**resInfo**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Tipo de elemento de menú. Este miembro puede ser uno de los siguientes valores.



| Value                                                                                                                                                                                                       | Significado                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MFR_END"></span><span id="mfr_end"></span><dl> <dt>**MFR \_ End**</dt> <dt>0x80</dt> </dl>       | El elemento de menú es el último de este submenú o recurso de menú; el sistema usa internamente esta marca.<br/> |
| <span id="MFR_POPUP"></span><span id="mfr_popup"></span><dl> <dt>**MFR \_ Ventana emergente**</dt> <dt>0x01</dt> </dl> | El elemento de menú abre un menú o un submenú; el sistema usa internamente la marca . <br/>                    |



 

</dd> <dt>

**menuText**
</dt> <dd>

Tipo: **szOrOrd**

</dd> <dd>

Cadena Unicode terminada en NULL que contiene el texto de este elemento de menú. No hay ningún límite fijo en el tamaño de esta cadena.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Hay una **estructura NORMALMENUITEM para** cada elemento de menú que no abre un menú o un submenú. Indique el último elemento de menú de un menú estableciendo el **miembro resInfo** en **MFR \_ END.**

Un separador de menús es un tipo especial de elemento de menú que está inactivo, pero que aparece como una barra divisora entre dos elementos de menú activos. Indique un separador de menús dejando vacío **el miembro menuText.**

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

[**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)
</dt> <dt>

[**POPUPMENUITEM**](popupmenuitem.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Recursos](resources.md)
</dt> </dl>

 

 





