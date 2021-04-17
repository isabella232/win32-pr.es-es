---
description: Especifica si el códec debe utilizar el filtro de desbloqueo en bucle durante la codificación.
ms.assetid: 395a356a-5f58-46b4-b2ff-47f98106f487
title: Propiedad MFPKEY_LOOPFILTER (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fbb723c4145f9769cc157d5db8eb7893d89b389
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696942"
---
# <a name="mfpkey_loopfilter-property"></a>\_Propiedad LOOPFILTER de MFPKEY

Especifica si el códec debe utilizar el filtro de desbloqueo en bucle durante la codificación.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCLoopFilter

## <a name="data-type"></a>Tipo de datos

VT \_ bool

## <a name="remarks"></a>Observaciones

El filtro en bucle es un método de desbloqueo que se aplica durante la codificación y la descodificación, para reducir los artefactos de bloqueo en el tiempo de codificación ("en el bucle") para que los fotogramas futuros y los fotogramas B no los lleven hacia delante.

El efecto de aplicar el filtro en bucle es que los bordes de los bloques de macros de los fotogramas de vídeo de salida son menos perceptibles. Al mismo tiempo, la imagen puede ser más blanda.

Aunque el filtro en bucle puede dar lugar a un detalle de la imagen reducida en algunos fotogramas, la calidad general del vídeo resultará muy ventajosa. El mayor inconveniente de usar el filtrado en bucle es el costo de rendimiento de la descodificación adicional.

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

 

 




