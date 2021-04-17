---
description: El método SendNMEvent envía eventos a Instrumental de administración de Windows (WMI).
ms.assetid: 85c33a71-72aa-4b0a-8e8b-3a220a080bb2
title: 'IMonitorEventer:: SendNMEvent (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer.SendNMEvent
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 3286fca4d5b852d4562c13446699c1a6b40f3efe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677518"
---
# <a name="imonitoreventersendnmevent-method"></a>IMonitorEventer:: SendNMEvent (método)

El método **SendNMEvent** envía eventos a instrumental de administración de Windows (WMI).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SendNMEvent(
  [in] PNMEVENTDATA pNMEventData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pNMEventData* \[ de\]
</dt> <dd>

Puntero al evento enviado a WMI.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, el valor devuelto es S \_ OK.

Si el método no se realiza correctamente, el valor devuelto es \_ NMERR \_ de \_ memoria insuficiente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




