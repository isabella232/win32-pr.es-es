---
title: Propiedad IMsTscAx SecuredSettings
description: Recupera un puntero de interfaz IMsTscSecuredSettings.
ms.assetid: 64d4059b-e617-449d-a733-c19c1d281132
ms.tgt_platform: multiple
keywords:
- Propiedad SecuredSettings Servicios de Escritorio remoto
- Propiedad SecuredSettings Servicios de Escritorio remoto interfaz , IMsTscAx
- Interfaz IMsTscAx Servicios de Escritorio remoto , propiedad SecuredSettings
- Propiedad SecuredSettings Servicios de Escritorio remoto interfaz , IMsRdpClient
- Interfaz IMsRdpClient Servicios de Escritorio remoto , propiedad SecuredSettings
- Propiedad SecuredSettings Servicios de Escritorio remoto interfaz , IMsRdpClient2
- Interfaz IMsRdpClient2 Servicios de Escritorio remoto , propiedad SecuredSettings
- Propiedad SecuredSettings Servicios de Escritorio remoto interfaz , IMsRdpClient3
- Interfaz IMsRdpClient3 Servicios de Escritorio remoto , propiedad SecuredSettings
- Propiedad SecuredSettings Servicios de Escritorio remoto interfaz , IMsRdpClient4
- Interfaz IMsRdpClient4 Servicios de Escritorio remoto , propiedad SecuredSettings
- Propiedad SecuredSettings Servicios de Escritorio remoto interfaz , IMsRdpClient5
- Interfaz IMsRdpClient5 Servicios de Escritorio remoto , propiedad SecuredSettings
- Propiedad SecuredSettings Servicios de Escritorio remoto interfaz , IMsRdpClient6
- Interfaz IMsRdpClient6 Servicios de Escritorio remoto , propiedad SecuredSettings
- Propiedad SecuredSettings Servicios de Escritorio remoto interfaz , IMsRdpClient7
- Interfaz IMsRdpClient7 Servicios de Escritorio remoto , propiedad SecuredSettings
- Propiedad SecuredSettings Servicios de Escritorio remoto interfaz , IMsRdpClient8
- Interfaz IMsRdpClient8 Servicios de Escritorio remoto , propiedad SecuredSettings
- Propiedad SecuredSettings Servicios de Escritorio remoto interfaz , IMsRdpClient9
- Interfaz IMsRdpClient9 Servicios de Escritorio remoto , propiedad SecuredSettings
topic_type:
- apiref
api_name:
- IMsTscAx.SecuredSettings
- IMsTscAx.get_SecuredSettings
- IMsRdpClient.SecuredSettings
- IMsRdpClient.get_SecuredSettings
- IMsRdpClient2.SecuredSettings
- IMsRdpClient2.get_SecuredSettings
- IMsRdpClient3.SecuredSettings
- IMsRdpClient3.get_SecuredSettings
- IMsRdpClient4.SecuredSettings
- IMsRdpClient4.get_SecuredSettings
- IMsRdpClient5.SecuredSettings
- IMsRdpClient5.get_SecuredSettings
- IMsRdpClient6.SecuredSettings
- IMsRdpClient6.get_SecuredSettings
- IMsRdpClient7.SecuredSettings
- IMsRdpClient7.get_SecuredSettings
- IMsRdpClient8.SecuredSettings
- IMsRdpClient8.get_SecuredSettings
- IMsRdpClient9.SecuredSettings
- IMsRdpClient9.get_SecuredSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4f43a089092919124ed3031bafd12a70af1e1ffa0850bf058a91cc9dfd66125
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119771095"
---
# <a name="imstscaxsecuredsettings-property"></a>Propiedad IMsTscAx::SecuredSettings

Recupera un puntero [**de interfaz IMsTscSecuredSettings.**](imstscsecuredsettings-interface.md)

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_SecuredSettings(
  [out] IMsTscSecuredSettings **ppSecuredSettings
);
```



## <a name="property-value"></a>Valor de propiedad

Puntero [**de interfaz IMsTscSecuredSettings.**](imstscsecuredsettings-interface.md)

## <a name="error-codes"></a>Códigos de error

Devuelve **S \_ OK si** se realiza correctamente.

## <a name="remarks"></a>Comentarios

Si el control se hospeda en una página web y la zona de seguridad Internet Explorer URL actual no permite la recuperación de la dirección de interfaz, este método devuelve **E \_ FAIL**.

Consulte [**SecuredSettingsEnabled para**](imstscax-securedsettingsenabled.md) obtener restricciones sobre la disponibilidad de la [**interfaz IMsTscSecuredSettings.**](imstscsecuredsettings-interface.md)

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

 





