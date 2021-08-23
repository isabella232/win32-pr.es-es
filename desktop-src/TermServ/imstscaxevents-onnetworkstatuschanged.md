---
title: Método IMsTscAxEvents OnNetworkStatusChanged
description: Se llama cuando el estado de la red ha cambiado. | Método IMsTscAxEvents OnNetworkStatusChanged
ms.assetid: 177A410E-2449-4FC7-8DE5-21F83A6DD028
ms.tgt_platform: multiple
keywords:
- Método OnNetworkStatusChanged Servicios de Escritorio remoto
- Método OnNetworkStatusChanged Servicios de Escritorio remoto , interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto método , OnNetworkStatusChanged
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnNetworkStatusChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c139dc314453d6ad921471857410285813afc9c9b48691bcc9c82bf33c8b517
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138408"
---
# <a name="imstscaxeventsonnetworkstatuschanged-method"></a>Método IMsTscAxEvents::OnNetworkStatusChanged

Se llama cuando el estado de la red ha cambiado.

## <a name="syntax"></a>Sintaxis


```C++
void OnNetworkStatusChanged(
  [in] ULONG qualityLevel,
  [in] LONG  bandwidth,
  [in] LONG  rtt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*qualityLevel* \[ En\]
</dt> <dd>

Especifica la nueva velocidad de conexión. Este será uno de los siguientes valores.

<dt>

1
</dt> <dd>

Menos de 512 kilobytes por segundo (KBps).

</dd> <dt>

2
</dt> <dd>

De 512 a 1999 KBps.

</dd> <dt>

3
</dt> <dd>

De 2000 a 9999 KBps.

</dd> <dt>

4
</dt> <dd>

Mayor o igual que 10 000 KBps.

</dd> </dl> </dd> <dt>

*ancho de banda* \[ En\]
</dt> <dd>

Especifica el ancho de banda de conexión.

</dd> <dt>

*rtt* \[ En\]
</dt> <dd>

Especifica la latencia de conexión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents se define como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





