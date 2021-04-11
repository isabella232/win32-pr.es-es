---
description: Ajusta el matiz.
ms.assetid: 8dc3c888-5ab8-40a1-8768-bec58b62eaf0
title: Propiedad MFPKEY_COLOR_HUE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b3ddf0109090bfb56102560dc06a853c970e7ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156097"
---
# <a name="mfpkey_color_hue-property"></a>\_Propiedad matiz de color MFPKEY \_

Ajusta el matiz.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

0

## <a name="applies-to"></a>Se aplica a

-   [DSP de transformación de control de color](colorcontroltransform.md)

## <a name="remarks"></a>Observaciones

El ajuste de matiz se realiza mediante la combinación de los valores CB y CR. (Si CB y CR están trazados en un espacio de 2 dimensiones, el ajuste de matiz se realiza girando alrededor del origen).

Esta propiedad tiene un intervalo de-127 a 127. Cero indica que no hay ningún cambio en el matiz.

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

 

 
