---
description: Especifica si los modos enumerados por el codificador se enclaves a los que cumplen un requisito de calidad dado por MFPKEY \_ DESIRED \_ VBRQUALITY.
ms.assetid: b2f1d5c5-d2bb-4a8a-94ea-fd969e07bb0e
title: MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d138bbf7e9e77673821b6deed574b7395a3d4e51269e71b18b67cda711ed4bbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117690447"
---
# <a name="mfpkey_constrain_enumerated_vbrquality-property"></a>Propiedad \_ \_ VBRQUALITY ENUMERADA DE RESTRICCIÓN \_ DE MFPKEY

Especifica si los modos enumerados por el codificador se enclaves a los que cumplen un requisito de calidad especificado por [**MFPKEY \_ DESIRED \_ VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md).

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

**VT \_ BOOL**

## <a name="default-value"></a>Valor predeterminado

**VARIANT \_ FALSE**

## <a name="remarks"></a>Comentarios

Para enumerar los modos de VBR que cumplen un determinado requisito de calidad, establezca las siguientes propiedades del codificador.

-   Establezca [**MFPKEY \_ VBRENABLED en**](mfpkey-vbrenabledproperty.md) VARIANT **\_ TRUE.**
-   Establezca **MFPKEY \_ CONSTRAIN \_ ENUMERATED \_ VBRQUALITY** en **VARIANT \_ TRUE.**
-   Establezca [**MFPKEY \_ DESIRED \_ VBRQUALITY en**](mfpkey-desired-vbrqualityproperty.md) la calidad deseada. Para los modos sin pérdida, establezca la calidad deseada en 100.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| Cliente<br/> | Windows Vista o Windows 7<br/>                                                   |
| Header<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 
