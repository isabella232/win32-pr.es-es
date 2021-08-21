---
description: Una vez completados los modelos conceptuales y lógicos, puede tomar decisiones sobre la implementación física de la aplicación.
ms.assetid: 18c440f0-88c8-4738-9f29-c82772439b51
title: 'Modelo físico: arquitectura de aplicación'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5147241b460763b4218734344340291af5c423c2ee2e7a8ec9e485b30221d795
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118812220"
---
# <a name="the-physical-model-application-architecture"></a>Modelo físico: arquitectura de aplicación

Una vez completados los modelos conceptuales y lógicos, puede tomar decisiones sobre la implementación física de la aplicación. Para crear el modelo físico, debe comprender dónde se deben encontrar los distintos servicios de la aplicación y cómo se deben implementar. Determinar dónde residen varios servicios debe ir antes de cómo se implementarán los servicios.

Una regla básica para determinar dónde residen varios servicios es esta: coloque el componente donde se usa. Por ejemplo, si un componente muestra información para el cliente base, debe ir en el equipo del usuario. Si un componente valida la información del cliente base, también debe residir en el equipo del cliente base. Si un componente actualiza la información de una base de datos, debe residir en el servidor de bases de datos.

Por supuesto, hay consideraciones adicionales que hacen excepciones a esta regla. Los problemas de rendimiento y seguridad también pueden determinar dónde se encuentra un componente. Tenga en cuenta lo siguiente.

-   ¿Va a cambiar con frecuencia un componente, lo que dificulta la distribución de actualizaciones?
-   ¿Usarán el componente otras aplicaciones, como un componente de comprobación de seguridad común?
-   ¿El componente realiza cálculos largos o realiza funciones, como la impresión, que se pueden descargar en un servidor?
-   ¿Se puede mejorar la seguridad de un componente si se coloca en un servidor?

Localizar correctamente los componentes de una aplicación también puede aislar al equipo de desarrollo de la costosa recuperación si cambia el sistema o la ubicación de los datos. Por ejemplo, al colocar las reglas de acceso a datos en una capa de datos en lugar de en procedimientos almacenados, la aplicación se aísla más fácilmente de la dependencia de un DBMS específico. No solo se limitan los cambios y se prueban compartimentados, sino que se pueden cambiar los orígenes de datos y distribuir los datos sin cambiar fundamentalmente la aplicación.

Por último, la búsqueda de componentes debe aprovechar las eficiencias del sistema. Es tiempo y rentable colocar objetos empresariales en ubicaciones centralizadas en la red. Los objetos se pueden compartir entre aplicaciones y las pruebas unitarias se pueden realizar antes de implementar cualquier componente. También se pueden reducir los costos de mantenimiento porque los cambios en las reglas solo se producen en un único punto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelo conceptual: requisitos de la aplicación](the-conceptual-model--application-requirements.md)
</dt> <dt>

[El modelo lógico: definición y planeamiento de la aplicación](the-logical-model--application-definition-and-planning.md)
</dt> </dl>

 

 



