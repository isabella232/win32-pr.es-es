---
description: 'Modelo conceptual: requisitos de la aplicación'
ms.assetid: 124b329b-f745-45b4-b266-7c177c76a5cd
title: 'Modelo conceptual: requisitos de la aplicación'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c19c69f8da7179765242815c4d01760c36b94e95714188f7db772600826d0416
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853925"
---
# <a name="the-conceptual-model-application-requirements"></a>Modelo conceptual: requisitos de la aplicación

Al diseñar el modelo conceptual, debe definir los problemas empresariales y las funciones necesarias para resolverlos. Un enfoque de procedimientos recomendados es hablar con personas que realmente usarán la aplicación, reunirse con una amplia gama de usuarios e incluir tantos escenarios empresariales o de usuario como sea posible. Determine las identidades y el número de usuarios potenciales del sistema, así como el tamaño y el ámbito de los datos implicados. Aunque recopilar esta información puede ser el aspecto menos técnico del proceso de diseño, es uno de los más importantes. Para desarrollar una aplicación correcta, necesita un conocimiento claro de los problemas empresariales y los procesos que deben solucionarse.

Al determinar los requisitos de la aplicación, tenga en cuenta las siguientes consideraciones:

-   Requisitos de rendimiento. ¿Cuál es el tiempo de respuesta esperado para las tareas de aplicación? ¿Qué compatibilidad con la conmutación por error para servidores fuera de servicio es necesaria? ¿Cuáles son las horas de disponibilidad?
-   Entorno. ¿Qué servidores están disponibles? ¿Están planeados servidores adicionales para controlar los requisitos de escalado?
-   Implementación. ¿Cómo se integrará la aplicación con un sistema actual? ¿Con qué otros sistemas interactuará la aplicación? ¿Qué sistemas operativos usan los demás sistemas? ¿Qué protocolos de comunicación deben ser compatibles? ¿Qué API puede usar para interactuar con los demás sistemas? ¿Dónde se encuentran los demás sistemas en la red? ¿Qué restricciones sobre el uso de la máquina existen? ¿Qué cuentas de usuario tienen acceso permitido?
-   Ubicación. ¿Dónde se encuentran los datos en relación con el cliente? ¿Se accede a los datos de forma remota o son locales?
-   Seguridad. ¿Hay requisitos de comprobación de integridad o cifrado? ¿Hay requisitos de autenticación o protección de datos?
-   Derechos de acceso. ¿Existen restricciones sobre quién puede realizar determinadas operaciones? Si es así, primero debe documentar qué operaciones requieren autorización y, a continuación, documentar los tipos de usuarios que pueden tener autorización. Estos requisitos pueden tener un gran impacto en cómo se implementan las partes de la aplicación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[El modelo lógico: definición y planeamiento de la aplicación](the-logical-model--application-definition-and-planning.md)
</dt> <dt>

[Modelo físico: arquitectura de aplicación](the-physical-model--application-architecture.md)
</dt> </dl>

 

 



