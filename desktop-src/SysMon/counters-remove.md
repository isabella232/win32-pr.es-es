---
title: Método Counters.Remove
description: Quita una instancia counterItem de la colección.
ms.assetid: 88e5907a-8c8f-4a24-9c5d-0c592f61dac0
keywords:
- Método Remove SysMon
- Método Remove SysMon , Clase Counters
- Método SysMon , Remove de la clase Counters
topic_type:
- apiref
api_name:
- Counters.Remove
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa82a1a988be3554c265c097ba2a582035547391
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068865"
---
# <a name="countersremove-method"></a>Método Counters.Remove

Quita una [**instancia counterItem**](counteritem.md) de la colección.

## <a name="syntax"></a>Sintaxis


```VB
Counters.Remove( _
  ByVal index As Object _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*index* \[ En\]
</dt> <dd>

Índice del objeto [**CounterItem**](counteritem.md) que se quitará de la colección. El índice se basa en uno.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="exceptions"></a>Excepciones



| Tipo de excepción                                  | Condición                                                      |
|-------------------------------------------------|----------------------------------------------------------------|
| **System.Runtime.InteropServices.COMException** | El índice especificado no es válido. El valor Err.Number es ???. |



 

## <a name="remarks"></a>Observaciones

Para quitar todos los contadores de la colección, puede llamar a [**SystemMonitor.Reset**](systemmonitor-reset.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Counters**](counters.md)
</dt> <dt>

[**SystemMonitor.Reset**](systemmonitor-reset.md)
</dt> </dl>

 

 





