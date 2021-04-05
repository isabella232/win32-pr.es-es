---
title: Propiedad SqlLogSetName de SystemMonitor
description: Recupera o establece el nombre descriptivo del conjunto de registros.
ms.assetid: a4593743-6b70-4f70-8e91-3324a808d97b
keywords:
- Propiedad SqlLogSetName SysMon
- Propiedad SqlLogSetName SysMon, interfaz SystemMonitor
- Interfaz SystemMonitor SysMon, propiedad SqlLogSetName
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078827"
---
# <a name="systemmonitorsqllogsetname-property"></a>SystemMonitor:: SqlLogSetName (propiedad)

Recupera o establece el nombre descriptivo del conjunto de registros.

## <a name="syntax"></a>Sintaxis


```VB
Property SqlLogSetName As String
```



## <a name="property-value"></a>Valor de propiedad

Nombre descriptivo del conjunto de registros, que corresponde a un único archivo de registro que contiene datos binarios o de texto en la base de datos SQL.

## <a name="remarks"></a>Observaciones

**Antes de Windows Vista:** No se puede modificar esta propiedad si el valor de [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) se establece en sysmonSqlLog.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor.SqlDsnName**](systemmonitor-sqllogsetname.md)
</dt> </dl>

 

 





