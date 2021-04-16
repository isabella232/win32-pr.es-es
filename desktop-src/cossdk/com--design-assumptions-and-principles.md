---
description: El modelo de programación distribuida de Microsoft consta de varias tecnologías, como MSMQ, IIS, DCOM y COM+. Todos estos servicios se diseñaron para su uso por parte de aplicaciones distribuidas.
ms.assetid: c72bbd47-0219-40ba-a7d5-2a6b725972d0
title: Hipótesis y principios de diseño de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7dea86c404896a3d6095d39ebd6031767f6ccdd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696136"
---
# <a name="com-design-assumptions-and-principles"></a>Hipótesis y principios de diseño de COM+

El modelo de programación distribuida de Microsoft consta de varias tecnologías, como MSMQ, IIS, DCOM y COM+. Todos estos servicios se diseñaron para su uso por parte de aplicaciones distribuidas.

COM+ se desarrolló para facilitar la creación de aplicaciones distribuidas. La arquitectura global se basa en un conjunto de hipótesis y principios.

## <a name="assumptions"></a>Supuestos

Las suposiciones son las siguientes:

-   **La aplicación COM+ será compatible con varios usuarios en varios servidores.** En otras palabras, está creando una aplicación distribuida y estos varios usuarios van a estar en distintos equipos host desde donde se ejecuta el código. Los usuarios van a tener acceso al código a través de Internet o a través de una red privada. La interfaz de usuario se va a presentar a través del explorador o quizás una aplicación personalizada, como una aplicación basada en formularios escrita con Microsoft Visual Basic o MFC. Esa interfaz de usuario se va a ubicar en el equipo cliente.
-   **La aplicación COM+ se puede convertir en escalable y puede proporcionar mayor disponibilidad y confiabilidad mediante la implementación de la aplicación en varios equipos servidor.** Al hacerlo, puede equilibrar la carga de trabajo de la aplicación y proporcionar tolerancia a errores mediante el uso de la organización por clústeres de Windows.
-   **Si hay algún problema, el estado de los datos persistentes, almacenados en una base de datos, de una aplicación COM+ se mantendrá si utiliza transacciones.** El estado de la aplicación debe sobrevivir a los accidentes que puedan producirse, como errores de aplicación, bloqueos del sistema o errores de red.

## <a name="principles"></a>Principios

Además de estas tres suposiciones, los siguientes principios pervade el modelo de programación de COM+:

-   **La lógica de la aplicación residirá en los equipos servidor, no en los equipos cliente.** Hay tres razones principales para hacerlo:
    -   Es posible que el equipo cliente no tenga la potencia de procesamiento o las características necesarias para ejecutar la lógica de la aplicación. Además, mantener la lógica de la aplicación en el servidor simplifica la implementación.
    -   Los equipos servidor suelen estar más cerca de los datos y estos datos suelen estar en una base de datos. Dado que la aplicación está accediendo a las bases de datos, querrá ser muy sensible al costo de las conexiones de base de datos. Al colocar la mayor parte de la lógica en los equipos servidor, puede compartir las conexiones de base de datos y obtener una mejora significativa en el rendimiento. Hay otros recursos en los equipos del servidor que también se pueden compartir, de nuevo con una ventaja de rendimiento.
    -   Tener la lógica de aplicación en los equipos servidor mantiene el control del contexto de seguridad con la aplicación. Tiene más control sobre la seguridad si mantiene esa seguridad en componentes de aplicaciones que se ejecutan en equipos servidor en lugar de en equipos cliente.
-   **Las transacciones son el núcleo.** Por diseño, las transacciones de forma que contengan el modelo de programación COM+ que sea muy importante para comprenderlos. Aunque puede usar muchos de los servicios de COM+ sin usar transacciones, si decide no utilizarlos, no puede aprovechar al máximo los servicios COM+ que tiene a su disposición. Entre las ventajas importantes del uso de transacciones se incluyen las siguientes:
    -   Las transacciones son una solución razonable para el problema de la administración de simultaneidad. Además, las transacciones ayudan a protegerse contra los bloqueos y tienen un buen modelo de recuperación de errores. Además, las transacciones se convierten en una excelente manera de administrar tareas en varios sistemas.
    -   Puede diseñar una aplicación COM+ basada en transacciones para trabajar con un administrador de recursos y una base de datos, lo que ayuda a proteger la mayoría de la información de estado. Al mantener el estado dentro de una base de datos u otro almacenamiento administrado por un administrador de recursos, no es necesario mantener muchos Estados dentro de los objetos reales que crea la aplicación. Aunque esto es una salida de un modelo orientado a objetos puro, funciona bien para crear aplicaciones distribuidas con recuperación de errores.
-   **La funcionalidad de la aplicación se genera como objetos COM, ajustando los protocolos que se usan para comunicarse con otros sistemas o tecnologías.** Dado que es probable que cree componentes que van a unir varias tecnologías o sistemas heredados, planee el uso de diversos protocolos de comunicación. Use HTTP para la comunicación de cliente/servidor o de aplicación a aplicación a través de Internet. Use DCOM para la comunicación de aplicación a aplicación o de componente a componente en el servidor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Directrices básicas para diseñar aplicaciones COM+](basic-guidelines-for-designing-com--applications.md)
</dt> <dt>

[Diseñar la aplicación COM+ mediante UML](designing-the-com--application-using-uml.md)
</dt> <dt>

[Sugerencias de diseño generales para el uso de COM+](general-design-tips-for-using-com-.md)
</dt> <dt>

[Optimizar interacciones con el nivel de lógica de negocios de COM+](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> <dt>

[Otras herramientas de Microsoft para compilar aplicaciones distribuidas](other-microsoft-tools-for-building-distributed-applications.md)
</dt> </dl>

 

 



