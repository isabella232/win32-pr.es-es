---
description: 'El modelo conceptual: requisitos de la aplicación'
ms.assetid: 124b329b-f745-45b4-b266-7c177c76a5cd
title: 'El modelo conceptual: requisitos de la aplicación'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5a287ff940f154bf104bbb50f6362bf573d9223
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153255"
---
# <a name="the-conceptual-model-application-requirements"></a>El modelo conceptual: requisitos de la aplicación

Al diseñar el modelo conceptual, debe definir los problemas empresariales y las funciones necesarias para solucionar esos problemas. Un enfoque de prácticas recomendadas es hablar con personas que realmente utilizarán la aplicación, se reunirán con una amplia gama de usuarios e incluirán tantos escenarios empresariales como usuarios como sea posible. Determinar las identidades y el número de usuarios potenciales del sistema, así como el tamaño y el ámbito de los datos implicados. Aunque la recopilación de esta información puede ser el aspecto menos técnico del proceso de diseño, es uno de los más importantes. Para desarrollar una aplicación correcta, necesita comprender claramente los problemas y procesos empresariales que deben solucionarse.

A la hora de determinar los requisitos de la aplicación, tenga en cuenta las consideraciones siguientes:

-   Requisitos de rendimiento. ¿Cuál es el tiempo de respuesta esperado para las tareas de aplicación? ¿Qué compatibilidad con la conmutación por error para servidores inactivos es necesaria? ¿Cuáles son las horas de disponibilidad?
-   Entorno. ¿Qué servidores están disponibles? ¿Se han planeado servidores adicionales para controlar los requisitos de escalado?
-   Implementación. ¿Cómo se integrará la aplicación con un sistema actual? ¿Con qué otros sistemas interactuará la aplicación? ¿Qué sistemas operativos usan los otros sistemas? ¿Qué protocolos de comunicación deben admitirse? ¿Qué API se puede usar para interactuar con los demás sistemas? ¿Dónde están los otros sistemas ubicados en la red? ¿Cuáles son las restricciones en el uso de la máquina? ¿A qué cuentas de usuario se permite el acceso?
-   Ubicación. ¿Dónde se encuentran los datos en relación con el cliente? ¿Se accede a los datos de forma remota o es local?
-   Seguridad. ¿Hay requisitos de cifrado o de comprobación de integridad? ¿Hay requisitos de autenticación o protección de datos?
-   Derechos de acceso. ¿Existen restricciones sobre quién puede realizar determinadas operaciones? Si es así, primero debe documentar las operaciones que requieren autorización y, a continuación, documentar los tipos de usuarios que pueden tener autorización. Estos requisitos pueden tener un gran impacto en el modo en que se implementan las partes de la aplicación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[El modelo lógico: definición y planeación de la aplicación](the-logical-model--application-definition-and-planning.md)
</dt> <dt>

[El modelo físico: arquitectura de la aplicación](the-physical-model--application-architecture.md)
</dt> </dl>

 

 



