---
description: Especifica si el DSP de captura de voz realiza el recorte central.
ms.assetid: 6830cadd-fa8d-41e1-ac11-a6c8f2795941
title: MFPKEY_WMAAECMA_FEATR_CENTER_CLIP propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: daf1e4b5760642b72f50c645306739592fe866eaeb8c424d08e2717d9835f839
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953545"
---
# <a name="mfpkey_wmaaecma_featr_center_clip-property"></a>Propiedad CLIP MFPKEY \_ WMAAECMA \_ FEATR \_ CENTER \_

Especifica si el DSP de captura de voz realiza el recorte central.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de datos

VT \_ BOOL

## <a name="default-value"></a>Valor predeterminado

VARIANT \_ TRUE

## <a name="applies-to"></a>Se aplica a

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Comentarios

El recorte del centro es un proceso que quita los valores residuales de eco pequeños que permanecen después del procesamiento de AEC, en situaciones de una sola conversación (cuando la voz se produce solo en un extremo de la línea).

Esta propiedad puede tener los siguientes valores.



| Value          | Descripción              |
|----------------|--------------------------|
| VARIANT \_ FALSE | Deshabilite el recorte del centro. |
| VARIANT \_ TRUE  | Habilite el recorte del centro.  |



 

El valor predeterminado de esta propiedad es VARIANT \_ TRUE (habilitado). Antes de establecer esta propiedad, debe establecer la propiedad [MFPKEY \_ WMAAECMA \_ FEATURE \_ MODE](mfpkey-wmaaecma-feature-modeproperty.md) en VARIANT \_ TRUE.

El DSP usa esta propiedad solo cuando el procesamiento de AEC está habilitado.

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

 

 
