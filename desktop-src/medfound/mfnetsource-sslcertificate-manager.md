---
description: Almacena el puntero IUnknown de la clase que implementa la interfaz IMFSSLCertificateManager.
ms.assetid: 13e05bda-96c2-4095-a266-74185760f33a
title: Propiedad MFNETSOURCE_SSLCERTIFICATE_MANAGER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf6e21962e3d521e8c5781d59b2e0fe6fed04aa4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714905"
---
# <a name="mfnetsource_sslcertificate_manager-property"></a>Propiedad del administrador de \_ SSLCERTIFICATE de MFNETSOURCE \_

Almacena el puntero **IUnknown** de la clase que implementa la interfaz [**IMFSSLCertificateManager**](/windows/desktop/api/mfidl/nn-mfidl-imfsslcertificatemanager) . La implementación del cliente proporciona métodos para obtener el certificado SSL del cliente cuando lo solicita el servidor.



Tipo de datos

Tipo PROPVARIANT (VT)

Miembro de PROPVARIANT

**IUnknown (puntero)**

VT \_ desconocido

**punkVal**



## <a name="remarks"></a>Observaciones

La constante **MFNETSOURCE de \_ SSLCERTIFICATE \_ Manager** define el GUID de la clave de propiedad. El identificador de propiedad (PID) es cero. Para establecer esta propiedad en el origen de red, pase un puntero **IPropertyStore** a la resolución de origen. Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).

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

 

 




