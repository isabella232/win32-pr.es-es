---
title: Objeto SystemMonitor (Isysmon. h)
description: Esta clase contiene los métodos y las propiedades que se usan para configurar el control de monitor del sistema.
ms.assetid: 5a6195ee-ed89-4f5d-85dd-88cf4a9b5155
keywords:
- Objeto SystemMonitor SysMon
- Objeto SystemMonitor SysMon, descrito
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666001"
---
# <a name="systemmonitor-object"></a>Objeto SystemMonitor

Esta clase contiene los métodos y las propiedades que se usan para configurar el control de monitor del sistema.

## <a name="members"></a>Miembros

El objeto **SystemMonitor** tiene estos tipos de miembros:

-   [Eventos](#events)
-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="events"></a>Events

El objeto **SystemMonitor** tiene estos eventos.



| Evento                                                         | Descripción                                                                                                                 |
|:--------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**OnCounterAdded**](systemmonitor-oncounteradded.md)        | Le informa cuando un contador se agrega a la colección de [**contadores**](counters.md) .<br/>                             |
| [**OnCounterDeleted**](-systemmonitor-oncounterdeleted.md)   | Le notifica antes de que se elimine un contador de la colección de [**contadores**](counters.md) .<br/>                       |
| [**OnCounterSelected**](-systemmonitor-oncounterselected.md) | Le notifica cuando se selecciona un contador.<br/>                                                                         |
| [**OnDblClick**](-systemmonitor-ondblclick.md)               | Le informa cuando un usuario hace doble clic en la línea del gráfico, en la barra de histograma o en el elemento de informe con el botón primario del mouse.<br/> |
| [**OnSampleCollected**](-systemmonitor-onsamplecollected.md) | Le informa cuando se han recopilado valores de ejemplo para los contadores.<br/>                                            |



 

### <a name="methods"></a>Métodos

El objeto **SystemMonitor** tiene estos métodos.



| Método                                                       | Descripción                                                                                                                                                              |
|:-------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BatchLocking**](systemmonitor-batchinglock.md)           | Bloquea el monitor de sistema para impedir que muestre los datos de contador del contador o el archivo de registro recién agregados.<br/>                                                   |
| [**BrowseCounters**](systemmonitor-browsecounters.md)       | Muestra el cuadro de diálogo **Agregar contador** .<br/>                                                                                                                      |
| [**ClearData**](systemmonitor-cleardata.md)                 | Borra todos los campos de datos del control.<br/>                                                                                                                        |
| [**CollectSample**](systemmonitor-collectsample.md)         | Muestrea un valor para cada contador en el objeto de colección **counters** .<br/>                                                                                       |
| [**Copiar**](systemmonitor-copy.md)                           | Copia la configuración de propiedades, la lista de contadores y los datos de contador del control en el portapapeles como un objeto HTML.<br/>                                                |
| [**DisplayProperties**](systemmonitor-displayproperties.md) | Muestra el cuadro de diálogo **propiedades del gráfico** .<br/>                                                                                                                 |
| [**GetLogViewRange**](systemmonitor-getlogviewrange.md)     | Recupera la fecha de inicio utilizada para recuperar los valores de contador de los archivos de registro.<br/>                                                                               |
| [**LoadSettings**](systemmonitor-loadsettings.md)           | Agrega los contadores del archivo de plantilla HTML al monitor de sistema.<br/>                                                                                            |
| [**Pegar**](systemmonitor-paste.md)                         | Anexa a la colección actual de contadores la lista de contadores que se copiaron en el portapapeles. <br/>                                                        |
| [**Registrar**](systemmonitor-relog.md)                         | Vuelve a registrar los datos del contador en un nuevo archivo. También puede utilizar este método para especificar un nuevo tipo de archivo y para reducir el número de ejemplos que contiene el archivo de registro.<br/> |
| [**Reset**](systemmonitor-reset.md)                         | Quita todos los objetos de [**elemento**](counteritem.md) de grupo del objeto de colección **counters** .<br/>                                                               |
| [**SaveAs**](systemmonitor-saveas.md)                       | Guarda los valores del contador en la vista del gráfico en un archivo de registro.<br/>                                                                                                     |
| [**ScaleToFit**](systemmonitor-scaletofit.md)               | Ajustar los valores del contador para que quepan en el gráfico.<br/>                                                                                                                     |
| [**SetLogViewRange**](systemmonitor-setlogviewrange.md)     | Establece la fecha de inicio utilizada para recuperar los valores de contador de los archivos de registro.<br/>                                                                                    |
| [**UpdateGraph**](systemmonitor-updategraph.md)             | Actualiza el contenido de las ventanas del monitor del sistema.<br/>                                                                                                         |



 

