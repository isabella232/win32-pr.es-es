---
description: Especifica si el DSP de captura de voz realiza el control de ganancia automático.
ms.assetid: 85ac8de0-ac36-4b34-a93d-0ac792a677b2
title: MFPKEY_WMAAECMA_FEATR_AGC propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f038b18657363677e0953f8fe973c2e3029130ffc2183a08344e1b0cd6905747
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119343815"
---
# <a name="mfpkey_wmaaecma_featr_agc-property"></a>Propiedad \_ AGC MFPKEY WMAAECMA \_ FEATR \_

Especifica si el DSP de captura de voz realiza el control de ganancia automático.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

VT \_ BOOL

## <a name="default-value"></a>Valor predeterminado

VARIANT \_ FALSE

## <a name="applies-to"></a>Se aplica a

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Comentarios

El control de ganancia automático es un componente de procesamiento de señales digitales (DSP) que ajusta la ganancia para que el nivel de salida de la señal permanezca dentro del mismo intervalo aproximado.

Esta propiedad puede tener los siguientes valores.



| Valor          | Descripción                     |
|----------------|---------------------------------|
| VARIANT \_ FALSE | Deshabilite el control de ganancia automático. |
| VARIANT \_ TRUE  | Habilite el control de ganancia automático.  |



 

El valor predeterminado de esta propiedad es VARIANT \_ FALSE (deshabilitado). Antes de establecer esta propiedad, debe establecer la propiedad [MFPKEY \_ WMAAECMA \_ FEATURE \_ MODE](mfpkey-wmaaecma-feature-modeproperty.md) en VARIANT \_ TRUE.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[DSP de captura de voz](voicecapturedmo.md)
</dt> </dl>

 

 
