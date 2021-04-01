---
title: Counters. Remove (método)
description: Quita una instancia de un objeto de la colección.
ms.assetid: 88e5907a-8c8f-4a24-9c5d-0c592f61dac0
keywords:
- Quitar método SysMon
- Remove (método) SysMon, counters (clase)
- Counters (clase) SysMon, Remove (método)
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996261"
---
# <a name="countersremove-method"></a>Counters. Remove (método)

Quita una instancia de un [**objeto**](counteritem.md) de la colección.

## <a name="syntax"></a>Sintaxis


```VB
Counters.Remove( _
  ByVal index As Object _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Índice* \[ de de\]
</dt> <dd>

Índice del objeto de [**elemento**](counteritem.md) que se va a quitar de la colección. El índice está basado en uno.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="exceptions"></a>Excepciones



| Tipo de excepción                                  | Condición                                                      |
|-------------------------------------------------|----------------------------------------------------------------|
| **System. Runtime. InteropServices. COMException** | El índice especificado no es válido. El valor de Err. number es???. |



 

## <a name="remarks"></a>Observaciones

Para quitar todos los contadores de la colección, puede llamar a [**SystemMonitor. Reset**](systemmonitor-reset.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Counters**](counters.md)
</dt> <dt>

[**SystemMonitor. Reset**](systemmonitor-reset.md)
</dt> </dl>

 

 





