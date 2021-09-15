---
title: Utilizar la UI Automation para pruebas automatizadas
description: En esta introducción se describe cómo Microsoft Automatización de la interfaz de usuario puede ser útil como marco para el acceso mediante programación en escenarios de pruebas automatizadas.
ms.assetid: 192162f9-55bf-4111-9f15-c0d3b5af2ab7
keywords:
- clientes, Automatización de la interfaz de usuario pruebas automatizadas
- clientes, pruebas automatizadas
- clients,testing
- clients,tools for automated testing
- clients,Automatización de la interfaz de usuario herramientas para pruebas automatizadas
- clients,Automatización de la interfaz de usuario testing
- Automatización de la interfaz de usuario, pruebas automatizadas
- Automatización de la interfaz de usuario,testing
- Automatización de la interfaz de usuario,herramientas para pruebas automatizadas
- pruebas automatizadas
- herramientas para pruebas automatizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 269ff32cae26f8bb8ea6bb5b55ac91f1e0486685
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359226"
---
# <a name="using-ui-automation-for-automated-testing"></a>Utilizar la UI Automation para pruebas automatizadas

En esta introducción se describe cómo Microsoft Automatización de la interfaz de usuario puede ser útil como marco para el acceso mediante programación en escenarios de pruebas automatizadas.

Automatización de la interfaz de usuario proporciona un modelo de objetos unificado que permite a todos los marcos de interfaz de usuario exponer una funcionalidad compleja y enriquecida de una manera accesible y fácil de automatizar.

Automatización de la interfaz de usuario desarrolló como sucesor de Microsoft Active Accessibility, un marco diseñado para proporcionar una solución para hacer que los controles y las aplicaciones se puedan acceder a él. Microsoft Active Accessibility no se diseñó pensando en la automatización de pruebas, aunque evolucionó a ese rol debido a los requisitos similares de accesibilidad y automatización. Automatización de la interfaz de usuario está diseñado específicamente para proporcionar una funcionalidad sólida para las pruebas automatizadas, además de proporcionar soluciones más refinadas para la accesibilidad. Por ejemplo, Microsoft Active Accessibility se basa en una única interfaz para exponer información sobre la interfaz de usuario y recopilar la información necesaria para los productos de tecnología de asistencia. Automatización de la interfaz de usuario separa los dos modelos.

Tanto un proveedor como un cliente deben implementar Automatización de la interfaz de usuario para que sea útil como una herramienta de prueba automatizada. Automatización de la interfaz de usuario son aplicaciones, como Microsoft Word, Microsoft Excel y otras aplicaciones o controles de terceros basados en el Windows operativo. Los clientes de automatización de interfaz de usuario incluyen scripts de pruebas y aplicaciones de tecnología de asistencia.

En este tema se incluyen las siguientes secciones.

