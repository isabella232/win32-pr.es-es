---
description: Duración del streaming acelerado para el origen de red, en milisegundos.
ms.assetid: 3f9cd762-f393-4130-ba25-d16da0642093
title: MFNETSOURCE_ACCELERATEDSTREAMINGDURATION propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ec37cfd7dd0aa8d60c3e192ae0f445f8a121e9e3cd3f85d46e8c18b21fc2b06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118243869"
---
# <a name="mfnetsource_acceleratedstreamingduration-property"></a>MFNETSOURCE \_ ACCELERATEDSTREAMINGDURATION, propiedad

Duración del streaming acelerado para el origen de red, en milisegundos.



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

**DWORD** (almacenado como **LONG)**

VT \_ I4

**lVal**



## <a name="remarks"></a>Comentarios

La constante **MFNETSOURCE \_ ACCELERATEDSTREAMINGDURATION** define el GUID de esta clave de propiedad. El identificador de propiedad (PID) es cero.

Las aplicaciones pueden usar esta propiedad para configurar el origen de red. Para establecer la propiedad , pase un **objeto IPropertyStore** al solucionador de origen. Para obtener más información, vea [Configuring a Media Source](configuring-a-media-source.md).

Esta propiedad se aplica a la característica Inicio rápido de Servicios de Windows Media, que reproduce el contenido rápidamente sin esperar a un almacenamiento en búfer inicial largo. Al usar Inicio rápido, el servidor que ejecuta Servicios de Windows Media enviará algunos datos al principio del contenido a una velocidad más rápida que la especificada por la velocidad de bits del contenido.

El valor predeterminado de esta propiedad es 10 000 milisegundos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[Características de origen de red](network-source-features.md)
</dt> <dt>

[Redes en Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




