---
description: COM+ proporciona varias características de seguridad que puede usar para ayudar a proteger las aplicaciones COM+, desde los servicios que configura administrativamente hasta las API a las que puede llamar dentro del código.
ms.assetid: 686fb391-d337-41b4-bb51-b70f27a0c300
title: Conceptos de seguridad de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b93ac113cf4ff2b1c679936fd610c2d44f29689ff175930c6a67274002457d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047533"
---
# <a name="com-security-concepts"></a>Conceptos de seguridad de COM+

COM+ proporciona varias características de seguridad que puede usar para ayudar a proteger las aplicaciones COM+, desde los servicios que configura administrativamente hasta las API a las que puede llamar dentro del código.

Siempre que sea posible, en el caso de las aplicaciones COM+, es mejor usar la seguridad automática, como la autenticación y la seguridad basada en roles declarativas, en lugar de configurar la seguridad dentro de los componentes. El uso de la seguridad automática facilita la escritura y el mantenimiento de los componentes, facilita el diseño de la seguridad en toda una aplicación y, como está configurada administrativamente, es más fácil modificar la directiva de seguridad de una aplicación. Estos servicios de seguridad automáticos le hacen posible dejar toda la funcionalidad relacionada con la seguridad fuera de los componentes. Cuando pueda activar los servicios y configurarlos correctamente, COM+ controlará los detalles de la aplicación de la directiva de seguridad que especifique.

Sin embargo, cuando los servicios de seguridad automáticos de COM+ no hacen exactamente lo que necesita que hagan, puede ampliarlos, a través de la plataforma de seguridad automática proporcionada por COM+. En los casos en los que decida no usar la seguridad automática o donde desee usarla, pero necesite basarse en ella para satisfacer los requisitos de seguridad de la aplicación, tiene las siguientes opciones para configurar la seguridad mediante programación:

-   Seguridad basada en roles mediante programación, por ejemplo, la comprobación de roles, que está disponible cuando la seguridad basada en roles está habilitada para la aplicación.
-   Suplantación: para cuando quiera usar la identidad de un cliente para acceder a un recurso protegido.
-   Características de auditoría basadas en información de contexto de llamada de seguridad, también disponible cuando la seguridad basada en roles está habilitada.

Los mecanismos que use para ayudar a proteger una aplicación determinada dependerán de los requisitos concretos de esa aplicación. Algunas opciones de seguridad pueden afectar a la forma de escribir componentes y otras pueden afectar significativamente al diseño de la aplicación. Antes de tomar decisiones sobre cómo implementar una estrategia de seguridad para una aplicación, debe tener en cuenta sus requisitos de seguridad en el contexto de su diseño general (requisitos de rendimiento, acceso a datos, diseño físico) y elegir la combinación más adecuada de características de seguridad. Para obtener más información sobre cómo implementar la seguridad mediante programación, vea [Seguridad de componentes de programación](programmatic-component-security.md).

Aquí se proporcionan breves descripciones de categorías de seguridad, características y problemas de COM+, con vínculos a temas de esta sección que proporcionan una explicación detallada de cada una de las áreas importantes.

> [!Note]  
> Aunque no se describe en esta sección, los componentes en cola también tienen problemas concretos relacionados con las características de seguridad que están disponibles para ellos. Para obtener más información, [vea Queued Components Security](queued-components-security.md) and [Developing Queued Components](developing-queued-components.md).

 

## <a name="role-based-security"></a>Seguridad basada en roles

La seguridad basada en roles es la característica central de la seguridad de aplicaciones COM+. Con los roles, puede crear administrativamente una directiva de autorización para una aplicación, eligiendo (hasta el nivel de método, si es necesario) qué usuarios pueden acceder a los recursos. Además, los roles proporcionan un marco para aplicar la comprobación de seguridad dentro del código si la aplicación requiere un control de acceso más específico.

La seguridad basada en roles se basa en un mecanismo general que le permite recuperar información de seguridad relacionada con todos los llamadores ascendentes de la cadena de llamadas al componente. Esta instalación es útil especialmente si desea realizar auditorías y registros detallados. Para obtener una descripción de las características de auditoría proporcionadas por COM+, vea [Accessing Security Call Context Information](accessing-security-call-context-information.md).

Para obtener una descripción de los problemas de seguridad y administración basados en roles que debe tener en cuenta al usarlo, vea [Administración de seguridad basada en roles](role-based-security-administration.md).

## <a name="client-authentication"></a>Autenticación de clientes

