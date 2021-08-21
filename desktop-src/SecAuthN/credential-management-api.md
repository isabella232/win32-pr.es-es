---
description: Credenciales API de Administración
ms.assetid: e393041b-f10c-4053-bc6c-65a89f40e74f
title: Credenciales API de Administración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a290cf9d7e5a2d527368c2fd7350fa1bb9549af862c7da7c3845ceae9efc8aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008843"
---
# <a name="credential-management-api"></a>Credenciales API de Administración

Las funciones de administración de credenciales constituyen el conjunto de funciones que debe implementar un administrador de credenciales. Estos son:

-   [**NPLogonNotify,**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify)una función de controlador de eventos a la que el MPR llama cuando un usuario inicia sesión.
-   [**NPPasswordChangeNotify,**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify)una función de controlador de eventos a la que mpR llama cuando se cambia una contraseña de cuenta.

Siempre se llama a las funciones de administración de credenciales en el contexto del sistema (LocalSystem) en lugar del contexto de usuario.

Para obtener más información sobre cómo crear y registrar una aplicación de administrador de credenciales, vea [Implementing a Administrador de credenciales](implementing-a-credential-manager.md) and [Registering Network Providers and Credential Managers](registering-network-providers-and-credential-managers.md).

 

 



