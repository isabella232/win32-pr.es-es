---
description: La seguridad solo se comprueba en los límites de la aplicación.
ms.assetid: 32a05150-a68a-4302-9983-b9c1269b368c
title: Límites de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfcfca8868677ba14c8544657aa77acf04262805
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973495"
---
# <a name="security-boundaries"></a>Límites de seguridad

La seguridad solo se comprueba en los límites de la aplicación. Es decir, para dos componentes de la misma aplicación, cuando un componente llama al otro, no se realizará ninguna comprobación de seguridad. Sin embargo, si dos aplicaciones comparten el mismo proceso y un componente en uno llama a un componente en el otro, se realiza una comprobación de seguridad porque se cruza un límite de la aplicación. Del mismo modo, si dos aplicaciones residen en procesos de servidor diferentes y un componente de la primera aplicación llama a un componente en la segunda aplicación, se realiza una comprobación de seguridad.

Por lo tanto, si tiene dos componentes y desea que se realizan comprobaciones de seguridad cuando uno llama al otro, debe colocar los componentes en aplicaciones COM+ independientes.

Dado que las aplicaciones de biblioteca COM+ se hospedan en otros procesos, hay un límite de seguridad entre la aplicación de biblioteca y el proceso de hospedaje. Además, la aplicación de biblioteca no controla la seguridad de nivel de proceso, lo que afecta a cómo debe configurar la seguridad para ella. Para obtener más información, vea [Library Application Security](library-application-security.md).

La determinación de si se debe realizar una comprobación de seguridad en una llamada a un componente se basa en la propiedad de seguridad en el contexto de objeto creado cuando se crea una instancia del componente configurado. Para obtener más información, vea [Propiedad de contexto de seguridad](security-context-property.md).

## <a name="component-level-access-checks"></a>Component-Level de acceso

Para una aplicación de servidor COM+, tiene la opción de aplicar comprobaciones de acceso en el nivel de componente o en el nivel de proceso.

Al seleccionar la comprobación de acceso de nivel de componente, se habilitan las asignaciones de roles detalladas. Puede asignar roles a componentes, interfaces y métodos y lograr una directiva de autorización articulada. Esta será la configuración estándar para las aplicaciones que usan la seguridad basada en roles.

En el caso de las aplicaciones de biblioteca COM+, debe seleccionar la seguridad de nivel de componente si desea usar roles. Las aplicaciones de biblioteca no pueden usar la seguridad de nivel de proceso.

Debe seleccionar la comprobación de acceso de nivel de componente si usa la seguridad basada en roles mediante programación. La información del contexto de llamada de seguridad solo está disponible cuando la seguridad de nivel de componente está habilitada. Para obtener más información, vea [Información de contexto de llamada de seguridad](security-call-context-information.md).

Además, al seleccionar la comprobación de acceso de nivel de componente, la propiedad de seguridad se incluirá en el contexto del objeto. Esto significa que la configuración de seguridad puede desempeñar un papel en cómo se activa el objeto. Para obtener más información, vea [Propiedad de contexto de seguridad](security-context-property.md).

## <a name="process-level-access-checks"></a>Process-Level de acceso

Las comprobaciones de nivel de proceso solo se aplican al límite de la aplicación. Es decir, los roles que ha definido para toda la aplicación COM+ determinarán a quién se le concede acceso a cualquier recurso dentro de la aplicación. No se aplican asignaciones de roles más detalladas. Básicamente, los roles se usan para crear un descriptor de seguridad con el que se valida cualquier llamada a los componentes de la aplicación. En este caso, no le gustaría crear una directiva de autorización detallada con varios roles. La aplicación usará un único descriptor de seguridad.

En el caso de las aplicaciones de biblioteca COM+, no seleccionaría comprobaciones de acceso de nivel de proceso. La aplicación de biblioteca se ejecutará hospedada en el proceso del cliente y, por tanto, no controlará la seguridad de nivel de proceso. Para obtener más información, vea [Library Application Security](library-application-security.md).

Con las comprobaciones de acceso de nivel de proceso habilitadas, la información del contexto de llamada de seguridad no está disponible. Esto significa que no se puede realizar la seguridad mediante programación cuando solo se usa la seguridad de nivel de proceso. Para obtener más información, vea [Información de contexto de llamada de seguridad](security-call-context-information.md).

Además, la propiedad de seguridad no se incluirá en el contexto del objeto. Esto significa que cuando solo se usan comprobaciones de acceso de nivel de proceso, la configuración de seguridad nunca desempeñará un papel en la forma en que se activa el objeto. Para obtener más información, vea [Propiedad de contexto de seguridad](security-context-property.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Diseño eficaz de roles](designing-roles-effectively.md)
</dt> <dt>

[Información de contexto de llamada de seguridad](security-call-context-information.md)
</dt> <dt>

[Propiedad contexto de seguridad](security-context-property.md)
</dt> <dt>

[Uso de roles para la autorización de cliente](using-roles-for-client-authorization.md)
</dt> </dl>

 

 



