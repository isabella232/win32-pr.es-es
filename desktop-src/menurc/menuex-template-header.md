---
title: Estructura de MENUEX_TEMPLATE_HEADER
description: Define el encabezado de una plantilla de menú extendida. Esta definición de estructura solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.
ms.assetid: df763349-7127-482e-8613-74e68addde5d
keywords:
- MENUEX_TEMPLATE_HEADER menús de estructura y otros recursos
topic_type:
- apiref
api_name:
- MENUEX_TEMPLATE_HEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: caa255ccdbe76c3959d9c730bcaa52ec07428742
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714557"
---
# <a name="menuex_template_header-structure"></a>Estructura del encabezado de \_ plantilla MENUEX \_

Define el encabezado de una plantilla de menú extendida. Esta definición de estructura solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  WORD  wVersion;
  WORD  wOffset;
  DWORD dwHelpId;
} MENUEX_TEMPLATE_HEADER;
```



## <a name="members"></a>Miembros

<dl> <dt>

**wVersion**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

El número de versión de la plantilla. Este miembro debe ser 1 para las plantillas de menú extendidas.

</dd> <dt>

**wOffset**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Desplazamiento a la primera estructura [**de \_ \_ elementos de plantilla MENUEX**](menuex-template-item.md) , con respecto al final de este miembro de estructura. Si la primera definición de elemento sigue inmediatamente al miembro **dwHelpId** , este miembro debe ser 4.

</dd> <dt>

**dwHelpId**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

El identificador de la ayuda de la barra de menús.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Una plantilla de menú extendida está formada por una estructura de **\_ \_ encabezado de plantilla de MENUEX** , seguida de una o varias estructuras de [**\_ \_ elemento de plantilla MENUEX**](menuex-template-item.md) contiguas. Las estructuras de **\_ \_ elementos de plantilla MENUEX** , que son de longitud variable, se alinean en los límites **DWORD** . Para crear un menú a partir de una plantilla de menú extendida en memoria, use la función [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta)
</dt> <dt>

[**\_elemento de plantilla MENUEX \_**](menuex-template-item.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Menús](menus.md)
</dt> </dl>

 

 





