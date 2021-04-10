---
description: Cuando se establece un nivel de suplantación para una aplicación, se determina el grado de autoridad que la aplicación concede a otras aplicaciones para usar su identidad cuando las llama.
ms.assetid: 5b5b2c2d-dc3d-4edd-9e13-e6cb13022ceb
title: Establecer un nivel de suplantación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1075ac3b10380892cdfdf770543a2dcbb32d56c8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153194"
---
# <a name="setting-an-impersonation-level"></a>Establecer un nivel de suplantación

Cuando se establece un nivel de suplantación para una aplicación, se determina el grado de autoridad que la aplicación concede a otras aplicaciones para usar su identidad cuando las llama. Solo puede establecer esta opción para las aplicaciones de servidor COM+: las aplicaciones de biblioteca se ejecutan bajo la identidad del proceso de hospedaje y usan el nivel de suplantación que especifica. Para obtener más información, consulte [niveles de suplantación](/windows/desktop/com/impersonation-levels).

**Para seleccionar un nivel de suplantación**

1.  Haga clic con el botón secundario en la aplicación COM+ para la que está configurando la suplantación y, a continuación, haga clic en **propiedades**.

2.  En el cuadro de diálogo Propiedades de la aplicación, haga clic en la pestaña **seguridad** .

3.  En el cuadro **nivel de suplantación** , seleccione el nivel adecuado. Los niveles son los siguientes, ordenados de la concesión de la autoridad de menos a la más importante:

    -   **Anónimo**. El cliente es anónimo para el servidor. El servidor puede suplantar al cliente, pero el token de suplantación (una credencial local) no contiene ninguna información acerca del cliente.
    -   **Identifique**. El servidor puede obtener la identidad del cliente y puede suplantar al cliente para realizar comprobaciones ACL.
    -   **Suplantar**. El servidor puede suplantar al cliente mientras actúa en su nombre, aunque con restricciones. El servidor puede obtener acceso a recursos del mismo equipo que el cliente. Si el servidor está en el mismo equipo que el cliente, puede obtener acceso a los mismos recursos de red que el cliente. Si el servidor se encuentra en un equipo diferente del cliente, solo podrá tener acceso a los recursos que se encuentren en el mismo equipo que el servidor. Ésta es la configuración predeterminada para las aplicaciones de servidor COM+.
    -   **Delegado**. El servidor puede suplantar al cliente mientras actúa en su nombre, ya sea en el mismo equipo que el cliente. Durante la suplantación, las credenciales del cliente (las con local y las que tienen la validez de la red) se pueden pasar a cualquier número de equipos.

4.  Haga clic en **OK**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de la seguridad de Role-Based](configuring-role-based-security.md)
</dt> <dt>

[Configuración de la Directiva de restricción de software](configuring-the-software-restriction-policy.md)
</dt> <dt>

[Habilitar la autenticación para una aplicación de biblioteca](enabling-authentication-for-a-library-application.md)
</dt> <dt>

[Establecer un nivel de autenticación para una aplicación de servidor](setting-an-authentication-level-for-a-server-application.md)
</dt> </dl>

 

 
