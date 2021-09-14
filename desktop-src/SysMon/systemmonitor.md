---
title: Objeto SystemMonitor (Isysmon.h)
description: Esta clase contiene los métodos y propiedades utilizados para configurar el control Monitor de sistema.
ms.assetid: 5a6195ee-ed89-4f5d-85dd-88cf4a9b5155
keywords:
- Objeto SystemMonitor SysMon
- Objeto SystemMonitor SysMon , descrito
topic_type:
- apiref
api_name:
- SystemMonitor
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 297f0e3e67134f911932aa7784396c244dc79f42
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127243836"
---
# <a name="systemmonitor-object"></a>Objeto SystemMonitor

Esta clase contiene los métodos y propiedades utilizados para configurar el control Monitor de sistema.

## <a name="members"></a>Members

El **objeto SystemMonitor** tiene estos tipos de miembros:

-   [Eventos](#events)
-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="events"></a>Eventos

El **objeto SystemMonitor** tiene estos eventos.



| Evento                                                         | Descripción                                                                                                                 |
|:--------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**OnCounter Agregado**](systemmonitor-oncounteradded.md)        | Le notifica cuándo se agrega un contador a la [**colección Counters.**](counters.md)<br/>                             |
| [**OnCounterDeleted**](-systemmonitor-oncounterdeleted.md)   | Le notifica antes de que se elimine un contador de [**la colección Contadores.**](counters.md)<br/>                       |
| [**OnCounterSelected**](-systemmonitor-oncounterselected.md) | Le notifica cuando se selecciona un contador.<br/>                                                                         |
| [**OnDblClick**](-systemmonitor-ondblclick.md)               | Le notifica cuando un usuario hace doble clic en la línea del gráfico, la barra del histograma o el elemento de informe con el botón izquierdo del mouse.<br/> |
| [**OnSampleCollected**](-systemmonitor-onsamplecollected.md) | Le notifica cuándo se han recopilado los valores de ejemplo de los contadores.<br/>                                            |



 

### <a name="methods"></a>Métodos

El **objeto SystemMonitor** tiene estos métodos.



| Método                                                       | Descripción                                                                                                                                                              |
|:-------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BatchLocking**](systemmonitor-batchinglock.md)           | Bloquea el Monitor de sistema para evitar que muestree los datos del contador o del archivo de registro recién agregados.<br/>                                                   |
| [**BrowseCounters**](systemmonitor-browsecounters.md)       | Muestra el **cuadro de diálogo Agregar** contador.<br/>                                                                                                                      |
| [**ClearData**](systemmonitor-cleardata.md)                 | Borra todos los campos de datos del control .<br/>                                                                                                                        |
| [**CollectSample**](systemmonitor-collectsample.md)         | Muestrea un valor para cada contador del **objeto de colección Counters.**<br/>                                                                                       |
| [**Copiar**](systemmonitor-copy.md)                           | Copia la configuración de propiedades del control, la lista de contadores y los datos del contador en el Portapapeles como un objeto HTML.<br/>                                                |
| [**DisplayProperties**](systemmonitor-displayproperties.md) | Muestra el cuadro **Graph propiedades.**<br/>                                                                                                                 |
| [**GetLogViewRange**](systemmonitor-getlogviewrange.md)     | Recupera la fecha de inicio utilizada para recuperar los valores de contador de los archivos de registro.<br/>                                                                               |
| [**LoadSettings**](systemmonitor-loadsettings.md)           | Agrega los contadores del archivo de plantilla HTML al Monitor de sistema.<br/>                                                                                            |
| [**Pegar**](systemmonitor-paste.md)                         | Anexa la lista de contadores que se copiaron en el Portapapeles a la colección actual de contadores. <br/>                                                        |
| [**Registro**](systemmonitor-relog.md)                         | Vuelve a cargar los datos del contador en un nuevo archivo. También puede usar este método para especificar un nuevo tipo de archivo y reducir el número de muestras contenidas en el archivo de registro.<br/> |
| [**Reset**](systemmonitor-reset.md)                         | Quita todos los [**objetos CounterItem**](counteritem.md) del **objeto de colección Counters.**<br/>                                                               |
| [**SaveAs**](systemmonitor-saveas.md)                       | Guarda los valores de contador de la vista de gráfico en un archivo de registro.<br/>                                                                                                     |
| [**ScaleToFit**](systemmonitor-scaletofit.md)               | Escale los valores de contador para que quepa en el gráfico.<br/>                                                                                                                     |
| [**SetLogViewRange**](systemmonitor-setlogviewrange.md)     | Establece la fecha de inicio utilizada para recuperar valores de contador de los archivos de registro.<br/>                                                                                    |
| [**UpdateGraph**](systemmonitor-updategraph.md)             | Actualiza el contenido de las ventanas del Monitor de sistema.<br/>                                                                                                         |



 

