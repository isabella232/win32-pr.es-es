---
title: Propiedad GatewayUserSelectedCredsSource de IMsRdpClientTransportSettings
description: Establece o recupera el origen de credenciales de puerta de enlace de escritorio remoto (puerta de enlace de RD) Escritorio remoto especificados por el usuario.
ms.assetid: 0c12ddf6-52c2-40a2-af2b-effd4e8bbdb6
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad GatewayUserSelectedCredsSource
- Propiedad GatewayUserSelectedCredsSource Servicios de Escritorio remoto, interfaz IMsRdpClientTransportSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientTransportSettings, propiedad GatewayUserSelectedCredsSource
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
ms.openlocfilehash: 1556088e62221df7ff91b4b0069bb1ec938ebf23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533874"
---
# <a name="imsrdpclienttransportsettingsgatewayuserselectedcredssource-property"></a>IMsRdpClientTransportSettings:: GatewayUserSelectedCredsSource (propiedad)

Establece o recupera el origen de credenciales de puerta de enlace de escritorio remoto (puerta de enlace de RD) Escritorio remoto especificados por el usuario.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_GatewayUserSelectedCredsSource(
  [in]  ULONG ulProxyCredsSource
);

HRESULT get_GatewayUserSelectedCredsSource(
  [out] ULONG *pulProxyCredsSource
);
```



## <a name="property-value"></a>Valor de propiedad

Variable **ULong** que especifica el método de autenticación de puerta de enlace de escritorio remoto. Este parámetro puede ser uno de los valores siguientes.

<dt>

<span id="TSC_PROXY_CREDS_MODE_USERPASS"></span><span id="tsc_proxy_creds_mode_userpass"></span>

<span id="TSC_PROXY_CREDS_MODE_USERPASS"></span><span id="tsc_proxy_creds_mode_userpass"></span>**TSC \_ \_Modo de credenciales de proxy \_ \_ USERPASS** (0 (0X0))


</dt> <dd>

Use una contraseña (NTLM) como método de autenticación para la puerta de enlace de escritorio remoto.

</dd> <dt>

<span id="TSC_PROXY_CREDS_MODE_SMARTCARD"></span><span id="tsc_proxy_creds_mode_smartcard"></span>

<span id="TSC_PROXY_CREDS_MODE_SMARTCARD"></span><span id="tsc_proxy_creds_mode_smartcard"></span>**TSC \_ \_ \_ \_ Tarjeta inteligente del modo de credenciales de proxy** (1 (0x1))


</dt> <dd>

Usar una tarjeta inteligente como método de autenticación para la puerta de enlace de escritorio remoto.

</dd> <dt>

<span id="TSC_PROXY_CREDS_MODE_ANY"></span><span id="tsc_proxy_creds_mode_any"></span>

<span id="TSC_PROXY_CREDS_MODE_ANY"></span><span id="tsc_proxy_creds_mode_any"></span>**TSC \_ \_Modo de credenciales de proxy \_ \_ any** (4 (0x4))


</dt> <dd>

Use cualquier método de autenticación para la puerta de enlace de escritorio remoto.

</dd> </dl>

## <a name="error-codes"></a>Códigos de error

Devuelve **S \_ correcto** si se realiza correctamente.

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

 

 





