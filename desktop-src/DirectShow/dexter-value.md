---
description: Identifica una propiedad que se va a establecer en una transición o efecto, junto con el número de valores distintos que la propiedad asume durante la duración de la transición o efecto.
ms.assetid: 3b1c35cf-f1f7-4f2c-8d94-1aaae4116833
title: DEXTER_VALUE estructura (Qedit.h)
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
ms.openlocfilehash: e8e76636a28f1eaa8f3bd948c29e4ab6b2440c75bb4265f6d3c1bf281599bbf6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051955"
---
# <a name="dexter_value-structure"></a>ESTRUCTURA VALUE DE LA ESTRUCTURA DE VALUE DE LA PROPIEDAD \_

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

Identifica una propiedad que se va a establecer en una transición o efecto, junto con el número de valores distintos que la propiedad asume durante la duración de la transición o efecto.

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

**V**
</dt> <dd>

Valor de la propiedad.

</dd> <dt>

**Rt**
</dt> <dd>

Hora a la que la propiedad asume el valor, en relación con el inicio de la transición o el efecto.

</dd> <dt>

**dwInterp**
</dt> <dd>

Marca que indica cómo progresa la propiedad del valor anterior a este valor. Debe ser una de las siguientes:



| Value                                                                                                                                                                           | Significado                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="DEXTERF_JUMP"></span><span id="dexterf_jump"></span><dl> <dt>**JUMP \_ DE**</dt> </dl>                      | La propiedad salta al instante al nuevo valor en el momento especificado.<br/>     |
| <span id="DEXTERF_INTERPOLATE"></span><span id="dexterf_interpolate"></span><dl> <dt>**INTERPOLACIÓN \_ DE INTERPOLACIÓN**</dt> </dl> | La propiedad se interpola linealmente a lo largo del tiempo con respecto al valor anterior.<br/> |



 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Qedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IPropertySetter**](ipropertysetter.md)
</dt> <dt>

[**PARAM DE \_**](dexter-param.md)
</dt> </dl>

 

 




