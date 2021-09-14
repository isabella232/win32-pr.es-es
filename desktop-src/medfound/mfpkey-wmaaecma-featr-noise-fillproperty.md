---
description: Especifica si el DSP de captura de voz realiza el relleno de ruido.
ms.assetid: 8bb64686-8f02-4e0d-a664-aeee1744fc8e
title: MFPKEY_WMAAECMA_FEATR_NOISE_FILL propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea0c0af2b47767a7798d9b583ac55ad5112ddf1f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363790"
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

## <a name="remarks"></a>Observaciones

El relleno de ruido agrega una pequeña cantidad de ruido a partes de la señal donde el recorte central ha quitado los ecos residuales. Esto da como resultado una mejor experiencia para el usuario que dejar espacios silenciosos en la señal.

Esta propiedad puede tener los siguientes valores.



| Value          | Descripción            |
|----------------|------------------------|
| VARIANT \_ TRUE  | Habilite el relleno de ruido.  |
| VARIANT \_ FALSE | Deshabilite el relleno de ruido. |



 

El valor predeterminado de esta propiedad es VARIANT \_ TRUE (habilitado). Antes de establecer esta propiedad, debe establecer la propiedad [MFPKEY \_ WMAAECMA \_ FEATURE \_ MODE](mfpkey-wmaaecma-feature-modeproperty.md) en VARIANT \_ TRUE.

El DSP usa esta propiedad solo cuando el procesamiento de AEC está habilitado.

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

 

 
