---
title: Propiedad IMsRdpClientTransportSettings GatewayUserSelectedCredsSource
description: Establece o recupera el origen de credenciales Escritorio remoto gateway (puerta de enlace de Escritorio remoto) especificado por el usuario.
ms.assetid: 0c12ddf6-52c2-40a2-af2b-effd4e8bbdb6
ms.tgt_platform: multiple
keywords:
- Propiedad GatewayUserSelectedCredsSource Servicios de Escritorio remoto
- Propiedad GatewayUserSelectedCredsSource Servicios de Escritorio remoto , interfaz IMsRdpClientTransportSettings
- Interfaz IMsRdpClientTransportSettings Servicios de Escritorio remoto , propiedad GatewayUserSelectedCredsSource
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayUserSelectedCredsSource
- IMsRdpClientTransportSettings.get_GatewayUserSelectedCredsSource
- IMsRdpClientTransportSettings.put_GatewayUserSelectedCredsSource
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7632609f34d0133f37af4e8df16ebd574b3ef84e248c2bb3d2b1a84313957b43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001015"
---
# <a name="imsrdpclienttransportsettingsgatewayuserselectedcredssource-property"></a>Propiedad IMsRdpClientTransportSettings::GatewayUserSelectedCredsSource

Establece o recupera el origen de credenciales Escritorio remoto gateway (puerta de enlace de Escritorio remoto) especificado por el usuario.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_GatewayUserSelectedCredsSource(
  [in]  ULONG ulProxyCredsSource
);

HRESULT get_GatewayUserSelectedCredsSource(
  [out] ULONG *pulProxyCredsSource
);
```



## <a name="property-value"></a>Valor de propiedad

Variable **ULONG que** especifica el método de autenticación de puerta de enlace de Escritorio remoto. Este parámetro puede ser uno de los valores siguientes.

<dt>

<span id="TSC_PROXY_CREDS_MODE_USERPASS"></span><span id="tsc_proxy_creds_mode_userpass"></span>

<span id="TSC_PROXY_CREDS_MODE_USERPASS"></span><span id="tsc_proxy_creds_mode_userpass"></span>**TSC \_ USERPASS \_ EN \_ MODO \_ CREDS DE PROXY** (0 (0x0))


</dt> <dd>

Use una contraseña (NTLM) como método de autenticación para la puerta de enlace de Escritorio remoto.

</dd> <dt>

<span id="TSC_PROXY_CREDS_MODE_SMARTCARD"></span><span id="tsc_proxy_creds_mode_smartcard"></span>

<span id="TSC_PROXY_CREDS_MODE_SMARTCARD"></span><span id="tsc_proxy_creds_mode_smartcard"></span>**TSC \_ TARJETA \_ INTELIGENTE DE MODO \_ \_ CREDS DE PROXY** (1 (0x1))


</dt> <dd>

Use una tarjeta inteligente como método de autenticación para puerta de enlace de Escritorio remoto.

</dd> <dt>

<span id="TSC_PROXY_CREDS_MODE_ANY"></span><span id="tsc_proxy_creds_mode_any"></span>

<span id="TSC_PROXY_CREDS_MODE_ANY"></span><span id="tsc_proxy_creds_mode_any"></span>**TSC \_ PROXY \_ CREDS \_ MODE \_ ANY** (4 (0x4))


</dt> <dd>

Use cualquier método de autenticación para puerta de enlace de Escritorio remoto.

</dd> </dl>

## <a name="error-codes"></a>Códigos de error

Devuelve **S \_ OK si** se realiza correctamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                         |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                   |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientTransportSettings se define como 720298C0-A099-46f5-9F82-96921BAE4701<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





