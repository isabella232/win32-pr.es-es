---
description: Contiene un puntero a la interfaz IMFSourceOpenMonitor de las aplicaciones.
ms.assetid: 5b94ae87-91fc-49d6-9355-83327cfdb3f3
title: Propiedad MFPKEY_SourceOpenMonitor (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a49826ee16a733993b9052e12d9e6fcd5003410
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156072"
---
# <a name="mfpkey_sourceopenmonitor-property"></a>\_Propiedad SourceOpenMonitor de MFPKEY

Contiene un puntero a la interfaz [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) de la aplicación.



Tipo de datos

Tipo PROPVARIANT (VT)

Miembro de PROPVARIANT

**IUnknown** (puntero)

VT \_ desconocido

**punkVal**



## <a name="remarks"></a>Observaciones

Las aplicaciones pueden pasar esta propiedad al solucionador de origen para obtener notificaciones de eventos del origen de red.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




