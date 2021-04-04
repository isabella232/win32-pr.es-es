---
description: API de administración de credenciales
ms.assetid: e393041b-f10c-4053-bc6c-65a89f40e74f
title: API de administración de credenciales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f3cae5054d0a32f42616f2845dcf18ab71ad0fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814742"
---
# <a name="credential-management-api"></a>API de administración de credenciales

Las funciones de administración de credenciales constituyen el conjunto de funciones que debe implementar un administrador de credenciales. Dichos componentes son:

-   [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify), una función de controlador de eventos a la que el MPR llama cuando un usuario inicia sesión.
-   [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify), una función de controlador de eventos a la que el MPR llama cuando se cambia una contraseña de cuenta.

Siempre se llama a las funciones de administración de credenciales en el contexto del sistema (LocalSystem) en lugar de en el contexto del usuario.

Para obtener más información acerca de cómo crear y registrar una aplicación de administrador de credenciales, consulte [implementar un administrador de credenciales](implementing-a-credential-manager.md) y [registrar proveedores de credenciales y administradores de credenciales](registering-network-providers-and-credential-managers.md).

 

 



