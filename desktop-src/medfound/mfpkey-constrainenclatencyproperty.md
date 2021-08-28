---
description: Especifica si el codificador está restringido por un requisito de latencia máxima.
ms.assetid: 8148ae1e-239e-40fa-a88d-810a1d93d8e9
title: MFPKEY_CONSTRAINENCLATENCY propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8172b92b0b4d39602f0535b8bf1ef4456a896972e56c6da10f6585e5221fa7e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113425"
---
# <a name="mfpkey_constrainenclatency-property"></a>Propiedad MFPKEY \_ CONSTRAINENCLATENCY

Especifica si el codificador está restringido por un requisito de latencia máxima.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de datos

**VT \_ BOOL**

## <a name="default-value"></a>Valor predeterminado

**VARIANT \_ FALSE**

## <a name="remarks"></a>Comentarios

Si deja esta propiedad en su valor predeterminado **de VARIANT \_ FALSE,** el codificador enumera un conjunto predeterminado de modos que tienen aproximadamente 2000 milisegundos de latencia del codificador. Si establece esta propiedad en **VARIANT \_ TRUE**, también debe especificar una latencia máxima del codificador estableciendo la propiedad [**\_ MFPKEY MAXENCLATENCYMS.**](mfpkey-maxenclatencymsproperty.md) En ese caso, el codificador crea modos que satisfacen el requisito de latencia y enumera solo esos modos. El codificador garantiza un ejemplo de salida en cuanto el codificador ha recibido una entrada durante un período de tiempo igual a **MFPKEY \_ MAXENCLATENCYMS**.

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

 

 
