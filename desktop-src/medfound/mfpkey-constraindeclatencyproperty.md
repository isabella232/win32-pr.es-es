---
description: Especifica si el codificador está restringido por un requisito máximo de latencia del descodificador.
ms.assetid: 054e445e-fc71-4d4f-9e9f-f5ff71f0b4ee
title: Propiedad MFPKEY_CONSTRAINDECLATENCY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 343bcc9bd365b9f1321b200baa203fc27784594c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696953"
---
# <a name="mfpkey_constraindeclatency-property"></a>\_Propiedad CONSTRAINDECLATENCY de MFPKEY

Especifica si el codificador está restringido por un requisito máximo de latencia del descodificador.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

**VT \_ bool**

## <a name="default-value"></a>Valor predeterminado

**VARIANTE \_ false**

## <a name="remarks"></a>Observaciones

Si deja esta propiedad en su valor predeterminado de **Variant \_ false**, el codificador enumera un conjunto predeterminado de modos que tienen aproximadamente 1500 milisegundos de latencia del descodificador. Si establece esta propiedad en **Variant \_ true**, también debe especificar una latencia máxima del descodificador estableciendo la propiedad [**MFPKEY \_ MAXDECLATENCYMS**](mfpkey-maxdeclatencymsproperty.md) . En ese caso, el codificador crea modos que satisfacen el requisito de latencia y enumera solo esos modos. El codificador garantiza que los requisitos de predesbordamiento (tamaño del búfer del descodificador) son menores o iguales que **MFPKEY \_ MAXDECLATENCYMS**.

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

 

 
