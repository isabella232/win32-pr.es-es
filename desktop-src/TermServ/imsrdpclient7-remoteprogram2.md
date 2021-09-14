---
title: Propiedad IMsRdpClient7 RemoteProgram2
description: Recupera un objeto que admite la interfaz ITSRemoteProgram2.
ms.assetid: fabdc933-c941-487f-9e49-c20a39e0c86e
ms.tgt_platform: multiple
keywords:
- Propiedad RemoteProgram2 Servicios de Escritorio remoto
- Propiedad RemoteProgram2 Servicios de Escritorio remoto , interfaz IMsRdpClient7
- Interfaz IMsRdpClient7 Servicios de Escritorio remoto , propiedad RemoteProgram2
- Propiedad RemoteProgram2 Servicios de Escritorio remoto , interfaz IMsRdpClient8
- Interfaz IMsRdpClient8 Servicios de Escritorio remoto , propiedad RemoteProgram2
- Propiedad RemoteProgram2 Servicios de Escritorio remoto , interfaz IMsRdpClient9
- Interfaz IMsRdpClient9 Servicios de Escritorio remoto , propiedad RemoteProgram2
- Propiedad RemoteProgram2 Servicios de Escritorio remoto , interfaz IMsRdpClient10
- Interfaz IMsRdpClient10 Servicios de Escritorio remoto , propiedad RemoteProgram2
topic_type:
- apiref
api_name:
- IMsRdpClient7.RemoteProgram2
- IMsRdpClient7.get_RemoteProgram2
- IMsRdpClient8.RemoteProgram2
- IMsRdpClient8.get_RemoteProgram2
- IMsRdpClient9.RemoteProgram2
- IMsRdpClient9.get_RemoteProgram2
- IMsRdpClient10.RemoteProgram2
- IMsRdpClient10.get_RemoteProgram2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1572aada1384a7edfe88b198826050927ae3cff5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968415"
---
# <a name="imsrdpclient7remoteprogram2-property"></a>Propiedad IMsRdpClient7::RemoteProgram2

Recupera un objeto que admite la [**interfaz ITSRemoteProgram2.**](itsremoteprogram2.md)

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_RemoteProgram2(
  [out, retval] ITSRemoteProgram2 **ppRemoteProgram
);
```



## <a name="property-value"></a>Valor de propiedad

Dirección de un puntero [**de interfaz ITSRemoteProgram2**](itsremoteprogram2.md) que recibe el objeto .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                      |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID IMsRdpClient7 se define como \_ b2a5b5ce-3461-444a-91d4-add26d070638<br/>       |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> </dl>

 

 





