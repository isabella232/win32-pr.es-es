---
description: Si la aplicación COM+ usa la seguridad basada en roles, hay varias tareas que deben completarse.
ms.assetid: f53b9945-cd34-4afc-a03a-dd72b0af160d
title: Configuración de Role-Based seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aba7df6b11bf44b53adaa9776435e43eabe3188fccb789a01d996f45331298dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859065"
---
# <a name="configuring-role-based-security"></a>Configuración de Role-Based seguridad

Si la aplicación COM+ usa la seguridad basada en roles, hay varias tareas que deben completarse. Al diseñar los componentes de la aplicación, defina los roles necesarios para ayudar a proteger el acceso a esos componentes. También puede decidir qué roles asignar a los componentes, interfaces y métodos de la aplicación. Durante la integración de aplicaciones, se usa la herramienta administrativa Servicios de componentes para agregar los roles definidos a la aplicación y asignar cada rol a los componentes, interfaces y métodos adecuados.

Al configurar la seguridad basada en roles, realice los pasos siguientes:

1.  Habilite las comprobaciones de acceso en el nivel de aplicación. Para activar la comprobación de seguridad de una aplicación. Consulte [Habilitación de comprobaciones de acceso para una aplicación](enabling-access-checks-for-an-application.md) para obtener más información sobre cómo realizar este paso.
2.  Establezca el nivel de seguridad para las comprobaciones de acceso. Para establecer la seguridad en el proceso o en el nivel de proceso y componente. Consulte [Establecer un nivel de seguridad para las comprobaciones de acceso](setting-a-security-level-for-access-checks.md) para obtener más información sobre cómo realizar este paso.
3.  Habilite las comprobaciones de acceso en el nivel de componente. Para activar la comprobación de seguridad en los niveles de componente, interfaz y método. Consulte [Habilitación de comprobaciones de acceso en el nivel de componente](enabling-access-checks-at-the-component-level.md) para obtener más información sobre cómo realizar este paso.
4.  Defina roles para una aplicación. Para crear roles para una aplicación. Consulte [Definición de roles para una aplicación](defining-roles-for-an-application.md) para obtener más información sobre cómo realizar este paso.
5.  Asigne roles a componentes, interfaces o métodos. Para asignar roles a recursos específicos dentro de una aplicación. Consulte [Asignación de roles a componentes, interfaces o métodos](assigning-roles-to-components--interfaces--or-methods.md) para obtener más información sobre cómo realizar este paso.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de la directiva de restricción de software](configuring-the-software-restriction-policy.md)
</dt> <dt>

[Establecer un nivel de suplantación](setting-an-impersonation-level.md)
</dt> </dl>

 

 



