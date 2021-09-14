---
description: Especifica la ventana de búfer, en milisegundos, de una secuencia restringida de velocidad de bits variable (VBR) a su velocidad de bits media (especificada por MFPKEY \_ BYTEG).
ms.assetid: 7eabceb5-976e-4ebc-9042-9c203044634c
title: MFPKEY_BAVG propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f2cc9984b803fc37c84fee032f95098c52a9b47
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363839"
---
# <a name="mfpkey_bavg-property"></a>Propiedad BAVG MFPKEY \_

Especifica la ventana de búfer, en milisegundos, de una secuencia restringida de velocidad de bits variable (VBR) a su velocidad de bits media (especificada por [MFPKEY \_ BYTEG).](mfpkey-ravgproperty.md)

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCBAvg

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

No hay ningún valor predeterminado, pero el códec calculará un valor adecuado en función de la otra configuración de VBR restringida.

## <a name="remarks"></a>Observaciones

El códec calcula este valor después del paso de codificación final. No debe consultar este valor hasta que se complete la codificación. El códec interpreta una solicitud para este valor como una señal de que la sesión de codificación ha terminado; el ejemplo siguiente que se procesa se trata como el principio de una nueva sesión.

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

 

 




