---
title: Configuración de autenticación dinámica
description: Las aplicaciones pueden cambiar las configuraciones de autenticación en un grupo de direcciones URL o una sesión de servidor en cualquier momento.
ms.assetid: 8a5cc119-0427-487d-a155-74c14e2104d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fda33e150826ed7d84ac45c4ab0771136991aa9aeb2766d5d395a65da270775
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014843"
---
# <a name="dynamic-authentication-configuration"></a>Configuración de autenticación dinámica

De forma predeterminada, la API del servidor HTTP no realiza la autenticación a menos que la aplicación la permita específicamente. Las aplicaciones pueden cambiar las configuraciones de autenticación en un grupo de direcciones URL o una sesión de servidor en cualquier momento. Los cambios en la configuración de autenticación no afectan a las solicitudes que ya están autenticadas o que se envían a la aplicación.

En el caso de los esquemas de autenticación en los que se requieren varias rondas de protocolo de enlace, la API del servidor HTTP quita el protocolo de enlace de autenticación si el esquema actual ya no se admite debido a los cambios de configuración de la aplicación. Por ejemplo, si la aplicación habilita Negotiate y deshabilita NTLM, y la API del servidor HTTP está en el protocolo de enlace de autenticación intermedio para NTLM, el protocolo de enlace para NTLM se descarta y la solicitud se pasa a la aplicación. La aplicación envía un desafío de autenticación 401 con los nuevos tipos de autenticación especificados en el encabezado WWW-Authenticate autenticación.

 

 




