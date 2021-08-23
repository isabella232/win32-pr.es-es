---
title: Método Conectar IMsTscAx
description: Inicia una conexión mediante las propiedades establecidas actualmente en el control .
ms.assetid: 9bcbdc13-6c66-4737-82a4-98329f173743
ms.tgt_platform: multiple
keywords:
- Conectar método Servicios de Escritorio remoto
- Conectar método Servicios de Escritorio remoto , interfaz IMsTscAx
- Interfaz IMsTscAx Servicios de Escritorio remoto , Conectar método
- Conectar método Servicios de Escritorio remoto , interfaz IMsRdpClient
- Interfaz IMsRdpClient Servicios de Escritorio remoto , Conectar método
- Conectar método Servicios de Escritorio remoto , interfaz IMsRdpClient2
- Interfaz IMsRdpClient2 Servicios de Escritorio remoto , Conectar método
- Conectar método Servicios de Escritorio remoto , interfaz IMsRdpClient3
- Interfaz IMsRdpClient3 Servicios de Escritorio remoto , Conectar método
- Conectar método Servicios de Escritorio remoto , interfaz IMsRdpClient4
- Interfaz IMsRdpClient4 Servicios de Escritorio remoto , Conectar método
- Conectar método Servicios de Escritorio remoto , interfaz IMsRdpClient5
- Interfaz IMsRdpClient5 Servicios de Escritorio remoto , Conectar método
- Conectar método Servicios de Escritorio remoto , interfaz IMsRdpClient6
- Interfaz IMsRdpClient6 Servicios de Escritorio remoto , Conectar método
- Conectar método Servicios de Escritorio remoto , interfaz IMsRdpClient7
- Interfaz IMsRdpClient7 Servicios de Escritorio remoto , Conectar método
- Conectar método Servicios de Escritorio remoto , interfaz IMsRdpClient8
- Interfaz IMsRdpClient8 Servicios de Escritorio remoto , Conectar método
- Conectar método Servicios de Escritorio remoto , interfaz IMsRdpClient9
- Interfaz IMsRdpClient9 Servicios de Escritorio remoto , Conectar método
topic_type:
- apiref
api_name:
- IMsTscAx.Connect
- IMsRdpClient.Connect
- IMsRdpClient2.Connect
- IMsRdpClient3.Connect
- IMsRdpClient4.Connect
- IMsRdpClient5.Connect
- IMsRdpClient6.Connect
- IMsRdpClient7.Connect
- IMsRdpClient8.Connect
- IMsRdpClient9.Connect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4372b19c9dba51714c6927d5e54468e143033689bfd9c74db78bbff8812e45ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513115"
---
# <a name="imstscaxconnect-method"></a>IMsTscAx::Conectar método

Inicia una conexión mediante las propiedades establecidas actualmente en el control .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Connect();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve **S \_ OK si** se realiza correctamente.

## <a name="remarks"></a>Comentarios

La única propiedad necesaria es el nombre del servidor. Consulte la [**propiedad**](imstscax-server.md) Server.

El control se conecta de forma asincrónica, por lo que una devolución de una llamada Conectar indica solo que la conexión se ha iniciado correctamente, no que se ha completado. Debe responder a eventos en la interfaz [**IMsTscAxEvents**](imstscaxevents-interface.md) para determinar cuándo el control se ha conectado correctamente (o se ha desconectado).

Este método devuelve **E \_ FAIL** si se llama mientras el control ya está conectado o en estado de conexión.

Después **Conectar** se ha llamado a , la mayoría de las propiedades del control ya no se pueden establecer hasta que el control vuelva al estado desconectado.

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

[**Desconectar**](imstscax-disconnect.md)
</dt> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> </dl>

 

 





