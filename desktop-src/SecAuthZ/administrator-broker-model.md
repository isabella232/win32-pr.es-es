---
description: La aplicación se divide en dos programas. Uno de los programas se ejecuta como un usuario estándar y el otro con privilegios de administrador.
ms.assetid: 1e661915-5797-421d-b96f-72949f441aba
title: Modelo de agente de administrador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5299d35c995fb56f969fc5983864cfc93b25b6c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910617"
---
# <a name="administrator-broker-model"></a>Modelo de agente de administrador

En el modelo de agente de administrador, la aplicación se divide en dos programas. Uno de los programas se ejecuta como un usuario estándar y el otro con privilegios de administrador.

Con un manifiesto de aplicación, marque el programa de usuario estándar con un **requestedExecutionLevel** de **asInvoker** y marque el programa administrativo con un **requestedExecutionLevel** de **requireAdministrator**. Un usuario inicia el programa de usuario estándar en primer lugar. Cuando el usuario intenta realizar una operación que requiere un token de acceso de administrador completo, el programa de usuario estándar llama a la función [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) para iniciar el programa administrativo. La función **ShellExecute** solicita al usuario la aprobación antes de ejecutar la aplicación con el token de acceso de administrador completo del usuario. El programa administrativo puede realizar tareas que requieren privilegios de administrador.

El programa administrativo no está completamente aislado del programa de usuario estándar. El programa administrativo puede habilitar la comunicación entre procesos con el programa de usuario estándar. Sin embargo, esta comunicación está limitada por la Directiva de integridad obligatoria predeterminada. Para obtener información sobre las consideraciones de integridad obligatorias, consulte [diseño de aplicaciones para que se ejecuten en un nivel de integridad bajo](/previous-versions/dotnet/articles/bb625960(v=msdn.10)).

A continuación se muestran los posibles usos del modelo de agente de administrador:

-   Desarrollo de asistentes. Cuando un asistente de hardware determina que un controlador requerido no está instalado en el equipo o que se encuentra en la ubicación aprobada de la empresa, llama a una aplicación con privilegios elevados con la capacidad de trasladar un controlador al almacén del equipo.
-   Autorun.exe llamar a Setup.exe. Cuando un usuario ejecuta software desde un CD, Autorun.exe, que se ejecuta como un usuario estándar, inicia Setup.exe, que se ejecuta como administrador, para instalar el software en el equipo.

A continuación se indican los inconvenientes del uso del modelo de agente de administrador:

-   Las transiciones de la aplicación a la aplicación pueden resultar confusas para el usuario. Puede ser difícil informar al usuario de por qué aparece una nueva aplicación en el monitor.
-   Puede ser difícil pasar información de estado entre las dos aplicaciones. Por ejemplo, no usaría este modelo para pasar información de estado entre un panel de control de usuario estándar (CPL) y su homólogo de administrador, simplemente para permitir que el mismo CPL tenga funcionalidad de usuario administrativo y estándar. El CPL de usuario estándar tendría que almacenar su estado en algún lugar.
-   Puede haber una gran cantidad de código replicado al dividir la funcionalidad entre dos programas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desarrollo de aplicaciones que requieren privilegios de administrador](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[Modelo de objetos COM de administrador](administrator-com-object-model.md)
</dt> <dt>

[Modelo de servicio del sistema operativo](operating-system-service-model.md)
</dt> <dt>

[Modelo de tareas elevado](elevated-task-model.md)
</dt> </dl>

 

 
