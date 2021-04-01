---
description: Especifica si el DSP de la captura de voz realiza el recorte del centro.
ms.assetid: 6830cadd-fa8d-41e1-ac11-a6c8f2795941
title: Propiedad MFPKEY_WMAAECMA_FEATR_CENTER_CLIP (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0936ddfe9e34664e55a20efea35a3c06dd6990e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275855"
---
# <a name="mfpkey_wmaaecma_featr_center_clip-property"></a>\_Propiedad de \_ \_ \_ recorte del centro de MFPKEY WMAAECMA

Especifica si el DSP de la captura de voz realiza el recorte del centro.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

VT \_ bool

## <a name="default-value"></a>Valor predeterminado

VARIANTE \_ true

## <a name="applies-to"></a>Se aplica a

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Observaciones

El recorte central es un proceso que quita los residuos de eco pequeños que permanecen después del procesamiento de AEC, en situaciones de una sola conversación (cuando la voz solo se produce en un extremo de la línea).

Esta propiedad puede tener los valores siguientes.



| Value          | Descripción              |
|----------------|--------------------------|
| VARIANTE \_ false | Deshabilitar el recorte del centro. |
| VARIANTE \_ true  | Habilitar el recorte del centro.  |



 

El valor predeterminado de esta propiedad es VARIANT \_ true (Enabled). Antes de establecer esta propiedad, debe establecer la propiedad de [ \_ modo de \_ característica \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) en Variant \_ true.

El DSP usa esta propiedad solo cuando el procesamiento de AEC está habilitado.

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

 

 
