---
description: El modelo de programación distribuida de Microsoft consta de varias tecnologías, como MSMQ, IIS, DCOM y COM+. Todos estos servicios se diseñaron para su uso por parte de aplicaciones distribuidas.
ms.assetid: c72bbd47-0219-40ba-a7d5-2a6b725972d0
title: Suposiciones y principios de diseño de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7dea86c404896a3d6095d39ebd6031767f6ccdd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973538"
---
# <a name="com-design-assumptions-and-principles"></a>Suposiciones y principios de diseño de COM+

El modelo de programación distribuida de Microsoft consta de varias tecnologías, como MSMQ, IIS, DCOM y COM+. Todos estos servicios se diseñaron para su uso por parte de aplicaciones distribuidas.

COM+ se desarrolló para facilitar la creación de aplicaciones distribuidas. La arquitectura general se basa en un conjunto de suposiciones y principios.

## <a name="assumptions"></a>Supuestos

Las suposiciones son las siguientes:

-   **La aplicación COM+ admitirá varios usuarios en varios servidores.** En otras palabras, está creando una aplicación distribuida y estos varios usuarios van a estar en equipos host diferentes desde donde se ejecuta el código. Los usuarios van a acceder al código a través de Internet o a través de una red privada. La interfaz de usuario se va a presentar a través del explorador o quizás una aplicación personalizada, como una aplicación basada en formularios escrita con Microsoft Visual Basic o MFC. Esa interfaz de usuario se va a encontrar en el equipo cliente.
-   **La aplicación COM+ se puede hacer escalable y puede proporcionar una mayor disponibilidad y confiabilidad mediante la implementación de la aplicación en varios equipos servidor.** Al hacerlo, puede equilibrar la carga de trabajo de la aplicación y proporcionar tolerancia a errores mediante Windows clústeres.
-   **Si las cosas van mal, el estado de los datos persistentes, almacenados en una base de datos, de una aplicación COM+ se mantendrá si usa transacciones.** El estado de la aplicación debe sobrevivir a los accidentes que pueden producirse, como errores de aplicación, bloqueos del sistema o errores de red.

## <a name="principles"></a>Principios

Además de estas tres suposiciones, los siguientes principios están basados en el modelo de programación com+:

-   **La lógica de aplicación residirá en equipos servidor, no en equipos cliente.** Hay tres razones principales para hacerlo:
    -   Es posible que el equipo cliente no tenga la potencia de procesamiento o las características necesarias para ejecutar la lógica de la aplicación. Además, mantener la lógica de aplicación en el servidor simplifica la implementación.
    -   Los equipos servidor suelen estar más cerca de los datos, y estos datos suelen estar en una base de datos. Dado que la aplicación tiene acceso a las bases de datos, quiere ser muy sensible al costo de las conexiones de base de datos. Al colocar la mayor parte de la lógica en los equipos servidor, puede compartir conexiones de base de datos y obtener una mejora significativa del rendimiento. Hay otros recursos en los equipos servidor que también se pueden compartir, de nuevo con una ventaja de rendimiento.
    -   El hecho de que la lógica de la aplicación resida en equipos servidor mantiene el control del contexto de seguridad con la aplicación. Tiene más control sobre la seguridad si mantiene esa seguridad en los componentes de aplicación que se ejecutan en equipos servidor en lugar de en equipos cliente.
-   **Las transacciones son el núcleo.** Por diseño, las transacciones permean tanto al modelo de programación COM+ que es muy importante que las comprenda. Aunque puede hacer uso de muchos de los servicios de COM+ sin usar transacciones, si decide no usarlos, no podrá aprovechar al máximo los servicios COM+ disponibles. Entre las ventajas importantes del uso de transacciones se incluyen las siguientes:
    -   Las transacciones son una solución razonable para el problema de administración de simultaneidad. Además, las transacciones ayudan a protegerse frente a bloqueos y tienen un buen modelo de recuperación de errores. Además, las transacciones son una excelente manera de administrar tareas en varios sistemas.
    -   Puede diseñar una aplicación COM+ basada en transacciones para trabajar con un administrador de recursos y una base de datos, lo que ayuda a proteger la mayoría de la información de estado. Al mantener el estado dentro de una base de datos o algún otro almacenamiento administrado por un administrador de recursos, no tiene que mantener mucho estado dentro de los objetos reales que crea la aplicación. Aunque esto es una salida de un modelo puro orientado a objetos, funciona bien para crear aplicaciones distribuidas con recuperación de errores.
-   **La funcionalidad de la aplicación se genera como objetos COM, encapsulando los protocolos usados para comunicarse con otros sistemas o tecnologías.** Dado que probablemente va a crear componentes que van a unir varias tecnologías o sistemas heredados, planee el uso de una variedad de protocolos de comunicación. Use HTTP para la comunicación cliente/servidor o la comunicación de aplicación a aplicación a través de Internet. Use DCOM para la comunicación de aplicación a aplicación o de componente a componente en el servidor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Directrices básicas para diseñar aplicaciones COM+](basic-guidelines-for-designing-com--applications.md)
</dt> <dt>

[Diseño de la aplicación COM+ mediante UML](designing-the-com--application-using-uml.md)
</dt> <dt>

[Diseño general Sugerencias para usar COM+](general-design-tips-for-using-com-.md)
</dt> <dt>

[Optimización de interacciones con el nivel de lógica de negocios de COM+](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> <dt>

[Otras herramientas de Microsoft para compilar aplicaciones distribuidas](other-microsoft-tools-for-building-distributed-applications.md)
</dt> </dl>

 

 



