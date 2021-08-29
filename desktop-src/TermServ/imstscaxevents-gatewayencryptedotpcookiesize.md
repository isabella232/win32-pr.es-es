---
title: Propiedad IMsRdpClientTransportSettings2 GatewayEncryptedOtpCookieSize
description: Especifica o recupera el tamaño de la cookie cifrada de contraseña de un solo uso (OTP).
ms.assetid: a4fdcd06-59ae-407f-9ac6-dfe4b52fb5d7
ms.tgt_platform: multiple
keywords:
- Propiedad GatewayEncryptedOtpCookieSize Servicios de Escritorio remoto
- Propiedad GatewayEncryptedOtpCookieSize Servicios de Escritorio remoto interfaz , IMsRdpClientTransportSettings2
- Interfaz IMsRdpClientTransportSettings2 Servicios de Escritorio remoto , propiedad GatewayEncryptedOtpCookieSize
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayEncryptedOtpCookieSize
- IMsRdpClientTransportSettings2.get_GatewayEncryptedOtpCookieSize
- IMsRdpClientTransportSettings2.put_GatewayEncryptedOtpCookieSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97346420f709707a239d7558fd871be1e685bb83301b06d37b1910e596515c2f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125255"
---
# <a name="imsrdpclienttransportsettings2gatewayencryptedotpcookiesize-property"></a>IMsRdpClientTransportSettings2::GatewayEncryptedOtpCookieSize, propiedad

Especifica o recupera el tamaño de la cookie cifrada de contraseña de un solo uso (OTP).

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_GatewayEncryptedOtpCookieSize(
  [in]  ULONG ulEncryptedOtpCookieSize
);

HRESULT get_GatewayEncryptedOtpCookieSize(
  [out] ULONG *pulEncryptedOtpCookieSize
);
```



## <a name="property-value"></a>Valor de propiedad

Especifica o recupera el tamaño de la cookie cifrada de contraseña de un solo uso (OTP).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista con SP1<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| IID<br/>                      | IID \_ IMsRdpClientTransportSettings2 se define como 67341688-D606-4c73-A5D2-2E0489009319<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md)
</dt> <dt>

[**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





