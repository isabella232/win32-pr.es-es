---
description: El desarrollo de una aplicación COM+ correcta requiere un diseño de arquitectura de aplicación inicial.
ms.assetid: 6a7cc610-e09a-4097-bc31-4e53db0ee152
title: Diseñar la aplicación COM+ mediante UML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48526623df5bc929daa4d8ce9cbe4d7592d6b30c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423316"
---
# <a name="designing-the-com-application-using-uml"></a>Diseñar la aplicación COM+ mediante UML

El desarrollo de una aplicación COM+ correcta requiere un diseño de arquitectura de aplicación inicial. El Lenguaje unificado de modelado (UML) es clave para este desarrollo de diseño. UML es una notación de modelado para los datos y procesos de la aplicación que combina los procedimientos recomendados del sector del software. Dado que el UML divide la aplicación en tres vistas que reflejan la aplicación, así como su empaquetado e implementación, la notación de modelado se amplía bien para admitir el modelado empresarial.

UML trata tres vistas de la aplicación, como se indica a continuación:

-   La vista estática, que está modelada por la información tomada de los escenarios de usuario y los diagramas de clases.
-   Vista dinámica, que se modela mediante diagramas de secuencia, colaboración y transición de estado.
-   La vista funcional, que es la narrativa más tradicional descriptivo con el pseudocódigo y las especificaciones.

La información de estas vistas se puede recopilar siguiendo los tres pasos de diseño que funcionan bien con el UML. Antes de escribir una sola línea de código, debe crear los siguientes modelos:

<dl> <dt>

<span id="Conceptual_model"></span><span id="conceptual_model"></span><span id="CONCEPTUAL_MODEL"></span>Modelo conceptual
</dt> <dd>

Decida qué componentes y servicios son necesarios.

</dd> <dt>

<span id="Logical_model"></span><span id="logical_model"></span><span id="LOGICAL_MODEL"></span>Modelo lógico
</dt> <dd>

Determine el nivel de diseño lógico al que pertenecen.

</dd> <dt>

<span id="Physical_model"></span><span id="physical_model"></span><span id="PHYSICAL_MODEL"></span>Modelo físico
</dt> <dd>

Determine dónde residen los componentes físicamente y cómo se van a codificar.

</dd> </dl>

Estos modelos se pueden usar con las herramientas de casos basados en UML. Para obtener más información sobre estos tres modelos de diseño, vea los temas siguientes en esta sección:

-   [El modelo conceptual: requisitos de la aplicación](the-conceptual-model--application-requirements.md)
-   [El modelo lógico: definición y planeación de la aplicación](the-logical-model--application-definition-and-planning.md)
-   [El modelo físico: arquitectura de la aplicación](the-physical-model--application-architecture.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Hipótesis y principios de diseño de COM+](com--design-assumptions-and-principles.md)
</dt> <dt>

[Sugerencias de diseño generales para el uso de COM+](general-design-tips-for-using-com-.md)
</dt> <dt>

[Optimizar interacciones con el nivel de lógica de negocios de COM+](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> <dt>

[Otras herramientas de Microsoft para compilar aplicaciones distribuidas](other-microsoft-tools-for-building-distributed-applications.md)
</dt> </dl>

 

 



