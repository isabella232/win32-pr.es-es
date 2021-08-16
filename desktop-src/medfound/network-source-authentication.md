---
description: Autenticación de origen de red
ms.assetid: bffc33ec-0fb0-4bbe-9bac-583b9d4e1153
title: Autenticación de origen de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3e90ae7d7a8e4fb29b56aaa1296ba0c5aa44049f801b01a2c7797009ec736aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973044"
---
# <a name="network-source-authentication"></a>Autenticación de origen de red

Algunos hosts multimedia pueden requerir credenciales de usuario de las aplicaciones cliente antes de permitir el acceso a los medios. Las credenciales de usuario incluyen la identificación y la prueba de identificación, como el nombre de usuario y la contraseña, que usa el servidor multimedia para conceder acceso al origen de red que hospeda. El origen de red puede proporcionar autenticación NTLM, Implícita o Básica.

Las aplicaciones basadas Media Foundation pueden almacenar credenciales de  usuario para una dirección URL específica en un objeto de credencial que expone la [**interfaz DE CREDENCIAL DE CREDENCIAL.**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) El objeto de credencial almacena credenciales cifradas y proporciona métodos para devolver información como el nombre de usuario, la contraseña y el dominio.

Los objetos de credencial se crean y mantienen en una memoria caché. El *objeto de caché de* credenciales, expuesto por la interfaz [**IMFNetCredentialCache,**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) proporciona métodos para recuperar los objetos de credenciales de la caché de credenciales.

Una aplicación que admita la autenticación debe implementar [**la interfaz IMFNetCredentialManager.**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) Media Foundation no proporciona una implementación predeterminada de esta interfaz. El administrador de credenciales es responsable de recopilar las credenciales necesarias para una dirección URL a partir de la entrada del usuario o la lectura del almacenamiento persistente.

Esta sección contiene los siguientes temas:

-   [Establecimiento de un Administrador de credenciales](setting-a-credential-manager.md)
-   [Uso de la caché de credenciales](using-the-credential-cache.md)
-   [Implementación de IMFNetCredentialManager](implementing-imfnetcredentialmanager.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Redes en Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 



