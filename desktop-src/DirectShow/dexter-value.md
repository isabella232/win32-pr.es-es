---
description: Identifica una propiedad que se va a establecer en una transición o efecto, junto con el número de valores distintos que la propiedad asume durante la duración de la transición o el efecto.
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
ms.openlocfilehash: 930b828e1b715cfcb53275192ed76a7df7d116ec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072226"
---
# <a name="dexter_value-structure"></a>ESTRUCTURA VALUE DE LA PROPIEDAD \_

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

Identifica una propiedad que se va a establecer en una transición o efecto, junto con el número de valores distintos que la propiedad asume durante la duración de la transición o el efecto.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  VARIANT        v;
  REFERENCE_TIME rt;
  DWORD          dwInterp;
} DEXTER_VALUE;
```



## <a name="members"></a>Members

<dl> <dt>

**V**
</dt> <dd>

Valor de la propiedad.

</dd> <dt>

**rt**
</dt> <dd>

Hora en la que la propiedad asume el valor, en relación con el inicio de la transición o el efecto.

</dd> <dt>

**dwInterp**
</dt> <dd>

Marca que indica cómo progresa la propiedad del valor anterior a este valor. Debe ser una de las siguientes:



| Value                                                                                                                                                                           | Significado                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="DEXTERF_JUMP"></span><span id="dexterf_jump"></span><dl> <dt>**JUMP DE JUMP DE \_**</dt> </dl>                      | La propiedad salta al instante al nuevo valor en el momento especificado.<br/>     |
| <span id="DEXTERF_INTERPOLATE"></span><span id="dexterf_interpolate"></span><dl> <dt>**INTERPOLACIÓN \_ DE INTERPOLACIÓN**</dt> </dl> | La propiedad se interpola linealmente a lo largo del tiempo con respecto al valor anterior.<br/> |



 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Qedit.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IPropertySetter**](ipropertysetter.md)
</dt> <dt>

[**PARAM DE \_**](dexter-param.md)
</dt> </dl>

 

 




