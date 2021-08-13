---
description: La autenticación es interactiva cuando se solicita al usuario que proporcione información de inicio de sesión. La autoridad de seguridad local (LSA) realiza una autenticación interactiva cuando un usuario inicia sesión a través de la interfaz de usuario de GINA.
ms.assetid: 86a318fa-4d7c-4191-a309-d25b492dd915
title: Autenticación interactiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 876f3aced39afba0d08a9643e14caae91336daf38a63f3855e76fe50136a16a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482304"
---
# <a name="interactive-authentication"></a>Autenticación interactiva

La autenticación es interactiva cuando se solicita al usuario que proporcione información de inicio de sesión. La [*autoridad de seguridad local*](../secgloss/l-gly.md) (LSA) realiza una autenticación interactiva cuando un usuario inicia sesión a través de la interfaz de usuario de [*GINA.*](../secgloss/g-gly.md) En la ilustración siguiente se muestran las partes de una autenticación interactiva típica.

![autenticación interactiva](images/lsaint3.png)

Un usuario indica al sistema que inicie la secuencia de [](../secgloss/s-gly.md) inicio de sesión escribiendo la secuencia de atención segura (SAS) CTRL+ALT+SUPR. [*Winlogon recibe*](../secgloss/w-gly.md) la SAS y llama a la GINA para mostrar una interfaz de usuario y obtener los datos de inicio de sesión del usuario, como un nombre de usuario y una contraseña.

Después de obtener los datos de inicio de sesión, GINA llama a la función [**LsaLogonUser**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) para autenticar al usuario, especificando qué paquete de autenticación debe usarse para evaluar los datos de inicio de sesión.

El LSA llama al paquete de autenticación especificado y le pasa los datos de inicio de sesión. El paquete de autenticación examina los datos y determina si la autenticación es correcta. El resultado de la autenticación se devuelve al LSA y desde el LSA, a la GINA.

El GINA muestra el éxito o error de la autenticación al usuario y devuelve el resultado de la autenticación a Winlogon. Si la autenticación se realiza correctamente, se inicia la sesión de inicio de sesión del usuario y se guarda un conjunto de credenciales de [*inicio*](../secgloss/c-gly.md) de sesión para futuras referencias.

> [!Note]  
> En general, un desarrollador que escribe una GINA personalizada para [](../secgloss/s-gly.md) aceptar datos de inicio de sesión especializados, como una tarjeta inteligente o datos de examen de retinal, también debe escribir un paquete de autenticación responsable de procesar esos datos y determinar su autenticidad.

 

Para obtener más información sobre Winlogon y LASA, vea [Winlogon y GINA.](winlogon-and-gina.md) Para obtener más información sobre los paquetes de autenticación, vea [Crear paquetes de seguridad personalizados.](creating-custom-security-packages.md)

 

 
