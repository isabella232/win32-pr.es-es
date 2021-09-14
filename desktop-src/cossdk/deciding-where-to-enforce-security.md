---
description: Las desventajas son inherentes a la aplicación de la seguridad.
ms.assetid: f01573f3-aae6-400e-bdd9-6f34f4e262f6
title: Decidir dónde aplicar la seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ac994fb98d50a7e26f1b8142e77dc9ff771f6b2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360862"
---
# <a name="deciding-where-to-enforce-security"></a>Decidir dónde aplicar la seguridad

Las desventajas son inherentes a la aplicación de la seguridad. Una base de datos puede ser un lugar natural para colocar la lógica de seguridad, dado que, en última instancia, los datos son lo más importante que se debe proteger. Sin embargo, esto tiene implicaciones significativas en el rendimiento. Aplicar la seguridad en la base de datos puede ser muy costoso, escala poco y es inflexible.

## <a name="enforcing-security-in-the-middle-tier"></a>Aplicación de la seguridad en el nivel intermedio

La regla general que se debe seguir con las aplicaciones escalables de varios niveles que usan COM+ es que, siempre que sea posible, debe aplicar la seguridad detallada en la aplicación COM+ en el nivel intermedio. Esto le permite aprovechar totalmente los servicios escalables proporcionados por COM+. Aplique la autenticación en la base de datos solo cuando sea absolutamente necesario y sopese totalmente las implicaciones de rendimiento de hacerlo.

La situación óptima es poder proteger las tablas de base de datos para que la aplicación COM+ pueda acceder a ellas bajo su propia identidad. La base de datos solo debe autenticar la aplicación COM+ y confiar en ella para autenticar y autorizar correctamente a los clientes que tendrán acceso a los datos. Las ventajas de este enfoque son las siguientes:

-   Permite la agrupación de conexiones entre todos los clientes, ya que las conexiones son completamente genéricas.
-   Por lo general, optimiza el acceso a los datos, a menudo un punto de atragante problemático al escalar aplicaciones.
-   Puede minimizar la sobrecarga lógica para aplicar la seguridad, especialmente si se puede usar la seguridad basada en roles declarativa.
-   Puede proporcionar una gran flexibilidad en una directiva de seguridad. Puede configurarlo y volver a configurarlo fácilmente, como se describe en [Administración de seguridad basada en roles](role-based-security-administration.md).

Pero, como se describe en Diseño eficaz de [roles,](designing-roles-effectively.md)aunque los roles se pueden aplicar de forma fácil y eficaz a algunas relaciones de datos de usuario, no son una solución universal para las decisiones de acceso de seguridad.

## <a name="enforcing-security-at-the-database"></a>Aplicación de la seguridad en la base de datos

A pesar de la preferencia de aplicar la seguridad en el nivel intermedio, hay una serie de motivos para aplicar la seguridad en la base de datos, como las siguientes:

-   No tiene ninguna opción, quizás por motivos heredados o quizás porque la decisión simplemente no está en sus manos.
-   Se accede a la base de datos mediante una amplia variedad de aplicaciones y su seguridad no se puede configurar en función de una sola aplicación.
-   Una base de datos se puede proteger de forma predecible. Si mantiene los datos críticos para la empresa en una base de datos, puede dibujar un carro ajustado alrededor y ayudar a controlar quién puede verlos.
-   La autenticación de clientes originales en la base de datos permite el registro detallado de quién ha hecho lo que ha hecho en la base de datos.
-   Algunos datos están enlazados inicialmente a usuarios concretos y la lógica de tomar decisiones de acceso muy detalladas podría realizarse de forma más eficaz en la propia base de datos, cerca de los datos.

Si tiene la dicha de diseñar conjuntamente la seguridad de la base de datos y la aplicación COM+, la mayoría de estos problemas pertenecen a las características de los propios datos y su relación con los usuarios que acceden a ellos. Con los datos a los que se puede acceder mediante categorías de usuarios predecibles, es eficaz controlar el acceso en el nivel intermedio mediante roles. Con los datos que están estrechamente enlazados a clases muy pequeñas de usuarios, esas relaciones se deben expresar a menudo con los propios datos y, por tanto, debe aplicar cierta seguridad en la base de datos.

### <a name="performance-implications-of-enforcing-security-at-the-database"></a>Implicaciones de rendimiento de aplicar la seguridad en la base de datos

Si autentica o autoriza a los usuarios en la base de datos, la identidad del usuario debe propagarse a través de la base de datos para admitir esto. Si la base de datos confía en la aplicación de nivel intermedio para hacerlo, es posible pasar información de seguridad del usuario en los parámetros. De lo contrario, la llamada a la base de datos debe realizarse bajo la identidad del usuario, lo que significa que la aplicación de servidor debe suplantar al cliente. Esto puede tener implicaciones de rendimiento como las siguientes:

-   La suplantación del cliente puede ser mucho más lenta que realizar la llamada directamente en la identidad de la aplicación. Para obtener más información, vea [Suplantación y delegación de cliente.](client-impersonation-and-delegation.md)
-   No se puede agrupar una conexión de base de datos realizada con una identidad de usuario específica.
-   Agregar lógica en la propia base de datos corre el riesgo de crear un cuello de botella de escalado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escenarios básicos para proteger datos en aplicaciones de niveles múltiples](basic-scenarios-for-securing-data-in-multi-tier-applications.md)
</dt> <dt>

[Seguridad de aplicaciones de niveles múltiples](multi-tier-application-security.md)
</dt> </dl>

 

 



