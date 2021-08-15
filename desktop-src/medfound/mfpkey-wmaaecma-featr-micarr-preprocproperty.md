---
description: Especifica si el DSP de captura de voz realiza el preprocesamiento de la matriz de micrófonos.
ms.assetid: 0f197165-e6e5-456b-9615-1edc8ada7bb5
title: MFPKEY_WMAAECMA_FEATR_MICARR_PREPROC (Propiedad, Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebbba5faeb1a1e70feb1ef6182d3ac2a397a52c4a56f27e767be93f4a3fff773
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117873019"
---
# <a name="mfpkey_wmaaecma_featr_micarr_preproc-property"></a>Propiedad PREPROC MICARR DE MFPKEY \_ WMAAECMA \_ \_ \_ FEATR

Especifica si el DSP de captura de voz realiza el preprocesamiento de la matriz de micrófonos.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de datos

VT \_ BOOL

## <a name="default-value"></a>Valor predeterminado

VARIANT \_ TRUE

## <a name="applies-to"></a>Se aplica a

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Comentarios

El preprocesamiento puede quitar los tonos fijos que interfieren con el procesamiento, como un tono con un tono fijo.

Esta propiedad puede tener los siguientes valores.



| Valor          | Descripción            |
|----------------|------------------------|
| VARIANT \_ FALSE | Deshabilite el preprocesamiento. |
| VARIANT \_ TRUE  | Habilite el preprocesamiento.  |



 

El valor predeterminado de esta propiedad es VARIANT \_ TRUE (habilitado). Antes de establecer esta propiedad, debe establecer la propiedad [MFPKEY \_ WMAAECMA \_ FEATURE \_ MODE](mfpkey-wmaaecma-feature-modeproperty.md) en VARIANT \_ TRUE.

El DSP usa esta propiedad solo cuando el procesamiento de la matriz de micrófonos está habilitado.

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

 

 
