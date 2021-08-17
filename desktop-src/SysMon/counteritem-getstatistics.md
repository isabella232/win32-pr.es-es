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
ms.openlocfilehash: bea1be162d68bb02db4842a7140effe653231dcc5105c4bea3b557abb02beab0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118883781"
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



| Valor                                                                                              | Significado                              |
|----------------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>0</dt> </dl>                       | Los valores son válidos.<br/>     |
| <dl> <dt>0xC0000BBA (3221228474)</dt> </dl> | Los valores no son válidos.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Solo se usan los valores de contador que están visibles en la ventana del gráfico para calcular los valores estadísticos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

 





