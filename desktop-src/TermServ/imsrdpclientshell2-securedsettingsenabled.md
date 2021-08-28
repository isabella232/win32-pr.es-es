---
title: IMsRdpClientShell2 SecuredSettingsEnabled, propiedad
description: Recupera un valor que indica si la página web actual está en una zona de seguridad de Internet Explorer url de confianza.
ms.assetid: 51988473-fff7-4574-bd6e-d05ca452da54
ms.tgt_platform: multiple
keywords:
- Propiedad SecuredSettingsEnabled Servicios de Escritorio remoto
- Propiedad SecuredSettingsEnabled Servicios de Escritorio remoto interfaz , IMsRdpClientShell2
- Interfaz IMsRdpClientShell2 Servicios de Escritorio remoto , propiedad SecuredSettingsEnabled
topic_type:
- apiref
api_name:
- IMsRdpClientShell2.SecuredSettingsEnabled
- IMsRdpClientShell2.get_SecuredSettingsEnabled
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d418df76de38313d681f9f01a4dea33ba0803ad67e42d92d90d2ba5a354a8eac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870885"
---
# <a name="imsrdpclientshell2securedsettingsenabled-property"></a>IMsRdpClientShell2::SecuredSettingsEnabled, propiedad

Recupera un valor que indica si la página web actual está en una zona de seguridad de Internet Explorer url de confianza.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_SecuredSettingsEnabled(
  [out, retval] BOOL *pSecuredSettingsEnabled
);
```



## <a name="property-value"></a>Valor de propiedad

Puntero a un valor booleano que indica si la página web actual está en una zona de seguridad de Internet Explorer url de confianza.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7<br/>                                                                          |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                             |
| Archivo DLL<br/>                      | <dl> <dt>MsRdpWebAccess.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientShell2**](imsrdpclientshell2.md)
</dt> </dl>

 

 





