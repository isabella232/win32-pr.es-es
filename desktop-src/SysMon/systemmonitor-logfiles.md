---
title: Propiedad SystemMonitor.LogFiles
description: Colección de uno o varios archivos de registro que se usarán como origen de los valores de contador mostrados en el Monitor de sistema.
ms.assetid: 6e9e7205-3516-404d-b67d-777e484900da
keywords:
- Propiedad SysMon de LogFiles
- Propiedad SysMon de LogFiles, objeto SystemMonitor
- Objeto SystemMonitor SysMon, propiedad LogFiles
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
ms.openlocfilehash: bed0ea39809d3dfe40ebcedf2fbf2105833af836c12b95ffdfe442d3956d52a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882185"
---
# <a name="systemmonitorlogfiles-property"></a>Propiedad SystemMonitor.LogFiles

Colección de uno o varios archivos de registro que se usarán como origen de los valores de contador mostrados en el Monitor de sistema.

## <a name="syntax"></a>Syntax


```VB
Property LogFiles As ILogFiles
```



## <a name="property-value"></a>Valor de propiedad

Colección de [**objetos LogFileItem**](logfileitem.md) que especifican los archivos de registro utilizados como origen de datos para el gráfico.

## <a name="remarks"></a>Comentarios

Para agregar o quitar un archivo de registro de la colección de archivos de registro, el valor de [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) no debe establecerse en sysmonLogFiles.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Systemmonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md)
</dt> <dt>

[**SystemMonitor.LogViewStart**](systemmonitor-logviewstart.md)
</dt> <dt>

[**SystemMonitor.LogViewStop**](systemmonitor-logviewstop.md)
</dt> <dt>

[**SystemMonitor.SqlLogSetName**](systemmonitor-sqllogsetname.md)
</dt> </dl>

 

 





