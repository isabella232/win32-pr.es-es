---
description: Especifica el nivel de calidad deseado para la codificación de velocidad de bits variable (VBR) basada en calidad (1 paso) de secuencias de audio.
ms.assetid: 0bbb4f51-78c3-4455-bd96-9a6d80110220
title: MFPKEY_DESIRED_VBRQUALITY propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f52ab8cc791a5309b5df6537d133bce68e49d66a15ab79c12beeb7411cece8e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939961"
---
# <a name="mfpkey_desired_vbrquality-property"></a>Propiedad \_ VBRQUALITY DESEADA DE MFPKEY \_

Especifica el nivel de calidad deseado para la codificación de velocidad de bits variable (VBR) basada en calidad (1 paso) de secuencias de audio.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

**VT \_ UI4**

## <a name="default-value"></a>Valor predeterminado

0

## <a name="remarks"></a>Comentarios

Este valor puede ser de 0 a 100, donde 100 es la calidad máxima. Un valor de 0 indica que no se va a usar el método de codificación VBR basado en calidad.

Para enumerar los modos de VBR que cumplen un determinado requisito de calidad, establezca las siguientes propiedades del codificador.

-   Establezca [**MFPKEY \_ VBRENABLED en**](mfpkey-vbrenabledproperty.md) VARIANT **\_ TRUE.**
-   Establezca [**MFPKEY \_ CONSTRAIN \_ ENUMERATED \_ VBRQUALITY**](mfpkey-constrain-enumerated-vbrqualityproperty.md) en **VARIANT \_ TRUE.**
-   Establezca **MFPKEY \_ DESIRED \_ VBRQUALITY en** la calidad deseada. Para los modos sin pérdida, establezca la calidad deseada en 100.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 
