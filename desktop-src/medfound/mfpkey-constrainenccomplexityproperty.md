---
description: Especifica si la complejidad del algoritmo de codificación de audio está restringida.
ms.assetid: a50b840f-9fe8-4291-b93f-f09c241fe802
title: MFPKEY_CONSTRAINENCOMPLEXITY propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdc6e3d5a7077c72e5933ecbc235092174e263fe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127257679"
---
# <a name="mfpkey_constrainencomplexity-property"></a>Propiedad MFPKEY \_ CONSTRAINENCOMPLEXITY

Especifica si la complejidad del algoritmo de codificación de audio está restringida.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de datos

**VT \_ BOOL**

## <a name="default-value"></a>Valor predeterminado

**VARIANT \_ FALSE**

## <a name="remarks"></a>Observaciones

Si deja esta propiedad en su valor predeterminado **de VARIANT \_ FALSE,** el codificador de audio usa su algoritmo predeterminado. El algoritmo predeterminado depende del tipo de salida y de la versión de Windows se está ejecutando. En la tabla siguiente se describe el comportamiento predeterminado de las distintas combinaciones.



| Sistema operativo | Comportamiento predeterminado                                                                                                                                                                                    |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Vista    | Para todos los tipos de salida, el codificador de audio usa el algoritmo más complejo de forma predeterminada.                                                                                                                 |
| Windows 7        | Para los tipos de salida estándar Professional, el codificador de audio usa el algoritmo más complejo de forma predeterminada. Para los tipos de salida sin pérdida, el codificador de audio usa el algoritmo menos complejo de forma predeterminada. |



 

Si establece esta propiedad en **VARIANT \_ TRUE**, también debe especificar un valor de complejidad estableciendo la [**propiedad MFPKEY \_ ENCCOMPLEXITY.**](mfpkey-enccomplexityproperty.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 
