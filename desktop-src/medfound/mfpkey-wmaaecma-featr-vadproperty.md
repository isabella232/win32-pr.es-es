---
description: Especifica el tipo de detección de la actividad de voz que realiza el DSP de la captura de voz.
ms.assetid: 59c8e348-8c08-4cf8-9c72-8d0f4fabc473
title: Propiedad MFPKEY_WMAAECMA_FEATR_VAD (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e41b8ad80d909a0285b266587d02c09c08d794
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705906"
---
# <a name="mfpkey_wmaaecma_featr_vad-property"></a>MFPKEY \_ WMAAECMA \_ feat \_ VAD (propiedad)

Especifica el tipo de detección de la actividad de voz que realiza el DSP de la captura de voz.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

0

## <a name="applies-to"></a>Se aplica a

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Observaciones

El valor de esta propiedad es un miembro de la enumeración de [ \_ \_ modo VAD de AEC](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_vad_mode) . La salida de la detección de actividad de voz es un número del 0 al 3, calculado para cada fotograma de audio. El DSP codifica el resultado en el bit más bajo de las dos primeras muestras de audio en cada fotograma de audio. El significado del valor depende del modo especificado.

En el código siguiente se muestra cómo extraer los resultados de los datos de audio. En este ejemplo, *pOutput* es un puntero al inicio de una trama de audio en los datos de salida.


```
int AecDecodeVAD(short *pOutput)
{
    int iVAD = (*pOutput) & 0x01;
    pOutput++;
    iVAD |= (*pOutput << 1) & 0x02;
    return iVAD;
}
```



El valor predeterminado de esta propiedad es 0 (deshabilitado). Antes de establecer esta propiedad, debe establecer la propiedad de [ \_ modo de \_ característica \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) en Variant \_ true.

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

 

 
