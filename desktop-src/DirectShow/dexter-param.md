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
ms.openlocfilehash: 22b0f6ef0a91f9a6d9163a03c17f6e86ee8b5f4e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072229"
---
# <a name="dexter_param-structure"></a>ESTRUCTURA DE PARAM DE PARAM DE \_ PARAM

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



## <a name="members"></a>Members

<dl> <dt>

**Nombre**
</dt> <dd>

Nombre de la propiedad.

</dd> <dt>

**dispID**
</dt> <dd>

Reservado. Establecer en cero.

</dd> <dt>

**nValores**
</dt> <dd>

Número de valores que la propiedad presupone.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El objeto debe admitir la **interfaz IDispatch.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Qedit.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IPropertySetter**](ipropertysetter.md)
</dt> <dt>

[**VALOR DE \_ DESASTROS**](dexter-value.md)
</dt> </dl>

 

 




