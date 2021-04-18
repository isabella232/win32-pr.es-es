---
description: Especifica si los modos enumerados por el codificador se Limeted a aquellos que cumplen un requisito de calidad proporcionado por \_ MFPKEY \_ VBRQUALITY deseado.
ms.assetid: b2f1d5c5-d2bb-4a8a-94ea-fd969e07bb0e
title: Propiedad MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cb9e63ab955bbe7726ab67bdab057fe2d397942
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700367"
---
# <a name="mfpkey_constrain_enumerated_vbrquality-property"></a>\_ \_ Propiedad VBRQUALITY enumerada MFPKEY restringida \_

Especifica si los modos enumerados por el codificador se Limeted a aquellos que cumplen un requisito de calidad proporcionado [**por \_ MFPKEY \_ VBRQUALITY deseado**](mfpkey-desired-vbrqualityproperty.md).

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

**VT \_ bool**

## <a name="default-value"></a>Valor predeterminado

**VARIANTE \_ false**

## <a name="remarks"></a>Observaciones

Para enumerar los modos VBR que cumplen un requisito de calidad determinado, establezca las siguientes propiedades del codificador.

-   Establezca [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) en **Variant \_ true**.
-   Establezca **MFPKEY \_ restricción de \_ \_ VBRQUALITY enumerada** en **Variant \_ true**.
-   Establezca [**MFPKEY \_ deseado \_ VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) en la calidad deseada. En el caso de los modos sin pérdida, establezca la calidad deseada en 100.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Remoto<br/> | Windows Vista o Windows 7<br/>                                                   |
| Encabezado<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
