---
title: NEWHEADER (estructura)
description: Contiene el número de componentes de icono o cursor de un grupo de recursos. La definición de estructura que se proporciona aquí es solo para una explicación; no está presente en ningún archivo de encabezado estándar.
ms.assetid: 1549579a-b558-42a9-9b3b-5b382334221c
keywords:
- Menús de estructura NEWHEADER y otros recursos
topic_type:
- apiref
api_name:
- NEWHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f8ce5407686d5e0e8ad4c0f17856241e9b47c70b2375f93f3b2b9046210d2faa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011775"
---
# <a name="newheader-structure"></a>NEWHEADER (estructura)

Contiene el número de componentes de icono o cursor de un grupo de recursos. La definición de estructura que se proporciona aquí es solo para una explicación; no está presente en ningún archivo de encabezado estándar.

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

Tipo: **WORD**

</dd> <dd>

Reservado; debe ser cero.

</dd> <dt>

**ResType**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

El tipo de recurso. Este miembro debe tener uno de los siguientes valores.



| Value                                                                                                                                                                                                       | Significado                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="RES_CURSOR"></span><span id="res_cursor"></span><dl> <dt>**RES \_ CURSOR**</dt> <dt>2</dt> </dl> | Tipo de recurso cursor.<br/> |
| <span id="RES_ICON"></span><span id="res_icon"></span><dl> <dt>**RES \_ ICONO**</dt> <dt>1</dt> </dl>       | Tipo de recurso de icono.<br/>   |



 

</dd> <dt>

**ResCount**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Número de componentes de icono o cursor del grupo de recursos.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Una o varias [**estructuras RESDIR**](resdir.md) siguen inmediatamente la **estructura NEWHEADER** en el archivo .res. El **miembro ResCount** especifica el número de estructuras **RESDIR.**

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

 

 





