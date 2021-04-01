---
description: Una vez completados los modelos lógicos y conceptuales, puede tomar decisiones sobre la implementación física de la aplicación.
ms.assetid: 18c440f0-88c8-4738-9f29-c82772439b51
title: 'El modelo físico: arquitectura de la aplicación'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f0fab87d76e445a365958ab330f572f657d1505
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153458"
---
# <a name="the-physical-model-application-architecture"></a>El modelo físico: arquitectura de la aplicación

Una vez completados los modelos lógicos y conceptuales, puede tomar decisiones sobre la implementación física de la aplicación. Para crear el modelo físico, debe saber dónde se deben ubicar los distintos servicios de la aplicación y cómo deben implementarse. La determinación de dónde residan los distintos servicios debe ir antes de que se implementen los servicios.

Una regla básica para determinar dónde residen los distintos servicios es: Coloque el componente en el que se está usando. Si, por ejemplo, un componente muestra información para el cliente base, debe ir en el equipo del usuario. Si un componente valida la información del cliente base, también debe residir en el equipo del cliente base. Si un componente actualiza la información en una base de datos, debe residir en el servidor de base de datos.

Por supuesto, existen consideraciones adicionales que realizan excepciones a esta regla. Los problemas de rendimiento y seguridad también pueden indicar dónde se encuentra un componente. Tenga en cuenta lo siguiente.

-   ¿Un componente va a cambiar con frecuencia, lo que dificulta la distribución de las actualizaciones?
-   ¿Usará el componente otras aplicaciones, como un componente de comprobación de seguridad común?
-   ¿El componente realiza cálculos largos o realiza funciones, como la impresión, que se pueden descargar en un servidor?
-   ¿Se puede mejorar la seguridad de un componente colocándolo en un servidor?

La ubicación correcta de los componentes de una aplicación también puede aislar al equipo de desarrollo de la recodificación costosa si el sistema o la ubicación de los datos cambian. Por ejemplo, si coloca las reglas de acceso a datos en una capa de datos en lugar de en procedimientos almacenados, la aplicación se aislará más fácilmente de la dependencia de un DBMS específico. No solo los cambios se limitan y prueban en compartimentos, pero los orígenes de datos se pueden cambiar y los datos se pueden distribuir sin cambiar fundamentalmente la aplicación.

Por último, la ubicación de los componentes debe aprovechar las eficiencias del sistema. Es tiempo y rentable colocar objetos de negocio en ubicaciones centralizadas en la red. Los objetos se pueden compartir entre aplicaciones y las pruebas unitarias se pueden realizar antes de que se implementen los componentes. También se pueden reducir los costos de mantenimiento, ya que los cambios de regla solo se producen en un único punto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[El modelo conceptual: requisitos de la aplicación](the-conceptual-model--application-requirements.md)
</dt> <dt>

[El modelo lógico: definición y planeación de la aplicación](the-logical-model--application-definition-and-planning.md)
</dt> </dl>

 

 



