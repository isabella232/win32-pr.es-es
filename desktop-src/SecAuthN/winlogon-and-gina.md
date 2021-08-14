---
description: Winlogon, GINA y los proveedores de red son las partes del modelo de inicio de sesión interactivo.
ms.assetid: d049d83f-b962-4c47-a79a-da556831e319
title: Winlogon y GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9cc39b905d6a49eb84ccab164f99481561133e6cdd9ea40cfd0b1067315569a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915074"
---
# <a name="winlogon-and-gina"></a>Winlogon y GINA

[*Winlogon,*](../secgloss/w-gly.md) [*GINA*](../secgloss/g-gly.md)y los proveedores de red son las partes del modelo de inicio de sesión interactivo. El procedimiento de inicio de sesión interactivo se controla normalmente mediante Winlogon, MSGina.dll y proveedores de red. Para cambiar el procedimiento de inicio de sesión interactivo, MSGina.dll se puede reemplazar por un archivo DLL de GINA personalizado.

Para trabajar con Winlogon, la GINA y los proveedores de red, debe tener un conocimiento firme [](../secgloss/a-gly.md)de la arquitectura de seguridad de Windows, especialmente con respecto a [*tokens,*](../secgloss/a-gly.md)paquetes de autenticación y asuntos relacionados.

> [!Note]  
> Los archivos DLL de GINA se omiten Windows Vista.

 

Para obtener información sobre funciones y estructuras específicas, vea [Referencia de autenticación](authentication-reference.md). En esta sección de referencia se incluyen descripciones de las funciones que debe implementar un archivo DLL de GINA, las funciones de compatibilidad de Winlogon a las que puede llamar el archivo DLL de GINA y las estructuras de datos usadas para pasar información entre Winlogon y GINA.

El código GINA de ejemplo se puede encontrar en los ejemplos de seguridad del Kit de desarrollo de software de plataforma (SDK). Los ejemplos contienen código C para implementar un código auxiliar de GINA y un enlace de GINA. Para obtener más información sobre el desarrollo de DLL de GINA personalizado, envíe un mensaje de correo electrónico a: ginareqs@microsoft.com .

Para obtener información sobre el modelo de autenticación compatible con Windows y para más información sobre los servicios de la Autoridad de seguridad [*local*](../secgloss/l-gly.md) (LSA) y las [*interfaces*](../secgloss/a-gly.md) de paquetes de autenticación, vea [Autenticación de LSA.](lsa-authentication.md)

Para obtener información sobre los aspectos de la autoridad de seguridad local relacionados con la administración de la directiva de seguridad, que incluye relaciones de confianza con otros equipos y dominios, asignación de privilegios, control de generación de auditoría, accesibilidad del sistema y otros temas similares, vea [Directiva LSA](../secmgmt/lsa-policy.md).

Para obtener información sobre Winlogon y GINA, consulte los temas siguientes.



| Tema                                                                              | Descripción                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Winlogon](winlogon.md)                                                           | Winlogon proporciona un conjunto de funciones de compatibilidad para el archivo DLL de GINA.<br/>                                                                                                                                                                 |
| [Gina](gina.md)                                                                   | Un archivo DLL de GINA proporciona procedimientos personalizables de identificación y autenticación de usuarios.<br/>                                                                                                                                            |
| [Funciones GINA de Terminal Services](terminal-services-gina-functions.md)           | Cuando Terminal Services está habilitado, GINA debe llamar a las funciones de soporte técnico de Winlogon para completar varias tareas.<br/>                                                                                                                   |
| [Interacción con proveedores de red](interaction-with-network-providers.md)       | Puede configurar un sistema para que admita cero o más proveedores de red.<br/>                                                                                                                                                          |
| [Responsabilidades y características](responsibilities-and-features.md)                 | Cada parte del proceso de inicio de sesión interactivo tiene un conjunto de responsabilidades.<br/>                                                                                                                                                      |
| [Interacción entre Winlogon y GINA](interaction-between-winlogon-and-gina.md) | El estado de Winlogon determina a qué función GINA se llama para procesar cualquier evento de secuencia de [*atención*](../secgloss/s-gly.md) segura (SAS) determinado.<br/> |
| [Paquetes de notificación de Winlogon](winlogon-notification-packages.md)               | Puede implementar un paquete de notificación para supervisar y responder a los eventos de Winlogon.<br/>                                                                                                                                            |



 

 

 
