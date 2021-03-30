---
description: Winlogon, GINA y proveedores de red son las partes del modelo de inicio de sesión interactivo.
ms.assetid: d049d83f-b962-4c47-a79a-da556831e319
title: Winlogon y GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a683077f275dc9bf38efca6649cbd8131e0b9334
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907862"
---
# <a name="winlogon-and-gina"></a>Winlogon y GINA

[*Winlogon*](../secgloss/w-gly.md), [*Gina*](../secgloss/g-gly.md)y proveedores de red son las partes del modelo de inicio de sesión interactivo. Normalmente, el procedimiento de inicio de sesión interactivo está controlado por Winlogon, MSGina.dll y proveedores de red. Para cambiar el procedimiento de inicio de sesión interactivo, MSGina.dll se puede reemplazar por un archivo DLL de GINA personalizado.

Para trabajar con Winlogon, GINA y proveedores de red, debe tener un conocimiento firme de la arquitectura de seguridad de Windows, especialmente con respecto a los [*tokens*](../secgloss/a-gly.md), los [*paquetes de autenticación*](../secgloss/a-gly.md)y los asuntos relacionados.

> [!Note]  
> Los archivos dll de GINA se omiten en Windows Vista.

 

Para obtener información sobre funciones y estructuras específicas, vea [referencia de autenticación](authentication-reference.md). Esta sección de referencia incluye descripciones de las funciones que un archivo DLL de GINA debe implementar, las funciones de compatibilidad de Winlogon a las que puede llamar el archivo DLL de GINA y las estructuras de datos usadas para pasar información entre Winlogon y GINA.

El código GINA de ejemplo puede encontrarse en los ejemplos de seguridad del kit de desarrollo de software (SDK) de la plataforma. Los ejemplos contienen código C para implementar un código auxiliar GINA y un enlace GINA. Para obtener más información acerca del desarrollo de archivos DLL GINA personalizados, envíe un mensaje de correo electrónico a: ginareqs@microsoft.com .

Para obtener información sobre el modelo de autenticación admitido por Windows y para obtener más información acerca de los servicios de [*autoridad de seguridad local*](../secgloss/l-gly.md) (LSA) y las interfaces de [*paquetes de autenticación*](../secgloss/a-gly.md) , consulte [LSA Authentication](lsa-authentication.md).

Para obtener información acerca de los aspectos de la autoridad de seguridad local relacionados con la administración de la Directiva de seguridad, que incluye relaciones de confianza con otros equipos y dominios, asignación de privilegios, control de generación de auditorías, accesibilidad del sistema y otros temas similares, vea [Directiva de LSA](../secmgmt/lsa-policy.md).

Para obtener información acerca de Winlogon y GINA, vea los temas siguientes.



| Tema                                                                              | Descripción                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Winlogon](winlogon.md)                                                           | Winlogon proporciona un conjunto de funciones de compatibilidad para el archivo DLL de GINA.<br/>                                                                                                                                                                 |
| [GINA](gina.md)                                                                   | Un archivo DLL de GINA proporciona procedimientos de autenticación e identificación de usuario personalizables.<br/>                                                                                                                                            |
| [Terminal Services funciones GINA](terminal-services-gina-functions.md)           | Cuando se habilitan Terminal Services, GINA debe llamar a las funciones de compatibilidad con Winlogon para realizar varias tareas.<br/>                                                                                                                   |
| [Interacción con proveedores de red](interaction-with-network-providers.md)       | Puede configurar un sistema para que admita cero o más proveedores de red.<br/>                                                                                                                                                          |
| [Responsabilidades y características](responsibilities-and-features.md)                 | Cada parte del proceso de inicio de sesión interactivo tiene un conjunto de responsabilidades.<br/>                                                                                                                                                      |
| [Interacción entre Winlogon y GINA](interaction-between-winlogon-and-gina.md) | El estado de Winlogon determina la función GINA a la que se llama para procesar cualquier evento de [*secuencia de atención segura*](../secgloss/s-gly.md) (SAS) determinado.<br/> |
| [Paquetes de notificación de Winlogon](winlogon-notification-packages.md)               | Puede implementar un paquete de notificación para supervisar y responder a los eventos de Winlogon.<br/>                                                                                                                                            |



 

 

 
