---
description: Especifica si el codificador debe usar un tamaño de fotograma preferido dado en el número de muestras por fotograma.
ms.assetid: c9baeff7-53fb-425f-b07b-4066a705ca54
title: MFPKEY_REQUESTING_A_FRAMESIZE propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c39d1d9ecdba27e46a1e49949f1607fc60d53501d321e49c4899f9b8928ccf1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555435"
---
# <a name="mfpkey_requesting_a_framesize-property"></a>MFPKEY \_ SOLICITANDO \_ UNA propiedad \_ FRAMESIZE

Especifica si el codificador debe usar un tamaño de fotograma preferido dado en el número de muestras por fotograma.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

**VT \_ BOOL**

## <a name="remarks"></a>Comentarios

Para establecer un tamaño de marco preferido, establezca las siguientes propiedades.

-   Establezca **MFPKEY \_ REQUESTING \_ A \_ FRAMESIZE** en VARIANT \_ TRUE.
-   Establezca [**MFPKEY \_ PREFERRED \_ FRAMESIZE en**](mfpkey-preferred-framesizeproperty.md) el número de muestras que desea en cada fotograma.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Cliente<br/> | Windows Vista o Windows 7<br/>                                                   |
| Header<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 
