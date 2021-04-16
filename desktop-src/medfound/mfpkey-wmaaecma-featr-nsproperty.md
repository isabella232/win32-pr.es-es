---
description: Especifica si el DSP de captura de voz realiza la supresión de ruido.
ms.assetid: d63e9ac1-9584-4f74-8404-c95d17eb8c2d
title: Propiedad MFPKEY_WMAAECMA_FEATR_NS (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c02218ce621123066e5e61435d93f8539de95e16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705907"
---
# <a name="mfpkey_wmaaecma_featr_ns-property"></a>\_ \_ \_ Propiedad NS del MFPKEY WMAAECMA

Especifica si el DSP de captura de voz realiza la supresión de ruido.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

1

## <a name="applies-to"></a>Se aplica a

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Observaciones

La supresión de ruidos es un componente de procesamiento de señal digital (DSP) que suprime o reduce el ruido de fondo estacionario en la señal de audio. La supresión de ruido se aplica después de la cancelación del eco acústico (AEC) y el procesamiento de la matriz de micrófono.

Esta propiedad puede tener los valores siguientes.



| Value | Descripción                |
|-------|----------------------------|
| 0     | Deshabilite la supresión de ruido. |
| 1     | Habilitar la supresión de ruido.  |



 

El valor predeterminado de esta propiedad es 1 (habilitado). Antes de establecer esta propiedad, debe establecer la propiedad de [ \_ modo de \_ característica \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) en Variant \_ true.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[DSP de captura de voz](voicecapturedmo.md)
</dt> </dl>

 

 
