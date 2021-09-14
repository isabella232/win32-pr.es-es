---
description: Contiene un puntero a la interfaz IMFNetCredentialManager.
ms.assetid: c0826956-9df1-40ec-8ad1-9e0dca34d847
title: MFNETSOURCE_CREDENTIAL_MANAGER propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3447369cedfa5c516e1d7696aae70834c6ce89a5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363858"
---
# <a name="mfnetsource_credential_manager-property"></a>Propiedad MFNETSOURCE \_ CREDENTIAL \_ MANAGER

Contiene un puntero a la [**interfaz IMFNetCredentialManager.**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) Use esta propiedad para pasar la implementación de LA aplicación de [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) al origen de red.



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

**Puntero IUnknown**

VT \_ UNKNOWN

**val**



## <a name="remarks"></a>Observaciones

La constante **MFNETSOURCE \_ CREDENTIAL \_ MANAGER** define el **GUID** de la clave de propiedad. El identificador de propiedad (PID) es cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[Autenticación de origen de red](network-source-authentication.md)
</dt> <dt>

[Redes en Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




