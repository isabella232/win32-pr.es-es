---
title: Procedimientos recomendados (Windows de filtrado de datos)
description: La lista siguiente contiene procedimientos recomendados para desarrollar aplicaciones mediante la API Windows Filtering Platform (WFP).
ms.assetid: 017ff210-8666-466e-8424-c95e750fd5ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e0ddb6038a9fe43070f1c16e545dbd7ac8929f3363fc88556aac391428175ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069465"
---
# <a name="best-practices-windows-filtering-platform"></a>Procedimientos recomendados (Windows de filtrado de datos)

La lista siguiente contiene procedimientos recomendados para desarrollar aplicaciones mediante la API Windows Filtering Platform (WFP).

-   Use sesiones dinámicas.

    Muchas aplicaciones agregan objetos de directiva de filtrado al principio y, a continuación, eliminan estos objetos en detenerse. Mediante el uso de una sesión dinámica, se garantiza que estos objetos se eliminan incluso si la aplicación se bloquea. Además, simplemente cerrar el identificador del motor al detener es más eficaz que realizar llamadas individuales para eliminar cada objeto.

-   Controle correctamente los tiempos de espera de transacción o establezca **la sesión txnWaitTimeoutInMSec** en infinito para evitar tiempos de espera.

    Aunque no use transacciones explícitas, la mayoría de las llamadas se siguen ejecutando en una transacción implícita y, por tanto, puede agotar el tiempo de espera.

-   Use transacciones explícitas para combinar operaciones de adición o eliminación relacionadas en una única transacción.

    Esto es más eficaz y facilita la limpieza de resultados parciales en rutas de acceso de error.

-   Use cadenas compatibles con HIPAA.

    Todas las cadenas localizables se almacenan en una estructura de datos común: [**FWPM \_ DISPLAY \_ DATA0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwpm_display_data0). Las cadenas dentro de esta estructura pueden ser cadenas indirectas del tipo admitido [**por SHLoadIndirectString**](/windows/win32/api/shlwapi/nf-shlwapi-shloadindirectstring). Antes de que cualquiera de las funciones devuelva una estructura **\_ FWPM DISPLAY \_ DATA0,** las cadenas indirectas se resuelven en el recurso de cadena especificado mediante la configuración regional del autor de la llamada.

-   Asocie todos los objetos a un proveedor.

    Cuando hay varios proveedores instalados en el sistema, esto facilita que las herramientas de diagnóstico determinen quién agregó qué.

-   Agregue filtros a su propia subcapa.

    Una vez alcanzado un filtro de terminación en una subcapa, no se evalúan más filtros en esa subcapa. Por lo tanto, si agrega los filtros a la misma subcapa que otro proveedor, puede impedir que se invoque el filtro del otro, lo que da lugar a resultados inesperados.

-   Use El cumplimiento de la capa de aplicación (ALE) en lugar del filtrado orientado a paquetes.

    El filtrado en la capa de paquetes es lento.

-   Filtre los errores ICMP y los eventos RST antes de que se generen.

    Esto es más eficaz que filtrar estos eventos después de que se generen.

-   Realice la inspección de paquetes en la capa de datos de flujo o datagrama en lugar de en la capa de transporte.

    Esto se aplica al desarrollo de llamadas. Para obtener más información, vea [Callout Driver Programming Considerations](/windows-hardware/drivers/network/callout-driver-programming-considerations) in the Windows Driver Kit (WDK).

-   Tenga en cuenta las implicaciones de rendimiento al usar filtros complejos.

    A partir Windows 7 y Windows Server 2008 R2, los filtros se pueden crear con varias condiciones que usan la misma clave de campo. Esto permite crear directivas complejas con menos filtros. Sin embargo, estos filtros complejos pueden incurrir en un rendimiento más lento para que el motor de filtros WFP clasifique. Se debe realizar una evaluación para determinar si el uso de estos filtros provoca un efecto adverso en el rendimiento general de la solución.

 

 
