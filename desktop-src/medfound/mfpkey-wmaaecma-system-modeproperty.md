---
description: Establece el modo de procesamiento del DSP de la captura de voz.
ms.assetid: 479b3525-5beb-4c6b-b1ad-8fa72c0d0fd0
title: Propiedad MFPKEY_WMAAECMA_SYSTEM_MODE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfca745b83c8a73a2eb4c17c8a2206f90255088c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666875"
---
# <a name="mfpkey_wmaaecma_system_mode-property"></a>\_Propiedad de \_ modo de sistema de MFPKEY WMAAECMA \_

Establece el modo de procesamiento del DSP de la captura de voz.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="applies-to"></a>Se aplica a

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Observaciones

El valor de esta propiedad es un miembro de la enumeración del [ \_ \_ modo del sistema AEC](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_system_mode) .

La propiedad debe ser uno de los valores siguientes.



| Value | Descripción                                 |
|-------|---------------------------------------------|
| 0     | Modo solo de cancelación de eco de audio (AEC)     |
| 2     | Modo solo de procesamiento de matriz de micrófono (mapa) |
| 4     | AEC y modo de mapa                            |
| 5     | Ni AEC ni el modo de asignación                    |



 

Debe establecer esta propiedad antes de usar el DSP de captura de voz. Después de establecer esta propiedad, puede usar el DSP con su configuración predeterminada o establecer propiedades adicionales.

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

 

 
