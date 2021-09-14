---
description: Especifica si el codificador está restringido por un requisito de latencia máxima.
ms.assetid: 8148ae1e-239e-40fa-a88d-810a1d93d8e9
title: MFPKEY_CONSTRAINENCLATENCY propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6f880006bf2aba04196547a79e74f94a7210edd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127257684"
---
# <a name="mfpkey_constrainenclatency-property"></a>Propiedad MFPKEY \_ CONSTRAINENCLATENCY

Especifica si el codificador está restringido por un requisito de latencia máxima.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

**VT \_ BOOL**

## <a name="default-value"></a>Valor predeterminado

**VARIANT \_ FALSE**

## <a name="remarks"></a>Observaciones

Si deja esta propiedad en su valor predeterminado **de VARIANT \_ FALSE**, el codificador enumera un conjunto predeterminado de modos que tienen aproximadamente 2000 milisegundos de latencia del codificador. Si establece esta propiedad en **VARIANT \_ TRUE**, también debe especificar una latencia máxima del codificador estableciendo la [**propiedad MFPKEY \_ MAXENCLATENCYMS.**](mfpkey-maxenclatencymsproperty.md) En ese caso, el codificador crea modos que satisfacen el requisito de latencia y enumera solo esos modos. El codificador garantiza un ejemplo de salida en cuanto el codificador ha recibido una entrada durante un período de tiempo igual a **MFPKEY \_ MAXENCLATENCYMS.**

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

 

 
