---
description: Especifica si el códec debe usar el filtrado de mediana durante la codificación.
ms.assetid: adfca033-4679-4f36-a802-6dd5df7100c8
title: MFPKEY_FORCEMEDIANSETTING propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38d0aa154798e2ed42a7373a6e85a4b46f8eeb7b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127263228"
---
# <a name="mfpkey_forcemediansetting-property"></a>Propiedad \_ FORCEMEDIANSETTING de MFPKEY

Especifica si el códec debe usar el filtrado de mediana durante la codificación.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCForceMedianSetting

## <a name="data-type"></a>Tipo de datos

VT \_ BOOL

## <a name="default-value"></a>Valor predeterminado

false

## <a name="remarks"></a>Observaciones

El filtrado de mediana indica al códec que ignore el ruido y el grano al calcular el movimiento entre fotogramas. Esto puede mejorar la calidad del vídeo con mucho ruido, pero puede dar lugar a seguimientos de movimiento (también conocidos como artefactos finales) cuando se aplican al vídeo de origen limpio.

De forma predeterminada, el códec usa lógica interna para determinar si se debe usar el filtrado de mediana. Si establece esta propiedad, esa lógica se invalidará.

> [!Note]  
> Este filtro no es lo mismo que los filtros de desenfoque medios que se encuentran en muchas aplicaciones de edición y procesamiento posterior de vídeo.

 

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

 

 