-   [Automatización de la interfaz de usuario en proveedores](#ui-automation-in-providers)
-   [Automatización de la interfaz de usuario en clientes](#ui-automation-in-clients)
    -   [Acceso mediante programación](#programmatic-access)
-   [Propiedades de clave para la automatización de pruebas](#key-properties-for-test-automation)
-   [Herramientas y tecnologías relacionadas](#related-tools-and-technologies)
-   [Temas relacionados](#related-topics)

## <a name="ui-automation-in-providers"></a>Automatización de la interfaz de usuario en proveedores

Para automatizar un elemento de la interfaz de usuario, el desarrollador debe ver qué acciones puede realizar un usuario final en el objeto de interfaz de usuario mediante la interacción estándar con el teclado y el mouse. Una vez identificadas estas acciones clave, los patrones de control Automatización de la interfaz de usuario que reflejan la funcionalidad y el comportamiento del elemento de interfaz de usuario deben implementarse en el control . Por ejemplo, la interacción del usuario con un control de cuadro combinado normalmente implica expandir y contraer el cuadro combinado para mostrar u ocultar una lista de elementos, seleccionar un elemento de la lista o agregar un nuevo valor a través de la entrada de teclado.

Con otros modelos de accesibilidad, los desarrolladores deben recopilar información directamente desde distintos botones, menús u otros controles individuales. Cada tipo de control tiene decenas de variaciones menores. En otras palabras, aunque 10 variaciones de un botón de inserción funcionan de la misma manera y realizan la misma función, todas deben tratarse como controles únicos. No hay ninguna manera de saber que estos controles sean funcionalmente equivalentes. Automatización de la interfaz de usuario patrones de control se desarrollaron para representar estos comportamientos de control comunes. Para obtener más información, consulta [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).

Sin el modelo unificado de patrones de control proporcionado por Automatización de la interfaz de usuario, las herramientas de prueba y los desarrolladores deben tener información específica del marco para exponer las propiedades y controlar los comportamientos en ese marco. Dado que varios marcos de interfaz de usuario diferentes pueden estar presentes al mismo tiempo en sistemas operativos de Windows, incluidos Microsoft Win32, Windows Forms y Windows Presentation Foundation (WPF), puede ser una tarea desalentador probar varias aplicaciones con controles que parecen similares. Por ejemplo, en la tabla siguiente se enumeran los nombres de propiedad específicos del marco necesarios para recuperar el nombre o el texto asociado a un control de botón y se muestra la propiedad Automatización de la interfaz de usuario equivalente.



| Tipo de control | Marco de interfaz de usuario | Propiedad específica del marco | Automatización de la interfaz de usuario propiedad |
|--------------|--------------|-----------------------------|------------------------|
| Botón       | WPF          | Contenido                     | Name (propiedad)          |
| Botón       | Win32        | Caption                     | Name (propiedad)          |
| Imagen        | HTML         | alt                         | Name (propiedad)          |



 

Automatización de la interfaz de usuario proveedores de recursos son responsables de asignar las propiedades específicas del marco de sus controles a las propiedades Automatización de la interfaz de usuario equivalentes. Para obtener información sobre cómo implementar Automatización de la interfaz de usuario en un proveedor, vea Automatización de la interfaz de usuario Guía del [programador del proveedor de proveedores](uiauto-providerportal.md). Para obtener información sobre cómo implementar patrones de control, vea [Implementing Automatización de la interfaz de usuario Control Patterns](uiauto-implementinguiautocontrolpatterns.md).

## <a name="ui-automation-in-clients"></a>Automatización de la interfaz de usuario en clientes

El objetivo de los escenarios y las herramientas de prueba automatizadas es la manipulación coherente y repetible de la interfaz de usuario. Por ejemplo, esto puede implicar la realización de pruebas unitarias de controles específicos y la grabación y ejecución de scripts de prueba que recorren en iteración una serie de acciones genéricas en un grupo de controles.

Una complicación en las aplicaciones automatizadas es la dificultad de sincronizar una prueba con un destino dinámico, por ejemplo, un control de cuadro de lista, como Windows Administrador de tareas, que muestra una lista de aplicaciones que se están ejecutando actualmente. Dado que los elementos del cuadro de lista se actualizan dinámicamente fuera del control de la aplicación de prueba, es imposible repetir la selección de un elemento específico en el cuadro de lista con cualquier coherencia. Pueden surgir problemas similares al intentar repetir cambios de foco sencillos en una interfaz de usuario que está fuera del control de la aplicación de prueba.

### <a name="programmatic-access"></a>Acceso mediante programación

El acceso mediante programación ofrece la capacidad de imitar, mediante código, cualquier interacción y experiencia expuestos por mouse tradicional y entrada de teclado. Automatización de la interfaz de usuario permite el acceso mediante programación a través de cinco componentes:

-   El Automatización de la interfaz de usuario facilita la navegación a través de la estructura de la interfaz de usuario. El árbol se genera a partir de la colección **de HWND.** Para obtener más información, [vea Información general Automatización de la interfaz de usuario árbol de árbol.](uiauto-treeoverview.md)
-   Los elementos de automatización son componentes individuales de la interfaz de usuario. A menudo, pueden ser más pormenorizados que **un HWND.**
-   Las propiedades de Automation proporcionan información específica sobre los elementos de la interfaz de usuario. Para obtener más información, consulta [UI Automation Properties Overview](uiauto-propertiesoverview.md).
-   Los patrones de control definen un aspecto concreto de la funcionalidad de un control; puede constar de propiedad, método, evento e información de estructura. Para obtener más información, consulta [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).
-   Los eventos de automatización ofrecen información y notificaciones de eventos. Para obtener más información, consulta [UI Automation Events Overview](uiauto-eventsoverview.md).

## <a name="key-properties-for-test-automation"></a>Propiedades de clave para la automatización de pruebas

La capacidad de identificar y localizar de forma única cualquier control en la interfaz de usuario proporciona la base para que las aplicaciones de prueba automatizadas funcionen en esa interfaz de usuario. Automatización de la interfaz de usuario las propiedades usadas por clientes y proveedores para identificar y localizar controles se describen en la tabla siguiente.



| Propiedad     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AutomationId | Distingue de forma única un elemento de automatización de sus elementos del mismo nivel. No se requiere compatibilidad con la propiedad AutomationId. Cuando está disponible, la propiedad AutomationId de un elemento es la misma en cualquier instancia de la aplicación, independientemente del idioma local. Aunque la propiedad AutomationId es única entre los elementos del mismo nivel, puede que no sea única en todo el escritorio. Por ejemplo, varias instancias de una aplicación o varias vistas de carpeta en Microsoft Windows Explorer pueden contener elementos con la misma AutomationIdProperty, como "SystemMenuBar". Los clientes no deben realizar suposiciones con respecto a los AutomationIds expuestos por otras aplicaciones. No se garantiza que AutomationId sea estable en diferentes versiones o compilaciones de una aplicación. |
| ControlType  | Identifica el tipo de control representado por un elemento de automatización. Se puede deducir información significativa del conocimiento del tipo de control. Para obtener más información, consulta [UI Automation Control Types Overview](uiauto-controltypesoverview.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Nombre         | Cadena de texto que identifica o explica el propósito de un elemento de automatización. Debe usarse con precaución porque se puede localizar. La propiedad Name no es un identificador único entre los elementos del mismo nivel. Para la automatización de pruebas, los clientes deben usar la propiedad AutomationId o la propiedad RuntimeId en su lugar.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| RuntimeId    | Matriz de enteros que representan un identificador para un elemento de automatización. El identificador es único en el escritorio, pero se garantiza que es único solo para la interfaz de usuario del escritorio en el que se generó. Los identificadores se pueden reutilizar con el tiempo. Use [**IUIAutomation::CompareElements**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-compareelements) para determinar si el elemento que tiene actualmente un identificador de tiempo de ejecución determinado es el mismo elemento que tenía anteriormente ese identificador. Además, el formato de la propiedad RuntimeId puede cambiar. Debe tratarse como un valor opaco y usarse solo para la comparación. por ejemplo, para determinar si un elemento de automatización está en la memoria caché.                                                                                                                       |



 

## <a name="related-tools-and-technologies"></a>Herramientas y tecnologías relacionadas

[Inspect](inspect-objects.md) (Inspect.exe) es una herramienta basada en Windows que se puede usar para recopilar información Automatización de la interfaz de usuario para el desarrollo y la depuración de clientes y proveedores. Inspect se incluye en Windows Software Development Kit (SDK).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Automatización de la interfaz de usuario consideraciones de seguridad](uiauto-securityoverview.md)
</dt> </dl>

 

 




