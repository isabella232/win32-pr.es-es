---
description: Especifica la complejidad del algoritmo de codificación.
ms.assetid: 5dd34818-f282-4859-b423-97e9c4944aec
title: Propiedad MFPKEY_ENCCOMPLEXITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51f50e7966a05affe8ae75869b670cf75f088b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908782"
---
# <a name="mfpkey_enccomplexity-property"></a>\_Propiedad ENCCOMPLEXITY de MFPKEY

Especifica la complejidad del algoritmo de codificación. El valor es un entero comprendido entre 0 y 100, donde 0 especifica el algoritmo menos complejo y 100 especifica el algoritmo más complejo.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

**VT \_ UI4**

## <a name="default-value"></a>Valor predeterminado

100 para Windows Media Audio 10 y Windows Media Audio 10 Professional

100 para la versión de Windows Vista de Windows Media Audio 10 Lossless

0 para Windows 7 Release Windows Media Audio 10 Lossless

## <a name="remarks"></a>Observaciones

Si la [**propiedad \_ CONSTRAINECOMPLEXITY de MFPKEY**](mfpkey-constrainenccomplexityproperty.md) tiene un valor de **Variant \_ true**, el codificador ajusta la complejidad de su algoritmo según el valor de esta propiedad.

En el caso del codificador Windows Media Audio 10 y el codificador Windows Media Audio 10 Professional, si el valor de esta propiedad es 100, el codificador coloca una gran demanda en la CPU y genera la salida de mayor calidad. A medida que se reduce el valor de esta propiedad, se reduce la demanda de la CPU, pero también se reduce la calidad de la salida.

En el caso del codificador de Windows Media Audio 10 sin pérdida de código, si el valor de esta propiedad es 0, el codificador pone una demanda baja en la CPU. A medida que aumenta el valor de esta propiedad, aumenta la demanda de la CPU y el tamaño de la salida del codificador se reduce ligeramente. La salida es sin pérdida, independientemente del valor de esta propiedad.

Si deja esta propiedad en su valor predeterminado de **Variant \_ false**, el codificador utiliza su algoritmo predeterminado. El algoritmo predeterminado depende del codificador que esté usando y de la versión de Windows que se esté ejecutando. En la tabla siguiente se describe el comportamiento predeterminado de las distintas combinaciones.



| Sistema operativo | Comportamiento predeterminado                                                                                                                                                                                                |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Vista    | Los codificadores Windows Media Audio 10, Windows Media Audio 10 Professional y Windows Media Audio 10 sin pérdida utilizan el algoritmo más complejo de forma predeterminada.                                                    |
| Windows 7        | Los codificadores Windows Media Audio 10 y Windows Media Audio 10 Professional usan el algoritmo más complejo de forma predeterminada. De forma predeterminada, el codificador sin pérdida de Windows Media Audio 10 usa el algoritmo menos complejo. |



 

Si la [**propiedad \_ CONSTRAINECOMPLEXITY de MFPKEY**](mfpkey-constrainenccomplexityproperty.md) tiene un valor de **Variant \_ false**, el codificador omite esta propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
