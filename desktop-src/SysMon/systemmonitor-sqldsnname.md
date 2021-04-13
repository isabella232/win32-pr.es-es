---
title: Propiedad SqlDsnName de SystemMonitor
description: Recupera o establece el nombre del origen de datos ODBC (DSN).
ms.assetid: 7906204a-a208-42c7-855b-c29689b4d36a
keywords:
- Propiedad SqlDsnName SysMon
- Propiedad SqlDsnName SysMon, interfaz SystemMonitor
- Interfaz SystemMonitor SysMon, propiedad SqlDsnName
topic_type:
- apiref
api_name:
- SystemMonitor.SqlDsnName
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 666b10ad91956adf7148e54b68f2b6db98e9a5b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421897"
---
# <a name="systemmonitorsqldsnname-property"></a>SystemMonitor:: SqlDsnName (propiedad)

Recupera o establece el nombre del origen de datos ODBC (DSN).

## <a name="syntax"></a>Sintaxis


```VB
Property SqlDsnName As String
```



## <a name="property-value"></a>Valor de propiedad

Nombre del origen de datos ODBC que apunta a una base de datos que contiene las tablas correctas de Perfmon. El formato es SQL: DSN.

## <a name="remarks"></a>Observaciones

Debe usar el complemento de MMC Perfmon. msc para generar el archivo de registro de SQL. Los registros de contador se encuentran en **registros y alertas de rendimiento**. Para especificar un registro de SQL, haga clic con el botón secundario en el archivo de registro que creó y seleccione **propiedades** en el menú. En la página de propiedades **archivos de registro** , seleccione **SQL Database** en el cuadro de lista desplegable tipo de **archivo de registro** .

**Antes de Windows Vista:** No se puede modificar esta propiedad si el valor de [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) está establecido en [**DataSourceTypeConstants.sysmonSqlLog**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants). En primer lugar, debe especificar el nombre y, a continuación, establecer **SystemMonitor. DataSourceType** en **DataSourceTypeConstants.sysmonSqlLog**.

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

[**SystemMonitor.SqlLogSetName**](systemmonitor-sqllogsetname.md)
</dt> </dl>

 

 





