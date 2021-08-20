---
description: Especifica si la complejidad del algoritmo de codificación de audio está restringida.
ms.assetid: a50b840f-9fe8-4291-b93f-f09c241fe802
title: MFPKEY_CONSTRAINENCOMPLEXITY (Propiedad, Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a954173cd49cb70a68b7ffff977b819af8a44139885425015624ac0aa029b31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117873552"
---
# <a name="mfpkey_constrainencomplexity-property"></a>Propiedad MFPKEY \_ CONSTRAINENCOMPLEXITY

Especifica si la complejidad del algoritmo de codificación de audio está restringida.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

**VT \_ BOOL**

## <a name="default-value"></a>Valor predeterminado

**VARIANT \_ FALSE**

## <a name="remarks"></a>Comentarios

Si deja esta propiedad en su valor predeterminado **de VARIANT \_ FALSE**, el codificador de audio usa su algoritmo predeterminado. El algoritmo predeterminado depende del tipo de salida y de la versión de Windows se está ejecutando. En la tabla siguiente se describe el comportamiento predeterminado de las distintas combinaciones.



| Sistema operativo | Comportamiento predeterminado                                                                                                                                                                                    |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Vista    | Para todos los tipos de salida, el codificador de audio usa el algoritmo más complejo de forma predeterminada.                                                                                                                 |
| Windows 7        | Para los tipos de salida Estándar Professional, el codificador de audio usa el algoritmo más complejo de forma predeterminada. Para los tipos de salida sin pérdida, el codificador de audio usa el algoritmo menos complejo de forma predeterminada. |



 

Si establece esta propiedad en **VARIANT \_ TRUE**, también debe especificar un valor de complejidad estableciendo la [**propiedad MFPKEY \_ ENCCOMPLEXITY.**](mfpkey-enccomplexityproperty.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 
