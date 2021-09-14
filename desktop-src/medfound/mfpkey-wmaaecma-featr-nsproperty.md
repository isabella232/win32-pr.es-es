---
description: Especifica si el DSP de captura de voz realiza la supresión de ruido.
ms.assetid: d63e9ac1-9584-4f74-8404-c95d17eb8c2d
title: MFPKEY_WMAAECMA_FEATR_NS propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c02218ce621123066e5e61435d93f8539de95e16
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360689"
---
# <a name="mfpkey_wmaaecma_featr_ns-property"></a>Propiedad \_ NS MFPKEY WMAAECMA \_ FEATR \_

Especifica si el DSP de captura de voz realiza la supresión de ruido.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

1

## <a name="applies-to"></a>Se aplica a

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Observaciones

La supresión de ruido es un componente de procesamiento de señal digital (DSP) que suprime o reduce el ruido de fondo fijo en la señal de audio. La supresión de ruido se aplica después de la cancelación de eco acústico (AEC) y el procesamiento de la matriz de micrófonos.

Esta propiedad puede tener los siguientes valores.



| Value | Descripción                |
|-------|----------------------------|
| 0     | Deshabilite la supresión de ruido. |
| 1     | Habilite la supresión de ruido.  |



 

El valor predeterminado de esta propiedad es 1 (habilitado). Antes de establecer esta propiedad, debe establecer la propiedad [MFPKEY \_ WMAAECMA \_ FEATURE \_ MODE](mfpkey-wmaaecma-feature-modeproperty.md) en VARIANT \_ TRUE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[DSP de captura de voz](voicecapturedmo.md)
</dt> </dl>

 

 
