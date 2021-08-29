---
description: Especifica el valor que una propiedad asume en un momento dado.
ms.assetid: 117868b7-65e5-4b3b-9e50-4106ee6a65d0
title: DEXTER_PARAM estructura (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEXTER_PARAM
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 13bd14602b331e334cdec8cd1aedc7250b04c0ae4df2e5e4e9997c67c84d707d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051965"
---
# <a name="dexter_param-structure"></a>ESTRUCTURA DE PARAM DE PARAM DE PARAM DE \_ PARAM

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

Especifica el valor que una propiedad asume en un momento dado.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  BSTR   Name;
  DISPID dispID;
  LONG   nValues;
} DEXTER_PARAM;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Nombre**
</dt> <dd>

Nombre de la propiedad.

</dd> <dt>

**dispID**
</dt> <dd>

Reservado. Establecer en cero.

</dd> <dt>

**nValues**
</dt> <dd>

Número de valores que la propiedad asume.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El objeto debe admitir la **interfaz IDispatch.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Qedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IPropertySetter**](ipropertysetter.md)
</dt> <dt>

[**VALUE DE LA \_ PROPIEDAD**](dexter-value.md)
</dt> </dl>

 

 




