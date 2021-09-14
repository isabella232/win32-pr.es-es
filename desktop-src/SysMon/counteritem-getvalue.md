---
title: Método CounterItem.GetValue
description: Recupera el último valor del contador.
ms.assetid: cf50d878-a119-42b0-bc59-b0e37ed15321
keywords:
- Método GetValue SysMon
- Método GetValue SysMon , clase CounterItem
- Clase CounterItem SysMon, método GetValue
topic_type:
- apiref
api_name:
- CounterItem.GetValue
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94e40950ce4a8bf24a6a4301db133779b34ce4ec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068883"
---
# <a name="counteritemgetvalue-method"></a>Método CounterItem.GetValue

Recupera el último valor del contador.

## <a name="syntax"></a>Sintaxis


```VB
CounterItem.GetValue( _
  ByRef value As Double, _
  ByRef status As Long _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Último valor muestreado del contador.

</dd> <dt>

*status* \[ out\]
</dt> <dd>

Indica si el valor es válido.



| Value                                                                                              | Significado                            |
|----------------------------------------------------------------------------------------------------|------------------------------------|
| <dl> <dt>0</dt> </dl>                       | El valor es válido.<br/>     |
| <dl> <dt>0xC0000BBA (3221228474)</dt> </dl> | El valor no es válido.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si el origen de los datos del contador es de un archivo de registro, el valor es el último valor de contador del archivo de registro.

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

[**CounterItem.GetStatistics**](counteritem-getstatistics.md)
</dt> <dt>

[**CounterItem.Value**](counteritem-value.md)
</dt> </dl>

 

 





