---
title: Estructura MENUHELPID
description: Contiene los datos finales escritos en el \_ recurso de menú RT para un menú o un submenú si el miembro resInfo de la estructura POPUPMENUITEM se establece en MFR \_ Popup.
ms.assetid: f17fdaaa-b37c-4902-bad4-a1181ffee9f9
keywords:
- Menús de la estructura MENUHELPID y otros recursos
topic_type:
- apiref
api_name:
- MENUHELPID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b90b5a4745433c92a859a168611aa1c14f1fa45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666073"
---
# <a name="menuhelpid-structure"></a>Estructura MENUHELPID

Contiene los datos finales escritos en el recurso de [**\_ menú RT**](/windows/desktop/menurc/resource-types) para un menú o un submenú si el miembro **ResInfo** de la estructura [**POPUPMENUITEM**](popupmenuitem.md) se establece en **MFR \_ popup**. La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  DWORD helpID;
} MENUHELPID;
```



## <a name="members"></a>Miembros

<dl> <dt>

**helpID**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

El identificador que se usa para identificar el menú durante el procesamiento de la [**\_ ayuda de WM**](/windows/desktop/shell/wm-help) .

</dd> </dl>

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

[**POPUPMENUITEM**](popupmenuitem.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Recursos](resources.md)
</dt> </dl>

 

