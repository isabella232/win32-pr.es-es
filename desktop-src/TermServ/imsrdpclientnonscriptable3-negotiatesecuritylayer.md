---
title: Propiedad NegotiateSecurityLayer de IMsRdpClientNonScriptable3
description: Especifica o recupera si la capa de seguridad de negociación está habilitada para la conexión.
ms.assetid: 7fc9e3c7-0723-48c4-8d29-5f68a24a522c
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad NegotiateSecurityLayer
- Propiedad NegotiateSecurityLayer Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable3, propiedad NegotiateSecurityLayer
- Propiedad NegotiateSecurityLayer Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable4, propiedad NegotiateSecurityLayer
- Propiedad NegotiateSecurityLayer Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad NegotiateSecurityLayer
- Servicios de Escritorio remoto de la propiedad NegotiateSecurityLayer, objeto MsRdpClient5
- Servicios de Escritorio remoto de objeto MsRdpClient5, propiedad NegotiateSecurityLayer
- Servicios de Escritorio remoto de la propiedad NegotiateSecurityLayer, objeto MsRdpClient6
- Servicios de Escritorio remoto de objeto MsRdpClient6, propiedad NegotiateSecurityLayer
- Servicios de Escritorio remoto de la propiedad NegotiateSecurityLayer, objeto MsRdpClient7
- Servicios de Escritorio remoto de objeto MsRdpClient7, propiedad NegotiateSecurityLayer
- Servicios de Escritorio remoto de la propiedad NegotiateSecurityLayer, objeto MsRdpClient8
- Servicios de Escritorio remoto de objeto MsRdpClient8, propiedad NegotiateSecurityLayer
- Servicios de Escritorio remoto de la propiedad NegotiateSecurityLayer, objeto MsRdpClient9
- Servicios de Escritorio remoto de objeto MsRdpClient9, propiedad NegotiateSecurityLayer
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
ms.openlocfilehash: e64533615c780cd6e3703be85363684e537b784a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676761"
---
# <a name="imsrdpclientnonscriptable3negotiatesecuritylayer-property"></a>IMsRdpClientNonScriptable3:: NegotiateSecurityLayer (propiedad)

Especifica o recupera si la capa de seguridad de negociación está habilitada para la conexión.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_NegotiateSecurityLayer(
  [in]  VARIANT_BOOL fNegotiate
);

HRESULT get_NegotiateSecurityLayer(
  [out] VARIANT_BOOL *pfNegotiate
);
```



## <a name="property-value"></a>Valor de propiedad

Especifica si se debe habilitar la negociación de la capa de seguridad.

## <a name="remarks"></a>Observaciones

Si esta propiedad se establece en **Variant \_ FALSE** y autenticación a nivel de red (NLA) está habilitada en el sistema operativo del cliente, el cliente no negociará el nivel de seguridad y, en su lugar, usará NLA para proteger la conexión RDP. Si esta propiedad se establece en **Variant \_ true**, el cliente negociará entre NLA y la seguridad básica de RDP.

> [!Note]  
> La deshabilitación de la negociación del nivel de seguridad solo es posible cuando se conecta a un servidor host de sesión de Escritorio remoto (host de sesión de escritorio remoto) que ejecuta Windows Vista o sistemas operativos posteriores. Si esta propiedad está habilitada y el cliente intenta conectarse a un servidor host de sesión de escritorio remoto que ejecuta un sistema operativo anterior, se producirá un error en la conexión.

 

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

 

 





