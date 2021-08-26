---
description: Especifica si el códec usará el filtro de ruido al codificar.
ms.assetid: 9e099378-bb77-4dca-9171-7fe58e0139de
title: MFPKEY_DENOISEOPTION propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0483edbda1c2eb3ec929fb662fe4544cb09e7d43dfd1b30421d14eb06d2a365b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954075"
---
# <a name="mfpkey_denoiseoption-property"></a>Propiedad MFPKEY \_ DENOISEOPTION

Especifica si el códec usará el filtro de ruido al codificar.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCDenoiseOption

## <a name="data-type"></a>Tipo de datos

VT \_ BOOL

## <a name="default-value"></a>Valor predeterminado

FALSE

## <a name="remarks"></a>Comentarios

El filtro de ruido puede mejorar la calidad de los orígenes de vídeo ruidosos, como la película que contiene una gran cantidad de grano o una toma de vídeo con poca luz. Este filtro se puede usar en escenarios de codificación en vivo donde el preprocesamiento externo no es una opción.

Este filtro debe deshabilitarse para orígenes de vídeo limpios, ya que puede reducir la calidad de la imagen cuando la calidad es buena para empezar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




