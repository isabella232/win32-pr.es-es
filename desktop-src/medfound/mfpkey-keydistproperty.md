---
description: Especifica el tiempo máximo, en milisegundos, entre los fotogramas clave de la salida del códec.
ms.assetid: 2a52e6a5-10a0-46dd-aa31-cb55094903b5
title: Propiedad MFPKEY_KEYDIST (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d55925811db71f24cf360113aa6d03a325bcdc11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908770"
---
# <a name="mfpkey_keydist-property"></a>\_Propiedad KEYDIST de MFPKEY

Especifica el tiempo máximo, en milisegundos, entre los fotogramas clave de la salida del códec.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCKeyframeDistance

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

El valor predeterminado depende de la versión de Windows que se esté ejecutando, tal como se muestra en la tabla siguiente.



| Sistema operativo | Valor predeterminado |
|------------------|---------------|
| Windows XP       | 8000          |
| Windows Vista    | 8000          |
| Windows 7        | 2000          |



 

## <a name="remarks"></a>Observaciones

La lógica interna del códec determina la ubicación real de cada fotograma clave. La distancia entre dos fotogramas clave puede ser menor que el valor de esta propiedad; sin embargo, nunca será mayor.

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

 

 




