---
title: Procedimientos recomendados (plataforma de filtrado de Windows)
description: La lista siguiente contiene los procedimientos recomendados para desarrollar aplicaciones mediante la API de la plataforma de filtrado de Windows (WFP).
ms.assetid: 017ff210-8666-466e-8424-c95e750fd5ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac43f103e0076945d566e26a1706bdec22916db
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104533675"
---
# <a name="best-practices-windows-filtering-platform"></a>Procedimientos recomendados (plataforma de filtrado de Windows)

La lista siguiente contiene los procedimientos recomendados para desarrollar aplicaciones mediante la API de la plataforma de filtrado de Windows (WFP).

-   Usar sesiones dinámicas.

    Muchas aplicaciones agregan objetos de directiva de filtrado en el inicio y, a continuación, eliminan estos objetos en la detención. Mediante el uso de una sesión dinámica, garantiza que estos objetos se eliminan incluso si se bloquea la aplicación. Además, simplemente cerrar el identificador del motor en la detención es más eficaz que realizar llamadas individuales para eliminar cada objeto.

-   Controlar los tiempos de espera de la transacción correctamente o establecer la **txnWaitTimeoutInMSec** de sesión en infinita para evitar Tiempos de espera.

    Incluso si no utiliza transacciones explícitas, la mayoría de las llamadas se siguen ejecutando en una transacción implícita y, por tanto, pueden agotar el tiempo de espera.

-   Use transacciones explícitas para combinar operaciones de adición o eliminación relacionadas en una única transacción.

    Esto es más eficaz y facilita la limpieza de los resultados parciales en rutas de acceso de error.

-   Usar cadenas compatibles con MUI.

    Todas las cadenas localizables se almacenan en una estructura de datos común: [**FWPM \_ Display \_ Data0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwpm_display_data0). Las cadenas dentro de esta estructura pueden ser cadenas indirectas del tipo admitido por [**SHLoadIndirectString**](/windows/win32/api/shlwapi/nf-shlwapi-shloadindirectstring). Antes de que una de las funciones devuelva una estructura **FWPM \_ Display \_ Data0** , las cadenas indirectas se resuelven en el recurso de cadena especificado mediante la configuración regional del llamador.

-   Asociar todos los objetos a un proveedor.

    Cuando hay varios proveedores instalados en el sistema, esto hace que sea más fácil para las herramientas de diagnóstico determinar quién agregó qué.

-   Agregue filtros a su propia subcapa.

    Una vez que se alcanza un filtro de terminación en una subcapa, no se evalúan más filtros en esa subcapa. Por lo tanto, si agrega los filtros a la misma subcapa que otro proveedor, puede impedir que se invoquen los filtros de los demás, lo que produce resultados inesperados.

-   Use el cumplimiento del nivel de aplicación (ALE) en lugar del filtrado orientado a paquetes.

    El filtrado en la capa de paquetes es lento.

-   Filtre los errores ICMP y los eventos RST antes de que se generen.

    Esto es más eficaz que filtrar estos eventos una vez que se generan.

-   Realizar la inspección de paquetes en el nivel de datos de flujo/datagrama en lugar de en el nivel de transporte.

    Esto se aplica al desarrollo de llamadas. Para obtener más información, consulte [consideraciones sobre la programación de controladores de llamada](/windows-hardware/drivers/network/callout-driver-programming-considerations) en el kit de controladores de Windows (WDK).

-   Tenga en cuenta las implicaciones de rendimiento al usar filtros complejos.

    A partir de Windows 7 y Windows Server 2008 R2, los filtros se pueden crear con varias condiciones que usan la misma clave de campo. Esto permite crear directivas complejas con menos filtros. Sin embargo, estos filtros complejos pueden incurrir en un rendimiento más lento para que el motor de filtro WFP los clasifique. Se debe realizar una evaluación para determinar si el uso de estos filtros provoca un efecto adverso en el rendimiento general de la solución.

 

 
