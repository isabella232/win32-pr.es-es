---
description: Explica los dos tipos de credenciales con las que funciona la API de administración de credenciales.
ms.assetid: eaf1c298-f0af-4b29-a09a-f399da20335d
title: Tipos de credenciales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f30968484b2cfc89b9238f624d9299fb75c72bd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002133"
---
# <a name="kinds-of-credentials"></a>Tipos de credenciales

La API de administración de credenciales funciona con dos tipos de credenciales:

-   [Credenciales de dominio](#domain-credentials)
-   [Credenciales genéricas](#generic-credentials)

## <a name="domain-credentials"></a>Credenciales del dominio

El sistema operativo usa las credenciales de dominio y las autentica la autoridad de seguridad local (LSA). Normalmente, las credenciales de dominio se establecen para un usuario cuando un paquete de seguridad registrado, como el protocolo Kerberos, autentica los datos de inicio de sesión proporcionados por el usuario. El sistema operativo almacena en caché las credenciales de inicio de sesión para que un inicio de sesión único proporcione al usuario acceso a muchos recursos diferentes. Por ejemplo, las conexiones de red pueden producirse de forma transparente y el acceso a los objetos del sistema protegidos se puede conceder en función de las credenciales de dominio almacenadas en caché del usuario.

Las funciones de administración de credenciales proporcionan un mecanismo para que las aplicaciones pidan a un usuario las credenciales de dominio después de que el usuario inicie sesión y para que el sistema operativo autentique la información proporcionada por el usuario.

La parte secreta de las credenciales de dominio, la contraseña, está protegida por el sistema operativo. Solo el código que se ejecuta en proceso con LSA puede leer y escribir credenciales de dominio. Las aplicaciones se limitan a escribir las credenciales de dominio.

Windows admite el uso expandido de credenciales de tarjeta inteligente y certificado. Para ayudar a garantizar la seguridad, la API de administración de credenciales nunca almacena el PIN de la tarjeta inteligente en el equipo.

## <a name="generic-credentials"></a>Credenciales genéricas

Las credenciales genéricas las definen y autentican las aplicaciones que administran la autorización y la seguridad directamente en lugar de delegar estas tareas en el sistema operativo. Por ejemplo, una aplicación puede requerir a los usuarios que escriban un nombre de usuario y una contraseña proporcionados por la aplicación o que generen un [*certificado*](../secgloss/c-gly.md) para tener acceso a un sitio Web.

Las aplicaciones usan funciones de administración de credenciales para solicitar a los usuarios información de credenciales, genéricas y definidas por la aplicación, como el nombre de usuario, el certificado, la tarjeta inteligente o la contraseña. La información especificada por el usuario se devuelve a la aplicación para la autenticación.

La administración de credenciales proporciona administración de caché personalizable y almacenamiento a largo plazo para las credenciales genéricas. Los procesos de usuario pueden leer y escribir las credenciales genéricas.

 

 
