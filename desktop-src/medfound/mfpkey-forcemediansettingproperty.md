---
description: Especifica si el códec debe usar el filtrado de mediana durante la codificación.
ms.assetid: adfca033-4679-4f36-a802-6dd5df7100c8
title: MFPKEY_FORCEMEDIANSETTING propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 722fca2f73f2114cf17664f228e00a12f46e5a399f54b8dc6990940f5c18d979
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953955"
---
# <a name="mfpkey_forcemediansetting-property"></a>Propiedad \_ FORCEMEDIANSETTING de MFPKEY

Especifica si el códec debe usar el filtrado de mediana durante la codificación.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCForceMedianSetting

## <a name="data-type"></a>Tipo de datos

VT \_ BOOL

## <a name="default-value"></a>Valor predeterminado

FALSE

## <a name="remarks"></a>Comentarios

El filtrado de mediana indica al códec que ignore el ruido y el grano al calcular el movimiento entre fotogramas. Esto puede mejorar la calidad del vídeo con mucho ruido, pero puede dar lugar a seguimientos de movimiento (también conocidos como artefactos finales) cuando se aplican al vídeo de origen limpio.

De forma predeterminada, el códec usa lógica interna para determinar si se debe usar el filtrado de mediana. Si establece esta propiedad, esa lógica se invalidará.

> [!Note]  
> Este filtro no es lo mismo que los filtros de desenfoque medios que se encuentran en muchas aplicaciones de edición y procesamiento posterior de vídeo.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




