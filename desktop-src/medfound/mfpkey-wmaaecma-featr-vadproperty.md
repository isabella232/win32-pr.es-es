---
description: Especifica el tipo de detección de actividad de voz que realiza el DSP de captura de voz.
ms.assetid: 59c8e348-8c08-4cf8-9c72-8d0f4fabc473
title: MFPKEY_WMAAECMA_FEATR_VAD (Propiedad, Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17e23662a8c6966a64140311f24c9af00dc53454cea19c025451698ddbbbd0dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953515"
---
# <a name="mfpkey_wmaaecma_featr_vad-property"></a>Propiedad \_ VAD MFPKEY WMAAECMA \_ FEATR \_

Especifica el tipo de detección de actividad de voz que realiza el DSP de captura de voz.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

0

## <a name="applies-to"></a>Se aplica a

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Comentarios

El valor de esta propiedad es un miembro de la [enumeración \_ AEC VAD \_ MODE.](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_vad_mode) La salida de la detección de actividad de voz es un número de 0 a 3, calculado para cada fotograma de audio. El DSP codifica el resultado en el bit más bajo de las dos primeras muestras de audio en cada fotograma de audio. El significado del valor depende del modo especificado.

El código siguiente muestra cómo extraer los resultados de los datos de audio. En este ejemplo, *pOutput* es un puntero al inicio de un fotograma de audio en los datos de salida.


```
int AecDecodeVAD(short *pOutput)
{
    int iVAD = (*pOutput) & 0x01;
    pOutput++;
    iVAD |= (*pOutput << 1) & 0x02;
    return iVAD;
}
```



El valor predeterminado de esta propiedad es 0 (deshabilitado). Antes de establecer esta propiedad, debe establecer la propiedad [MFPKEY \_ WMAAECMA \_ FEATURE \_ MODE](mfpkey-wmaaecma-feature-modeproperty.md) en VARIANT \_ TRUE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 
