---
description: Especifica si el códec debe usar el filtro de desbloqueo en bucle durante la codificación.
ms.assetid: 395a356a-5f58-46b4-b2ff-47f98106f487
title: MFPKEY_LOOPFILTER propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fbb723c4145f9769cc157d5db8eb7893d89b389
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127268983"
---
# <a name="mfpkey_loopfilter-property"></a>Propiedad MFPKEY \_ LOOPFILTER

Especifica si el códec debe usar el filtro de desbloqueo en bucle durante la codificación.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCLoopFilter

## <a name="data-type"></a>Tipo de datos

VT \_ BOOL

## <a name="remarks"></a>Observaciones

El filtro en bucle es un método de desbloqueo que se aplica durante la codificación y la codificación, para reducir los artefactos de bloqueo en tiempo de codificación ("en el bucle") para que los futuros fotogramas P y B no los lleven hacia delante.

El efecto de aplicar el filtro en bucle es que los bordes de los bloques de macros en los fotogramas de vídeo de salida son menos perceptibles. Al mismo tiempo, la imagen puede volverse más suave en apariencia.

Aunque el filtro en bucle puede dar lugar a un menor detalle de la imagen en algunos fotogramas, la calidad general del vídeo se beneficiará notablemente. La mayor desventaja de usar el filtrado en bucle es el costo de rendimiento de la decodación adicional.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