### <a name="properties"></a>Propiedades

El objeto **SystemMonitor** tiene estas propiedades.



| Propiedad                                                                                | Descripción                                                                                                                                                                                                                             |
|:----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Aspecto**](systemmonitor-appearance.md)<br/>                               | Recupera o establece la apariencia del control para incluir u omitir los efectos de visualización tridimensionales.<br/>                                                                                                                        |
| [**BackColor**](systemmonitor-backcolor.md)<br/>                                 | Recupera o establece el color de fondo del gráfico y las vistas de informe.<br/>                                                                                                                                                        |
| [**BackColorCtl**](systemmonitor-backcolorctl.md)<br/>                           | Recupera o establece el color de fondo del control.<br/>                                                                                                                                                                       |
| [**BorderStyle**](systemmonitor-borderstyle.md)<br/>                             | Recupera o establece el estilo de borde del control.<br/>                                                                                                                                                                           |
| [**ChartScroll**](systemmonitor-chartscroll.md)<br/>                             | Recupera o establece un valor que determina si el gráfico de líneas se desplaza en la vista.<br/>                                                                                                                                             |
| [**Counters**](systemmonitor-counters.md)<br/>                                   | Recupera la colección de objetos de elementos de un [**elemento**](counteritem.md) .<br/>                                                                                                                                                      |
| [**DataPointCount**](systemmonitor-datapointcount.md)<br/>                       | Recupera o establece el número de puntos de datos mostrados en un gráfico de líneas.<br/>                                                                                                                                                       |
| [**DataSourceType**](systemmonitor-datasourcetype.md)<br/>                       | Recupera o establece el origen de los datos del contador de rendimiento.<br/>                                                                                                                                                                |
| [**TipoDePresentación**](systemmonitor-displaytype.md)<br/>                             | Recupera o establece el tipo de gráfico que se usa para representar gráficamente los datos del contador de rendimiento.<br/>                                                                                                                                              |
| [**EnableDigitGrouping**](systemmonitor-enabledigitgrouping.md)<br/>             | Recupera o establece un valor que determina si SYSMON usa la agrupación de dígitos al mostrar valores numéricos.<br/>                                                                                                                      |
| [**EnableToolTips**](systemmonitor-enabletooltips.md)<br/>                       | Recupera o establece un valor que determina si se muestra una información sobre herramientas cuando se mantiene el mouse sobre un contador en una de las vistas del gráfico.<br/>                                                                                             |
| [**Tipo**](systemmonitor-font.md)<br/>                                           | Recupera o establece la fuente utilizada en el control.<br/>                                                                                                                                                                              |
| [**ForeColor**](systemmonitor-forecolor.md)<br/>                                 | Recupera o establece el color del texto que aparece en el control.<br/>                                                                                                                                                         |
| [**GraphTitle**](systemmonitor-graphtitle.md)<br/>                               | Recupera o establece el título del gráfico.<br/>                                                                                                                                                                                    |
| [**GridColor**](systemmonitor-gridcolor.md)<br/>                                 | Recupera o establece el color de las líneas de cuadrícula utilizadas en el gráfico.<br/>                                                                                                                                                             |
| [**Resaltar**](systemmonitor-highlight.md)<br/>                                 | Recupera o establece un valor que indica si los valores de los contadores seleccionados se resaltan en el gráfico.<br/>                                                                                                               |
| [**NombreDeArchivoDeRegistro**](systemmonitor-logfilename.md)<br/>                             | Obsoleto. Recupera o establece el nombre de un archivo de registro que se va a utilizar como origen de los valores de contador mostrados en el monitor de sistema.<br/>                                                                                                   |
| [**LogFiles**](systemmonitor-logfilename.md)<br/>                                | Colección de uno o más archivos de registro que se van a utilizar como origen de los valores de contador mostrados en el monitor de sistema.<br/>                                                                                                                  |
| [**LogSourceStartTime**](systemmonitor-logsourcestarttime.md)<br/>               | Recupera la marca de tiempo del valor del contador más antiguo de un contador de la colección de contadores que se registró en los archivos de registro.<br/>                                                                                           |
| [**LogSourceStopTime**](systemmonitor-logsourcestoptime.md)<br/>                 | Recupera la marca de tiempo del último valor del contador de un contador de la colección de contadores que se registró en los archivos de registro.<br/>                                                                                             |
| [**LogViewStart**](systemmonitor-logviewstart.md)<br/>                           | Recupera o establece la fecha de inicio utilizada para recuperar los valores de contador de los archivos de registro.<br/>                                                                                                                                      |
| [**LogViewStop**](systemmonitor-logviewstop.md)<br/>                             | Recupera o establece la fecha de finalización utilizada para recuperar los valores de contador de los archivos de registro.<br/>                                                                                                                                        |
| [**ManualUpdate**](systemmonitor-manualupdate.md)<br/>                           | Recupera o establece un valor que indica si el contenido del monitor de sistema se actualizará manualmente o automáticamente a intervalos especificados.<br/>                                                                           |
| [**MaximumScale**](systemmonitor-maximumscale.md)<br/>                           | Recupera o establece el valor máximo del eje vertical (Y) del gráfico.<br/>                                                                                                                                                   |
| [**MinimumScale**](systemmonitor-minimumscale.md)<br/>                           | Recupera o establece el valor mínimo del eje vertical (Y) del gráfico.<br/>                                                                                                                                                   |
| [**MonitorDuplicateInstances**](systemmonitor-monitorduplicateinstances.md)<br/> | Recupera o establece un valor que determina si se pueden supervisar varias instancias de un contador.<br/>                                                                                                                          |
| [**ReadOnly**](systemmonitor-readonly.md)<br/>                                   | Recupera o establece un valor que determina si un usuario puede modificar los valores de propiedad del control.<br/>                                                                                                                      |
| [**ReportValueType**](systemmonitor-reportvaluetype.md)<br/>                     | Recupera o establece un valor que determina si el histograma y las vistas de informe representan el último valor muestreado durante el intervalo de muestreo o un valor calculado del muestreo, como el valor del contador promedio o mínimo.<br/> |
| [**ShowHorizontalGrid**](systemmonitor-showhorizontalgrid.md)<br/>               | Recupera o establece un valor que determina si las líneas de cuadrícula horizontales se muestran en el gráfico.<br/>                                                                                                                          |
| [**ShowLegend**](systemmonitor-showlegend.md)<br/>                               | Recupera o establece un valor que determina si se muestra la leyenda.<br/>                                                                                                                                                   |
| [**ShowScaleLabels**](systemmonitor-showscalelabels.md)<br/>                     | Recupera o establece un valor que determina si las etiquetas de escala se muestran en el eje vertical del gráfico.<br/>                                                                                                          |
| [**ShowTimeAxisLabels**](systemmonitor-showtimeaxislabels.md)<br/>               | Recupera o establece un valor que determina si el eje horizontal (X) de la vista de gráfico contiene etiquetas.<br/>                                                                                                                      |
| [**ShowToolbar**](systemmonitor-showtoolbar.md)<br/>                             | Recupera o establece un valor que determina si la barra de herramientas se muestra en el control.<br/>                                                                                                                                   |
| [**ShowValueBar**](systemmonitor-showvaluebar.md)<br/>                           | Recupera o establece un valor que determina si la barra de valores (el conjunto de valores estadísticos por debajo del gráfico) se muestra en el control.<br/>                                                                                 |
| [**ShowVerticalGrid**](systemmonitor-showverticalgrid.md)<br/>                   | Recupera o establece un valor que determina si las líneas de cuadrícula verticales se muestran en el gráfico.<br/>                                                                                                                            |
| [**SqlDsnName**](systemmonitor-sqldsnname.md)<br/>                               | Recupera o establece el nombre del origen de datos ODBC.<br/>                                                                                                                                                                                 |
| [**SqlLogSetName**](systemmonitor-sqllogsetname.md)<br/>                         | Recupera o establece el nombre descriptivo del conjunto de registros.<br/>                                                                                                                                                                          |
| [**TimeBarColor**](systemmonitor-timebarcolor.md)<br/>                           | Recupera o establece el color de la barra de tiempo (la barra vertical que se desplaza por la ventana del gráfico para indicar el paso de cada intervalo de muestreo en la vista del gráfico de líneas).<br/>                                                  |
| [**UpdateInterval**](systemmonitor-updateinterval.md)<br/>                       | Recupera o establece el período de tiempo que SYSMON espera antes de la próxima vez que actualice el gráfico o el informe.<br/>                                                                                                                  |
| [**YAxisLabel**](systemmonitor-yaxislabel.md)<br/>                               | Recupera o establece la etiqueta del eje vertical (Y) del gráfico.<br/>                                                                                                                                                           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Isysmon. h</dt> </dl>  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



 

 





