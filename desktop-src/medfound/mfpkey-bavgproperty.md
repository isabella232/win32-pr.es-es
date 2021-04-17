---
description: Especifica la ventana de búfer, en milisegundos, de una secuencia de velocidad de bits variable (VBR) restringida con la velocidad de bits media (especificada por MFPKEY \_ RAVG).
ms.assetid: 7eabceb5-976e-4ebc-9042-9c203044634c
title: Propiedad MFPKEY_BAVG (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f2cc9984b803fc37c84fee032f95098c52a9b47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105697144"
---
# <a name="mfpkey_bavg-property"></a>\_Propiedad BAVG de MFPKEY

Especifica la ventana de búfer, en milisegundos, de una secuencia de velocidad de bits variable (VBR) restringida con la velocidad de bits media (especificada por [MFPKEY \_ RAVG](mfpkey-ravgproperty.md)).

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCBAvg

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

No hay ningún valor predeterminado, pero el códec calculará un valor adecuado en función de la configuración de VBR limitada.

## <a name="remarks"></a>Observaciones

El códec calcula este valor después de la fase de codificación final. No debe consultar este valor hasta que se complete la codificación. El códec interpreta una solicitud de este valor como una señal en la que se encuentra la sesión de codificación. el siguiente ejemplo que se procesa se trata como el principio de una nueva sesión.

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

 

 




