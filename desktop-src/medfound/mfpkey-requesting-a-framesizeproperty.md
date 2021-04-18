---
description: Especifica si el codificador debe usar un tamaño de marco preferido dado en número de muestras por fotograma.
ms.assetid: c9baeff7-53fb-425f-b07b-4066a705ca54
title: Propiedad MFPKEY_REQUESTING_A_FRAMESIZE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3355e84318ba4ad7995ac5ad0f002f4d70767b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700400"
---
# <a name="mfpkey_requesting_a_framesize-property"></a>MFPKEY \_ solicitar \_ una \_ propiedad de trama

Especifica si el codificador debe usar un tamaño de marco preferido dado en número de muestras por fotograma.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

**VT \_ bool**

## <a name="remarks"></a>Observaciones

Para especificar un tamaño de marco preferido, establezca las siguientes propiedades.

-   Establezca **MFPKEY para \_ solicitar \_ una \_ trama** a Variant \_ true.
-   Establezca [**MFPKEY \_ preferido \_ tramas**](mfpkey-preferred-framesizeproperty.md) en el número de muestras que desee en cada fotograma.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Remoto<br/> | Windows Vista o Windows 7<br/>                                                   |
| Encabezado<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
