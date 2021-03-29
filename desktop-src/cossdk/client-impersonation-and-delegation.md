---
description: En algunas circunstancias, una aplicación de servidor necesita presentar una identidad de clientes a los recursos a los que se tiene acceso en el nombre de los clientes, normalmente para hacer que las comprobaciones de acceso o la autenticación se realicen en la identidad de los clientes.
ms.assetid: fd75eb54-eefe-411f-a7aa-0bc8628f8778
title: Suplantación y delegación de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7557dcde4cadf559dd8e116cf4e7bece4221aaae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666191"
---
# <a name="client-impersonation-and-delegation"></a>Suplantación y delegación de cliente

En algunas circunstancias, una aplicación de servidor necesita presentar la identidad de un cliente a los recursos a los que tiene acceso en nombre del cliente, normalmente para hacer que las comprobaciones de acceso o la autenticación se realicen en la identidad del cliente. En cierta medida, el servidor puede actuar bajo la identidad del cliente, una acción a la que se hace referencia como suplantar al cliente.

La *suplantación* es la capacidad de un subproceso de ejecutarse en un contexto de seguridad diferente del proceso que posee el subproceso. El subproceso de servidor utiliza un token de acceso que representa las credenciales del cliente y, con esto, puede tener acceso a los recursos a los que el cliente puede tener acceso.

El uso de la suplantación garantiza que el servidor puede hacer exactamente lo que puede hacer el cliente. El acceso a los recursos puede estar restringido o expandirse, en función de lo que el cliente tenga permiso para hacerlo.

Puede decidir que un servidor suplante a un cliente al conectarse a una base de datos para que la base de datos pueda autenticar y autorizar el cliente para sí mismo. O bien, si la aplicación tiene acceso a los archivos que están protegidos con un descriptor de seguridad y para permitir que el cliente obtenga acceso autorizado a la información de estos archivos, la aplicación puede suplantar al cliente antes de tener acceso a los archivos.

## <a name="how-to-implement-impersonation"></a>Cómo implementar la suplantación

La suplantación requiere la participación del cliente y del servidor (y, en algunos casos, de los administradores del sistema). El cliente debe indicar su voluntad para permitir que el servidor use su identidad y el servidor debe asumir explícitamente la identidad del cliente mediante programación. Para obtener más información, consulte los temas [requisitos del cliente para la suplantación](client-side-requirements-for-impersonation.md) y [los requisitos del servidor para la suplantación](server-side-requirements-for-impersonation.md).

## <a name="administrative-requirements-for-delegate-level-impersonation"></a>Requisitos administrativos para la suplantación de Delegate-Level

Para usar eficazmente la forma más eficaz de suplantación, la *delegación*, que es la suplantación de clientes a través de la red, las cuentas de usuario de cliente y servidor deben estar configuradas correctamente en el servicio de Active Directory para que sea compatible (además de la autoridad de concesión de cliente para realizar la suplantación de nivel de delegado), de la manera siguiente:

-   La identidad del servidor se debe marcar como "de confianza para delegación" en el servicio de Active Directory.
-   La identidad del cliente no se debe marcar como "la cuenta es importante y no se puede delegar" en el servicio de Active Directory.

Estas características de configuración proporcionan al administrador de dominio un alto grado de control sobre la delegación, que es deseable, dada la cantidad de confianza (y, por tanto, el riesgo de seguridad) que conlleva. Para obtener más información acerca de la delegación, consulte [delegación y suplantación](/windows/desktop/com/delegation-and-impersonation).

## <a name="cloaking"></a>Esconder

Junto con la autoridad que un cliente concede a un servidor a través del nivel de suplantación, la capacidad de Cloaking del servidor determina en gran medida cómo se comportará la suplantación. La ocultación afecta a qué identidad presenta realmente el servidor cuando realiza llamadas en el nombre del cliente (es decir, el propio o el del cliente). Para obtener más información, consulte [Cloaking](cloaking.md).

## <a name="performance-implications"></a>Implicaciones de rendimiento

La suplantación puede afectar significativamente al rendimiento y al escalado. Por lo general, es más caro suplantar a un cliente en una llamada que para hacer la llamada directamente. A continuación se indican algunos de los problemas que se deben tener en cuenta:

-   La sobrecarga computacional de pasar la identidad en patrones complicados, especialmente si está habilitado el Cloaking dinámico.
-   La complejidad general de la aplicación de comprobaciones de seguridad redundantes en numerosos lugares, en lugar de hacerlo de forma centralizada en el nivel intermedio.
-   Los recursos, como las conexiones de base de datos, cuando se abre la suplantación de un cliente, no se pueden reutilizar en varios clientes, un obstáculo muy grande para el escalado adecuado.

A veces, la única solución efectiva a un problema es usar la suplantación, pero esta decisión debe sopesarse con cuidado. Para obtener más información sobre estos problemas, consulte [seguridad de aplicaciones de niveles múltiples](multi-tier-application-security.md).

## <a name="queued-components"></a>Componentes en cola

[Los componentes en cola](com--queued-components.md) no admiten la suplantación. Cuando un cliente realiza una llamada a un objeto en cola, la llamada se realiza realmente a la grabadora, que la empaqueta como parte de un mensaje en el servidor. A continuación, el agente de escucha lee el mensaje de la cola y lo pasa al reproductor, que invoca el componente de servidor real y realiza la misma llamada de método. Como tal, cuando el servidor recibe la llamada, el token de cliente original no está disponible a través de la suplantación. La seguridad basada en roles se sigue aplicando, sin embargo, y la seguridad mediante programación con la interfaz [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) funcionará. Para obtener más información, vea [seguridad de componentes en cola](queued-components-security.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Autenticación de cliente](client-authentication.md)
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

 

 
