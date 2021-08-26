---
description: Especifica si el DSP de captura de voz aplica el límite de ganancia de micrófono.
ms.assetid: b9f0bcc7-57ab-4339-bf1d-2b12c8744f01
title: MFPKEY_WMAAECMA_MIC_GAIN_BOUNDER propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7d00e906ec953e2fd00d9c288336c322c2d0dc07ea1c2d74a014ab78ae21acd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113155"
---
# <a name="mfpkey_wmaaecma_mic_gain_bounder-property"></a>MFPKEY \_ WMAAECMA \_ MIC \_ GAIN \_ BOUNDER Property

Especifica si el DSP de captura de voz aplica el límite de ganancia de micrófono.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

VT \_ BOOL

## <a name="default-value"></a>Valor predeterminado

VARIANT \_ TRUE

## <a name="applies-to"></a>Se aplica a

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Comentarios

El límite de la ganancia del micrófono garantiza que el micrófono tenga el nivel de ganancia correcto. Si la ganancia es demasiado alta, la señal capturada podría estar saturada y se recortará. El recorte es un efecto no lineal, lo que provocará un error en el algoritmo de cancelación de eco acústico (AEC). Si la ganancia es demasiado baja, la relación señal-ruido es baja, lo que también puede hacer que el algoritmo AEC no se realice correctamente o no.

Esta propiedad puede tener los siguientes valores.



| Value          | Descripción                       |
|----------------|-----------------------------------|
| VARIANT \_ TRUE  | Habilite el límite de ganancia de micrófono.  |
| VARIANT \_ FALSE | Deshabilite el límite de ganancia de micrófono. |



 

El valor predeterminado de esta propiedad es VARIANT \_ TRUE (habilitado).

El límite de la ganancia de micrófono solo se aplica cuando el DSP funciona en modo de origen. En el modo de filtro, la aplicación debe asegurarse de que el micrófono tiene el nivel de ganancia correcto.

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

 

 
