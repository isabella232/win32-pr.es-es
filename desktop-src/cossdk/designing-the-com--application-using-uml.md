---
description: El desarrollo de una aplicación COM+ correcta requiere un diseño de arquitectura de aplicación por adelantado.
ms.assetid: 6a7cc610-e09a-4097-bc31-4e53db0ee152
title: Diseño de la aplicación COM+ mediante UML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48526623df5bc929daa4d8ce9cbe4d7592d6b30c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465694"
---
# <a name="designing-the-com-application-using-uml"></a>Diseño de la aplicación COM+ mediante UML

El desarrollo de una aplicación COM+ correcta requiere un diseño de arquitectura de aplicación por adelantado. El Lenguaje unificado de modelado (UML) es clave para este desarrollo de diseño. UML es una notación de modelado para los datos y procesos de la aplicación que combina los procedimientos recomendados del sector de software. Dado que UML divide la aplicación en tres vistas que reflejan la aplicación, así como su empaquetado e implementación, la notación de modelado se extiende bien para admitir el modelado empresarial.

UML aborda tres vistas de la aplicación, como se muestra a continuación:

-   La vista estática, que se modela mediante la información tomada de escenarios de usuario y diagramas de clases.
-   La vista dinámica, que se modela mediante diagramas de secuencia, colaboración y transición de estado.
-   La vista funcional, que es la narrativa descriptiva más tradicional mediante pseudocódigo y especificaciones.

La información de estas vistas se puede recopilar siguiendo tres pasos de diseño que funcionan bien con uml. Antes de escribir una sola línea de código, debe crear los siguientes modelos:

<dl> <dt>

<span id="Conceptual_model"></span><span id="conceptual_model"></span><span id="CONCEPTUAL_MODEL"></span>Modelo conceptual
</dt> <dd>

Decida qué componentes y servicios son necesarios.

</dd> <dt>

<span id="Logical_model"></span><span id="logical_model"></span><span id="LOGICAL_MODEL"></span>Modelo lógico
</dt> <dd>

Determine a qué nivel de diseño lógico pertenecen.

</dd> <dt>

<span id="Physical_model"></span><span id="physical_model"></span><span id="PHYSICAL_MODEL"></span>Modelo físico
</dt> <dd>

Determine dónde residen físicamente los componentes y cómo se van a codificar.

</dd> </dl>

Estos modelos se pueden usar con las herramientas CASE basadas en UML. Para obtener más información sobre estos tres modelos de diseño, vea los temas siguientes en esta sección:

-   [Modelo conceptual: requisitos de la aplicación](the-conceptual-model--application-requirements.md)
-   [El modelo lógico: definición y planeamiento de la aplicación](the-logical-model--application-definition-and-planning.md)
-   [Modelo físico: arquitectura de aplicación](the-physical-model--application-architecture.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Suposiciones y principios de diseño de COM+](com--design-assumptions-and-principles.md)
</dt> <dt>

[Diseño general Sugerencias para usar COM+](general-design-tips-for-using-com-.md)
</dt> <dt>

[Optimización de interacciones con el nivel de lógica de negocios de COM+](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> <dt>

[Otras herramientas de Microsoft para compilar aplicaciones distribuidas](other-microsoft-tools-for-building-distributed-applications.md)
</dt> </dl>

 

 



