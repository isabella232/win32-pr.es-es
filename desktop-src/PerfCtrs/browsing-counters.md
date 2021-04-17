---
description: Para mostrar un cuadro de diálogo que muestra los objetos y contadores de rendimiento definidos en el equipo, llame a la función PdhBrowseCounters.
ms.assetid: f2fac1d3-f643-43c9-a445-112015baecdd
title: Examinar contadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd4bae5ce5ae7a21ae247cf66515f7386b8d0265
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667348"
---
# <a name="browsing-counters"></a>Examinar contadores

Para mostrar un cuadro de diálogo que muestra los objetos y contadores de rendimiento definidos en el equipo, llame a la función [**PdhBrowseCounters**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa) . El cuadro de diálogo permite al usuario examinar y seleccionar los contadores de rendimiento. Use la estructura de configuración de [**PDH \_ Browse \_ Dlg \_**](/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_a) para especificar la configuración del cuadro de diálogo. Por ejemplo, puede configurar el cuadro de diálogo para devolver una selección o varias selecciones.

En la entrada, el miembro **szReturnPathBuffer** contiene el objeto de rendimiento predeterminado y el contador que está seleccionado en el cuadro de diálogo. En la salida, el búfer contiene el objeto de rendimiento y el contador que el usuario seleccionó. También puede usar el miembro **pCallBack** para especificar una función de devolución de llamada que procese los nombres de contador devueltos por el cuadro de diálogo.

Tenga en cuenta que este cuadro de diálogo puede devolver el cuadro de diálogo PDH \_ \_ cancelado si **bSingleCounterPerDialog** es **false** y el usuario hace clic en el botón Cerrar, por lo que el control de errores tendría que tener en cuenta esto.

Para obtener un ejemplo en el que se usa la función [**PdhBrowseCounters**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa) , vea [examinar los contadores de rendimiento](browsing-performance-counters.md).

Para recuperar una lista de objetos de rendimiento en el equipo, también puede llamar a la función [**PdhEnumObjects**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectsa) . Para recuperar una lista de contadores e instancias para un objeto de rendimiento, llame a la función [**PdhEnumObjectItems**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsa) . También puede utilizar estas funciones para identificar los objetos de rendimiento y los contadores contenidos en un archivo de registro. Las llamadas repetidas a **PdhEnumObjectItems** devolverán la misma lista de contadores e instancias hasta que llame a **PdhEnumObjects** para actualizar la lista de objetos de rendimiento en primer lugar. Para obtener un ejemplo en el que se enumeran objetos y contadores, consulte [enumeración de objetos de proceso](enumerating-process-objects.md).

## <a name="selecting-the-data-source"></a>Seleccionar el origen de datos

Puede usar [**PdhSelectDataSource**](/windows/desktop/api/Pdh/nf-pdh-pdhselectdatasourcea) junto con [**PdhBrowseCounters**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa) para solicitar al usuario que seleccione si el origen de datos se encuentra en tiempo real o en un archivo de registro, y, si es un archivo de registro, su nombre. Si no desea que se muestre el cuadro de diálogo origen de datos, puede llamar a **PdhSelectDataSource** para mostrar solo el catálogo del explorador de archivos. Para ello, especifique \_ \_ \_ el explorador de archivos de marcas de PDH \_ únicamente como el segundo parámetro de la llamada a **PdhSelectDataSource**.

 

 



