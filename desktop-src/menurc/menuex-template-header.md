---
title: MENUEX_TEMPLATE_HEADER estructura
description: Define el encabezado de una plantilla de menú extendida. Esta definición de estructura es solo para explicación; no está presente en ningún archivo de encabezado estándar.
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
ms.openlocfilehash: 31e52661e04a036cf7a49791be96af002b801af0e0ed1c4b6ad3ddebf971c2c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119226125"
---
# <a name="menuex_template_header-structure"></a>ESTRUCTURA DE ENCABEZADO \_ DE \_ PLANTILLA MENUEX

Define el encabezado de una plantilla de menú extendida. Esta definición de estructura es solo para explicación; no está presente en ningún archivo de encabezado estándar.

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

Tipo: **WORD**

</dd> <dd>

Número de versión de la plantilla. Este miembro debe ser 1 para las plantillas de menú extendidas.

</dd> <dt>

**wOffset**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Desplazamiento a la primera estructura [**MENUEX \_ TEMPLATE \_ ITEM,**](menuex-template-item.md) con respecto al final de este miembro de estructura. Si la definición del primer elemento sigue inmediatamente al **miembro dwHelpId,** este miembro debe ser 4.

</dd> <dt>

**dwHelpId**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Identificador de ayuda de la barra de menús.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Una plantilla de menú extendida consta de una estructura **MENUEX \_ TEMPLATE \_ HEADER** seguida de una o varias estructuras [**MENUEX \_ TEMPLATE ITEM contiguas. \_**](menuex-template-item.md) Las **estructuras MENUEX \_ TEMPLATE \_ ITEM,** que tienen una longitud variable, se alinean en **los límites DWORD.** Para crear un menú a partir de una plantilla de menú extendida en memoria, use la [**función LoadMenuIndirect.**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta)

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

[**ELEMENTO DE PLANTILLA \_ MENUEX \_**](menuex-template-item.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Menús](menus.md)
</dt> </dl>

 

 





