---
description: Especifica el incremento diferencial entre el cuantificador de imágenes del marco de anclaje y el cuantificador de imágenes del fotograma B.
ms.assetid: 8ab9401b-6fed-4178-955f-2e0bf950bf60
title: Propiedad MFPKEY_BDELTAQP (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7ba1ca7d30e17841badeda0312f77471116a8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105697142"
---
# <a name="mfpkey_bdeltaqp-property"></a>\_Propiedad BDELTAQP de MFPKEY

Especifica el incremento diferencial entre el cuantificador de imágenes del marco de anclaje y el cuantificador de imágenes del fotograma B.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCBDeltaQP

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

0

## <a name="remarks"></a>Observaciones

El cuantificador de imágenes (QP) es una medida de la compresión de un fotograma. Los valores más altos representan mayores proporciones de compresión. La QP se puede establecer en incrementos de punto medio. Un fotograma B normalmente se comprime en una QP igual que o 0,5 más arriba que el valor de QP del fotograma del delimitador. Al especificar una diferencia de QP de fotogramas B superior a 0, es posible comprimir los fotogramas B con una relación de compresión incluso mayor.

La diferencia de fotogramas Delta QP solo se puede establecer en incrementos de punto entero. Esta propiedad debe establecerse en un valor entero comprendido entre 0 y 31. El valor recomendado es 1.

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

 

 




