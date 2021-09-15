---
description: Explica los dos tipos de credenciales con las que funciona API de Administración credenciales.
ms.assetid: eaf1c298-f0af-4b29-a09a-f399da20335d
title: Tipos de credenciales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f30968484b2cfc89b9238f624d9299fb75c72bd7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473482"
---
# <a name="kinds-of-credentials"></a>Tipos de credenciales

El cuadro API de Administración credenciales funciona con dos tipos de credenciales:

-   [Credenciales de dominio](#domain-credentials)
-   [Credenciales genéricas](#generic-credentials)

## <a name="domain-credentials"></a>Credenciales del dominio

El sistema operativo usa las credenciales de dominio y las autentica la autoridad de seguridad local (LSA). Normalmente, las credenciales de dominio se establecen para un usuario cuando un paquete de seguridad registrado, como el protocolo Kerberos, autentica los datos de inicio de sesión proporcionados por el usuario. El sistema operativo almacena en caché las credenciales de inicio de sesión para que un inicio de sesión único dé acceso al usuario a muchos recursos diferentes. Por ejemplo, las conexiones de red pueden producirse de forma transparente y se puede conceder acceso a objetos del sistema protegidos en función de las credenciales de dominio almacenadas en caché del usuario.

Las funciones de administración de credenciales proporcionan un mecanismo para que las aplicaciones soliciten a un usuario las credenciales de dominio después de que el usuario inicie sesión y que el sistema operativo autentique la información proporcionada por el usuario.

La parte secreta de las credenciales de dominio, la contraseña, está protegida por el sistema operativo. Solo el código que se ejecuta en proceso con LSA puede leer y escribir credenciales de dominio. Las aplicaciones se limitan a escribir credenciales de dominio.

Windows admite el uso ampliado de credenciales de certificado y tarjeta inteligente. Para ayudar a garantizar la seguridad, el API de Administración nunca almacena el PIN de tarjeta inteligente en el equipo.

## <a name="generic-credentials"></a>Credenciales genéricas

Las credenciales genéricas las definen y autentican las aplicaciones que administran la autorización y la seguridad directamente en lugar de delegar estas tareas en el sistema operativo. Por ejemplo, una aplicación puede requerir que los usuarios escriban un nombre de usuario y una contraseña proporcionados por la aplicación o que produzcan un certificado [*para*](../secgloss/c-gly.md) acceder a un sitio web.

Las aplicaciones usan las funciones de administración de credenciales para solicitar a los usuarios información de credenciales, genérica y definida por la aplicación, como el nombre de usuario, el certificado, la tarjeta inteligente o la contraseña. La información especificada por el usuario se devuelve a la aplicación para la autenticación.

Administración de credenciales proporciona administración de caché personalizable y almacenamiento a largo plazo para credenciales genéricas. Los procesos de usuario pueden leer y escribir credenciales genéricas.

 

 
