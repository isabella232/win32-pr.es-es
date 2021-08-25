---
description: Cuando se establece un nivel de suplantación para una aplicación, se determina qué grado de autoridad concede la aplicación a otras aplicaciones para usar su identidad cuando las llama.
ms.assetid: 5b5b2c2d-dc3d-4edd-9e13-e6cb13022ceb
title: Establecer un nivel de suplantación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0c23b8d0b54f12cbce92af43187681922854519c69e8614e952fda241e4fa89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895955"
---
# <a name="setting-an-impersonation-level"></a>Establecer un nivel de suplantación

Cuando se establece un nivel de suplantación para una aplicación, se determina qué grado de autoridad concede la aplicación a otras aplicaciones para usar su identidad cuando las llama. Solo se puede establecer para aplicaciones de servidor COM+: las aplicaciones de biblioteca se ejecutan bajo la identidad del proceso de hospedaje y usan el nivel de suplantación que especifica. Para obtener más información, vea [Niveles de suplantación.](/windows/desktop/com/impersonation-levels)

**Para seleccionar un nivel de suplantación**

1.  Haga clic con el botón derecho en la aplicación COM+ para la que va a establecer la suplantación y, a continuación, haga clic en **Propiedades**.

2.  En el cuadro de diálogo propiedades de la aplicación, haga clic en **la pestaña** Seguridad .

3.  En el **cuadro Nivel de suplantación,** seleccione el nivel adecuado. Los niveles son los siguientes, ordenados desde la concesión de la menor a la máxima autoridad:

    -   **Anónimo**. El cliente es anónimo para el servidor. El servidor puede suplantar al cliente, pero el token de suplantación (una credencial local) no contiene ninguna información acerca del cliente.
    -   **Identifique**. El servidor puede obtener la identidad del cliente y puede suplantar al cliente para realizar comprobaciones de ACL.
    -   **Suplantar**. El servidor puede suplantar al cliente mientras actúa en su nombre, aunque con restricciones. El servidor puede obtener acceso a recursos del mismo equipo que el cliente. Si el servidor está en el mismo equipo que el cliente, puede obtener acceso a los mismos recursos de red que el cliente. Si el servidor está en un equipo diferente del cliente, solo puede acceder a los recursos que se encuentran en el mismo equipo que el servidor. Ésta es la configuración predeterminada para las aplicaciones de servidor COM+.
    -   **Delegue**. El servidor puede suplantar al cliente mientras actúa en su nombre, ya sea en el mismo equipo que el cliente. Durante la suplantación, las credenciales del cliente (tanto las que tienen un valor local como las que tienen validez de red) se pueden pasar a cualquier número de máquinas.

4.  Haga clic en **Aceptar**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de Role-Based seguridad](configuring-role-based-security.md)
</dt> <dt>

[Configuración de la directiva de restricción de software](configuring-the-software-restriction-policy.md)
</dt> <dt>

[Habilitar la autenticación para una aplicación de biblioteca](enabling-authentication-for-a-library-application.md)
</dt> <dt>

[Establecer un nivel de autenticación para una aplicación de servidor](setting-an-authentication-level-for-a-server-application.md)
</dt> </dl>

 

 
