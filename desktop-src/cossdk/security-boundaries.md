---
description: La seguridad solo se comprueba en los límites de la aplicación.
ms.assetid: 32a05150-a68a-4302-9983-b9c1269b368c
title: Límites de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfcfca8868677ba14c8544657aa77acf04262805
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705370"
---
# <a name="security-boundaries"></a>Límites de seguridad

La seguridad solo se comprueba en los límites de la aplicación. Es decir, para dos componentes de la misma aplicación, cuando un componente llama a otro, no se realizará ninguna comprobación de seguridad. Sin embargo, si dos aplicaciones comparten el mismo proceso y un componente de en una llama a un componente en el otro, se realiza una comprobación de seguridad porque se cruza un límite de la aplicación. Del mismo modo, si dos aplicaciones residen en distintos procesos de servidor y un componente de la primera aplicación llama a un componente de la segunda aplicación, se realiza una comprobación de seguridad.

Por lo tanto, si tiene dos componentes y desea que las comprobaciones de seguridad se realicen cuando una llama a la otra, debe colocar los componentes en aplicaciones COM+ independientes.

Dado que otros procesos hospedan aplicaciones de biblioteca COM+, existe un límite de seguridad entre la aplicación de biblioteca y el proceso de hospedaje. Además, la aplicación de biblioteca no controla la seguridad de nivel de proceso, lo que afecta a la forma en que necesita configurar la seguridad para ella. Para obtener más información, vea [seguridad de aplicaciones de biblioteca](library-application-security.md).

Determinar si una comprobación de seguridad debe realizarse en una llamada a un componente se basa en la propiedad de seguridad en el contexto del objeto creado cuando se crea una instancia del componente configurado. Para obtener más información, vea [propiedad de contexto de seguridad](security-context-property.md).

## <a name="component-level-access-checks"></a>Comprobaciones de acceso Component-Level

En el caso de una aplicación de servidor COM+, tiene la opción de aplicar las comprobaciones de acceso en el nivel de componente o en el nivel de proceso.

Al seleccionar la comprobación de acceso de nivel de componente, se habilitan las asignaciones de roles específicas. Puede asignar roles a componentes, interfaces y métodos y lograr una directiva de autorización articulada. Esta será la configuración estándar para las aplicaciones que usan la seguridad basada en roles.

En el caso de las aplicaciones de biblioteca COM+, debe seleccionar seguridad de nivel de componente Si desea usar roles. Las aplicaciones de biblioteca no pueden utilizar la seguridad de nivel de proceso.

Debe seleccionar la comprobación de acceso de nivel de componente si usa la seguridad basada en roles mediante programación. La información del contexto de llamada de seguridad solo está disponible cuando está habilitada la seguridad de nivel de componente. Para obtener más información, vea [información sobre el contexto de llamada de seguridad](security-call-context-information.md).

Además, al seleccionar la comprobación de acceso de nivel de componente, la propiedad de seguridad se incluirá en el contexto del objeto. Esto significa que la configuración de seguridad puede desempeñar un rol en el modo en que se activa el objeto. Para obtener más información, vea [propiedad de contexto de seguridad](security-context-property.md).

## <a name="process-level-access-checks"></a>Comprobaciones de acceso Process-Level

Las comprobaciones de nivel de proceso solo se aplican al límite de la aplicación. Es decir, los roles que ha definido para toda la aplicación COM+ determinarán quién tiene acceso a cualquier recurso de la aplicación. No se aplican asignaciones de roles específicas. Esencialmente, los roles se usan para crear un descriptor de seguridad en el que se validan las llamadas a los componentes de la aplicación. En este caso, no querrá crear una directiva de autorización detallada con varios roles. La aplicación usará un solo descriptor de seguridad.

En el caso de las aplicaciones de biblioteca COM+, no se seleccionarán comprobaciones de acceso de nivel de proceso. La aplicación de biblioteca se ejecutará hospedada en el proceso del cliente y, por tanto, no controlará la seguridad de nivel de proceso. Para obtener más información, vea [seguridad de aplicaciones de biblioteca](library-application-security.md).

Con las comprobaciones de acceso de nivel de proceso habilitadas, la información de contexto de llamada de seguridad no está disponible. Esto significa que no se puede realizar la seguridad mediante programación cuando se usa solo la seguridad de nivel de proceso. Para obtener más información, vea [información sobre el contexto de llamada de seguridad](security-call-context-information.md).

Además, la propiedad de seguridad no se incluirá en el contexto del objeto. Esto significa que cuando se usan solo comprobaciones de acceso de nivel de proceso, la configuración de seguridad nunca desempeñará un rol en la forma en que se activa el objeto. Para obtener más información, vea [propiedad de contexto de seguridad](security-context-property.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Diseñar roles de forma eficaz](designing-roles-effectively.md)
</dt> <dt>

[Información de contexto de llamada de seguridad](security-call-context-information.md)
</dt> <dt>

[Propiedad de contexto de seguridad](security-context-property.md)
</dt> <dt>

[Uso de roles para la autorización de cliente](using-roles-for-client-authorization.md)
</dt> </dl>

 

 



