---
title: Método CounterItem.GetStatistics
description: Recupera los valores promedio, máximo y mínimo del contador.
ms.assetid: fb55d68b-1dbe-48b1-88c8-51f33048ec24
keywords:
- Método SysMon de GetStatistics
- Método GetStatistics SysMon , clase CounterItem
- Clase CounterItem SysMon, método GetStatistics
topic_type:
- apiref
api_name:
- CounterItem.GetStatistics
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c993ed8b9bb39a4d8bb3ff18663f2d884ece156
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068885"
---
# <a name="counteritemgetstatistics-method"></a>Método CounterItem.GetStatistics

Recupera los valores promedio, máximo y mínimo del contador.

## <a name="syntax"></a>Sintaxis


```VB
CounterItem.GetStatistics( _
  ByRef max As Double, _
  ByRef min As Double, _
  ByRef average As Double, _
  ByRef status As Long _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*max* \[ out\]
</dt> <dd>

Valor máximo del contador.

</dd> <dt>

*min* \[ out\]
</dt> <dd>

Valor mínimo del contador.

</dd> <dt>

*average* \[ out\]
</dt> <dd>

Valor medio del contador.

</dd> <dt>

*status* \[ out\]
</dt> <dd>

Indica si los valores son válidos.



| Value                                                                                              | Significado                              |
|----------------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>0</dt> </dl>                       | Los valores son válidos.<br/>     |
| <dl> <dt>0xC0000BBA (3221228474)</dt> </dl> | Los valores no son válidos.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Solo se usan los valores de contador que están visibles en la ventana del gráfico para calcular los valores estadísticos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CounterItem**](counteritem.md)
</dt> <dt>

[**CounterItem.GetDataAt**](counteritem-getdataat.md)
</dt> <dt>

[**CounterItem.GetValue**](counteritem-getvalue.md)
</dt> </dl>

 

 





