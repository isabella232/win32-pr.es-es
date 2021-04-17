---
description: Especifica si la complejidad del algoritmo de codificación de audio está restringida.
ms.assetid: a50b840f-9fe8-4291-b93f-f09c241fe802
title: Propiedad MFPKEY_CONSTRAINENCOMPLEXITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdc6e3d5a7077c72e5933ecbc235092174e263fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696955"
---
# <a name="mfpkey_constrainencomplexity-property"></a>\_Propiedad CONSTRAINENCOMPLEXITY de MFPKEY

Especifica si la complejidad del algoritmo de codificación de audio está restringida.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

**VT \_ bool**

## <a name="default-value"></a>Valor predeterminado

**VARIANTE \_ false**

## <a name="remarks"></a>Observaciones

Si deja esta propiedad en su valor predeterminado de **Variant \_ false**, el codificador de audio utiliza su algoritmo predeterminado. El algoritmo predeterminado depende del tipo de salida y de la versión de Windows que se está ejecutando. En la tabla siguiente se describe el comportamiento predeterminado de las distintas combinaciones.



| Sistema operativo | Comportamiento predeterminado                                                                                                                                                                                    |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Vista    | En todos los tipos de salida, el codificador de audio usa el algoritmo más complejo de forma predeterminada.                                                                                                                 |
| Windows 7        | En el caso de los tipos de salida Standard y Professional, el codificador de audio usa el algoritmo más complejo de forma predeterminada. En el caso de los tipos de salida sin pérdida, el codificador de audio usa el algoritmo menos complejo de forma predeterminada. |



 

Si establece esta propiedad en **Variant \_ true**, también debe especificar un valor de complejidad estableciendo la propiedad [**MFPKEY \_ ENCCOMPLEXITY**](mfpkey-enccomplexityproperty.md) .

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

 

 
