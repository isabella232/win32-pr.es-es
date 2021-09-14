---
description: Para mostrar un cuadro de diálogo que muestra los objetos de rendimiento y los contadores definidos en el equipo, llame a la función PdhBrowseCounters.
ms.assetid: f2fac1d3-f643-43c9-a445-112015baecdd
title: Examinar contadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd4bae5ce5ae7a21ae247cf66515f7386b8d0265
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073906"
---
# <a name="browsing-counters"></a>Examinar contadores

Para mostrar un cuadro de diálogo que muestra los objetos de rendimiento y los contadores definidos en el equipo, llame a la [**función PdhBrowseCounters.**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa) El cuadro de diálogo permite al usuario examinar y seleccionar contadores de rendimiento. Para especificar la configuración del cuadro de diálogo, use la estructura [**de configuración \_ DE \_ DLG \_ PDH BROWSE.**](/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_a) Por ejemplo, puede configurar el cuadro de diálogo para devolver una selección o varias selecciones.

En la entrada, el **miembro szReturnPathBuffer** contiene el objeto de rendimiento predeterminado y el contador seleccionados en el cuadro de diálogo. En la salida, el búfer contiene el objeto de rendimiento y el contador seleccionados por el usuario. También puede usar el miembro **pCallBack** para especificar una función de devolución de llamada para procesar los nombres de contador devueltos por el cuadro de diálogo.

Tenga en cuenta que este cuadro de diálogo puede devolver PDH DIALOG CANCELLED si \_ \_ **bSingleCounterPerDialog** es **FALSE** y el usuario hace clic en el botón Cerrar, por lo que el control de errores tendría que tener en cuenta esto.

Para obtener un ejemplo que usa la [**función PdhBrowseCounters,**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa) vea [Examinar contadores de rendimiento.](browsing-performance-counters.md)

Para recuperar una lista de objetos de rendimiento en el equipo, también puede llamar a la [**función PdhEnumObjects.**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectsa) Para recuperar una lista de contadores e instancias de un objeto de rendimiento, llame a la [**función PdhEnumObjectItems.**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsa) También puede usar estas funciones para identificar los objetos de rendimiento y los contadores contenidos en un archivo de registro. Las llamadas repetidas a **PdhEnumObjectItems** devolverán la misma lista de contadores e instancias hasta que llame a **PdhEnumObjects para** actualizar primero la lista de objetos de rendimiento. Para obtener un ejemplo que enumera objetos y contadores, vea [Enumerar objetos de proceso](enumerating-process-objects.md).

## <a name="selecting-the-data-source"></a>Selección del origen de datos

Puede usar [**PdhSelectDataSource**](/windows/desktop/api/Pdh/nf-pdh-pdhselectdatasourcea) junto con [**PdhBrowseCounters**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa) para pedir al usuario que seleccione si el origen de datos está en tiempo real o desde un archivo de registro y, si es un archivo de registro, su nombre. Si no desea que se muestre el cuadro de diálogo del origen de datos, puede llamar a **PdhSelectDataSource** para mostrar solo el catálogo del explorador de archivos. Para ello, especifique PDH FLAGS FILE BROWSER ONLY como segundo parámetro de la llamada \_ \_ a \_ \_ **PdhSelectDataSource**.

 

 



