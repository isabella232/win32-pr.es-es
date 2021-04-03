---
title: Utilizar la UI Automation para pruebas automatizadas
description: En esta información general se describe cómo la automatización de la interfaz de usuario de Microsoft puede ser útil como marco para el acceso mediante programación en escenarios de pruebas automatizadas.
ms.assetid: 192162f9-55bf-4111-9f15-c0d3b5af2ab7
keywords:
- clientes, pruebas automatizadas de UI Automation
- clientes, pruebas automatizadas
- clientes, pruebas
- clientes, herramientas para pruebas automatizadas
- clientes, herramientas de automatización de la interfaz de usuario para pruebas automatizadas
- clientes, pruebas de UI Automation
- Automatización de la interfaz de usuario, pruebas automatizadas
- Automatización de la interfaz de usuario, prueba
- Automatización de la interfaz de usuario, herramientas para pruebas automatizadas
- pruebas automatizadas
- herramientas para pruebas automatizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 269ff32cae26f8bb8ea6bb5b55ac91f1e0486685
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075730"
---
# <a name="using-ui-automation-for-automated-testing"></a>Utilizar la UI Automation para pruebas automatizadas

En esta información general se describe cómo la automatización de la interfaz de usuario de Microsoft puede ser útil como marco para el acceso mediante programación en escenarios de pruebas automatizadas.

La automatización de la interfaz de usuario proporciona un modelo de objetos unificado que permite a todos los marcos de interfaz de usuario exponer funcionalidades complejas y enriquecidas de una manera accesible y fácil de automatizar.

La automatización de la interfaz de usuario se desarrolló como sucesor de Microsoft Active Accessibility, un marco diseñado para ofrecer una solución para hacer que los controles y las aplicaciones sean accesibles. Microsoft Active Accessibility no se diseñó pensando en la automatización de pruebas, aunque evolucionó en ese rol debido a los requisitos similares de accesibilidad y automatización. La automatización de la interfaz de usuario está diseñada específicamente para proporcionar una sólida funcionalidad para las pruebas automatizadas, además de proporcionar soluciones más refinadas para mejorar la accesibilidad. Por ejemplo, Microsoft Active Accessibility se basa en una única interfaz para exponer información sobre la interfaz de usuario y para recopilar la información necesaria para los productos de tecnología de asistencia; La automatización de la interfaz de usuario separa los dos modelos.

Tanto un proveedor como un cliente son necesarios para implementar la automatización de la interfaz de usuario para que sea útil como herramienta de pruebas automatizada. Los proveedores de automatización de la interfaz de usuario son aplicaciones, como Microsoft Word, Microsoft Excel y otras aplicaciones de terceros o controles basados en el sistema operativo Windows. Los clientes de automatización de interfaz de usuario incluyen scripts de pruebas y aplicaciones de tecnología de asistencia.

En este tema se incluyen las siguientes secciones.

