---
description: Especifica el valor que supone una propiedad en un momento dado.
ms.assetid: 117868b7-65e5-4b3b-9e50-4106ee6a65d0
title: DEXTER_PARAM estructura (QEDIT. h)
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
ms.openlocfilehash: 22b0f6ef0a91f9a6d9163a03c17f6e86ee8b5f4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653724"
---
# <a name="dexter_param-structure"></a>Estructura del parámetro DEXTERity \_

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

Especifica el valor que supone una propiedad en un momento dado.

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

**Nvalores**
</dt> <dd>

Número de valores que asume la propiedad.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El objeto debe admitir la interfaz **IDispatch** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>QEDIT. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IPropertySetter**](ipropertysetter.md)
</dt> <dt>

[**valor de DEXTERity \_**](dexter-value.md)
</dt> </dl>

 

 




