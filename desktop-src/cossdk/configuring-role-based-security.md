---
description: Si la aplicación COM+ utiliza la seguridad basada en roles, hay varias tareas que deben completarse.
ms.assetid: f53b9945-cd34-4afc-a03a-dd72b0af160d
title: Configuración de la seguridad de Role-Based
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eafa71430dfa13f497b0e4f7f7cea45229a422e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360027"
---
# <a name="configuring-role-based-security"></a>Configuración de la seguridad de Role-Based

Si la aplicación COM+ utiliza la seguridad basada en roles, hay varias tareas que deben completarse. Al diseñar los componentes en la aplicación, debe definir los roles necesarios para ayudar a proteger el acceso a esos componentes. También puede decidir qué roles asignar a los componentes, interfaces y métodos de la aplicación. Durante la integración de la aplicación, se usa la herramienta administrativa Servicios de componentes para agregar los roles definidos a la aplicación y asignar cada rol a los componentes, interfaces y métodos adecuados.

Al configurar la seguridad basada en roles, realice los pasos siguientes:

1.  Habilite las comprobaciones de acceso en el nivel de aplicación. Para activar la comprobación de seguridad para una aplicación. Consulte [habilitación de comprobaciones de acceso para una aplicación](enabling-access-checks-for-an-application.md) para obtener más información sobre cómo realizar este paso.
2.  Establezca el nivel de seguridad para las comprobaciones de acceso. Para establecer la seguridad en el proceso o en el nivel de componente y de proceso. Consulte [configuración de un nivel de seguridad para las comprobaciones de acceso](setting-a-security-level-for-access-checks.md) para obtener más información sobre cómo realizar este paso.
3.  Habilite las comprobaciones de acceso en el nivel de componente. Para activar la comprobación de seguridad en los niveles de componente, interfaz y método. Consulte [habilitación de comprobaciones de acceso en el nivel de componente](enabling-access-checks-at-the-component-level.md) para obtener más información sobre cómo realizar este paso.
4.  Definir roles para una aplicación. Crear roles para una aplicación. Consulte [definición de roles para una aplicación](defining-roles-for-an-application.md) para más información sobre cómo realizar este paso.
5.  Asignar roles a componentes, interfaces o métodos. Para asignar roles a recursos específicos dentro de una aplicación. Vea [asignar roles a componentes, interfaces o métodos](assigning-roles-to-components--interfaces--or-methods.md) para obtener más información sobre cómo realizar este paso.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de la Directiva de restricción de software](configuring-the-software-restriction-policy.md)
</dt> <dt>

[Establecer un nivel de suplantación](setting-an-impersonation-level.md)
</dt> </dl>

 

 