### <a name="properties"></a>Propiedades

El **objeto SystemMonitor** tiene estas propiedades.



| Propiedad                                                                                | Descripción                                                                                                                                                                                                                             |
|:----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Aspecto**](systemmonitor-appearance.md)<br/>                               | Recupera o establece la apariencia del control para incluir u omitir efectos de visualización tridimensionales.<br/>                                                                                                                        |
| [**Backcolor**](systemmonitor-backcolor.md)<br/>                                 | Recupera o establece el color de fondo del gráfico y las vistas de informe.<br/>                                                                                                                                                        |
| [**BackColorCtl**](systemmonitor-backcolorctl.md)<br/>                           | Recupera o establece el color de fondo del control.<br/>                                                                                                                                                                       |
| [**BorderStyle**](systemmonitor-borderstyle.md)<br/>                             | Recupera o establece el estilo de borde del control.<br/>                                                                                                                                                                           |
| [**ChartScroll**](systemmonitor-chartscroll.md)<br/>                             | Recupera o establece un valor que determina si el gráfico de líneas se desplaza en la vista.<br/>                                                                                                                                             |
| [**Counters**](systemmonitor-counters.md)<br/>                                   | Recupera la colección de [**objetos CounterItem.**](counteritem.md)<br/>                                                                                                                                                      |
| [**DataPointCount**](systemmonitor-datapointcount.md)<br/>                       | Recupera o establece el número de puntos de datos que se muestran en un gráfico de líneas.<br/>                                                                                                                                                       |
| [**DataSourceType**](systemmonitor-datasourcetype.md)<br/>                       | Recupera o establece el origen de los datos del contador de rendimiento.<br/>                                                                                                                                                                |
| [**Displaytype**](systemmonitor-displaytype.md)<br/>                             | Recupera o establece el tipo de gráfico utilizado para representar los datos del contador de rendimiento.<br/>                                                                                                                                              |
| [**EnableDigitGrouping**](systemmonitor-enabledigitgrouping.md)<br/>             | Recupera o establece un valor que determina si SYSMON usa la agrupación de dígitos al mostrar valores numéricos.<br/>                                                                                                                      |
| [**EnableToolTips**](systemmonitor-enabletooltips.md)<br/>                       | Recupera o establece un valor que determina si se muestra una sugerencia de herramientas cuando el mouse mantiene el puntero sobre un contador en una de las vistas del gráfico.<br/>                                                                                             |
| [**Font**](systemmonitor-font.md)<br/>                                           | Recupera o establece la fuente utilizada en el control .<br/>                                                                                                                                                                              |
| [**ForeColor**](systemmonitor-forecolor.md)<br/>                                 | Recupera o establece el color del texto que aparece en el control .<br/>                                                                                                                                                         |
| [**GraphTitle**](systemmonitor-graphtitle.md)<br/>                               | Recupera o establece el título del gráfico.<br/>                                                                                                                                                                                    |
| [**GridColor**](systemmonitor-gridcolor.md)<br/>                                 | Recupera o establece el color de las líneas de cuadrícula usadas en el gráfico.<br/>                                                                                                                                                             |
| [**Resaltar**](systemmonitor-highlight.md)<br/>                                 | Recupera o establece un valor que indica si los valores de los contadores seleccionados están resaltados en el gráfico.<br/>                                                                                                               |
| [**LogFileName**](systemmonitor-logfilename.md)<br/>                             | Obsoleto. Recupera o establece el nombre de un archivo de registro que se usará como origen de los valores de contador mostrados en el Monitor de sistema.<br/>                                                                                                   |
| [**LogFiles**](systemmonitor-logfilename.md)<br/>                                | Colección de uno o varios archivos de registro que se usarán como origen de los valores de contador mostrados en el Monitor de sistema.<br/>                                                                                                                  |
| [**LogSourceStartTime**](systemmonitor-logsourcestarttime.md)<br/>               | Recupera la marca de tiempo del valor de contador más antiguo de un contador de la colección de contadores que se registró en los archivos de registro.<br/>                                                                                           |
| [**LogSourceStopTime**](systemmonitor-logsourcestoptime.md)<br/>                 | Recupera la marca de tiempo del último valor de contador de un contador de la colección de contadores que se registró en los archivos de registro.<br/>                                                                                             |
| [**LogViewStart**](systemmonitor-logviewstart.md)<br/>                           | Recupera o establece la fecha de inicio utilizada para recuperar valores de contador de los archivos de registro.<br/>                                                                                                                                      |
| [**LogViewStop**](systemmonitor-logviewstop.md)<br/>                             | Recupera o establece la fecha de finalización utilizada para recuperar valores de contador de los archivos de registro.<br/>                                                                                                                                        |
| [**ManualUpdate**](systemmonitor-manualupdate.md)<br/>                           | Recupera o establece un valor que indica si el contenido del Monitor de sistema se actualizará manualmente o automáticamente a intervalos especificados.<br/>                                                                           |
| [**MaximumScale**](systemmonitor-maximumscale.md)<br/>                           | Recupera o establece el valor máximo del eje vertical (Y) del gráfico.<br/>                                                                                                                                                   |
| [**MinimumScale**](systemmonitor-minimumscale.md)<br/>                           | Recupera o establece el valor mínimo del eje vertical (Y) del gráfico.<br/>                                                                                                                                                   |
| [**MonitorDuplicateInstances**](systemmonitor-monitorduplicateinstances.md)<br/> | Recupera o establece un valor que determina si se pueden supervisar varias instancias de un contador.<br/>                                                                                                                          |
| [**Readonly**](systemmonitor-readonly.md)<br/>                                   | Recupera o establece un valor que determina si un usuario puede modificar los valores de propiedad del control.<br/>                                                                                                                      |
| [**ReportValueType**](systemmonitor-reportvaluetype.md)<br/>                     | Recupera o establece un valor que determina si el gráfico histograma y vistas de informe representa el último valor muestreado durante el intervalo de muestreo o un valor calculado del muestreo, como el valor promedio o mínimo del contador.<br/> |
| [**ShowHorizontalGrid**](systemmonitor-showhorizontalgrid.md)<br/>               | Recupera o establece un valor que determina si las líneas de cuadrícula horizontales se muestran en el gráfico.<br/>                                                                                                                          |
| [**ShowLegend**](systemmonitor-showlegend.md)<br/>                               | Recupera o establece un valor que determina si se muestra la leyenda.<br/>                                                                                                                                                   |
| [**ShowScaleLabels**](systemmonitor-showscalelabels.md)<br/>                     | Recupera o establece un valor que determina si las etiquetas de escala se muestran en el eje vertical del gráfico.<br/>                                                                                                          |
| [**ShowTimeAxisLabels**](systemmonitor-showtimeaxislabels.md)<br/>               | Recupera o establece un valor que determina si el eje horizontal (X) de la vista de gráfico contiene etiquetas.<br/>                                                                                                                      |
| [**ShowToolbar**](systemmonitor-showtoolbar.md)<br/>                             | Recupera o establece un valor que determina si la barra de herramientas se muestra en el control .<br/>                                                                                                                                   |
| [**ShowValueBar**](systemmonitor-showvaluebar.md)<br/>                           | Recupera o establece un valor que determina si la barra de valores (el conjunto de valores estadísticos debajo del gráfico) se muestra en el control .<br/>                                                                                 |
| [**ShowVerticalGrid**](systemmonitor-showverticalgrid.md)<br/>                   | Recupera o establece un valor que determina si las líneas de cuadrícula verticales se muestran en el gráfico.<br/>                                                                                                                            |
| [**SqlDsnName**](systemmonitor-sqldsnname.md)<br/>                               | Recupera o establece el nombre del origen de datos ODBC.<br/>                                                                                                                                                                                 |
| [**SqlLogSetName**](systemmonitor-sqllogsetname.md)<br/>                         | Recupera o establece el nombre descriptivo del conjunto de registros.<br/>                                                                                                                                                                          |
| [**TimeBarColor**](systemmonitor-timebarcolor.md)<br/>                           | Recupera o establece el color de la barra de tiempo (la barra vertical que se mueve a través de la ventana del gráfico para indicar el paso de cada intervalo de muestreo en la vista de gráfico de líneas).<br/>                                                  |
| [**UpdateInterval**](systemmonitor-updateinterval.md)<br/>                       | Recupera o establece el período de tiempo que SYSMON espera antes de la próxima vez que actualice el gráfico o informe.<br/>                                                                                                                  |
| [**YAxisLabel**](systemmonitor-yaxislabel.md)<br/>                               | Recupera o establece la etiqueta del eje vertical (Y) del gráfico.<br/>                                                                                                                                                           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Isysmon.h</dt> </dl>  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



 

 





