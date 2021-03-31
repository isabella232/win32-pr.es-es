---
description: Duración del streaming acelerado para el origen de red, en milisegundos.
ms.assetid: 3f9cd762-f393-4130-ba25-d16da0642093
title: Propiedad MFNETSOURCE_ACCELERATEDSTREAMINGDURATION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57980fbe08d3c6f48cf2638b35e88c455e566e75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908249"
---
# <a name="mfnetsource_acceleratedstreamingduration-property"></a>\_Propiedad ACCELERATEDSTREAMINGDURATION de MFNETSOURCE

Duración del streaming acelerado para el origen de red, en milisegundos.



Tipo de datos

Tipo PROPVARIANT (VT)

Miembro de PROPVARIANT

**DWORD** (almacenado como **Long**)

VT \_ I4

**lVal**



## <a name="remarks"></a>Observaciones

La constante **MFNETSOURCE \_ ACCELERATEDSTREAMINGDURATION** define el GUID para esta clave de propiedad. El identificador de propiedad (PID) es cero.

Las aplicaciones pueden utilizar esta propiedad para configurar el origen de red. Para establecer la propiedad, pase un objeto **IPropertyStore** a la resolución de origen. Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).

Esta propiedad se aplica a la característica de inicio rápido de Windows Media Services, que reproduce el contenido rápidamente sin tener que esperar al almacenamiento en búfer inicial largo. Al usar Inicio rápido, el servidor que ejecuta Windows Media Services enviará algunos datos al principio del contenido con una velocidad mayor que la especificada en la velocidad de bits del contenido.

El valor predeterminado de esta propiedad es 10.000 milisegundos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Características de origen de red](network-source-features.md)
</dt> <dt>

[Funciones de red en Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




