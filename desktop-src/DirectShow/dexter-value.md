---
description: Identifica una propiedad que se va a establecer en una transición o efecto, junto con el número de valores distintos que la propiedad asume a lo largo de la transición o efecto.
ms.assetid: 3b1c35cf-f1f7-4f2c-8d94-1aaae4116833
title: DEXTER_VALUE estructura (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEXTER_VALUE
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 930b828e1b715cfcb53275192ed76a7df7d116ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680420"
---
# <a name="dexter_value-structure"></a>Estructura del valor de DEXTERity \_

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

Identifica una propiedad que se va a establecer en una transición o efecto, junto con el número de valores distintos que la propiedad asume a lo largo de la transición o efecto.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  VARIANT        v;
  REFERENCE_TIME rt;
  DWORD          dwInterp;
} DEXTER_VALUE;
```



## <a name="members"></a>Miembros

<dl> <dt>

**v**
</dt> <dd>

Valor de la propiedad.

</dd> <dt>

**RT**
</dt> <dd>

Hora a la que la propiedad asume el valor, en relación con el inicio de la transición o efecto.

</dd> <dt>

**dwInterp**
</dt> <dd>

Marca que indica cómo progresa la propiedad desde el valor anterior a este valor. Debe ser una de las siguientes:



| Value                                                                                                                                                                           | Significado                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="DEXTERF_JUMP"></span><span id="dexterf_jump"></span><dl> <dt>**salto de DEXTERF \_**</dt> </dl>                      | La propiedad salta inmediatamente al nuevo valor en el momento especificado.<br/>     |
| <span id="DEXTERF_INTERPOLATE"></span><span id="dexterf_interpolate"></span><dl> <dt>**DEXTERF \_ interpolación**</dt> </dl> | La propiedad se interpola linealmente a lo largo del tiempo desde el valor anterior.<br/> |



 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>QEDIT. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IPropertySetter**](ipropertysetter.md)
</dt> <dt>

[**parámetro DEXTERity \_**](dexter-param.md)
</dt> </dl>

 

 




