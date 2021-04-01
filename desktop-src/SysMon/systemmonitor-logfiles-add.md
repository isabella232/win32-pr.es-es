---
title: LogFiles. Add (método)
description: Agrega un archivo de registro a la colección.
ms.assetid: f6b671ea-9620-49a7-8b0c-0c8e1d9819b0
keywords:
- Agregar método SysMon
- Agregar método SysMon, logfiles (clase)
- Logfiles (clase) SysMon, Add (método)
topic_type:
- apiref
api_name:
- LogFiles.Add
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f690670606cd7ee307ba945fc2daabe92953e81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150335"
---
# <a name="logfilesadd-method"></a>LogFiles. Add (método)

Agrega un archivo de registro a la colección.

## <a name="syntax"></a>Sintaxis


```VB
LogFiles.Add( _
  ByVal pathname As String _
) As LogFileItem
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*nombreruta* \[ de\]
</dt> <dd>

Ruta de acceso al archivo de registro. Puede especificar la ruta de acceso como una ruta de acceso absoluta, relativa o UNC. La extensión de nombre de archivo de registro debe ser. csv,. TSV o. BLG.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Debe usar la herramienta Logman.exe o el complemento MMC Perfmon. msc para generar los archivos de registro que se agregan a esta colección. En el caso de Perfmon. msc, los registros de contador se encuentran en **registros y alertas de rendimiento**. Para obtener información detallada sobre el uso de Logman.exe o Perfmon. msc, busque Logman o use performance, respectivamente, en el **centro de ayuda y soporte técnico**.

**Antes de Windows Vista:** No puede Agregar archivos de registro a la [**colección de archivos de registro**](systemmonitor-logfiles.md) si el valor de [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) está establecido en [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants). En primer lugar, establezca **SystemMonitor. DataSourceType** en **DataSourceTypeConstants.sysmonNullDataSource**, agregue los archivos de registro y los contadores y, a continuación, establezca **SystemMonitor. DataSourceType** en **DataSourceTypeConstants.sysmonLogFiles**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[LogFiles](logfiles.md)
</dt> <dt>

[**LogFileItem**](logfileitem.md)
</dt> <dt>

[**LogFiles**](systemmonitor-logfiles.md)
</dt> </dl>

 

 





