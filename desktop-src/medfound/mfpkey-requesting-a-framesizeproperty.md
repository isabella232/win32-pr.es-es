---
description: Especifica si el codificador debe usar un tamaño de fotograma preferido dado en número de muestras por fotograma.
ms.assetid: c9baeff7-53fb-425f-b07b-4066a705ca54
title: MFPKEY_REQUESTING_A_FRAMESIZE propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3355e84318ba4ad7995ac5ad0f002f4d70767b4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468633"
---
# <a name="mfpkey_requesting_a_framesize-property"></a>MFPKEY \_ SOLICITANDO \_ UNA propiedad \_ FRAMESIZE

Especifica si el codificador debe usar un tamaño de fotograma preferido dado en número de muestras por fotograma.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de datos

**VT \_ BOOL**

## <a name="remarks"></a>Observaciones

Para establecer un tamaño de marco preferido, establezca las siguientes propiedades.

-   Establezca **MFPKEY \_ REQUESTING \_ A \_ FRAMESIZE** en VARIANT \_ TRUE.
-   Establezca [**MFPKEY \_ PREFERRED \_ FRAMESIZE**](mfpkey-preferred-framesizeproperty.md) en el número de muestras que desea en cada fotograma.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Remoto<br/> | Windows Vista o Windows 7<br/>                                                   |
| Encabezado<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 
