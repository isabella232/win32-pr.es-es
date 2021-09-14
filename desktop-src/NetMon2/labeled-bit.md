---
description: La estructura LABELED \_ BIT define un par BIT de etiqueta.
ms.assetid: 500b5159-bf9f-49d4-8567-d8e462015eb0
title: LABELED_BIT estructura (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_BIT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 24a56e832600b551dd3ab43ea93d59c5805af630
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071529"
---
# <a name="labeled_bit-structure"></a>Labeled \_ BIT (estructura)

La **estructura LABELED \_ BIT** define un par BIT de etiqueta.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _LABELED_BIT {
  BYTE  BitNumber;
  LPSTR LabelOff;
  LPSTR LabelOn;
} LABELED_BIT, *LPLABELED_BIT;
```



## <a name="members"></a>Members

<dl> <dt>

**BitNumber**
</dt> <dd>

Número BIT del par BIT de etiqueta. Los valores oscilan entre 0 y 255. Establezca el **miembro Bitnumber** en el BIT utilizado en la comparación del valor de propiedad.

</dd> <dt>

**LabelOff**
</dt> <dd>

Cadena o etiqueta que se muestra cuando el BIT especificado en **BitNumber** es igual a cero. Por ejemplo, una posible etiqueta es "Bit OFF".

</dd> <dt>

**LabelOn**
</dt> <dd>

Cadena o etiqueta que se muestra cuando el BIT especificado en **BitNumber** es igual a 1. Por ejemplo, una posible etiqueta es "Bit ON".

</dd> </dl>

## <a name="remarks"></a>Observaciones

Se usa una **matriz de estructuras LABELED \_ BIT** para definir un conjunto de pares BIT de etiqueta. Se especifica un puntero a la matriz en el **miembro lpLabeledBit** de la [estructura SET.](set.md) Los pares se usan cuando se desea mostrar una etiqueta en función de la configuración de cada BIT. Normalmente, este tipo de conjunto se usa para indicar el valor ON u OFF de los BIT.

Cuando se especifica un conjunto DE BITS, Monitor de red muestra solo los BI incluidos en la matriz de **estructuras SET.** No se muestran los BIT que no están en la **estructura SET.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[SET](set.md)
</dt> </dl>

 

 




