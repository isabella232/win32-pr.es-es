---
title: Uso de Monitor de red para ver archivos ETL
description: Monitor de red 3.3 permite a los usuarios analizar, filtrar y ver un archivo ETL (mediante Windows Vista o posterior).
ms.assetid: 932be193-70f9-48f9-95d8-18916d3b7064
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc8c794b04837cc9d32b265eb81bfeb08fa47bdc1730672971ff6824b31c8ca0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685701"
---
# <a name="using-network-monitor-to-view-etl-files"></a>Uso de Monitor de red para ver archivos ETL

[Monitor de red 3.3](https://connect.microsoft.com/site/sitehome.aspx?SiteID=216) permite a los usuarios analizar, filtrar y ver un archivo ETL (mediante Windows Vista o posterior). (Si usa Monitor de red 3.2, deberá descargar e instalar analizadores adicionales de [CodePlex](https://www.codeplex.com/NMParsers) para representar los eventos de seguimiento de red).

Los archivos ETL correlacionados agrupan los eventos pertinentes. En la ilustración siguiente se muestra un archivo correlacionado abierto en Monitor de red, con la conversación habilitada.

![Captura de pantalla que muestra Monitor de red, con eventos correlacionados resaltados en la ventana izquierda y UTEvent resaltados en la lista desplegable.](images/ut-netmon1.png)

Los eventos correlacionados se agrupan por actividad en el panel izquierdo. Puede seleccionar un evento en el panel Resumen de fotogramas y, a continuación, hacer clic con el botón derecho para seleccionar la conversación en el nivel de evento de red. Se mostrará una actividad relacionada en el panel izquierdo.

Al seleccionar una actividad determinada en el panel izquierdo y expandirla, se mostrará la lista de proveedores para los eventos correlacionados.

![Captura de pantalla que muestra Monitor de red con una actividad seleccionada en el panel izquierdo y los eventos correspondientes a ese evento en el panel derecho.](images/ut-netmon2.png)

Al seleccionar un proveedor específico en el panel izquierdo, se mostrará una lista de eventos específicos de ese proveedor y actividad en el panel Resumen de fotogramas.

![Captura de pantalla que muestra un proveedor específico seleccionado en el panel izquierdo y una lista de eventos específicos del proveedor resaltados en el panel superior derecho.](images/ut-netmon3.png)

Los filtros se pueden aplicar Monitor de red para facilitar la visualización y búsqueda de los eventos o paquetes adecuados. Por ejemplo, puede aplicar un filtro a los eventos de error seleccionados (por ejemplo, **UTEvent.Header.Descriptor.Level == 2**) para mostrarlos en un color determinado.

![Captura de pantalla que muestra el cuadro de diálogo "Editar filtro de color".](images/ut-netmon4.png)

También se pueden aplicar filtros para marcar distintos proveedores en distintos colores para que los resultados sean más fáciles de ver.

![Captura de pantalla que muestra un ejemplo de diferentes proveedores marcados en colores diferentes.](images/ut-netmon5.png)

Para aplicar un filtro, haga clic **en ColorFilters en** el **menú** Filtros.

En la tabla siguiente se muestran algunos ejemplos de filtros útiles.



| Filter                                                                        | Descripción                                                       |
|-------------------------------------------------------------------------------|-------------------------------------------------------------------|
| UTEvent.Header.Descriptor.Level == 2                                          | Filtra solo los eventos de error.                                        |
| UTEvent.Header.Descriptor.Level == 3                                          | Filtra solo los eventos de advertencia.                                      |
| UTEvent.Header.Descriptor.Id == 2001                                          | Filtra solo los eventos con el identificador de evento 2001.                           |
| WLAN \_ MicrosoftWindowsWLANAutoConfig                                          | Filtra solo los eventos del servicio WLAN.                            |
| N802 \_ MicrosoftWindowsNWiFi                                                   | Filtra solo los eventos del controlador De Wi-Fi nativo.                  |
| WLAN \_ MicrosoftWindowsWLANAutoConfig AND UTEvent.Header.Descriptor.Id == 2001 | Filtra solo los eventos con el identificador de evento 2001 emitido desde el servicio WLAN. |



 

 

 




