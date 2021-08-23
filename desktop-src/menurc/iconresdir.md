---
title: ICONRESDIR (estructura)
description: Contiene las dimensiones y el formato de color de una imagen de icono individual en un grupo de recursos. La definición de estructura que se proporciona aquí es solo para explicación; no está presente en ningún archivo de encabezado estándar.
ms.assetid: 4c727369-2e90-40ad-85af-96d7e060b97a
keywords:
- ICONRESDIR structure Menus and Other Resources
topic_type:
- apiref
api_name:
- ICONRESDIR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f81f8b0a530e7c6c85f2ad1749e0a7373f68b0bf902b71a86889b92184806ffc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034283"
---
# <a name="iconresdir-structure"></a>ICONRESDIR (estructura)

Contiene las dimensiones y el formato de color de una imagen de icono individual en un grupo de recursos. La definición de estructura que se proporciona aquí es solo para explicación; no está presente en ningún archivo de encabezado estándar.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  BYTE Width;
  BYTE Height;
  BYTE ColorCount;
  BYTE reserved;
} ICONRESDIR;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Width**
</dt> <dd>

Tipo: **BYTE**

</dd> <dd>

Ancho del icono, en píxeles. Los valores aceptables son 16, 32 y 64.

</dd> <dt>

**Height**
</dt> <dd>

Tipo: **BYTE**

</dd> <dd>

Alto del icono, en píxeles. Los valores aceptables son 16, 32 y 64.

</dd> <dt>

**ColorCount**
</dt> <dd>

Tipo: **BYTE**

</dd> <dd>

Número de colores del icono. Los valores aceptables son 2, 8 y 16.

</dd> <dt>

**reserved**
</dt> <dd>

Tipo: **BYTE**

</dd> <dd>

Reservado; debe establecerse en el mismo valor que el del campo reservado en el encabezado de archivo de icono.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **estructura ICONRESDIR** se pasa en la [**estructura RESDIR**](resdir.md) si la **estructura RESDIR** describe un icono.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**RESDIR**](resdir.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Recursos](resources.md)
</dt> </dl>

 

 





