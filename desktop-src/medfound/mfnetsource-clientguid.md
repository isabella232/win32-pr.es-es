---
description: Identificador único por el que el servidor identifica el cliente.
ms.assetid: 490a2b03-aba8-4510-80c5-ca12f4037747
title: Propiedad MFNETSOURCE_CLIENTGUID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc5df46741d4a0b9a6a125396b6f93dd32bfadf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154964"
---
# <a name="mfnetsource_clientguid-property"></a>\_Propiedad CLIENTGUID de MFNETSOURCE

Identificador único por el que el servidor identifica el cliente.



Tipo de datos

Tipo PROPVARIANT (VT)

Miembro de PROPVARIANT

**GUID**

VT \_ CLSID

**puuid**



## <a name="remarks"></a>Observaciones

La constante **MFNETSOURCE \_ CLIENTGUID** define el GUID de la clave de propiedad. El identificador de propiedad (PID) es cero. Para establecer esta propiedad en el origen de red, pase un puntero **IPropertyStore** a la resolución de origen. Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).

Si no se establece o se establece como **GUID \_ NULL**, Microsoft Media Foundation genera un GUID anónimo por sesión que garantiza la privacidad del usuario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                            |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Funciones de red en Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




