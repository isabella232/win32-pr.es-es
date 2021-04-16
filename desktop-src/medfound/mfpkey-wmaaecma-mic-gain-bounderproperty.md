---
description: Especifica si el DSP de la captura de voz aplica el límite de ganancia de micrófono.
ms.assetid: b9f0bcc7-57ab-4339-bf1d-2b12c8744f01
title: Propiedad MFPKEY_WMAAECMA_MIC_GAIN_BOUNDER (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c1b09f2095f5accb44e4e0edaff2b8c94941d3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705905"
---
# <a name="mfpkey_wmaaecma_mic_gain_bounder-property"></a>\_Propiedad del \_ \_ enlazador de ganancia de WMAAECMA \_ de MFPKEY

Especifica si el DSP de la captura de voz aplica el límite de ganancia de micrófono.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

VT \_ bool

## <a name="default-value"></a>Valor predeterminado

VARIANTE \_ true

## <a name="applies-to"></a>Se aplica a

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Observaciones

El límite de ganancia de micrófono garantiza que el micrófono tenga el nivel de ganancia correcto. Si la ganancia es demasiado alta, la señal capturada podría estar saturada y se recortará. El recorte es un efecto no lineal, lo que hará que se produzca un error en el algoritmo de cancelación del eco acústico (AEC). Si la ganancia es demasiado baja, la relación señal-ruido es baja, lo que también puede provocar un error en el algoritmo AEC o no funcionar correctamente.

Esta propiedad puede tener los valores siguientes.



| Value          | Descripción                       |
|----------------|-----------------------------------|
| VARIANTE \_ true  | Habilitar el límite de ganancia de micrófono.  |
| VARIANTE \_ false | Deshabilite el límite de ganancia de micrófono. |



 

El valor predeterminado de esta propiedad es VARIANT \_ true (Enabled).

El límite de ganancia de micrófono solo se aplica cuando el DSP funciona en modo de origen. En el modo de filtro, la aplicación debe asegurarse de que el micrófono tiene el nivel de ganancia correcto.

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

 

 
