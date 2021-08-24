---
description: Un proveedor de servicios de telefonía (TSPI) controla los controles específicos del dispositivo para la programación de comunicaciones.
ms.assetid: da54e219-9adb-4a12-baab-52f2b2fb7c66
title: Interfaz del proveedor de servicios de telefonía (TSPI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fac57f3b86acdf105c4c78f46f4f1d1d0e270c2a0b1be2d8bd1f55009926329
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681805"
---
# <a name="telephony-service-provider-interface-tspi"></a>Interfaz del proveedor de servicios de telefonía (TSPI)

Un proveedor de servicios de telefonía (TSPI) controla los controles específicos del dispositivo para la programación de comunicaciones. Un TSP debe cumplir con el proveedor de servicios de telefonía (TSPI) para funcionar como proveedor de servicios en el entorno de telefonía de Microsoft. TSPI define las funciones externas expuestas por un proveedor de servicios de telefonía suministrado con equipos de comunicaciones.

Un autor de TSP debe estar familiarizado con el material de Introducción a la telefonía de [Microsoft,](./microsoft-telephony-overview.md)que trata la arquitectura de telefonía general y proporciona información general del material común a varias API de telefonía. Por ejemplo, esta sección contiene una lista de operaciones de control de sesión, como Park, con descripciones de cada operación y salta a los elementos de programación TAPI 2.2, TAPI 3 y TSPI relacionados.

Las siguientes información general cubren material específico para las necesidades de un autor de TSP. Tenga en cuenta que las partes más difíciles de escribir un TSP son los detalles específicos del dispositivo y del sistema operativo, que están fuera del ámbito de este documento.

La información general de TSPI se divide en las secciones siguientes:

-   Consideraciones generales de programación cubre los requisitos de DLL, el control adecuado de las versiones, las comprobaciones de errores [realizadas](/previous-versions/windows/desktop/legacy/ms725196(v=vs.85)) por TAPI, un resumen de cómo las funciones de TSPI se corresponden con las funciones de TAPI 2.2 (TAPI/C) y una explicación de los niveles de servicio expresados en TSPI.
-   El [ciclo de vida de un proveedor de servicios de](life-cycle-of-a-telephony-service-provider.md) telefonía contiene un resumen de alto nivel de las fases operativas de un TSP.
-   [Acceso a dispositivos](/previous-versions/windows/desktop/legacy/ms725183(v=vs.85)) cubre los conceptos básicos de cómo un TSP expone la información y los controles del dispositivo a TAPI.
-   [El acceso a](/previous-versions/windows/desktop/legacy/ms725266(v=vs.85)) la sesión cubre lo que TAPI espera de un TSP durante una sesión de comunicaciones.
-   [Acceso multimedia](/previous-versions/windows/desktop/legacy/ms725240(v=vs.85)) proporciona un conjunto limitado de controles sobre secuencias multimedia. Es posible un control mucho más preciso mediante el uso de un proveedor de servicios multimedia, y los autores del proveedor de servicios deben usar esta API siempre que sea posible. El TSPI proporciona comunicaciones entre un par TSP/MSP.
-   [Teléfono dispositivos cubre](/previous-versions/windows/desktop/legacy/ms725257(v=vs.85)) la información complementaria y las operaciones expuestas si un TSP controla el control del conjunto de teléfonos. Estas operaciones son opcionales.
-   [La interfaz DLL](the-telephony-service-provider-ui-dll-interface.md) de interfaz de usuario del proveedor de servicios de telefonía cubre funciones especiales que se pueden implementar para permitir que un usuario establezca directamente muchos aspectos de la funcionalidad de un TSP.

Consulte la Referencia [de TSPI para](tspi-reference.md) obtener más información sobre los elementos de programación de TSPI.

 

 
