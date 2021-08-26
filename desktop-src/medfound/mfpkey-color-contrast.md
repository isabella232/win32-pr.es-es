---
description: Ajusta el contraste.
ms.assetid: 32ae514a-eeba-4205-b6e6-70fc01b93a95
title: MFPKEY_COLOR_CONTRAST (Propiedad, Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94c1c794b10580cbb323d19f52eed7d3bfb5fc6cf96e316d708491025776cfff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954475"
---
# <a name="mfpkey_color_contrast-property"></a>Propiedad MFPKEY \_ COLOR \_ CONTRAST

Ajusta el contraste.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

0

## <a name="applies-to"></a>Se aplica a

-   [DSP de transformación de control de color](colorcontroltransform.md)

## <a name="remarks"></a>Comentarios

El ajuste de contraste se realiza multiplicando los valores de YCbCr por un factor de escalado.

Esta propiedad tiene un intervalo de -127 a 127. Cero indica que no hay ningún cambio en el contraste.

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

 

 
