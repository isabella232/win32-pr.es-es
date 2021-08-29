---
description: Especifica el número preferido de muestras por fotograma.
ms.assetid: ad629dbd-49d8-43d0-95a8-03f2043e397e
title: MFPKEY_PREFERRED_FRAMESIZE propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a82fbc234235d0caf46b5c1a0fa3278fc98b174db318a894d735ec2878492de9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119463245"
---
# <a name="mfpkey_preferred_framesize-property"></a>Propiedad MFPKEY \_ PREFERRED \_ FRAMESIZE

Especifica el número preferido de muestras por fotograma.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

**VT \_ UI4**

## <a name="remarks"></a>Observaciones

Para establecer un tamaño de marco preferido, establezca las siguientes propiedades.

-   Establezca [**MFPKEY \_ REQUESTING \_ A \_ FRAMESIZE**](mfpkey-requesting-a-framesizeproperty.md) en **VARIANT \_ TRUE.**
-   Establezca **MFPKEY \_ PREFERRED \_ FRAMESIZE en** el número de muestras que desea en cada fotograma.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Cliente<br/> | Windows Vista o Windows 7<br/>                                                   |
| Header<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 
