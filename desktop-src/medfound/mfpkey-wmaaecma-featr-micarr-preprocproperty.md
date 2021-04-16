---
description: Especifica si el DSP de la captura de voz realiza el preprocesamiento de la matriz de micrófono.
ms.assetid: 0f197165-e6e5-456b-9615-1edc8ada7bb5
title: Propiedad MFPKEY_WMAAECMA_FEATR_MICARR_PREPROC (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f992d8d26ba547eb1b5d1eac470536a963209f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705909"
---
# <a name="mfpkey_wmaaecma_featr_micarr_preproc-property"></a>MFPKEY \_ WMAAECMA \_ feat \_ MICARR \_ Preproc (propiedad)

Especifica si el DSP de la captura de voz realiza el preprocesamiento de la matriz de micrófono.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

VT \_ bool

## <a name="default-value"></a>Valor predeterminado

VARIANTE \_ true

## <a name="applies-to"></a>Se aplica a

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Observaciones

El preprocesamiento puede quitar los tonos estacionales que interfieren con el procesamiento, como un tono con un tono fijo.

Esta propiedad puede tener los valores siguientes.



| Value          | Descripción            |
|----------------|------------------------|
| VARIANTE \_ false | Deshabilitar el preprocesamiento. |
| VARIANTE \_ true  | Habilite el preprocesamiento.  |



 

El valor predeterminado de esta propiedad es VARIANT \_ true (Enabled). Antes de establecer esta propiedad, debe establecer la propiedad de [ \_ modo de \_ característica \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) en Variant \_ true.

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

 

 
