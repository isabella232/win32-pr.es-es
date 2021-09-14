---
title: Propiedad IMsRdpClient ExtendedDisconnectReason
description: Contiene información extendida sobre el motivo de desconexión del control.
ms.assetid: 5729992f-6695-44c0-8cf0-0d6b4cbddb62
ms.tgt_platform: multiple
keywords:
- Propiedad ExtendedDisconnectReason Servicios de Escritorio remoto
- Propiedad ExtendedDisconnectReason Servicios de Escritorio remoto , interfaz IMsRdpClient
- Interfaz IMsRdpClient Servicios de Escritorio remoto , propiedad ExtendedDisconnectReason
- Propiedad ExtendedDisconnectReason Servicios de Escritorio remoto , interfaz IMsRdpClient2
- Interfaz IMsRdpClient2 Servicios de Escritorio remoto , propiedad ExtendedDisconnectReason
- Propiedad ExtendedDisconnectReason Servicios de Escritorio remoto , interfaz IMsRdpClient3
- Interfaz IMsRdpClient3 Servicios de Escritorio remoto , propiedad ExtendedDisconnectReason
- Propiedad ExtendedDisconnectReason Servicios de Escritorio remoto , interfaz IMsRdpClient4
- Interfaz IMsRdpClient4 Servicios de Escritorio remoto , propiedad ExtendedDisconnectReason
- Propiedad ExtendedDisconnectReason Servicios de Escritorio remoto , interfaz IMsRdpClient5
- Interfaz IMsRdpClient5 Servicios de Escritorio remoto , propiedad ExtendedDisconnectReason
- Propiedad ExtendedDisconnectReason Servicios de Escritorio remoto , interfaz IMsRdpClient6
- Interfaz IMsRdpClient6 Servicios de Escritorio remoto , propiedad ExtendedDisconnectReason
- Propiedad ExtendedDisconnectReason Servicios de Escritorio remoto , interfaz IMsRdpClient7
- Interfaz IMsRdpClient7 Servicios de Escritorio remoto , propiedad ExtendedDisconnectReason
- Propiedad ExtendedDisconnectReason Servicios de Escritorio remoto , interfaz IMsRdpClient8
- Interfaz IMsRdpClient8 Servicios de Escritorio remoto , propiedad ExtendedDisconnectReason
- Propiedad ExtendedDisconnectReason Servicios de Escritorio remoto , interfaz IMsRdpClient9
- Interfaz IMsRdpClient9 Servicios de Escritorio remoto , propiedad ExtendedDisconnectReason
- Propiedad ExtendedDisconnectReason Servicios de Escritorio remoto , interfaz IMsRdpClient10
- Interfaz IMsRdpClient10 Servicios de Escritorio remoto , propiedad ExtendedDisconnectReason
topic_type:
- apiref
api_name:
- IMsRdpClient.ExtendedDisconnectReason
- IMsRdpClient.get_ExtendedDisconnectReason
- IMsRdpClient2.ExtendedDisconnectReason
- IMsRdpClient2.get_ExtendedDisconnectReason
- IMsRdpClient3.ExtendedDisconnectReason
- IMsRdpClient3.get_ExtendedDisconnectReason
- IMsRdpClient4.ExtendedDisconnectReason
- IMsRdpClient4.get_ExtendedDisconnectReason
- IMsRdpClient5.ExtendedDisconnectReason
- IMsRdpClient5.get_ExtendedDisconnectReason
- IMsRdpClient6.ExtendedDisconnectReason
- IMsRdpClient6.get_ExtendedDisconnectReason
- IMsRdpClient7.ExtendedDisconnectReason
- IMsRdpClient7.get_ExtendedDisconnectReason
- IMsRdpClient8.ExtendedDisconnectReason
- IMsRdpClient8.get_ExtendedDisconnectReason
- IMsRdpClient9.ExtendedDisconnectReason
- IMsRdpClient9.get_ExtendedDisconnectReason
- IMsRdpClient10.ExtendedDisconnectReason
- IMsRdpClient10.get_ExtendedDisconnectReason
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b94c2612b231e24aaec855b6ebd1f9a0498b63c3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126891060"
---
# <a name="imsrdpclientextendeddisconnectreason-property"></a>Propiedad IMsRdpClient::ExtendedDisconnectReason

Contiene información extendida sobre el motivo de desconexión del control.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_ExtendedDisconnectReason(
  [out] ExtendedDisconnectReasonCode *pExtendedDisconnectReason
);
```



## <a name="property-value"></a>Valor de propiedad

Puntero al [**valor ExtendedDisconnectReasonCode**](extendeddisconnectreasoncode.md) que indica el motivo de la desconexión del cliente.

## <a name="error-codes"></a>Códigos de error

Si el método se realiza correctamente, **se devuelve S \_ OK.** Cualquier otro **valor HRESULT** indica que se ha dado error en la llamada.

## <a name="remarks"></a>Observaciones

Normalmente, se llama a este método en el controlador de eventos [**IMsTscAxEvents::OnDisconnected**](imstscaxevents-ondisconnected.md) para recuperar información adicional sobre el evento de desconexión.

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClient se define como 92b4a539-7115-4b7c-a5a9-e5d9efc2780a<br/>        |



## <a name="see-also"></a>Consulte también

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

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> <dt>

[**IMsTscAxEvents::OnDisconnected**](imstscaxevents-ondisconnected.md)
</dt> </dl>

 

 





