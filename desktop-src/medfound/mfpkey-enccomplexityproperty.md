---
description: Especifica la complejidad del algoritmo de codificación.
ms.assetid: 5dd34818-f282-4859-b423-97e9c4944aec
title: MFPKEY_ENCCOMPLEXITY propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d93abe02b50f862fec706f75449e00643228a3917bc22ca9dafa9285d9d46be3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117690130"
---
# <a name="mfpkey_enccomplexity-property"></a>Propiedad MFPKEY \_ ENCCOMPLEXITY

Especifica la complejidad del algoritmo de codificación. El valor es un entero entre 0 y 100, donde 0 especifica el algoritmo menos complejo y 100 especifica el algoritmo más complejo.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de datos

**VT \_ UI4**

## <a name="default-value"></a>Valor predeterminado

100 para Windows Media Audio 10 y Windows Media Audio 10 Professional

100 para la versión Windows Vista de Windows Media Audio 10 Sin pérdida

0 para la versión Windows 7 Windows Media Audio 10 Sin pérdidas

## <a name="remarks"></a>Comentarios

Si la [**propiedad MFPKEY \_ CONSTRAINECOMPLEXITY**](mfpkey-constrainenccomplexityproperty.md) tiene un valor **de VARIANT \_ TRUE**, el codificador ajusta la complejidad de su algoritmo según el valor de esta propiedad.

Para el codificador Windows Media Audio 10 y el codificador Professional Windows Media Audio 10, si el valor de esta propiedad es 100, el codificador coloca una alta demanda en la CPU y genera la salida de mayor calidad. A medida que disminuye el valor de esta propiedad, la demanda en la CPU disminuye, pero también disminuye la calidad de la salida.

Para el Windows media audio 10 sin pérdida, si el valor de esta propiedad es 0, el codificador coloca una baja demanda en la CPU. A medida que aumenta el valor de esta propiedad, aumenta la demanda en la CPU y el tamaño de la salida del codificador disminuye ligeramente. La salida no tiene pérdidas, independientemente del valor de esta propiedad.

Si deja esta propiedad en su valor predeterminado **de VARIANT \_ FALSE,** el codificador usa su algoritmo predeterminado. El algoritmo predeterminado depende del codificador que use y de la versión de Windows ejecuta. En la tabla siguiente se describe el comportamiento predeterminado de las distintas combinaciones.



| Sistema operativo | Comportamiento predeterminado                                                                                                                                                                                                |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Vista    | Los codificadores sin pérdida Windows Media Audio 10, Windows Media Audio 10 Professional y Windows Media Audio 10 usan el algoritmo más complejo de forma predeterminada.                                                    |
| Windows 7        | Los Windows media audio 10 y Windows media audio 1 Professional 0 usan el algoritmo más complejo de forma predeterminada. El Windows media audio 10 sin pérdida usa el algoritmo menos complejo de forma predeterminada. |



 

Si la [**propiedad MFPKEY \_ CONSTRAINECOMPLEXITY**](mfpkey-constrainenccomplexityproperty.md) tiene un valor **de VARIANT \_ FALSE,** el codificador omite esta propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 
