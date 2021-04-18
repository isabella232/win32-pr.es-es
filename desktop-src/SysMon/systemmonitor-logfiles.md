---
title: Propiedad SystemMonitor. LogFiles
description: Colección de uno o más archivos de registro que se van a utilizar como origen de los valores de contador mostrados en el monitor de sistema.
ms.assetid: 6e9e7205-3516-404d-b67d-777e484900da
keywords:
- Propiedad logfiles SysMon
- Propiedad logfiles SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, propiedad logfiles
topic_type:
- apiref
api_name:
- SystemMonitor.LogFiles
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8127433319290b44498b272834923784b714052
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665985"
---
# <a name="systemmonitorlogfiles-property"></a>Propiedad SystemMonitor. LogFiles

Colección de uno o más archivos de registro que se van a utilizar como origen de los valores de contador mostrados en el monitor de sistema.

## <a name="syntax"></a>Sintaxis


```VB
Property LogFiles As ILogFiles
```



## <a name="property-value"></a>Valor de propiedad

Colección de objetos [**LogFileItem**](logfileitem.md) que especifican los archivos de registro que se usan como origen de datos para el gráfico.

## <a name="remarks"></a>Observaciones

Para agregar o quitar un archivo de registro de la colección de archivos de registro, el valor de [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) no debe estar establecido en sysmonLogFiles.

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

[**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md)
</dt> <dt>

[**SystemMonitor.LogViewStart**](systemmonitor-logviewstart.md)
</dt> <dt>

[**SystemMonitor.LogViewStop**](systemmonitor-logviewstop.md)
</dt> <dt>

[**SystemMonitor.SqlLogSetName**](systemmonitor-sqllogsetname.md)
</dt> </dl>

 

 





