---
title: Método GetDataAt
description: Recupera el valor del contador especificado de un punto concreto del gráfico.
ms.assetid: e8484301-4575-41ee-9c6d-a454eca0e82d
keywords:
- Método GetDataAt SysMon
- Método GetDataAt SysMon, objeto de contraelemento
- Objeto de contraelemento SysMon, método GetDataAt
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
ms.openlocfilehash: 354d8242e6cb765980878a7783805416bb1a1009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534306"
---
# <a name="counteritemgetdataat-method"></a>Método GetDataAt

Recupera el valor del contador especificado de un punto concreto del gráfico.

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

*Índice* \[ de de\]
</dt> <dd>

Índice de base cero del punto del gráfico cuyo valor se desea recuperar. Los valores válidos van de 0 a ([**SystemMonitor. DataPointCount**](systemmonitor-datapointcount.md) -1).

</dd> <dt>

*qué* \[ de\]
</dt> <dd>

Tipo de valor de contador que se va a recuperar, por ejemplo, el valor medio del contador tal y como se muestra en la ventana del gráfico. Para obtener los valores posibles, vea [**SysmonDataType**](/windows/win32/api/isysmon/ne-isysmon-sysmondatatype).

</dd> <dt>

*variante* \[ enuncia\]
</dt> <dd>

Valor del contador que se recuperó.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Use este método solo si

-   [**SystemMonitor. DisplayType**](systemmonitor-displaytype.md) está establecido en sysmonLineGraph
-   [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) está establecido en SysmonLogFiles o sysmonSqlLog

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento de**](counteritem.md)
</dt> <dt>

[**Elemento de GetStatistics**](counteritem-getstatistics.md)
</dt> <dt>

[**Peritem. GetValue**](counteritem-getvalue.md)
</dt> </dl>

 

 





