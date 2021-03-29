---
title: Estructura NORMALMENUITEM
description: Contiene información sobre cada elemento de un recurso de menú que no abre un menú o un submenú. La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.
ms.assetid: c1b84264-2d7f-4bc3-8e74-7b921a0bfe30
keywords:
- Menús de la estructura NORMALMENUITEM y otros recursos
topic_type:
- apiref
api_name:
- NORMALMENUITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c90efe624346e30483c42f6f8ff51cd6d3550922
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359701"
---
# <a name="normalmenuitem-structure"></a>Estructura NORMALMENUITEM

Contiene información sobre cada elemento de un recurso de menú que no abre un menú o un submenú. La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.

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

Tipo: **Word**

</dd> <dd>

El tipo de elemento de menú. Este miembro puede ser uno de los valores siguientes.



| Value                                                                                                                                                                                                       | Significado                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MFR_END"></span><span id="mfr_end"></span><dl> <dt>**MFR \_ FINALIZAR**</dt> <dt>0x80</dt> </dl>       | El elemento de menú es el último de este recurso de menú o submenú; Este marcador lo utiliza internamente el sistema.<br/> |
| <span id="MFR_POPUP"></span><span id="mfr_popup"></span><dl> <dt>**MFR \_ EMERGENTE**</dt> <dt>0x01</dt> </dl> | El elemento de menú abre un menú o un submenú; el sistema utiliza internamente la marca. <br/>                    |



 

</dd> <dt>

**menuText**
</dt> <dd>

Tipo: **szOrOrd**

</dd> <dd>

Una cadena Unicode terminada en null que contiene el texto de este elemento de menú. No hay ningún límite fijo en el tamaño de esta cadena.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Hay una estructura **NORMALMENUITEM** para cada elemento de menú que no abre un menú o un submenú. Indicar el último elemento de menú de un menú estableciendo el miembro **resInfo** en **MFR \_ End**.

Un separador de menús es un tipo especial de elemento de menú que está inactivo, pero aparece como una barra divisoria entre dos elementos de menú activos. Indicar un separador de menús manteniendo el miembro de **menuText** vacío.

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

**Vista**
</dt> <dt>

[Recursos](resources.md)
</dt> </dl>

 

 





