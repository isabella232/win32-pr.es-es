---
description: Autenticación de origen de red
ms.assetid: bffc33ec-0fb0-4bbe-9bac-583b9d4e1153
title: Autenticación de origen de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09c38968fccf501f49ac7666a066b88528b237bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082295"
---
# <a name="network-source-authentication"></a>Autenticación de origen de red

Algunos hosts multimedia pueden requerir credenciales de usuario de las aplicaciones cliente antes de permitir el acceso a los medios. Las credenciales de usuario incluyen la identificación y la prueba de identificación, como el nombre de usuario y la contraseña, que el servidor multimedia usa para conceder acceso al origen de red que hospeda. El origen de red puede proporcionar autenticación NTLM, implícita o básica.

Las aplicaciones basadas en Media Foundation pueden almacenar las credenciales de usuario para una dirección URL específica en un objeto de *credenciales* que exponga la interfaz [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) . El objeto Credential almacena las credenciales cifradas y proporciona métodos para devolver información como el nombre de usuario, la contraseña y el dominio.

Los objetos de credenciales se crean y mantienen en una memoria caché. El objeto de *caché de credenciales* , expuesto por la interfaz [**IMFNetCredentialCache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) , proporciona métodos para recuperar los objetos de credenciales de la memoria caché de credenciales.

Una aplicación que admite la autenticación debe implementar la interfaz [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) . Media Foundation no proporciona una implementación predeterminada de esta interfaz. El administrador de credenciales es responsable de recopilar las credenciales necesarias para una dirección URL de la entrada del usuario o de la lectura desde el almacenamiento persistente.

Esta sección contiene los siguientes temas:

-   [Establecer un administrador de credenciales](setting-a-credential-manager.md)
-   [Uso de la caché de credenciales](using-the-credential-cache.md)
-   [Implementación de IMFNetCredentialManager](implementing-imfnetcredentialmanager.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones de red en Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 



