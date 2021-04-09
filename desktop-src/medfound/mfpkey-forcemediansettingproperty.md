---
description: Especifica si el códec debe utilizar el filtrado medio durante la codificación.
ms.assetid: adfca033-4679-4f36-a802-6dd5df7100c8
title: Propiedad MFPKEY_FORCEMEDIANSETTING (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38d0aa154798e2ed42a7373a6e85a4b46f8eeb7b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "103914173"
---
# <a name="mfpkey_forcemediansetting-property"></a>\_Propiedad FORCEMEDIANSETTING de MFPKEY

Especifica si el códec debe utilizar el filtrado medio durante la codificación.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCForceMedianSetting

## <a name="data-type"></a>Tipo de datos

VT \_ bool

## <a name="default-value"></a>Valor predeterminado

false

## <a name="remarks"></a>Observaciones

El filtrado medio indica al códec que omita el ruido y el grano al calcular el movimiento entre los fotogramas. Esto puede mejorar la calidad del vídeo muy ruidoso, pero puede dar lugar a los seguimientos de movimiento (también conocidos como artefactos finales) cuando se aplican al vídeo de origen limpio.

De forma predeterminada, el códec usa la lógica interna para determinar si se debe usar el filtrado de mediana. Si establece esta propiedad, se invalidará esa lógica.

> [!Note]  
> Este filtro no es el mismo que el de los filtros de desenfoque medio que se encuentran en muchas aplicaciones de edición y postprocesamiento de vídeo.

 

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

 

 




