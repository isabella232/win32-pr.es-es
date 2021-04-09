---
description: COM+ proporciona varias características de seguridad que puede usar para ayudar a proteger las aplicaciones COM+, desde los servicios que configure de forma administrativa a las API a las que puede llamar desde el código.
ms.assetid: 686fb391-d337-41b4-bb51-b70f27a0c300
title: Conceptos de seguridad de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ca5126f4b715f84c2b8801c8ec1adc29b3cbb83
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080272"
---
# <a name="com-security-concepts"></a>Conceptos de seguridad de COM+

COM+ proporciona varias características de seguridad que puede usar para ayudar a proteger las aplicaciones COM+, desde los servicios que configure de forma administrativa a las API a las que puede llamar desde el código.

Siempre que sea posible, en el caso de las aplicaciones COM+, es mejor usar la seguridad automática, como la seguridad basada en roles y la autenticación declarativas, en lugar de configurar la seguridad dentro de los componentes. El uso de la seguridad automática facilita la escritura y el mantenimiento de los componentes, facilita el diseño de la seguridad en toda la aplicación y, puesto que se configura administrativamente, es más fácil modificar la Directiva de seguridad de una aplicación. Estos servicios de seguridad automático permiten dejar toda la funcionalidad relacionada con la seguridad de sus componentes. Cuando puede activar los servicios y configurarlos de forma adecuada, COM+ controlará los detalles de la aplicación de la Directiva de seguridad que especifique.

Sin embargo, cuando los servicios de seguridad automáticos de COM+ no hacen exactamente lo que necesita, puede ampliarlos, compilando en la plataforma de seguridad automática que proporciona COM+. En los casos en los que decida no usar la seguridad automática o donde quiera usarla pero necesite basarse en ella para satisfacer los requisitos de seguridad de su aplicación, tiene las siguientes opciones para configurar la seguridad mediante programación:

-   Seguridad basada en roles mediante programación, por ejemplo, la comprobación de roles, que está disponible cuando se habilita la seguridad basada en roles para la aplicación.
-   Suplantación: para cuando desee usar la identidad de un cliente para tener acceso a un recurso protegido.
-   Características de auditoría basadas en la información de contexto de llamada de seguridad, que también está disponible cuando se habilita la seguridad basada en roles.

Los mecanismos que se usan para ayudar a proteger una aplicación determinada dependerán de los requisitos específicos de esa aplicación. Algunas opciones de seguridad pueden afectar al modo en que se escriben los componentes y otros pueden afectar significativamente al diseño de la aplicación. Antes de tomar decisiones sobre cómo implementar una estrategia de seguridad para una aplicación, debe tener en cuenta sus requisitos de seguridad en el contexto de su diseño general (requisitos de rendimiento, acceso a datos, diseño físico) y elegir la combinación más adecuada de características de seguridad. Para obtener más información sobre cómo implementar la seguridad mediante programación, vea [seguridad de componentes de programación](programmatic-component-security.md).

Aquí se proporcionan descripciones breves de las categorías, características y problemas de seguridad de COM+, con vínculos a los temas de esta sección que proporcionan una explicación detallada de cada una de las áreas importantes.

> [!Note]  
> Aunque no se trata en esta sección, los componentes en cola también tienen problemas específicos relacionados con las características de seguridad que están disponibles para ellos. Para obtener más información, vea [seguridad de componentes en cola](queued-components-security.md) y [desarrollar componentes en cola](developing-queued-components.md).

 

## <a name="role-based-security"></a>Seguridad basada en roles

La seguridad basada en roles es la característica central de la seguridad de las aplicaciones COM+. Mediante el uso de roles, puede crear de forma administrativa una directiva de autorización para una aplicación, eligiendo (hasta el nivel de método, si es necesario) a qué usuarios pueden acceder los recursos. Además, los roles proporcionan un marco para aplicar la comprobación de seguridad en el código si la aplicación requiere un control de acceso más específico.

La seguridad basada en roles se basa en un mecanismo general que permite recuperar información de seguridad con respecto a todos los llamadores ascendentes en la cadena de llamadas al componente. Esta característica es útil especialmente si desea realizar auditorías y registros detallados. Para obtener una descripción de las características de auditoría proporcionadas por COM+, vea [acceso a la información de contexto de llamada de seguridad](accessing-security-call-context-information.md).

Para obtener una descripción de los problemas de seguridad y administración basados en roles que debe tener en cuenta al usarlo, consulte [Administración de la seguridad basada en roles](role-based-security-administration.md).

## <a name="client-authentication"></a>Autenticación de clientes

