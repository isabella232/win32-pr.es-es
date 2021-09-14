---
title: Objeto LogFiles (Isysmon.h)
description: Use esta clase para administrar una colección de uno o varios archivos de registro que contienen datos de contador de rendimiento. Para recuperar este objeto, llame a SystemMonitor.LogFiles.
ms.assetid: 1af475c5-ed0c-49b4-a558-13eb8758a986
keywords:
- Objeto LogFiles SysMon
- Objeto LogFiles SysMon , descrito
topic_type:
- apiref
api_name:
- LogFiles
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ab30de5c371c012e1320950e4a491021bb0b15c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068857"
---
# <a name="logfiles-object"></a>Objeto LogFiles

Use esta clase para administrar una colección de uno o varios archivos de registro que contienen datos de contador de rendimiento.

Para recuperar este objeto, llame [**a SystemMonitor.LogFiles.**](systemmonitor-logfiles.md)

## <a name="members"></a>Members

El **objeto LogFiles** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto LogFiles** tiene estos métodos.



| Método                                          | Descripción                                                                           |
|:------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**Añadir**](systemmonitor-logfiles-add.md)       | Agrega una [**instancia de LogFileItem**](logfileitem.md) a la colección.<br/>      |
| [**Remove**](systemmonitor-logfiles-remove.md) | Quita una instancia [**de LogFileItem**](logfileitem.md) de la colección.<br/> |



 

### <a name="properties"></a>Propiedades

El **objeto LogFiles** tiene estas propiedades.



| Propiedad                                                 | Descripción                                                                                         |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [**Contar**](systemmonitor-logfiles-count.md)<br/> | Recupera el número de [**instancias de LogFileItem**](logfileitem.md) de la colección.<br/>  |
| [**Elemento**](systemmonitor-logfiles-item.md)<br/>   | Recupera la instancia de [**LogFileItem especificada**](logfileitem.md) de la colección.<br/> |



 

## <a name="remarks"></a>Observaciones

Para que SYSMON muestre los contadores de rendimiento de un archivo de registro, establezca [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) en [**DataSourceTypeConstants.sysmonLogFiles.**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants) Después de agregar los archivos de registro a la colección, use la colección [**Contadores**](counters.md) para especificar los datos de contadores que desea leer de los archivos de registro. Tenga en cuenta que si **SystemMonitor.DataSourceType** está establecido en **DataSourceTypeConstants.sysmonLogFiles,** SYSMON volverá a muestrear los archivos de registro cada vez que agregue un archivo de registro o un contador a sus respectivas colecciones.

**Antes de Windows Vista:** No se pueden agregar [](systemmonitor-logfiles.md) archivos de registro a la colección de archivos de registro si el valor de [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) está establecido en [**DataSourceTypeConstants.sysmonLogFiles.**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants) En primer lugar, establezca **SystemMonitor.DataSourceType** en **DataSourceTypeConstants.sysmonNullDataSource,** agregue los archivos de registro y los contadores y, a continuación, establezca **SystemMonitor.DataSourceType** en **DataSourceTypeConstants.sysmonLogFiles.**

Las [**propiedades SystemMonitor.LogViewStart**](systemmonitor-logviewstart.md) y [**SystemMonitor.LogViewStop**](systemmonitor-logviewstop.md) especifican el intervalo de valores muestreados de los archivos de registro al grafo. SYSMON solo representa una vista de los datos del archivo de registro (la vista de gráfico no se desplaza como hace al representar la actividad actual del equipo). Si los datos muestreados superan lo que se puede mostrar en una sola vista de gráfico, SYSMON comprime los datos muestreados (cada punto grafo representa el promedio de varios valores muestreados) para ajustar todos los datos muestreados de los archivos de registro en el gráfico.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Isysmon.h</dt> </dl>  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



 

 





