---
description: Especifica si se debe usar un algoritmo que genere vídeo de mayor calidad o un algoritmo más rápido.
ms.assetid: a6760e7e-7c99-4412-bde5-05958fad89a1
title: Propiedad MFPKEY_RESIZE_QUALITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e79ae1cac78b4d836261905afdacaf14fc227fc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715872"
---
# <a name="mfpkey_resize_quality-property"></a>MFPKEY \_ propiedad de calidad de REdimensionamiento \_

Especifica si se debe usar un algoritmo que genere vídeo de mayor calidad o un algoritmo más rápido.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

VT \_ bool

## <a name="applies-to"></a>Se aplica a

-   [Vídeo de tamaño DSP](videoresizer.md)

## <a name="remarks"></a>Observaciones

Utilice uno de los valores siguientes:



| Value     | Descripción          |
|-----------|----------------------|
| VT \_ falso | Algoritmo más rápido     |
| VT \_ true  | Vídeo de mayor calidad |



 

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

 

 
