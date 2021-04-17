---
description: La estructura de \_ bits con etiqueta define un par de bits de etiqueta.
ms.assetid: 500b5159-bf9f-49d4-8567-d8e462015eb0
title: Estructura de LABELED_BIT (Netmon. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652457"
---
# <a name="labeled_bit-structure"></a>Estructura de \_ bits con etiqueta

La estructura de **\_ bits con etiqueta** define un par de bits de etiqueta.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _LABELED_BIT {
  BYTE  BitNumber;
  LPSTR LabelOff;
  LPSTR LabelOn;
} LABELED_BIT, *LPLABELED_BIT;
```



## <a name="members"></a>Miembros

<dl> <dt>

**BitNumber**
</dt> <dd>

Número de bits del par de bits de etiqueta. Los valores oscilan entre 0 y 255. Establezca el miembro **Bitnumber** en el bit usado en la comparación del valor de propiedad.

</dd> <dt>

**LabelOff**
</dt> <dd>

Cadena o etiqueta que se muestra cuando el BIT especificado en **BitNumber** es igual a cero. Por ejemplo, una posible etiqueta es "bit OFF".

</dd> <dt>

**Etiquetaon**
</dt> <dd>

Cadena o etiqueta que se muestra cuando el BIT especificado en **BitNumber** es igual a 1. Por ejemplo, una posible etiqueta es "bit ON".

</dd> </dl>

## <a name="remarks"></a>Observaciones

Una matriz de estructuras de **\_ bits con etiqueta** se utiliza para definir un conjunto de pares de bits de etiqueta. Un puntero a la matriz se especifica en el miembro **lpLabeledBit** de la estructura [set](set.md) . Los pares se usan cuando se desea mostrar una etiqueta basada en la configuración de cada BIT. Normalmente, este tipo de conjunto se usa para indicar el valor ON u OFF de BITs.

Cuando se especifica un conjunto de bits, Monitor de red muestra solo los BITs incluidos en la matriz de estructuras de **conjunto** . No se muestran los BITs que no están en la estructura **set** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[SET](set.md)
</dt> </dl>

 

 