Para poder autorizar a los clientes a tener acceso a los recursos, debe estar seguro de que son quienes dicen ser. Para habilitar esta comprobación de identidad, COM+ proporciona servicios de autenticación. Aunque estos servicios se proporcionan realmente en un nivel más fundamental mediante COM y Microsoft Windows, una aplicación COM+ le permite simplemente activar el servicio de autenticación de forma administrativa para que funcione en segundo plano, transparente para la aplicación. Para obtener una descripción de los servicios de autenticación, vea [Autenticación de cliente.](client-authentication.md)

## <a name="client-impersonation-and-delegation"></a>Suplantación y delegación de cliente

En algunos casos, la aplicación debe funcionar en nombre de un cliente mediante la identidad del cliente, por ejemplo, al acceder a una base de datos que va a autenticar al cliente original. Esto requiere que la aplicación suplante al cliente. COM+ proporciona funciones para habilitar varios niveles de suplantación. La suplantación se configura administrativamente, pero también debe proporcionar compatibilidad para la suplantación con el código de los componentes de la aplicación. Para obtener una descripción de la suplantación y los problemas relacionados con su uso, vea [Suplantación y delegación de cliente.](client-impersonation-and-delegation.md)

## <a name="using-the-software-restriction-policy-in-com"></a>Uso de la directiva de restricción de software en COM+

Una directiva de restricción de software proporciona una manera de ejecutar código que no es de confianza y, por tanto, potencialmente perjudicial, en un entorno restringido para que no pueda usar incorrectamente los privilegios del usuario. Para ello, asigna niveles de confianza a los archivos que el usuario puede ejecutar. Por ejemplo, ciertos archivos del sistema pueden ser de plena confianza y tener acceso sin restricciones a los privilegios del usuario, mientras que un archivo que se descargó de Internet podría no ser de plena confianza y, por tanto, puede ejecutarse solo en un entorno restringido en el que no se permite el uso de privilegios de usuario que tienen en cuenta la seguridad.

La directiva de restricción de software de todo el sistema se controla a través de la herramienta administrativa Directiva de seguridad local, que permite a los administradores configurar niveles de confianza para archivos individuales. Sin embargo, todas las aplicaciones de servidor COM+ se ejecutan en dllhost.exe archivo. Por lo tanto, COM+ proporciona una manera de especificar la directiva de restricción de software para cada aplicación de servidor para que no tenga que depender de la directiva de restricción del archivo dllhost.exe servidor. Para obtener una explicación sobre cómo usar la directiva de restricción de software en COM+, consulte Uso de la directiva de restricción [de software en COM+.](using-the-software-restriction-policy-in-com-.md)

## <a name="library-application-security"></a>Seguridad de la aplicación de biblioteca

Las aplicaciones de biblioteca tienen consideraciones de seguridad especiales. Dado que estas aplicaciones se ejecutan en el proceso del cliente, se ven afectadas por la seguridad que exige el proceso de hospedaje mientras no pueden controlar la seguridad de nivel de proceso. Para obtener una descripción de los factores que se deben tener en cuenta para las aplicaciones de biblioteca, vea [Library Application Security](library-application-security.md).

## <a name="multi-tier-application-security"></a>Seguridad de aplicaciones de niveles múltiples

Las aplicaciones COM+ suelen ser aplicaciones de nivel intermedio; es decir, mueven información entre clientes y recursos back-end como bases de datos. Se pueden tomar decisiones difíciles para determinar dónde se debe aplicar la seguridad y hasta qué punto. La seguridad implica intrínsecamente desventajas en el rendimiento. Algunas de las más graves se producen cuando se debe aplicar la comprobación de seguridad tanto en la capa de datos como en el nivel intermedio. Para obtener una explicación de los problemas que se deben tener en cuenta, [consulte Seguridad de aplicaciones de niveles múltiples.](multi-tier-application-security.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Autenticación de cliente](client-authentication.md)
</dt> <dt>

[Suplantación y delegación de cliente](client-impersonation-and-delegation.md)
</dt> <dt>

[Tareas de seguridad de COM+](com--security-tasks.md)
</dt> <dt>

[Seguridad de la aplicación de biblioteca](library-application-security.md)
</dt> <dt>

[Seguridad de aplicaciones de niveles múltiples](multi-tier-application-security.md)
</dt> <dt>

[Seguridad de componentes mediante programación](programmatic-component-security.md)
</dt> <dt>

[Administración de seguridad basada en roles](role-based-security-administration.md)
</dt> <dt>

[Uso de la directiva de restricción de software en COM+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 



