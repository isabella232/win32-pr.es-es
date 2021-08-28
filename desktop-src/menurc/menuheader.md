---
title: MENUHEADER (estructura)
description: Contiene información de versión del recurso de menú. La definición de estructura que se proporciona aquí es solo para explicación; no está presente en ningún archivo de encabezado estándar.
ms.assetid: 1e34b0b6-18ff-4cb6-901e-a2aabad0df74
keywords:
- Menús de estructura MENUHEADER y otros recursos
topic_type:
- apiref
api_name:
- MENUHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3e78b577d52f0e40737f90186903aff9bfe2470d7050eac1ee00bc79ca7f596f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972014"
---
# <a name="menuheader-structure"></a>MENUHEADER (estructura)

Contiene información de versión del recurso de menú. La definición de estructura que se proporciona aquí es solo para explicación; no está presente en ningún archivo de encabezado estándar.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  WORD wVersion;
  WORD cbHeaderSize;
} MENUHEADER;
```



## <a name="members"></a>Miembros

<dl> <dt>

**wVersion**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Número de versión de la plantilla de menú. Este miembro debe ser igual a cero para indicar que se trata de un [**\_ MENÚ RT creado**](/windows/desktop/menurc/resource-types) con una plantilla de menú estándar.

</dd> <dt>

**cbHeaderSize**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Tamaño del encabezado de plantilla de menú. Este valor es cero para los menús que cree con una plantilla de menú estándar.

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

[**ENCABEZADO DE PLANTILLA \_ MENUEX \_**](menuex-template-header.md)
</dt> <dt>

[**ELEMENTO DE PLANTILLA MENUEX \_ \_**](menuex-template-item.md)
</dt> <dt>

[**MENUITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate)
</dt> <dt>

[**MENUITEMTEMPLATEHEADER**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader)
</dt> <dt>

[**NORMALMENUITEM**](normalmenuitem.md)
</dt> <dt>

[**POPUPMENUITEM**](popupmenuitem.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Recursos](resources.md)
</dt> </dl>

 

