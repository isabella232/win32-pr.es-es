---
description: Identificador único por el que el servidor identifica el cliente.
ms.assetid: 490a2b03-aba8-4510-80c5-ca12f4037747
title: MFNETSOURCE_CLIENTGUID propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc5df46741d4a0b9a6a125396b6f93dd32bfadf6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127257735"
---
# <a name="mfnetsource_clientguid-property"></a>Propiedad \_ MFNETSOURCE CLIENTGUID

Identificador único por el que el servidor identifica el cliente.



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

**GUID**

VT \_ CLSID

**puuid**



## <a name="remarks"></a>Observaciones

La **constante MFNETSOURCE \_ CLIENTGUID** define el GUID de la clave de propiedad. El identificador de propiedad (PID) es cero. Para establecer esta propiedad en el origen de red, pase un **puntero IPropertyStore** al solucionador de origen. Para obtener más información, vea [Configuring a Media Source](configuring-a-media-source.md).

Si no se establece o establece como **GUID \_ NULL,** Microsoft Media Foundation genera un GUID anónimo por sesión que garantiza la privacidad del usuario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 \[ aplicaciones de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                            |
| Encabezado<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[Redes en Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




