---
description: Especifica si el DSP de captura de voz realiza el relleno de ruido.
ms.assetid: 8bb64686-8f02-4e0d-a664-aeee1744fc8e
title: MFPKEY_WMAAECMA_FEATR_NOISE_FILL (Propiedad, Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec3f2f6780157da97263bd6e68ac5f38c9448a5633fafe6481b082ed033331dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035123"
---
# <a name="mfpkey_wmaaecma_featr_noise_fill-property"></a>Propiedad MFPKEY \_ WMAAECMA \_ FEATR \_ NOISE \_ FILL

Especifica si el DSP de captura de voz realiza el relleno de ruido.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

VT \_ BOOL

## <a name="default-value"></a>Valor predeterminado

VARIANT \_ TRUE

## <a name="applies-to"></a>Se aplica a

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Comentarios

El relleno de ruido agrega una pequeña cantidad de ruido a partes de la señal donde el recorte central ha quitado los ecos residuales. Esto da como resultado una mejor experiencia para el usuario que dejar espacios silenciosos en la señal.

Esta propiedad puede tener los siguientes valores.



| Value          | Descripción            |
|----------------|------------------------|
| VARIANT \_ TRUE  | Habilite el relleno de ruido.  |
| VARIANT \_ FALSE | Deshabilite el relleno de ruido. |



 

El valor predeterminado de esta propiedad es VARIANT \_ TRUE (habilitado). Antes de establecer esta propiedad, debe establecer la propiedad [MFPKEY \_ WMAAECMA \_ FEATURE \_ MODE](mfpkey-wmaaecma-feature-modeproperty.md) en VARIANT \_ TRUE.

El DSP usa esta propiedad solo cuando el procesamiento de AEC está habilitado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[DSP de captura de voz](voicecapturedmo.md)
</dt> </dl>

 

 
