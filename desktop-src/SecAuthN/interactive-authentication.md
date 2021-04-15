---
description: La autenticación es interactiva cuando se solicita al usuario que proporcione información de inicio de sesión. La autoridad de seguridad local (LSA) realiza una autenticación interactiva cuando un usuario inicia sesión a través de la interfaz de usuario GINA.
ms.assetid: 86a318fa-4d7c-4191-a309-d25b492dd915
title: Autenticación interactiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afeb09044f4b34f28c02cd0f03b3358a8158af65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361211"
---
# <a name="interactive-authentication"></a>Autenticación interactiva

La autenticación es interactiva cuando se solicita al usuario que proporcione información de inicio de sesión. La [*autoridad de seguridad local*](../secgloss/l-gly.md) (LSA) realiza una autenticación interactiva cuando un usuario inicia sesión a través de la interfaz de usuario [*Gina*](../secgloss/g-gly.md) . En la ilustración siguiente se muestran las partes de una autenticación interactiva típica.

![autenticación interactiva](images/lsaint3.png)

Un usuario indica al sistema que comience la secuencia de inicio de sesión escribiendo la [*secuencia de atención de seguridad*](../secgloss/s-gly.md) (SAS) Ctrl + Alt + Supr. [*Winlogon*](../secgloss/w-gly.md) recibe la SAS y llama a Gina para mostrar una interfaz de usuario y obtener los datos de inicio de sesión del usuario, como un nombre de usuario y una contraseña.

Después de obtener los datos de inicio de sesión, GINA llama a la función [**LsaLogonUser**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) para autenticar al usuario, especificando qué paquete de autenticación debe usarse para evaluar los datos de inicio de sesión.

LSA llama al paquete de autenticación especificado y le pasa los datos de inicio de sesión. El paquete de autenticación examina los datos y determina si la autenticación se realiza correctamente. El resultado de la autenticación se devuelve a la LSA y de la LSA a GINA.

GINA muestra el éxito o el error de la autenticación al usuario y devuelve el resultado de la autenticación a Winlogon. Si la autenticación se realiza correctamente, se inicia la sesión de inicio de sesión del usuario y se guarda un conjunto de [*credenciales*](../secgloss/c-gly.md) de inicio de sesión para futuras referencias.

> [!Note]  
> En general, un desarrollador que escribe una GINA personalizada para aceptar datos de inicio de sesión especializados, como una [*tarjeta inteligente*](../secgloss/s-gly.md) o datos de análisis de retina, también debe escribir un paquete de autenticación responsable de procesar los datos y determinar su autenticidad.

 

Para obtener más información acerca de Winlogon y GINAs, consulte [Winlogon y Gina](winlogon-and-gina.md). Para obtener más información acerca de los paquetes de autenticación, vea [crear paquetes de seguridad personalizados](creating-custom-security-packages.md).

 

 