Para poder autorizar a los clientes a tener acceso a los recursos, debe estar seguro de que son quienes dicen ser. Para habilitar esta comprobación de identidad, COM+ proporciona servicios de autenticación. Aunque estos servicios se proporcionan realmente en un nivel más fundamental mediante COM y Microsoft Windows, una aplicación COM+ le permite simplemente activar el servicio de autenticación de forma administrativa para que funcione en segundo plano, sea transparente para la aplicación. Para obtener una descripción de los servicios de autenticación, consulte [autenticación del cliente](client-authentication.md).

## <a name="client-impersonation-and-delegation"></a>Suplantación y delegación de cliente

En algunos casos, la aplicación debe realizar trabajo en nombre de un cliente mediante la identidad del cliente, por ejemplo, al obtener acceso a una base de datos que va a autenticar al cliente original. Esto requiere que la aplicación suplante al cliente. COM+ proporciona funciones para habilitar diversos niveles de suplantación. La suplantación se configura administrativamente, pero también debe proporcionar compatibilidad para la suplantación con el código de los componentes de la aplicación. Para obtener una descripción de la suplantación y los problemas relacionados con su uso, vea [suplantación y delegación del cliente](client-impersonation-and-delegation.md).

## <a name="using-the-software-restriction-policy-in-com"></a>Usar la Directiva de restricción de software en COM+

Una directiva de restricción de software proporciona una manera de ejecutar código que no es de confianza y, por tanto, potencialmente perjudicial, en un entorno restringido para que no pueda utilizar el uso incorrecto de los privilegios del usuario. Esto se realiza mediante la asignación de niveles de confianza a los archivos que el usuario puede ejecutar. Por ejemplo, algunos archivos del sistema pueden ser de plena confianza y tener un acceso no restringido a los privilegios del usuario, mientras que un archivo que se haya descargado de Internet podría no ser de confianza y, por tanto, solo se puede ejecutar en un entorno restringido en el que no se permita el uso de privilegios de usuario confidenciales de seguridad.

La Directiva de restricción de software para todo el sistema se controla a través de la herramienta administrativa Directiva de seguridad local, que permite a los administradores configurar niveles de confianza para archivos individuales. Sin embargo, todas las aplicaciones de servidor COM+ se ejecutan en el archivo de dllhost.exe. Por lo tanto, COM+ proporciona una manera de especificar la Directiva de restricción de software para cada aplicación de servidor, de modo que no sea necesario depender de la Directiva de restricción del archivo de dllhost.exe. Para obtener una explicación sobre cómo usar la Directiva de restricción de software en COM+, consulte [usar la Directiva de restricción de software en com+](using-the-software-restriction-policy-in-com-.md).

## <a name="library-application-security"></a>Seguridad de aplicaciones de biblioteca

Las aplicaciones de biblioteca tienen consideraciones de seguridad especiales. Dado que estas aplicaciones se ejecutan en el proceso del cliente, se ven afectadas por la seguridad impuesta por el proceso de hospedaje mientras no se puede controlar la seguridad de nivel de proceso. Para obtener una descripción de los factores que se deben tener en cuenta para las aplicaciones de biblioteca, vea [seguridad de aplicaciones de biblioteca](library-application-security.md).

## <a name="multi-tier-application-security"></a>Seguridad de aplicaciones de niveles múltiples

Las aplicaciones COM+ suelen ser aplicaciones de nivel intermedio; es decir, mueven información entre los clientes y los recursos de back-end, como las bases de datos. Se pueden aplicar opciones difíciles para determinar dónde se debe aplicar la seguridad y hasta qué punto. La seguridad implica de forma inherente a las ventajas del rendimiento. Algunas de las más graves se producen cuando se debe aplicar la comprobación de seguridad tanto en el nivel de datos como en el nivel intermedio. Para obtener una explicación de los problemas que se deben tener en cuenta, consulte [seguridad de aplicaciones de niveles múltiples](multi-tier-application-security.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Autenticación de cliente](client-authentication.md)
</dt> <dt>

[Suplantación y delegación de cliente](client-impersonation-and-delegation.md)
</dt> <dt>

[Tareas de seguridad de COM+](com--security-tasks.md)
</dt> <dt>

[Seguridad de aplicaciones de biblioteca](library-application-security.md)
</dt> <dt>

[Seguridad de aplicaciones de niveles múltiples](multi-tier-application-security.md)
</dt> <dt>

[Seguridad de componentes mediante programación](programmatic-component-security.md)
</dt> <dt>

[Administración de la seguridad basada en roles](role-based-security-administration.md)
</dt> <dt>

[Usar la Directiva de restricción de software en COM+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 



