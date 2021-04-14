---
description: Especifica el nivel de calidad deseado para la codificación de velocidad de bits variable (VBR) (1-pass) de la calidad de las secuencias de audio.
ms.assetid: 0bbb4f51-78c3-4455-bd96-9a6d80110220
title: Propiedad MFPKEY_DESIRED_VBRQUALITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8aa0f2cf86db076fa211f9c850db15de730a3a14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648309"
---
# <a name="mfpkey_desired_vbrquality-property"></a>MFPKEY \_ \_ propiedad VBRQUALITY deseada

Especifica el nivel de calidad deseado para la codificación de velocidad de bits variable (VBR) (1-pass) de la calidad de las secuencias de audio.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

**VT \_ UI4**

## <a name="default-value"></a>Valor predeterminado

0

## <a name="remarks"></a>Observaciones

Este valor puede estar comprendido entre 0 y 100, donde 100 es la calidad máxima. Un valor de 0 indica que no se va a usar el método de codificación VBR basado en la calidad.

Para enumerar los modos VBR que cumplen un requisito de calidad determinado, establezca las siguientes propiedades del codificador.

-   Establezca [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) en **Variant \_ true**.
-   Establezca [**MFPKEY \_ restricción de \_ \_ VBRQUALITY enumerada**](mfpkey-constrain-enumerated-vbrqualityproperty.md) en **Variant \_ true**.
-   Establezca **MFPKEY \_ deseado \_ VBRQUALITY** en la calidad deseada. En el caso de los modos sin pérdida, establezca la calidad deseada en 100.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
