---
title: MENUHELPID (estructura)
description: Contiene los datos finales escritos en el recurso RT MENU para un menú o submenú si el miembro resInfo de la estructura POPUPMENUITEM está establecido \_ en MFR \_ POPUP.
ms.assetid: f17fdaaa-b37c-4902-bad4-a1181ffee9f9
keywords:
- Menús de estructura MENUHELPID y otros recursos
topic_type:
- apiref
api_name:
- MENUHELPID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4831074d5e7b663210f880bf6684cbc6484ad3487a0c6c9e5be308aebc66291a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825955"
---
# <a name="menuhelpid-structure"></a>MENUHELPID (estructura)

Contiene los datos finales escritos en el recurso [**RT \_ MENU**](/windows/desktop/menurc/resource-types) de un menú o submenú si el **miembro resInfo** de la estructura [**POPUPMENUITEM**](popupmenuitem.md) está establecido en **MFR \_ POPUP.** La definición de estructura que se proporciona aquí es solo para una explicación; no está presente en ningún archivo de encabezado estándar.

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

Identificador utilizado para identificar el menú durante el [**procesamiento de \_ WM HELP.**](/windows/desktop/shell/wm-help)

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

**Conceptual**
</dt> <dt>

[Recursos](resources.md)
</dt> </dl>

 

