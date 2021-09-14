---
description: Especifica el nivel de calidad deseado para la codificación de velocidad de bits variable (VBR) basada en calidad (1 paso) de secuencias de audio.
ms.assetid: 0bbb4f51-78c3-4455-bd96-9a6d80110220
title: MFPKEY_DESIRED_VBRQUALITY propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8aa0f2cf86db076fa211f9c850db15de730a3a14
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127257580"
---
# <a name="mfpkey_desired_vbrquality-property"></a>Propiedad MFPKEY \_ DESIRED \_ VBRQUALITY

Especifica el nivel de calidad deseado para la codificación de velocidad de bits variable (VBR) basada en calidad (1 paso) de secuencias de audio.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de datos

**VT \_ UI4**

## <a name="default-value"></a>Valor predeterminado

0

## <a name="remarks"></a>Observaciones

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
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 
