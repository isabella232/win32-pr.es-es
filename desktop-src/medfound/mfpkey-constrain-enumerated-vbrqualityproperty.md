---
description: Especifica si los modos enumerados por el codificador se acalo a los que cumplen un requisito de calidad especificado por MFPKEY \_ DESIRED \_ VBRQUALITY.
ms.assetid: b2f1d5c5-d2bb-4a8a-94ea-fd969e07bb0e
title: MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cb9e63ab955bbe7726ab67bdab057fe2d397942
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127257700"
---
# <a name="mfpkey_constrain_enumerated_vbrquality-property"></a>Propiedad \_ \_ VBRQUALITY ENUMERADA DE MFPKEY CONSTRAIN \_

Especifica si los modos enumerados por el codificador se acalo a los que cumplen un requisito de calidad dado por [**MFPKEY \_ DESIRED \_ VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md).

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de datos

**VT \_ BOOL**

## <a name="default-value"></a>Valor predeterminado

**VARIANT \_ FALSE**

## <a name="remarks"></a>Observaciones

Para enumerar los modos de VBR que cumplen un determinado requisito de calidad, establezca las siguientes propiedades del codificador.

-   Establezca [**MFPKEY \_ VBRENABLED en**](mfpkey-vbrenabledproperty.md) VARIANT **\_ TRUE.**
-   Establezca **MFPKEY \_ CONSTRAIN \_ ENUMERATED \_ VBRQUALITY** en **VARIANT \_ TRUE.**
-   Establezca [**MFPKEY \_ DESIRED \_ VBRQUALITY en**](mfpkey-desired-vbrqualityproperty.md) la calidad deseada. Para los modos sin pérdida, establezca la calidad deseada en 100.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Remoto<br/> | Windows Vista o Windows 7<br/>                                                   |
| Encabezado<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 
