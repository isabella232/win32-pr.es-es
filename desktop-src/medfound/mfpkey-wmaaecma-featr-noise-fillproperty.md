---
description: Especifica si el DSP de la captura de voz realiza el relleno de ruido.
ms.assetid: 8bb64686-8f02-4e0d-a664-aeee1744fc8e
title: Propiedad MFPKEY_WMAAECMA_FEATR_NOISE_FILL (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea0c0af2b47767a7798d9b583ac55ad5112ddf1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705908"
---
# <a name="mfpkey_wmaaecma_featr_noise_fill-property"></a>\_Propiedad de \_ relleno de \_ ruido \_ de MFPKEY WMAAECMA

Especifica si el DSP de la captura de voz realiza el relleno de ruido.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

VT \_ bool

## <a name="default-value"></a>Valor predeterminado

VARIANTE \_ true

## <a name="applies-to"></a>Se aplica a

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Observaciones

El relleno de ruido agrega una pequeña cantidad de ruido a partes de la señal en las que el recorte del centro ha quitado los ecos residuales. Esto da como resultado una mejor experiencia para el usuario que la salida de brechas silenciosas en la señal.

Esta propiedad puede tener los valores siguientes.



| Value          | Descripción            |
|----------------|------------------------|
| VARIANTE \_ true  | Habilitar el relleno de ruido.  |
| VARIANTE \_ false | Deshabilitar el relleno de ruido. |



 

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

 

 
