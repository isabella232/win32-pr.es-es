---
title: Propiedad IMsTscAx SecuredSettingsEnabled
description: Indica si la interfaz IMsTscSecuredSettings está disponible. Es decir, si la página web que contiene el control se encuentra actualmente en una de las zonas de seguridad Internet Explorer URL permitidas.
ms.assetid: 0747eab0-9d62-4c10-b02d-fc65ca2f752e
ms.tgt_platform: multiple
keywords:
- Propiedad SecuredSettingsEnabled Servicios de Escritorio remoto
- Propiedad SecuredSettingsEnabled Servicios de Escritorio remoto interfaz , IMsTscAx
- Interfaz IMsTscAx Servicios de Escritorio remoto propiedad , SecuredSettingsEnabled
- Propiedad SecuredSettingsEnabled Servicios de Escritorio remoto interfaz , IMsRdpClient
- Interfaz IMsRdpClient Servicios de Escritorio remoto , propiedad SecuredSettingsEnabled
- Propiedad SecuredSettingsEnabled Servicios de Escritorio remoto interfaz , IMsRdpClient2
- Interfaz IMsRdpClient2 Servicios de Escritorio remoto , propiedad SecuredSettingsEnabled
- Propiedad SecuredSettingsEnabled Servicios de Escritorio remoto interfaz , IMsRdpClient3
- Interfaz IMsRdpClient3 Servicios de Escritorio remoto propiedad , SecuredSettingsEnabled
- Propiedad SecuredSettingsEnabled Servicios de Escritorio remoto interfaz , IMsRdpClient4
- Interfaz IMsRdpClient4 Servicios de Escritorio remoto propiedad , SecuredSettingsEnabled
- Propiedad SecuredSettingsEnabled Servicios de Escritorio remoto interfaz , IMsRdpClient5
- Interfaz IMsRdpClient5 Servicios de Escritorio remoto propiedad , SecuredSettingsEnabled
- Propiedad SecuredSettingsEnabled Servicios de Escritorio remoto interfaz , IMsRdpClient6
- Interfaz IMsRdpClient6 Servicios de Escritorio remoto propiedad , SecuredSettingsEnabled
- Propiedad SecuredSettingsEnabled Servicios de Escritorio remoto interfaz , IMsRdpClient7
- Interfaz IMsRdpClient7 Servicios de Escritorio remoto propiedad , SecuredSettingsEnabled
- Propiedad SecuredSettingsEnabled Servicios de Escritorio remoto interfaz , IMsRdpClient8
- Interfaz IMsRdpClient8 Servicios de Escritorio remoto , propiedad SecuredSettingsEnabled
- Propiedad SecuredSettingsEnabled Servicios de Escritorio remoto interfaz , IMsRdpClient9
- Interfaz IMsRdpClient9 Servicios de Escritorio remoto propiedad , SecuredSettingsEnabled
topic_type:
- apiref
api_name:
- IMsTscAx.SecuredSettingsEnabled
- IMsTscAx.get_SecuredSettingsEnabled
- IMsRdpClient.SecuredSettingsEnabled
- IMsRdpClient.get_SecuredSettingsEnabled
- IMsRdpClient2.SecuredSettingsEnabled
- IMsRdpClient2.get_SecuredSettingsEnabled
- IMsRdpClient3.SecuredSettingsEnabled
- IMsRdpClient3.get_SecuredSettingsEnabled
- IMsRdpClient4.SecuredSettingsEnabled
- IMsRdpClient4.get_SecuredSettingsEnabled
- IMsRdpClient5.SecuredSettingsEnabled
- IMsRdpClient5.get_SecuredSettingsEnabled
- IMsRdpClient6.SecuredSettingsEnabled
- IMsRdpClient6.get_SecuredSettingsEnabled
- IMsRdpClient7.SecuredSettingsEnabled
- IMsRdpClient7.get_SecuredSettingsEnabled
- IMsRdpClient8.SecuredSettingsEnabled
- IMsRdpClient8.get_SecuredSettingsEnabled
- IMsRdpClient9.SecuredSettingsEnabled
- IMsRdpClient9.get_SecuredSettingsEnabled
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc03fb9cff3a99d77006989b7adade40a15ad4bb4d63e6f940092b765b1e250f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119771065"
---
# <a name="imstscaxsecuredsettingsenabled-property"></a>Propiedad IMsTscAx::SecuredSettingsEnabled

Indica si la [**interfaz IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) está disponible. Es decir, si la página web que contiene el control se encuentra actualmente en una de las zonas de seguridad Internet Explorer URL permitidas.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_SecuredSettingsEnabled(
  [out] BOOL *pSecuredSettingsEnabled
);
```



## <a name="property-value"></a>Valor de propiedad

El valor de este parámetro es **TRUE si** la interfaz está disponible y **FALSE** en caso contrario.

## <a name="error-codes"></a>Códigos de error

Devuelve **S \_ OK si** se realiza correctamente.

## <a name="remarks"></a>Comentarios

Use este método para consultar si la [**interfaz IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) está disponible antes de recuperar la [**propiedad SecuredSettings.**](imstscax-securedsettings.md)

Consulte Proporcionar [seguridad de cliente RDP](providing-for-rdp-client-security.md) para obtener una lista de zonas de seguridad de direcciones URL restringidas.

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsTscAx se define como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489<br/>            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClient**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> <dt>

[**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





