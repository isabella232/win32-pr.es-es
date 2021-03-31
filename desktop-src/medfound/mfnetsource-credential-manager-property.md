---
description: Contiene un puntero a la interfaz IMFNetCredentialManager.
ms.assetid: c0826956-9df1-40ec-8ad1-9e0dca34d847
title: Propiedad MFNETSOURCE_CREDENTIAL_MANAGER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3447369cedfa5c516e1d7696aae70834c6ce89a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154961"
---
# <a name="mfnetsource_credential_manager-property"></a>\_Propiedad del administrador de credenciales de MFNETSOURCE \_

Contiene un puntero a la interfaz [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) . Utilice esta propiedad para pasar la implementación de [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) de la aplicación al origen de red.



Tipo de datos

Tipo PROPVARIANT (VT)

Miembro de PROPVARIANT

**IUnknown** (puntero)

VT \_ desconocido

**punkVal**



## <a name="remarks"></a>Observaciones

La constante **MFNETSOURCE \_ Credential \_ Manager** define el **GUID** de la clave de propiedad. El identificador de propiedad (PID) es cero.

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

[Autenticación de origen de red](network-source-authentication.md)
</dt> <dt>

[Funciones de red en Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




