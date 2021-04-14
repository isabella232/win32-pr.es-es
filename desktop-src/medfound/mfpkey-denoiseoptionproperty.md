---
description: Especifica si el códec usará el filtro de ruido al codificar.
ms.assetid: 9e099378-bb77-4dca-9171-7fe58e0139de
title: Propiedad MFPKEY_DENOISEOPTION (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7f318e294f69095758fe300fce19043c23cf376
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648310"
---
# <a name="mfpkey_denoiseoption-property"></a>\_Propiedad DENOISEOPTION de MFPKEY

Especifica si el códec usará el filtro de ruido al codificar.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCDenoiseOption

## <a name="data-type"></a>Tipo de datos

VT \_ bool

## <a name="default-value"></a>Valor predeterminado

false

## <a name="remarks"></a>Observaciones

El filtro de ruido puede mejorar la calidad de los orígenes de vídeo ruidosos, como la película que contiene una gran cantidad de grano o vídeo captado en baja luz. Este filtro se puede usar en escenarios de codificación en directo donde el preprocesamiento externo no es una opción.

Este filtro debe estar deshabilitado para los orígenes de vídeo limpios, ya que puede reducir la calidad de la imagen cuando la calidad es buena para empezar.

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

 

 




