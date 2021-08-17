---
description: La autenticación no interactiva solo se puede usar después de que se haya realizado una autenticación interactiva. Durante la autenticación no interactiva, el usuario no introduce datos de inicio de sesión; en su lugar, se usan las credenciales establecidas anteriormente.
ms.assetid: 1539cbfa-d84f-4989-8380-6cfc7c496310
title: Autenticación no inactiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e259a2b14d48f4d7109966fa01f6fbd6a505a1343e90ea312c557ebfb9c84ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117786623"
---
# <a name="noninteractive-authentication"></a>Autenticación no inactiva

La autenticación no interactiva solo se puede usar después de que se [haya](interactive-authentication.md) realizado una autenticación interactiva. Durante la autenticación no inactiva, el usuario no introduce [*datos*](../secgloss/l-gly.md)de inicio de sesión; en su lugar, se usan las credenciales [*establecidas*](../secgloss/c-gly.md) previamente.

La autenticación no inactiva se [](../secgloss/s-gly.md) realiza cuando una aplicación usa la interfaz del proveedor de soporte técnico de seguridad (SSPI) y un paquete de seguridad para establecer una conexión de red segura. La autenticación no interactiva es el mecanismo en marcha cuando un usuario se conecta a varias máquinas de una red sin tener que volver a escribir la información de inicio de sesión para cada máquina. Por ejemplo, si una aplicación necesita abrir una carpeta segura en un equipo remoto y el usuario de la aplicación ya ha iniciado sesión interactivamente en una cuenta de dominio, la aplicación no requiere que el usuario vuelva a proporcionar los datos de inicio de sesión. En su lugar, la aplicación puede solicitar una autenticación no inactiva mediante SSPI para pasar la información de seguridad establecida previamente a un paquete de seguridad. A continuación, el paquete de seguridad usa funciones LSA para comprobar las [*credenciales*](../secgloss/c-gly.md). En el diagrama siguiente se muestra este procedimiento.

![autenticación no interactiva](images/lsasspi2.png)

En el diagrama anterior, la aplicación cliente inicia una llamada a SSPI para solicitar una conexión de red autenticada. SSPI pasa la solicitud del cliente a un paquete de seguridad para su procesamiento. El paquete de seguridad autentica al usuario llamando [*a*](../secgloss/a-gly.md) la autoridad de seguridad [*local*](../secgloss/l-gly.md) (LSA) y especificando un paquete de autenticación y proporcionando las credenciales existentes del usuario.

El resultado de la autenticación se pasa desde el paquete [*de autenticación*](../secgloss/a-gly.md), a través del LSA, al paquete de seguridad [*y,*](../secgloss/s-gly.md)por último, a SSPI. SSPI notifica a la aplicación cliente el resultado de la solicitud.

Para obtener más información sobre SSPI, vea [Security Support Provider Interface](sspi.md).

 

 
