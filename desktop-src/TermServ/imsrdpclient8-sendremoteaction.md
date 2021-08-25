---
title: Método IMsRdpClient8 SendRemoteAction
description: Hace que se realice una acción en la sesión remota.
ms.assetid: d6a43662-7e51-404a-a3f9-a8b51cbc69d1
ms.tgt_platform: multiple
keywords:
- Método SendRemoteAction Servicios de Escritorio remoto
- Método SendRemoteAction Servicios de Escritorio remoto interfaz , IMsRdpClient8
- Interfaz IMsRdpClient8 Servicios de Escritorio remoto , método SendRemoteAction
- Método SendRemoteAction Servicios de Escritorio remoto interfaz , IMsRdpClient9
- Interfaz IMsRdpClient9 Servicios de Escritorio remoto , método SendRemoteAction
- Método SendRemoteAction Servicios de Escritorio remoto interfaz , IMsRdpClient10
- Interfaz IMsRdpClient10 Servicios de Escritorio remoto , método SendRemoteAction
topic_type:
- apiref
api_name:
- IMsRdpClient8.SendRemoteAction
- IMsRdpClient9.SendRemoteAction
- IMsRdpClient10.SendRemoteAction
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c41cdc5c5d164a0154f00d6fa4e8130d0860bfecbf77db7639272cbdd60f401f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080029"
---
# <a name="imsrdpclient8sendremoteaction-method"></a>IMsRdpClient8::SendRemoteAction (método)

Hace que se realice una acción en la sesión remota.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SendRemoteAction(
  [in] RemoteSessionActionType actionType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*actionType* \[ En\]
</dt> <dd>

Valor de la [**enumeración RemoteSessionActionType**](remotesessionactiontype.md) que especifica la acción que se enviará a la sesión remota.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClient8 se define como 4247E044-9271-43A9-BC49-E2AD9E855D62<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> </dl>

 

 





