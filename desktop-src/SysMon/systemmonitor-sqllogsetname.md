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
ms.openlocfilehash: ce06e396b6a90a46de88d915a0191258da723bef31dfe82f67a20c9507b2939d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118881312"
---
# <a name="systemmonitorsqllogsetname-property"></a>Propiedad SystemMonitor::SqlLogSetName

Recupera o establece el nombre descriptivo del conjunto de registros.

## <a name="syntax"></a>Syntax


```VB
Property SqlLogSetName As String
```



## <a name="property-value"></a>Valor de propiedad

Nombre descriptivo del conjunto de registros, que corresponde a un único archivo de registro que contiene datos binarios o de texto en la base SQL datos.

## <a name="remarks"></a>Comentarios

**Antes de Windows Vista:** No se puede modificar esta propiedad si el valor [**de SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) está establecido en sysmonSqlLog.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

 





