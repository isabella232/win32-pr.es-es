---
description: Especifica si se debe usar un algoritmo que genera vídeo de mayor calidad o un algoritmo más rápido.
ms.assetid: a6760e7e-7c99-4412-bde5-05958fad89a1
title: MFPKEY_RESIZE_QUALITY propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e8aeb59935c8fc3462b713967ed2b14a0adfcf731fa1a71fec434b0e07d4309
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973414"
---
# <a name="mfpkey_resize_quality-property"></a>Propiedad RESIZE QUALITY de MFPKEY \_ \_

Especifica si se debe usar un algoritmo que genera vídeo de mayor calidad o un algoritmo más rápido.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de datos

VT \_ BOOL

## <a name="applies-to"></a>Se aplica a

-   [Video Resizer DSP](videoresizer.md)

## <a name="remarks"></a>Comentarios

Utilice uno de los valores siguientes:



| Value     | Descripción          |
|-----------|----------------------|
| VT \_ FALSE | Algoritmo más rápido     |
| VT \_ TRUE  | Vídeo de mayor calidad |



 

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

 

 
