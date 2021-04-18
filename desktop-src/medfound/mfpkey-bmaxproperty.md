---
description: Especifica la ventana de búfer, en milisegundos, de una secuencia de velocidad de bits variable (VBR) restringida en la velocidad de bits máxima (especificada por MFPKEY \_ RMAX).
ms.assetid: ef27b179-4d9b-4ce7-867a-f62b0f9b735d
title: Propiedad MFPKEY_BMAX (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feaca172e97c27e6e8d97902fbe3c969efc933eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697699"
---
# <a name="mfpkey_bmax-property"></a>\_Propiedad Bmax de MFPKEY

Especifica la ventana de búfer, en milisegundos, de una secuencia de velocidad de bits variable (VBR) restringida en la velocidad de bits máxima (especificada por [MFPKEY \_ RMAX](mfpkey-rmaxproperty.md)).

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCBMax

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

No hay valor predeterminado.

## <a name="remarks"></a>Observaciones

Debe establecer este valor para la codificación VBR máxima limitada. Después de comenzar a procesar ejemplos, no debe consultar este valor hasta que termine de codificar la secuencia. El códec interpreta una solicitud de este valor como una señal en la que se encuentra la sesión de codificación. el siguiente ejemplo que se procesa se trata como el principio de una nueva sesión.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




