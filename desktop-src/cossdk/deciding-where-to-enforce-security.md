---
description: Las ventajas e inconvenientes son inherentes a la exigencia de seguridad.
ms.assetid: f01573f3-aae6-400e-bdd9-6f34f4e262f6
title: Decidir dónde aplicar la seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ac994fb98d50a7e26f1b8142e77dc9ff771f6b2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538596"
---
# <a name="deciding-where-to-enforce-security"></a>Decidir dónde aplicar la seguridad

Las ventajas e inconvenientes son inherentes a la exigencia de seguridad. Una base de datos puede ser un lugar natural para colocar la lógica de seguridad, dado que en última instancia los datos son los más importantes que se deben proteger. Sin embargo, esto tiene importantes implicaciones en el rendimiento. Forzar la seguridad en la base de datos puede resultar muy caro, escalar de manera deficiente y es inflexible.

## <a name="enforcing-security-in-the-middle-tier"></a>Aplicar la seguridad en el nivel intermedio

La regla general que debe seguir con las aplicaciones escalables de varios niveles mediante COM+ es que, siempre que sea posible, debe exigir una seguridad detallada en la aplicación COM+ en el nivel intermedio. De este modo, podrá aprovechar al máximo los servicios escalables que proporciona COM+. Aplique la autenticación en la base de datos solo cuando sea absolutamente necesario y evalúe completamente las implicaciones de rendimiento de hacerlo.

La situación óptima es poder proteger las tablas de base de datos para que la aplicación COM+ pueda acceder a ellas en su propia identidad. La base de datos solo debe autenticar la aplicación COM+ y confiar en ella para autenticar y autorizar correctamente a los clientes que van a tener acceso a los datos. Las ventajas de este enfoque son las siguientes:

-   Habilita la agrupación de conexiones entre todos los clientes, ya que las conexiones son completamente genéricas.
-   Generalmente, optimiza el acceso a los datos, a menudo un punto de retracción problemático al escalar las aplicaciones.
-   Puede minimizar la sobrecarga lógica para aplicar la seguridad, especialmente si se puede usar la seguridad declarativa basada en roles.
-   Puede proporcionar una gran flexibilidad en una directiva de seguridad. Puede configurarlo y volver a configurarlo fácilmente, como se describe en [Administración de la seguridad basada en roles](role-based-security-administration.md).

Pero, como se describe en [diseñar roles de forma eficaz](designing-roles-effectively.md), mientras que los roles se pueden aplicar de manera fácil y eficaz a algunas relaciones de datos de usuario, no son una solución universal para las decisiones de acceso de seguridad.

## <a name="enforcing-security-at-the-database"></a>Forzar la seguridad en la base de datos

A pesar de la preferibilidad de aplicar la seguridad en el nivel intermedio, hay una serie de motivos para exigir la seguridad en la base de datos, como la siguiente:

-   No tiene ninguna opción, por ejemplo, por motivos de herencia o quizás porque la decisión no está simplemente en sus manos.
-   Una gran variedad de aplicaciones accede a la base de datos y su seguridad no se puede configurar en función de una sola aplicación.
-   Una base de datos se puede proteger de forma predecible. Si mantiene los datos críticos para la empresa en una base de datos, puede dibujar un vago carro en torno a él y ayudar a controlar quién llega a verlo.
-   La autenticación de clientes originales en la base de datos de permite el registro detallado de quién ha realizado lo que hay en la base de datos.
-   Algunos datos se enlazan de forma aislada a usuarios particulares, y la lógica de tomar decisiones de acceso muy específicas puede realizarse de forma más eficaz en la base de datos, cerca de los datos.

Cuando tenga el lujo de diseñar la seguridad de la base de datos y la aplicación COM+ en tándem, la mayoría de estos problemas se aplican a las características de los datos en sí y a su relación con los usuarios que acceden a él. Con los datos a los que pueden tener acceso las categorías de usuarios predecibles, es eficaz controlar el acceso en el nivel intermedio mediante roles. Con los datos que se enlazan de forma complicada a clases muy pequeñas de usuarios, estas relaciones deben expresarse con los propios datos y, por lo tanto, debe exigir cierta seguridad en la base de datos.

### <a name="performance-implications-of-enforcing-security-at-the-database"></a>Implicaciones de rendimiento de la aplicación de seguridad en la base de datos

Si autentica o autoriza a los usuarios en la base de datos, es necesario propagar la identidad del usuario a la base de datos para que sea compatible. Si la base de datos confía en la aplicación de nivel intermedio para hacerlo, es posible pasar la información de seguridad del usuario en parámetros. De lo contrario, la llamada a la base de datos debe realizarse en la identidad del usuario, lo que significa que la aplicación de servidor debe suplantar al cliente. Esto puede tener implicaciones de rendimiento como las siguientes:

-   La suplantación del cliente puede ser mucho más lenta que realizar la llamada directamente en la identidad de la aplicación. Para obtener más información, vea [suplantación y delegación de cliente](client-impersonation-and-delegation.md).
-   No se puede agrupar una conexión de base de datos realizada con una identidad de usuario específica.
-   La adición de lógica en la base de datos se queda con el riesgo de crear un cuello de botella de escalado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escenarios básicos para la protección de datos en aplicaciones de niveles múltiples](basic-scenarios-for-securing-data-in-multi-tier-applications.md)
</dt> <dt>

[Seguridad de aplicaciones de niveles múltiples](multi-tier-application-security.md)
</dt> </dl>

 

 



