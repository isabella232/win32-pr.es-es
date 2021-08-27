---
title: Método LogFiles.Add
description: Agrega un archivo de registro a la colección.
ms.assetid: f6b671ea-9620-49a7-8b0c-0c8e1d9819b0
keywords:
- Adición del método SysMon
- Agregar método SysMon , clase LogFiles
- Clase LogFiles SysMon , Método Add
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
ms.openlocfilehash: af01c5c7a1bbe16826457d7e1f8700df01876827c522a36db41f6c3843101d6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882340"
---
# <a name="logfilesadd-method"></a>Método LogFiles.Add

Agrega un archivo de registro a la colección.

## <a name="syntax"></a>Sintaxis


```VB
LogFiles.Add( _
  ByVal pathname As String _
) As LogFileItem
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pathname* \[ En\]
</dt> <dd>

Ruta de acceso al archivo de registro. Puede especificar la ruta de acceso como una ruta de acceso absoluta, relativa o UNC. La extensión de nombre de archivo de registro debe ser .csv, .tsv o .blg.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Debe usar la herramienta Logman.exe o el complemento MMC Perfmon.msc para generar los archivos de registro que agregue a esta colección. Para Perfmon.msc, los registros de contador se encuentran en **Registros y alertas de rendimiento**. Para obtener más información sobre Logman.exe o Perfmon.msc, busque Logman o Using Performance, respectivamente, **en el Centro de ayuda y soporte técnico**.

**Antes de Windows Vista:** No se pueden agregar [](systemmonitor-logfiles.md) archivos de registro a la colección de archivos de registro si el valor de [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) está establecido [**enDataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants). En primer lugar, establezca **SystemMonitor.DataSourceType** en **DataSourceTypeConstants.sysmonNullDataSource,** agregue los archivos de registro y los contadores y, a continuación, establezca **SystemMonitor.DataSourceType** en **DataSourceTypeConstants.sysmonLogFiles**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[LogFiles](logfiles.md)
</dt> <dt>

[**LogFileItem**](logfileitem.md)
</dt> <dt>

[**LogFiles**](systemmonitor-logfiles.md)
</dt> </dl>

 

 





