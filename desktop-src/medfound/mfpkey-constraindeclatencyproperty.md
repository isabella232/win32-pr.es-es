---
description: Especifica si el codificador está restringido por un requisito de latencia máxima del descodificador.
ms.assetid: 054e445e-fc71-4d4f-9e9f-f5ff71f0b4ee
title: MFPKEY_CONSTRAINDECLATENCY propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa96418b3709bdf1d9672c8753f1c968279e1c395492843b4b71560512a04342
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117690427"
---
# <a name="mfpkey_constraindeclatency-property"></a>Propiedad MFPKEY \_ CONSTRAINDECLATENCY

Especifica si el codificador está restringido por un requisito de latencia máxima del descodificador.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

**VT \_ BOOL**

## <a name="default-value"></a>Valor predeterminado

**VARIANT \_ FALSE**

## <a name="remarks"></a>Comentarios

Si deja esta propiedad en su valor predeterminado **de VARIANT \_ FALSE,** el codificador enumera un conjunto predeterminado de modos que tienen aproximadamente 1500 milisegundos de latencia de descodificador. Si establece esta propiedad en **VARIANT \_ TRUE**, también debe especificar una latencia máxima del descodificador estableciendo la propiedad [**\_ MFPKEY MAXDECLATENCYMS.**](mfpkey-maxdeclatencymsproperty.md) En ese caso, el codificador crea modos que satisfacen el requisito de latencia y enumera solo esos modos. El codificador garantiza que los requisitos de inscripción previa (tamaño del búfer del descodificador) son menores o iguales que **MFPKEY \_ MAXDECLATENCYMS.**

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

 

 
