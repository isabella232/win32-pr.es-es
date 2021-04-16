---
description: Especifica si el DSP de la captura de voz realiza el control automático de ganancia.
ms.assetid: 85ac8de0-ac36-4b34-a93d-0ac792a677b2
title: Propiedad MFPKEY_WMAAECMA_FEATR_AGC (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f42c7abd854b8fe18b5cfd4fe23ededb28faa6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696699"
---
# <a name="mfpkey_wmaaecma_featr_agc-property"></a>\_Propiedad AGC del MFPKEY WMAAECMA \_ feat \_

Especifica si el DSP de la captura de voz realiza el control automático de ganancia.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

VT \_ bool

## <a name="default-value"></a>Valor predeterminado

VARIANTE \_ false

## <a name="applies-to"></a>Se aplica a

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Observaciones

El control de ganancia automática es un componente de procesamiento de señal digital (DSP) que ajusta la ganancia para que el nivel de salida de la señal permanezca dentro del mismo intervalo aproximado.

Esta propiedad puede tener los valores siguientes.



| Value          | Descripción                     |
|----------------|---------------------------------|
| VARIANTE \_ false | Deshabilitar el control de ganancia automática. |
| VARIANTE \_ true  | Habilitar el control de ganancia automática.  |



 

El valor predeterminado de esta propiedad es VARIANT \_ false (disabled). Antes de establecer esta propiedad, debe establecer la propiedad de [ \_ modo de \_ característica \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) en Variant \_ true.

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

 

 
