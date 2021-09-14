---
description: Establece el modo de procesamiento para el DSP de captura de voz.
ms.assetid: 479b3525-5beb-4c6b-b1ad-8fa72c0d0fd0
title: MFPKEY_WMAAECMA_SYSTEM_MODE propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfca745b83c8a73a2eb4c17c8a2206f90255088c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127268799"
---
# <a name="mfpkey_wmaaecma_system_mode-property"></a>Propiedad MFPKEY \_ WMAAECMA \_ SYSTEM \_ MODE

Establece el modo de procesamiento para el DSP de captura de voz.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="applies-to"></a>Se aplica a

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Observaciones

El valor de esta propiedad es un miembro de la [enumeración AEC \_ SYSTEM \_ MODE.](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_system_mode)

La propiedad debe ser uno de los siguientes valores.



| Value | Descripción                                 |
|-------|---------------------------------------------|
| 0     | Modo solo de cancelación de eco de audio (AEC)     |
| 2     | Modo solo de procesamiento de matriz de micrófonos (MAP) |
| 4     | Modo AEC y MAP                            |
| 5     | Ni AEC ni modo MAP                    |



 

Debe establecer esta propiedad antes de usar el DSP de captura de voz. Después de establecer esta propiedad, puede usar el DSP con su configuración predeterminada o establecer propiedades adicionales.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[DSP de captura de voz](voicecapturedmo.md)
</dt> </dl>

 

 
