---
description: Ajusta el matiz.
ms.assetid: 8dc3c888-5ab8-40a1-8768-bec58b62eaf0
title: MFPKEY_COLOR_HUE propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 646d9e3ae0e72e11ae8952d28df9e4e3afc4147eaa7983bd1f0e9c82266ca5c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954445"
---
# <a name="mfpkey_color_hue-property"></a>Propiedad MFPKEY \_ COLOR \_ HUE

Ajusta el matiz.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

0

## <a name="applies-to"></a>Se aplica a

-   [DSP de transformación de control de color](colorcontroltransform.md)

## <a name="remarks"></a>Comentarios

El ajuste de matiz se realiza mediante la combinación de los valores Cb y Cr. (Si Cb y Cr se trazan en un espacio bidimensional, el ajuste de matiz se realiza girando alrededor del origen).

Esta propiedad tiene un intervalo de -127 a 127. Cero indica que no hay ningún cambio en el matiz.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 
