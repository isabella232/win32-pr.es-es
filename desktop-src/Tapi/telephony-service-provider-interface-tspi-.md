---
description: Un proveedor de servicios de telefonía (TSPI) controla los controles específicos del dispositivo para la programación de comunicaciones.
ms.assetid: da54e219-9adb-4a12-baab-52f2b2fb7c66
title: Interfaz del proveedor de servicios de telefonía (TSPI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a9d8ac4fd15fbc2685073e5954e14951f33acd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678351"
---
# <a name="telephony-service-provider-interface-tspi"></a>Interfaz del proveedor de servicios de telefonía (TSPI)

Un proveedor de servicios de telefonía (TSPI) controla los controles específicos del dispositivo para la programación de comunicaciones. Un TSP debe cumplir con el proveedor de servicios de telefonía (TSPI) para que funcione como un proveedor de servicios en el entorno de telefonía de Microsoft. TSPI define las funciones externas expuestas por un proveedor de servicios de telefonía proporcionado con el equipo de comunicaciones.

Un autor de TSP debe estar familiarizado con el material de [información general de telefonía de Microsoft](./microsoft-telephony-overview.md), que abarca la arquitectura de telefonía general y proporciona información general sobre el material común a varias API de telefonía. Por ejemplo, esta sección contiene una lista de operaciones de control de sesión, como Park, con descripciones de cada operación y salta a los elementos de programación TAPI 2,2, TAPI 3 y TSPI relacionados.

En la información general siguiente se incluyen material específico de las necesidades de un autor de TSP. Tenga en cuenta que las partes más difíciles de escribir un TSP son detalles específicos del dispositivo y del sistema operativo, que están fuera del ámbito de este documento.

La información general de TSPI se divide en las siguientes secciones:

-   En las [consideraciones de programación generales](/previous-versions/windows/desktop/legacy/ms725196(v=vs.85)) se tratan los requisitos de dll, el control adecuado de las versiones, las comprobaciones de errores realizadas por TAPI, un resumen de cómo las funciones de TSPI se corresponden con las funciones de TAPI 2,2 (TAPI/C) y una descripción de los niveles de servicio según se expresa en TSPI.
-   El [ciclo de vida de un proveedor de servicios de telefonía](life-cycle-of-a-telephony-service-provider.md) contiene un resumen de alto nivel de las fases operativas de un TSP.
-   El [acceso al dispositivo](/previous-versions/windows/desktop/legacy/ms725183(v=vs.85)) cubre los aspectos básicos de cómo un TSP expone la información y los controles del dispositivo en TAPI.
-   El [acceso a la sesión](/previous-versions/windows/desktop/legacy/ms725266(v=vs.85)) cubre lo que TAPI espera de un TSP durante una sesión de comunicaciones.
-   El [acceso a los medios](/previous-versions/windows/desktop/legacy/ms725240(v=vs.85)) proporciona un conjunto limitado de controles sobre flujos multimedia. Es posible un control mucho más preciso a través del uso de un proveedor de servicios multimedia y los autores de proveedores de servicios deben usar esta API siempre que sea factible. TSPI proporciona comunicaciones entre un par de TSP/MSP.
-   Los [dispositivos telefónicos](/previous-versions/windows/desktop/legacy/ms725257(v=vs.85)) cubren la información complementaria y las operaciones expuestas Si un TSP controla el control de juego de teléfono. Estas operaciones son opcionales.
-   [La interfaz del archivo dll de la interfaz de usuario del proveedor de servicios de telefonía](the-telephony-service-provider-ui-dll-interface.md) cubre funciones especiales que se pueden implementar para permitir que los usuarios establezcan directamente muchos aspectos de la funcionalidad de un TSP.

Consulte la [referencia de TSPI](tspi-reference.md) para obtener más información sobre los elementos de programación de TSPI.

 

 
