---
title: Uso de Monitor de red para ver archivos ETL
description: Monitor de red 3,3 permite a los usuarios analizar, filtrar y ver un archivo ETL (con Windows Vista o posterior).
ms.assetid: 932be193-70f9-48f9-95d8-18916d3b7064
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04120f860654f4859aa930f32a4711999682eaf8
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/03/2021
ms.locfileid: "104003255"
---
# <a name="using-network-monitor-to-view-etl-files"></a>Uso de Monitor de red para ver archivos ETL

[Monitor de red 3,3](https://connect.microsoft.com/site/sitehome.aspx?SiteID=216) permite a los usuarios analizar, filtrar y ver un archivo ETL (con Windows Vista o posterior). (Si usa Monitor de red 3,2, tendrá que descargar e instalar analizadores adicionales desde [CodePlex](https://www.codeplex.com/NMParsers) para representar los eventos de seguimiento de red).

Los archivos ETL correlacionados agrupan los eventos correspondientes. En el ScrollBar siguiente se muestra un archivo correlacionado abierto en Monitor de red, con la conversación habilitada.

![Captura de pantalla que muestra el Monitor de red, con eventos correlacionados resaltados en la ventana de la izquierda y UTEvent resaltados en la lista desplegable.](images/ut-netmon1.png)

Los eventos correlacionados se agrupan por actividad en el panel izquierdo. Puede seleccionar un evento en el panel de Resumen de fotogramas y, a continuación, hacer clic con el botón derecho para seleccionar la conversación en el nivel de evento de red. Esto mostrará una actividad relacionada en el panel izquierdo.

Si selecciona una actividad determinada en el panel izquierdo y la expande, se mostrará la lista de proveedores de los eventos correlacionados.

![Captura de pantalla que muestra el Monitor de red con una actividad seleccionada en el panel izquierdo y los eventos correspondientes a ese evento en el panel derecho.](images/ut-netmon2.png)

Al seleccionar un proveedor específico en el panel izquierdo, se mostrará una lista de eventos específicos de ese proveedor y actividad en el panel Resumen de fotogramas.

![Captura de pantalla que muestra un proveedor específico seleccionado en el panel izquierdo y una lista de eventos específicos del proveedor que se resaltan en el panel superior derecho.](images/ut-netmon3.png)

Los filtros se pueden aplicar en Monitor de red para que sea más fácil ver y encontrar los eventos o paquetes correctos. Por ejemplo, puede aplicar un filtro a los eventos de error seleccionados (por ejemplo, **UTEvent. header. descriptor. LEVEL = = 2**) para mostrarlos en un determinado color.

![Captura de pantalla que muestra el cuadro de diálogo "editar filtro de color".](images/ut-netmon4.png)

Los filtros también se pueden aplicar para marcar diferentes proveedores en diferentes colores para que los resultados sean más fáciles de ver.

![Captura de pantalla que muestra un ejemplo de distintos proveedores marcados con distintos colores.](images/ut-netmon5.png)

Para aplicar un filtro, haga clic en **ColorFilters** en el menú **filtros** .

En la tabla siguiente se muestran algunos ejemplos de filtros útiles.



| Filter                                                                        | Descripción                                                       |
|-------------------------------------------------------------------------------|-------------------------------------------------------------------|
| UTEvent. header. descriptor. LEVEL = = 2                                          | Filtra solo los eventos de error.                                        |
| UTEvent. header. descriptor. Level = = 3                                          | Filtra solo los eventos de advertencia.                                      |
| UTEvent.Header.Descriptor.Id = = 2001                                          | Filtra solo los eventos con el ID. de evento 2001.                           |
| MicrosoftWindowsWLANAutoConfig de WLAN \_                                          | Filtra solo los eventos del servicio WLAN.                            |
| N802 \_ MicrosoftWindowsNWiFi                                                   | Filtra solo los eventos del controlador WIFI nativo.                  |
| WLAN \_ MICROSOFTWINDOWSWLANAUTOCONFIG y UTEvent.header.descriptor.ID = = 2001 | Filtra solo los eventos con el ID. de evento 2001 emitido desde el servicio WLAN. |



 

 

 




