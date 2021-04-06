---
description: La autenticación no interactiva solo puede usarse después de que se haya producido una autenticación interactiva. Durante la autenticación no interactiva, el usuario no especifica los datos de inicio de sesión, sino que se usan las credenciales establecidas previamente.
ms.assetid: 1539cbfa-d84f-4989-8380-6cfc7c496310
title: Autenticación no interactiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 658cba212403da2f970e056d7bacc1bc1bcaa559
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001086"
---
# <a name="noninteractive-authentication"></a>Autenticación no interactiva

La autenticación no interactiva solo puede usarse después de que se haya producido una [autenticación interactiva](interactive-authentication.md) . Durante la autenticación no interactiva, el usuario no especifica los [*datos de inicio de sesión*](../secgloss/l-gly.md), sino que se usan [*las credenciales*](../secgloss/c-gly.md) establecidas previamente.

La autenticación no interactiva se realiza cuando una aplicación usa la [*interfaz del proveedor de compatibilidad para seguridad*](../secgloss/s-gly.md) (SSPI) y un paquete de seguridad para establecer una conexión de red segura. La autenticación no interactiva es el mecanismo en el trabajo cuando un usuario se conecta a varios equipos de una red sin tener que volver a escribir la información de inicio de sesión de cada equipo. Por ejemplo, si una aplicación necesita abrir una carpeta segura en un equipo remoto y el usuario de la aplicación ya ha iniciado sesión de forma interactiva en una cuenta de dominio, la aplicación no requiere que el usuario proporcione los datos de inicio de sesión de nuevo. En su lugar, la aplicación puede solicitar una autenticación no interactiva mediante SSPI para pasar la información de seguridad establecida previamente a un paquete de seguridad. A continuación, el paquete de seguridad utiliza las funciones de LSA para comprobar las [*credenciales*](../secgloss/c-gly.md). En el siguiente diagrama se ilustra este procedimiento.

![autenticación no interactiva](images/lsasspi2.png)

En el diagrama anterior, la aplicación cliente inicia una llamada a SSPI para solicitar una conexión de red autenticada. SSPI pasa la solicitud del cliente a un paquete de seguridad para su procesamiento. El paquete de seguridad autentica al usuario mediante una llamada a la [*autoridad de seguridad local*](../secgloss/l-gly.md) (LSA) y especifica un [*paquete de autenticación*](../secgloss/a-gly.md) y proporcionando las credenciales existentes del usuario.

El resultado de la autenticación se pasa desde el [*paquete de autenticación*](../secgloss/a-gly.md), a través de la LSA, al [*paquete de seguridad*](../secgloss/s-gly.md)y, finalmente, a SSPI. SSPI notifica a la aplicación cliente el resultado de la solicitud.

Para obtener más información sobre SSPI, vea [interfaz del proveedor de compatibilidad con seguridad](sspi.md).

 

 
