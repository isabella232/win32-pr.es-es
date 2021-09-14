---
description: La aplicación se divide en dos programas. Uno de los programas se ejecuta como un usuario estándar y el otro se ejecuta con privilegios de administrador.
ms.assetid: 1e661915-5797-421d-b96f-72949f441aba
title: Modelo de agente de administrador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5299d35c995fb56f969fc5983864cfc93b25b6c7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073724"
---
# <a name="administrator-broker-model"></a>Modelo de agente de administrador

En el modelo de agente de administrador, la aplicación se divide en dos programas. Uno de los programas se ejecuta como un usuario estándar y el otro se ejecuta con privilegios de administrador.

Mediante un manifiesto de aplicación, marque el programa de usuario estándar con **un requestedExecutionLevel** de **asInvoker** y marque el programa administrativo con un **requestedExecutionLevel** de **requireAdministrator**. Un usuario inicia primero el programa de usuario estándar. Cuando el usuario intenta realizar una operación que requiere un token de acceso de administrador completo, el programa de usuario estándar llama a la [**función ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) para iniciar el programa administrativo. La **función ShellExecute** solicita al usuario la aprobación antes de ejecutar la aplicación con el token de acceso de administrador completo del usuario. A continuación, el programa administrativo puede realizar tareas que requieren privilegios de administrador.

El programa administrativo no está completamente aislado del programa de usuario estándar. El programa administrativo puede habilitar la comunicación entre procesos con el programa de usuario estándar. Sin embargo, esta comunicación está limitada por la directiva de integridad obligatoria predeterminada. Para obtener información sobre las consideraciones de integridad obligatorias, vea [Designing Applications to Run at a Low Integrity Level](/previous-versions/dotnet/articles/bb625960(v=msdn.10)).

Los siguientes son posibles usos para el modelo de agente de administrador:

-   Asistentes para desarrollo. Cuando un asistente de hardware determina que un controlador necesario no está instalado en el equipo o se encuentra en la ubicación aprobada de la empresa, llama a una aplicación con privilegios elevados con la capacidad de mover un controlador al almacén de equipos.
-   Autorun.exe a Setup.exe. Cuando un usuario ejecuta software desde un CD, Autorun.exe, que se ejecuta como un usuario estándar, inicia Setup.exe, que se ejecuta como administrador, para instalar el software en el equipo.

Estos son los inconvenientes de usar el modelo de agente de administrador:

-   Las transiciones de la aplicación a la aplicación pueden resultar confusas para el usuario. Puede ser difícil informar al usuario de por qué aparece una nueva aplicación en el monitor.
-   Puede ser difícil pasar información de estado entre las dos aplicaciones. Por ejemplo, no usaría este modelo para pasar información de estado entre un panel de control de usuario estándar (CPL) y su homólogo de administrador simplemente para permitir que la misma CPL tenga funcionalidad de usuario administrativa y estándar. El usuario estándar CPL tendría que almacenar su estado en algún lugar.
-   Puede haber una gran cantidad de código replicado al dividir la funcionalidad entre dos programas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desarrollo de aplicaciones que requieren privilegios de administrador](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[Modelo de objetos COM de administrador](administrator-com-object-model.md)
</dt> <dt>

[Modelo de servicio de sistema operativo](operating-system-service-model.md)
</dt> <dt>

[Modelo de tareas con privilegios elevados](elevated-task-model.md)
</dt> </dl>

 

 
