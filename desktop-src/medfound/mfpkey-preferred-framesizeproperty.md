---
description: Especifica el número preferido de muestras por fotograma.
ms.assetid: ad629dbd-49d8-43d0-95a8-03f2043e397e
title: Propiedad MFPKEY_PREFERRED_FRAMESIZE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fe04ad37c6cd684e3179cbd16328346fd6f11dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700289"
---
# <a name="mfpkey_preferred_framesize-property"></a>MFPKEY \_ propiedad de trama preferida \_

Especifica el número preferido de muestras por fotograma.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

**VT \_ UI4**

## <a name="remarks"></a>Observaciones

Para especificar un tamaño de marco preferido, establezca las siguientes propiedades.

-   Establezca [**MFPKEY para \_ solicitar \_ una \_ trama**](mfpkey-requesting-a-framesizeproperty.md) a **Variant \_ true**.
-   Establezca **MFPKEY \_ preferido \_ tramas** en el número de muestras que desee en cada fotograma.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Remoto<br/> | Windows Vista o Windows 7<br/>                                                   |
| Encabezado<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
