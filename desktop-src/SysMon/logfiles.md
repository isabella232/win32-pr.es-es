---
title: Objeto LogFiles (Isysmon.h)
description: Utilice esta clase para administrar una colección de uno o varios archivos de registro que contengan datos del contador de rendimiento. Para recuperar este objeto, llame a SystemMonitor. logfiles.
ms.assetid: 1af475c5-ed0c-49b4-a558-13eb8758a986
keywords:
- LogFiles (objeto) SysMon
- LogFiles (objeto) SysMon, descrito
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104488944"
---
# <a name="logfiles-object"></a>LogFiles (objeto)

Utilice esta clase para administrar una colección de uno o varios archivos de registro que contengan datos del contador de rendimiento.

Para recuperar este objeto, llame a [**SystemMonitor. logfiles**](systemmonitor-logfiles.md).

## <a name="members"></a>Miembros

El objeto **logfiles** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto **logfiles** tiene estos métodos.



| Método                                          | Descripción                                                                           |
|:------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**Agréguela**](systemmonitor-logfiles-add.md)       | Agrega una instancia de [**LogFileItem**](logfileitem.md) a la colección.<br/>      |
| [**Retirar**](systemmonitor-logfiles-remove.md) | Quita una instancia de [**LogFileItem**](logfileitem.md) de la colección.<br/> |



 

### <a name="properties"></a>Propiedades

El objeto **logfiles** tiene estas propiedades.



| Propiedad                                                 | Descripción                                                                                         |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [**Contabiliza**](systemmonitor-logfiles-count.md)<br/> | Recupera el número de instancias de [**LogFileItem**](logfileitem.md) de la colección.<br/>  |
| [**Elemento**](systemmonitor-logfiles-item.md)<br/>   | Recupera la instancia de [**LogFileItem**](logfileitem.md) especificada de la colección.<br/> |



 

## <a name="remarks"></a>Observaciones

Para que SYSMON muestre los contadores de rendimiento de un archivo de registro, establezca [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) en [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants). Después de agregar los archivos de registro a la colección, utilice la colección [**counters**](counters.md) para especificar los datos de los contadores que desea leer de los archivos de registro. Tenga en cuenta que si **SystemMonitor. DataSourceType** está establecido en **DataSourceTypeConstants.sysmonLogFiles**, SYSMON volverá a muestrear los archivos de registro cada vez que agregue un archivo de registro o un contador a sus respectivas colecciones.

**Antes de Windows Vista:** No puede Agregar archivos de registro a la [**colección de archivos de registro**](systemmonitor-logfiles.md) si el valor de [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) está establecido en [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants). En primer lugar, establezca **SystemMonitor. DataSourceType** en **DataSourceTypeConstants.sysmonNullDataSource**, agregue los archivos de registro y los contadores y, a continuación, establezca **SystemMonitor. DataSourceType** en **DataSourceTypeConstants.sysmonLogFiles**.

Las propiedades [**SystemMonitor. LogViewStart**](systemmonitor-logviewstart.md) y [**SystemMonitor. LogViewStop**](systemmonitor-logviewstop.md) especifican el intervalo de valores muestreados de los archivos de registro a Graph. SYSMON los gráficos solo representan los datos del archivo de registro (la vista de gráfico no se desplaza como lo hace al representar gráficamente la actividad actual del equipo). Si los datos muestreados superan lo que se puede mostrar en una sola vista de gráfico, SYSMON comprime los datos muestreados (cada punto en el gráfico representa el promedio de varios valores muestreados) para ajustar todos los datos muestreados de los archivos de registro del gráfico.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Isysmon. h</dt> </dl>  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



 

 





