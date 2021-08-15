---
description: Establece el modo de procesamiento para el DSP de captura de voz.
ms.assetid: 479b3525-5beb-4c6b-b1ad-8fa72c0d0fd0
title: MFPKEY_WMAAECMA_SYSTEM_MODE propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 722b3e502b783f98ef4871cfc6dd184389dfce7f7f942bde1827468e96f5fa7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973274"
---
# <a name="mfpkey_wmaaecma_system_mode-property"></a>Propiedad MFPKEY \_ WMAAECMA \_ SYSTEM \_ MODE

Establece el modo de procesamiento para el DSP de captura de voz.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="applies-to"></a>Se aplica a

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Comentarios

El valor de esta propiedad es un miembro de la [enumeración AEC \_ SYSTEM \_ MODE.](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_system_mode)

La propiedad debe ser uno de los siguientes valores.



| Valor | Descripción                                 |
|-------|---------------------------------------------|
| 0     | Modo solo de cancelación de eco de audio (AEC)     |
| 2     | Modo de procesamiento de matriz de micrófonos (MAP) |
| 4     | Modo AEC y MAP                            |
| 5     | Ni el modo AEC ni MAP                    |



 

Debe establecer esta propiedad antes de usar el DSP de captura de voz. Después de establecer esta propiedad, puede usar el DSP con su configuración predeterminada o establecer propiedades adicionales.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[DSP de captura de voz](voicecapturedmo.md)
</dt> </dl>

 

 
