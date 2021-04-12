---
description: Especifica cómo el DSP de la captura de voz realiza el procesamiento de la matriz de micrófono.
ms.assetid: 5e04fe50-d764-4497-9999-37279e156204
title: Propiedad MFPKEY_WMAAECMA_FEATR_MICARR_MODE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25bf8ffcae465e8abfddedb3e6d6dded683bb2bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275853"
---
# <a name="mfpkey_wmaaecma_featr_micarr_mode-property"></a>MFPKEY \_ WMAAECMA \_ feat \_ MICARR \_ Mode (propiedad)

Especifica cómo el DSP de la captura de voz realiza el procesamiento de la matriz de micrófono.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

MICARRAY de \_ un solo \_ rayo

## <a name="applies-to"></a>Se aplica a

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Observaciones

El valor de esta propiedad es un miembro de la enumeración de [ \_ \_ modo de matriz de MIC](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mic_array_mode) . El valor predeterminado es MICARRAY de \_ un solo \_ rayo. Antes de establecer esta propiedad, debe establecer la propiedad de [ \_ modo de \_ característica \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) en Variant \_ true.

El DSP usa esta propiedad solo cuando está habilitado el procesamiento de la matriz de micrófono.

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

 

 
