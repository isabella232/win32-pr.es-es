---
description: Almacena el puntero IUnknown de la clase que implementa la interfaz IMFSSLCertificateManager.
ms.assetid: 13e05bda-96c2-4095-a266-74185760f33a
title: MFNETSOURCE_SSLCERTIFICATE_MANAGER propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d6f853ae3fe44a9c4508386df4096e4adac36f3cec8a8cf199eb91cb87e1fe2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118243299"
---
# <a name="mfnetsource_sslcertificate_manager-property"></a>Propiedad MFNETSOURCE \_ SSLCERTIFICATE \_ MANAGER

Almacena el **puntero IUnknown** de la clase que implementa la [**interfaz IMFSSLCertificateManager.**](/windows/desktop/api/mfidl/nn-mfidl-imfsslcertificatemanager) La implementación de cliente proporciona métodos para obtener el certificado SSL de cliente cuando lo solicita el servidor.



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

**Puntero IUnknown**

VT \_ UNKNOWN

**val**



## <a name="remarks"></a>Comentarios

La **constante MFNETSOURCE \_ SSLCERTIFICATE \_ MANAGER** define el GUID de la clave de propiedad. El identificador de propiedad (PID) es cero. Para establecer esta propiedad en el origen de red, pase un **puntero IPropertyStore** al solucionador de origen. Para obtener más información, vea [Configuring a Media Source](configuring-a-media-source.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[Redes en Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




