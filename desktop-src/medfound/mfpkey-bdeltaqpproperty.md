---
description: Especifica el aumento diferencial entre el cuantificador de imágenes del marco delimitador y el cuantificador de imágenes del fotograma B.
ms.assetid: 8ab9401b-6fed-4178-955f-2e0bf950bf60
title: MFPKEY_BDELTAQP (Propiedad, Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7ba1ca7d30e17841badeda0312f77471116a8e2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360448"
---
# <a name="mfpkey_bdeltaqp-property"></a>Propiedad MFPKEY \_ BDELTAQP

Especifica el aumento diferencial entre el cuantificador de imágenes del marco delimitador y el cuantificador de imágenes del fotograma B.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCBDeltaQP

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

0

## <a name="remarks"></a>Observaciones

El cuantificador de imágenes (QP) es una medida de la compresión de un marco. Los valores más altos representan mayores proporciones de compresión. El QP se puede establecer en incrementos de medio punto. Normalmente, un fotograma B se comprime en un QP igual o 0,5 más alto que el QP del marco delimitador. Al especificar una diferencia de QP de fotograma B superior a 0, es posible comprimir fotogramas B con una relación de compresión aún mayor.

El QP delta de fotograma B solo se puede establecer en incrementos de punto entero. Esta propiedad debe establecerse en un valor entero de 0 a 31. El valor recomendado es 1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




