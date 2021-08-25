---
title: Propiedad NegotiateSecurityLayer de IMsRdpClientNonScriptable3
description: Especifica o recupera si la capa de seguridad de negociación está habilitada para la conexión.
ms.assetid: 7fc9e3c7-0723-48c4-8d29-5f68a24a522c
ms.tgt_platform: multiple
keywords:
- Propiedad NegotiateSecurityLayer Servicios de Escritorio remoto
- Propiedad NegotiateSecurityLayer Servicios de Escritorio remoto , interfaz IMsRdpClientNonScriptable3
- Interfaz IMsRdpClientNonScriptable3 Servicios de Escritorio remoto , propiedad NegotiateSecurityLayer
- Propiedad NegotiateSecurityLayer Servicios de Escritorio remoto , interfaz IMsRdpClientNonScriptable4
- Interfaz IMsRdpClientNonScriptable4 Servicios de Escritorio remoto , propiedad NegotiateSecurityLayer
- Propiedad NegotiateSecurityLayer Servicios de Escritorio remoto , interfaz IMsRdpClientNonScriptable5
- Interfaz IMsRdpClientNonScriptable5 Servicios de Escritorio remoto , propiedad NegotiateSecurityLayer
- Propiedad NegotiateSecurityLayer Servicios de Escritorio remoto , objeto MsRdpClient5
- Objeto MsRdpClient5 Servicios de Escritorio remoto , propiedad NegotiateSecurityLayer
- Propiedad NegotiateSecurityLayer Servicios de Escritorio remoto , objeto MsRdpClient6
- Objeto MsRdpClient6 Servicios de Escritorio remoto , propiedad NegotiateSecurityLayer
- Propiedad NegotiateSecurityLayer Servicios de Escritorio remoto , objeto MsRdpClient7
- Objeto MsRdpClient7 Servicios de Escritorio remoto , propiedad NegotiateSecurityLayer
- Propiedad NegotiateSecurityLayer Servicios de Escritorio remoto , objeto MsRdpClient8
- Objeto MsRdpClient8 Servicios de Escritorio remoto , propiedad NegotiateSecurityLayer
- Propiedad NegotiateSecurityLayer Servicios de Escritorio remoto , objeto MsRdpClient9
- Objeto MsRdpClient9 Servicios de Escritorio remoto , propiedad NegotiateSecurityLayer
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.NegotiateSecurityLayer
- IMsRdpClientNonScriptable3.get_NegotiateSecurityLayer
- IMsRdpClientNonScriptable3.put_NegotiateSecurityLayer
- IMsRdpClientNonScriptable4.NegotiateSecurityLayer
- IMsRdpClientNonScriptable4.get_NegotiateSecurityLayer
- IMsRdpClientNonScriptable4.put_NegotiateSecurityLayer
- IMsRdpClientNonScriptable5.NegotiateSecurityLayer
- IMsRdpClientNonScriptable5.get_NegotiateSecurityLayer
- IMsRdpClientNonScriptable5.put_NegotiateSecurityLayer
- MsRdpClient5.NegotiateSecurityLayer
- MsRdpClient6.NegotiateSecurityLayer
- MsRdpClient7.NegotiateSecurityLayer
- MsRdpClient8.NegotiateSecurityLayer
- MsRdpClient9.NegotiateSecurityLayer
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13f87abb5323289e60e3d29fa93d5e858a9a755224e7161ba28970ef5ccb186f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119771555"
---
# <a name="imsrdpclientnonscriptable3negotiatesecuritylayer-property"></a>Propiedad IMsRdpClientNonScriptable3::NegotiateSecurityLayer

Especifica o recupera si la capa de seguridad de negociación está habilitada para la conexión.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_NegotiateSecurityLayer(
  [in]  VARIANT_BOOL fNegotiate
);

HRESULT get_NegotiateSecurityLayer(
  [out] VARIANT_BOOL *pfNegotiate
);
```



## <a name="property-value"></a>Valor de propiedad

Especifica si se va a habilitar la negociación de la capa de seguridad.

## <a name="remarks"></a>Comentarios

Si esta propiedad se establece en **VARIANT \_ FALSE** y Autenticación a nivel de red (NLA) está habilitado en el sistema operativo cliente, el cliente no negociará la capa de seguridad y, en su lugar, usará NLA para proteger la conexión RDP. Si esta propiedad se establece en **VARIANT \_ TRUE,** el cliente negociará entre NLA y la seguridad rdp básica.

> [!Note]  
> Deshabilitar la negociación de la capa de seguridad solo es posible cuando se conecta a un servidor de host de sesión de Escritorio remoto (host de sesión de Escritorio remoto) que ejecuta Windows Vista o sistemas operativos posteriores. Si esta propiedad está habilitada y el cliente intenta conectarse a un servidor host de sesión de Escritorio remoto que ejecuta un sistema operativo anterior, se producirá un error en la conexión.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                      |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable3 se define como b3378d90-0728-45c7-8ed7-b6159fb92219<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





