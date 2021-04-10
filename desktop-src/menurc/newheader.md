---
title: Estructura NEWHEADER
description: Contiene el número de componentes de icono o de cursor de un grupo de recursos. La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.
ms.assetid: 1549579a-b558-42a9-9b3b-5b382334221c
keywords:
- Menús de la estructura NEWHEADER y otros recursos
topic_type:
- apiref
api_name:
- NEWHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d215bc00ef414d4e626d3da657dcecfd7a8a6c8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996068"
---
# <a name="newheader-structure"></a>Estructura NEWHEADER

Contiene el número de componentes de icono o de cursor de un grupo de recursos. La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  WORD Reserved;
  WORD ResType;
  WORD ResCount;
} NEWHEADER, *NEWHEADER;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Reserved**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Sector debe ser cero.

</dd> <dt>

**ResType**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

El tipo de recurso. Este miembro debe tener uno de los valores siguientes.



| Value                                                                                                                                                                                                       | Significado                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="RES_CURSOR"></span><span id="res_cursor"></span><dl> <dt>**Res \_ CURSOR**</dt> <dt>2</dt> </dl> | Tipo de recurso de cursor.<br/> |
| <span id="RES_ICON"></span><span id="res_icon"></span><dl> <dt>**Res \_ ICONO**</dt> <dt>1</dt> </dl>       | Tipo de recurso de icono.<br/>   |



 

</dd> <dt>

**ResCount**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

El número de componentes de icono o de cursor en el grupo de recursos.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Una o varias estructuras [**RESDIR**](resdir.md) siguen inmediatamente a la estructura **NEWHEADER** del archivo. res. El miembro **ResCount** especifica el número de estructuras **RESDIR** .

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

 

 





