---
description: En algunas circunstancias, una aplicación de servidor debe presentar una identidad de clientes a los recursos a los que accede en nombre de los clientes, normalmente para que se realicen comprobaciones de acceso o autenticación en la identidad de los clientes.
ms.assetid: fd75eb54-eefe-411f-a7aa-0bc8628f8778
title: Suplantación y delegación de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8b0262f3d8dd6736d183fa76eb5d3f0946d50b2724e76bcea73843644aaefb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129377"
---
# <a name="client-impersonation-and-delegation"></a>Suplantación y delegación de cliente

En algunas circunstancias, una aplicación de servidor debe presentar la identidad de un cliente a los recursos a los que accede en nombre del cliente, normalmente para que se realicen comprobaciones de acceso o autenticación en la identidad del cliente. Hasta cierto punto, el servidor puede actuar bajo la identidad del cliente, una acción denominada suplantación del cliente.

*La suplantación* es la capacidad de un subproceso de ejecutarse en un contexto de seguridad diferente del del proceso que posee el subproceso. El subproceso de servidor usa un token de acceso que representa las credenciales del cliente y, con esto, puede acceder a los recursos a los que el cliente puede acceder.

El uso de la suplantación garantiza que el servidor puede hacer exactamente lo que el cliente puede hacer. El acceso a los recursos puede estar restringido o expandido, en función de lo que el cliente tenga permiso para hacer.

Puede optar por que un servidor suplante a un cliente al conectarse a una base de datos para que la base de datos pueda autenticarse y autorizar al cliente por sí mismo. O bien, si la aplicación accede a archivos protegidos con un descriptor de seguridad y para permitir que el cliente obtenga acceso autorizado a la información de estos archivos, la aplicación puede suplantar al cliente antes de acceder a los archivos.

## <a name="how-to-implement-impersonation"></a>Cómo implementar la suplantación

La suplantación requiere la participación tanto del cliente como del servidor (y, en algunos casos, de los administradores del sistema). El cliente debe indicar su disposición a permitir que el servidor use su identidad y el servidor debe asumir explícitamente la identidad del cliente mediante programación. Para obtener más información, vea los temas [Requisitos](client-side-requirements-for-impersonation.md) del lado cliente para la suplantación y Requisitos del lado servidor [para la suplantación.](server-side-requirements-for-impersonation.md)

## <a name="administrative-requirements-for-delegate-level-impersonation"></a>Requisitos administrativos para Delegate-Level suplantación

Para usar eficazmente la forma más eficaz de suplantación, delegación , que es la suplantación de clientes a través de la red, las cuentas de usuario de cliente y servidor deben configurarse correctamente en el servicio Active Directory para admitirlo (además de la autoridad de concesión de cliente para realizar la suplantación de nivel de delegado), como se muestra a continuación:

-   La identidad del servidor debe marcarse como "Trusted for delegation" (Confianza para la delegación) en Active Directory Service.
-   La identidad del cliente no debe marcarse como "La cuenta es confidencial y no se puede delegar" en Active Directory Service.

Estas características de configuración dan al administrador del dominio un alto grado de control sobre la delegación, lo que es deseable, dada la confianza (y, por tanto, el riesgo de seguridad) que implica. Para obtener más información sobre la delegación, vea [Delegación y suplantación.](/windows/desktop/com/delegation-and-impersonation)

## <a name="cloaking"></a>Ocultación

Junto con la autoridad que un cliente concede a un servidor a través del nivel de suplantación, la funcionalidad de ocultación del servidor determina en gran medida cómo se comportará la suplantación. La ocultación afecta a la identidad que presenta realmente el servidor cuando realiza llamadas en nombre del cliente, la suya propia o la del cliente. Para obtener más información, [vea Arroba.](cloaking.md)

## <a name="performance-implications"></a>Implicaciones de rendimiento

La suplantación puede afectar significativamente al rendimiento y al escalado. Por lo general, es más costoso suplantar a un cliente en una llamada que realizar la llamada directamente. Estos son algunos de los problemas que se deben tener en cuenta:

-   La sobrecarga computacional de pasar la identidad en patrones complicados, especialmente si está habilitada la dinámica.
-   La complejidad general de aplicar la comprobación de seguridad redundante en numerosos lugares, en lugar de simplemente centralmente en el nivel intermedio.
-   Los recursos, como las conexiones de base de datos, cuando se abren suplantando a un cliente, no se pueden reutilizar en varios clientes, un obstáculo muy grande para escalar bien.

A veces, la única solución eficaz a un problema es usar la suplantación, pero esta decisión debe ponderarse cuidadosamente. Para obtener más información sobre estos problemas, consulte [Seguridad de aplicaciones de niveles múltiples.](multi-tier-application-security.md)

## <a name="queued-components"></a>Componentes en cola

[Los componentes en cola](com--queued-components.md) no admiten la suplantación. Cuando un cliente realiza una llamada a un objeto en cola, la llamada se realiza realmente a la grabadora, que la empaqueta como parte de un mensaje al servidor. A continuación, el agente de escucha lee el mensaje de la cola y lo pasa al reproductor, que invoca el componente de servidor real y realiza la misma llamada de método. Por lo tanto, cuando el servidor recibe la llamada, el token de cliente original no está disponible mediante suplantación. Sin embargo, la seguridad basada en roles se sigue aplicando y la seguridad mediante programación mediante [**la interfaz ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) funcionará. Para obtener más información, vea [Queued Components Security](queued-components-security.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Autenticación de cliente](client-authentication.md)
</dt> <dt>

[Seguridad de aplicaciones de biblioteca](library-application-security.md)
</dt> <dt>

[Seguridad de aplicaciones de varios niveles](multi-tier-application-security.md)
</dt> <dt>

[Seguridad de componentes mediante programación](programmatic-component-security.md)
</dt> <dt>

[Administración de seguridad basada en roles](role-based-security-administration.md)
</dt> <dt>

[Uso de la directiva de restricción de software en COM+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 
