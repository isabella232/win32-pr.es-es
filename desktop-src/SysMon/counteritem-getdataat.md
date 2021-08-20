---
title: Método CounterItem.GetDataAt
description: Recupera el valor de contador especificado de un punto específico del gráfico.
ms.assetid: e8484301-4575-41ee-9c6d-a454eca0e82d
keywords:
- Método GetDataAt SysMon
- Método GetDataAt SysMon , objeto CounterItem
- Objeto CounterItem SysMon, método GetDataAt
topic_type:
- apiref
api_name:
- CounterItem.GetDataAt
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a02ec2b98fa75df138f8cd315c3464192e7714dc737c2b360e721085c8eebd77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117957160"
---
# <a name="counteritemgetdataat-method"></a>Método CounterItem.GetDataAt

Recupera el valor de contador especificado de un punto específico del gráfico.

## <a name="syntax"></a>Sintaxis


```VB
CounterItem.GetDataAt( _
  ByVal index As Long, _
  ByVal which As SysmonDataType, _
  ByRef variant As Object _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*index* \[ En\]
</dt> <dd>

Índice de base cero del punto de gráfico cuyo valor desea recuperar. Los valores válidos van de 0 a ([**SystemMonitor.DataPointCount**](systemmonitor-datapointcount.md) - 1).

</dd> <dt>

*que* \[ En\]
</dt> <dd>

Tipo de valor de contador que se recuperará, por ejemplo, el valor medio del contador como se muestra en la ventana del gráfico. Para obtener los valores posibles, [**vea SysmonDataType**](/windows/win32/api/isysmon/ne-isysmon-sysmondatatype).

</dd> <dt>

*variant* \[ out\]
</dt> <dd>

Valor de contador que se recuperó.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Use este método solo si

-   [**SystemMonitor.DisplayType**](systemmonitor-displaytype.md) se establece en sysmonLineGraph
-   [**SystemMonitor.DataSourceType se**](systemmonitor-datasourcetype.md) establece en sysmonLogFiles o sysmonSqlLog.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CounterItem**](counteritem.md)
</dt> <dt>

[**CounterItem.GetStatistics**](counteritem-getstatistics.md)
</dt> <dt>

[**CounterItem.GetValue**](counteritem-getvalue.md)
</dt> </dl>

 

 