-   [Automatización de la interfaz de usuario en proveedores](#ui-automation-in-providers)
-   [Automatización de la interfaz de usuario en clientes](#ui-automation-in-clients)
    -   [Acceso mediante programación](#programmatic-access)
-   [Propiedades de clave para la automatización de pruebas](#key-properties-for-test-automation)
-   [Herramientas y tecnologías relacionadas](#related-tools-and-technologies)
-   [Temas relacionados](#related-topics)

## <a name="ui-automation-in-providers"></a>Automatización de la interfaz de usuario en proveedores

Para automatizar un elemento de la interfaz de usuario, el desarrollador debe ver las acciones que puede realizar un usuario final en el objeto de interfaz de usuario mediante la interacción del mouse y el teclado estándar. Una vez identificadas estas acciones clave, los patrones de control de automatización de la interfaz de usuario que reflejan la funcionalidad y el comportamiento del elemento de la interfaz de usuario deben implementarse en el control. Por ejemplo, la interacción del usuario con un control de cuadro combinado suele implicar expandir y contraer el cuadro combinado para mostrar u ocultar una lista de elementos, seleccionar un elemento de la lista o agregar un nuevo valor mediante la entrada del teclado.

Con otros modelos de accesibilidad, los desarrolladores deben recopilar información directamente desde distintos botones, menús u otros controles individuales. Cada tipo de control incluye docenas de pequeñas variaciones. En otras palabras, aunque diez variaciones de un pulsador funcionan de la misma manera y llevan a cabo la misma función, todas deben tratarse como controles únicos. No hay ninguna manera de saber que estos controles sean funcionalmente equivalentes. Los patrones de control de UI Automation se desarrollaron para representar estos comportamientos de control comunes. Para obtener más información, consulta [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).

Sin el modelo unificado de patrones de control que proporciona la automatización de la interfaz de usuario, las herramientas de prueba y los desarrolladores deben tener información específica del marco de trabajo para exponer propiedades y controles de comportamiento en ese marco. Dado que varios marcos de interfaz de usuario pueden estar presentes al mismo tiempo en los sistemas operativos Windows, incluidos Microsoft Win32, Windows Forms y Windows Presentation Foundation (WPF), puede ser una tarea desalentadora para probar varias aplicaciones con controles que parezcan similares. Por ejemplo, en la tabla siguiente se enumeran los nombres de propiedades específicas del marco de trabajo necesarias para recuperar el nombre o el texto asociado a un control de botón y se muestra la propiedad de automatización de la interfaz de usuario equivalente.



| Tipo de control | Marco de interfaz de usuario | Propiedad específica del marco de trabajo | Propiedad de automatización de la interfaz de usuario |
|--------------|--------------|-----------------------------|------------------------|
| Botón       | WPF          | Contenido                     | Name (propiedad)          |
| Botón       | Win32        | Caption                     | Name (propiedad)          |
| Imagen        | HTML         | alt                         | Name (propiedad)          |



 

Los proveedores de automatización de la interfaz de usuario son responsables de asignar las propiedades específicas del marco de trabajo de sus controles a las propiedades equivalentes de automatización de la interfaz de usuario. Para obtener información sobre la implementación de la automatización de la interfaz de usuario en un proveedor, vea [la guía del programador del proveedor de UI Automation](uiauto-providerportal.md). Para obtener información sobre la implementación de patrones de control, vea [implementar patrones de control de automatización](uiauto-implementinguiautocontrolpatterns.md)de la interfaz de usuario.

## <a name="ui-automation-in-clients"></a>Automatización de la interfaz de usuario en clientes

El objetivo de las herramientas y los escenarios de pruebas automatizadas es la manipulación coherente y repetible de la interfaz de usuario. Por ejemplo, esto puede incluir controles específicos de pruebas unitarias y grabar y ejecutar scripts de prueba que recorren una serie de acciones genéricas en un grupo de controles.

Una complicación en las aplicaciones automatizadas es la dificultad de sincronizar una prueba con un destino dinámico, por ejemplo, un control de cuadro de lista, como el administrador de tareas de Windows, que muestra una lista de aplicaciones actualmente en ejecución. Dado que los elementos del cuadro de lista se actualizan dinámicamente fuera del control de la aplicación de prueba, es imposible repetir la selección de un elemento específico en el cuadro de lista con cualquier coherencia. Pueden surgir problemas similares al intentar repetir cambios de foco sencillos en una interfaz de usuario que está fuera del control de la aplicación de prueba.

### <a name="programmatic-access"></a>Acceso mediante programación

El acceso mediante programación ofrece la capacidad de imitar, mediante código, cualquier interacción y experiencia expuestos por mouse tradicional y entrada de teclado. La automatización de la interfaz de usuario permite el acceso mediante programación a través de cinco componentes:

-   El árbol de automatización de la interfaz de usuario facilita la navegación a través de la estructura de la interfaz de usuario. El árbol se crea a partir de la colección de **hWnd** s. Para obtener más información, vea [UI Automation Tree Overview](uiauto-treeoverview.md).
-   Los elementos de automatización son componentes individuales en la interfaz de usuario. A menudo pueden ser más granulares que un **hWnd**.
-   Las propiedades de automatización proporcionan información específica sobre los elementos de la interfaz de usuario. Para obtener más información, consulta [UI Automation Properties Overview](uiauto-propertiesoverview.md).
-   Los patrones de control definen un aspecto concreto de la funcionalidad de un control; puede constar de propiedad, método, evento e información de estructura. Para obtener más información, consulta [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).
-   Los eventos de automatización ofrecen información y notificaciones de eventos. Para obtener más información, consulta [UI Automation Events Overview](uiauto-eventsoverview.md).

## <a name="key-properties-for-test-automation"></a>Propiedades de clave para la automatización de pruebas

La capacidad de identificar de forma exclusiva y ubicar posteriormente cualquier control en la interfaz de usuario proporciona la base para que las aplicaciones de prueba automatizadas operen en esa interfaz de usuario. En la tabla siguiente se describen las propiedades de automatización de la interfaz de usuario que usan los clientes y los proveedores para identificar y buscar controles.



| Propiedad     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AutomationId | Distingue de forma única un elemento de automatización de sus elementos del mismo nivel. No es necesaria la compatibilidad con la propiedad AutomationId. Cuando está disponible, la propiedad AutomationId de un elemento es la misma en cualquier instancia de la aplicación, independientemente del idioma local. Aunque la propiedad AutomationId es única entre los elementos del mismo nivel, puede que no sea único en todo el escritorio. Por ejemplo, varias instancias de una aplicación o varias vistas de carpeta en el explorador de Microsoft Windows, pueden contener elementos con el mismo AutomationIdProperty, como "SystemMenuBar". Los clientes no deben hacer suposiciones sobre el AutomationIds expuesto por otras aplicaciones. No se garantiza que AutomationId sea estable en las distintas versiones o compilaciones de una aplicación. |
| ControlType  | Identifica el tipo de control representado por un elemento de automatización. Se puede deducir información significativa del conocimiento del tipo de control. Para obtener más información, consulta [UI Automation Control Types Overview](uiauto-controltypesoverview.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Nombre         | Cadena de texto que identifica o explica el propósito de un elemento de automatización. Debe utilizarse con precaución, ya que se puede localizar. La propiedad Name no es un identificador único entre elementos del mismo nivel. En la automatización de prueba, los clientes deben usar la propiedad AutomationId o la propiedad RuntimeId en su lugar.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| RuntimeId    | Matriz de enteros que representa un identificador para un elemento de automatización. El identificador es único en el escritorio, pero se garantiza que es único solo en la interfaz de usuario del escritorio en el que se generó. Los identificadores se pueden reutilizar con el tiempo. Use [**IUIAutomation:: CompareElements**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-compareelements) para determinar si el elemento que tiene actualmente un identificador en tiempo de ejecución determinado es el mismo elemento que anteriormente tenía ese ID. Además, el formato de la propiedad RuntimeId puede cambiar. Se debe tratar como un valor opaco y usarse solo para la comparación; por ejemplo, para determinar si un elemento de automatización está en la memoria caché.                                                                                                                       |



 

## <a name="related-tools-and-technologies"></a>Herramientas y tecnologías relacionadas

[Inspeccionar](inspect-objects.md) (Inspect.exe) es una herramienta basada en Windows que puede usar para recopilar información de automatización de la interfaz de usuario para el desarrollo y la depuración de proveedores y clientes. Inspeccionar se incluye en el kit de desarrollo de software (SDK) de Windows.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Consideraciones de seguridad de UI Automation](uiauto-securityoverview.md)
</dt> </dl>

 

 




