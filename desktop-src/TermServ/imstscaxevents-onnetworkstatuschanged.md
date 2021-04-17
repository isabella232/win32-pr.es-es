---
title: IMsTscAxEvents OnNetworkStatusChanged, método
description: Se llama cuando el estado de la red ha cambiado. | IMsTscAxEvents OnNetworkStatusChanged, método
ms.assetid: 177A410E-2449-4FC7-8DE5-21F83A6DD028
ms.tgt_platform: multiple
keywords:
- Método OnNetworkStatusChanged Servicios de Escritorio remoto
- Método OnNetworkStatusChanged Servicios de Escritorio remoto, interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto, método OnNetworkStatusChanged
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
ms.openlocfilehash: c2b9bdcd7774493fcc54e1390ad199a6a56a7c51
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105678675"
---
# <a name="imstscaxeventsonnetworkstatuschanged-method"></a>IMsTscAxEvents:: OnNetworkStatusChanged (método)

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

*qualityLevel* \[ de\]
</dt> <dd>

Especifica la nueva velocidad de conexión. Será uno de los valores siguientes.

<dt>

1
</dt> <dd>

Menos de 512 kilobytes por segundo (KBps).

</dd> <dt>

2
</dt> <dd>

de 512 a 1.999 KBps.

</dd> <dt>

3
</dt> <dd>

de 2.000 a 9.999 KBps.

</dd> <dt>

4
</dt> <dd>

Mayor o igual que 10.000 KBps.

</dd> </dl> </dd> <dt>

*ancho de banda* \[ de\]
</dt> <dd>

Especifica el ancho de banda de conexión.

</dd> <dt>

*RTT* \[ de\]
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

 

 





