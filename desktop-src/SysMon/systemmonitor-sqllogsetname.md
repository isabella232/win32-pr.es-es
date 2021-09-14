---
title: Propiedad SystemMonitor SqlLogSetName
description: Recupera o establece el nombre descriptivo del conjunto de registros.
ms.assetid: a4593743-6b70-4f70-8e91-3324a808d97b
keywords:
- Propiedad SysMon de SqlLogSetName
- Propiedad SqlLogSetName SysMon, interfaz SystemMonitor
- SystemMonitor interface SysMon , Propiedad SqlLogSetName
topic_type:
- apiref
api_name:
- SystemMonitor.SqlLogSetName
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be20ccc561eb3e9292b4a95dcc654ed7bac00ba7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127243860"
---
# <a name="systemmonitorsqllogsetname-property"></a>Propiedad SystemMonitor::SqlLogSetName

Recupera o establece el nombre descriptivo del conjunto de registros.

## <a name="syntax"></a>Sintaxis


```VB
Property SqlLogSetName As String
```



## <a name="property-value"></a>Valor de propiedad

Nombre descriptivo del conjunto de registros, que corresponde a un único archivo de registro que contiene datos binarios o de texto en la base SQL datos.

## <a name="remarks"></a>Observaciones

**Antes de Windows Vista:** No se puede modificar esta propiedad si el valor [**de SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) está establecido en sysmonSqlLog.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Systemmonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor.SqlDsnName**](systemmonitor-sqllogsetname.md)
</dt> </dl>

 

 





