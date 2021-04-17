---
title: Estructura ICONRESDIR
description: Contiene las dimensiones y el formato de color de una imagen de icono individual de un grupo de recursos. La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.
ms.assetid: 4c727369-2e90-40ad-85af-96d7e060b97a
keywords:
- Menús de la estructura ICONRESDIR y otros recursos
topic_type:
- apiref
api_name:
- ICONRESDIR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: de3d15bf250685e0b0cad935cd5e8094b2f2ceee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666019"
---
# <a name="iconresdir-structure"></a>Estructura ICONRESDIR

Contiene las dimensiones y el formato de color de una imagen de icono individual de un grupo de recursos. La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.

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

Tipo: **byte**

</dd> <dd>

Ancho del icono, en píxeles. Los valores aceptables son 16, 32 y 64.

</dd> <dt>

**Height**
</dt> <dd>

Tipo: **byte**

</dd> <dd>

Alto del icono, en píxeles. Los valores aceptables son 16, 32 y 64.

</dd> <dt>

**ColorCount**
</dt> <dd>

Tipo: **byte**

</dd> <dd>

El número de colores en el icono. Los valores aceptables son 2, 8 y 16.

</dd> <dt>

**sector**
</dt> <dd>

Tipo: **byte**

</dd> <dd>

Sector debe establecerse en el mismo valor que el del campo reservado en el encabezado del archivo de icono.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La estructura **ICONRESDIR** se pasa en la estructura [**RESDIR**](resdir.md) si la estructura **RESDIR** describe un icono.

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

**Vista**
</dt> <dt>

[Recursos](resources.md)
</dt> </dl>

 

 





