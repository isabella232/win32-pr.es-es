---
description: Especifica cómo el DSP de captura de voz realiza el procesamiento de la matriz de micrófonos.
ms.assetid: 5e04fe50-d764-4497-9999-37279e156204
title: MFPKEY_WMAAECMA_FEATR_MICARR_MODE propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb948ff15655ccbdc0bf647194b2f6d3d7d1a40c36da32f6d65479152c76c3e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953525"
---
# <a name="mfpkey_wmaaecma_featr_micarr_mode-property"></a>Propiedad MFPKEY \_ WMAAECMA \_ FEATR \_ MICARR \_ MODE

Especifica cómo el DSP de captura de voz realiza el procesamiento de la matriz de micrófonos.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

MICARRAY \_ SINGLE \_ BEAM

## <a name="applies-to"></a>Se aplica a

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Comentarios

El valor de esta propiedad es un miembro de la [enumeración MIC \_ ARRAY \_ MODE.](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mic_array_mode) El valor predeterminado es MICARRAY \_ SINGLE \_ BEAM. Antes de establecer esta propiedad, debe establecer la propiedad [MFPKEY \_ WMAAECMA \_ FEATURE \_ MODE](mfpkey-wmaaecma-feature-modeproperty.md) en VARIANT \_ TRUE.

El DSP usa esta propiedad solo cuando el procesamiento de la matriz de micrófonos está habilitado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

 
