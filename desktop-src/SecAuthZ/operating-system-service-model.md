---
description: Una aplicación que se ejecuta como un usuario estándar se comunica con un servicio que se ejecuta como sistema mediante la llamada a procedimiento remoto (RPC).
ms.assetid: c0bcebe3-f7eb-471f-a21d-5840d2e26729
title: Modelo de servicio del sistema operativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ce545c60da8e480247c8fc8b02cfc01e4487340
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002353"
---
# <a name="operating-system-service-model"></a>Modelo de servicio del sistema operativo

En el modelo de servicio del sistema operativo, una aplicación que se ejecuta como un usuario estándar se comunica con un servicio que se ejecuta como **sistema** mediante la [llamada a procedimiento remoto](/windows/desktop/Rpc/rpc-start-page) (RPC).

La aplicación de usuario estándar se marca en el manifiesto de aplicación con un **requestedExecutionLevel** de **asInvoker**. Para realizar una operación que requiere privilegios de administrador, la aplicación de usuario estándar realiza una solicitud al servicio.

Un uso del modelo de servicio del sistema operativo consiste en administrar aplicaciones que podrían afectar al sistema, como antivirus u otro software y spyware no deseados. La aplicación de usuario estándar permite que el usuario que ha iniciado sesión controle algunos aspectos del servicio. El servicio es responsable de determinar qué operaciones realiza para una aplicación de usuario estándar. Por ejemplo, un servicio antivirus podría permitir a un usuario estándar iniciar un examen del sistema, pero es posible que no permita que un usuario estándar deshabilite la comprobación de virus en tiempo real.

Una ventaja importante del uso del modelo de servicio del sistema operativo es que no se requiere ninguna solicitud de elevación.

Un inconveniente de usar el modelo de servicio del sistema operativo es que un servicio que se ejecuta en el sistema utiliza más recursos que una tarea y un usuario estándar no puede detener un servicio. Considere la posibilidad de usar el [modelo de tarea elevado](elevated-task-model.md) si es suficiente.

Para implementar el modelo de servicio del sistema operativo, cree una aplicación cliente de usuario estándar y un servicio de sistema operativo. Instale el servicio en el sistema operativo durante la instalación del producto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desarrollo de aplicaciones que requieren privilegios de administrador](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[Modelo de agente de administrador](administrator-broker-model.md)
</dt> <dt>

[Modelo de objetos COM de administrador](administrator-com-object-model.md)
</dt> <dt>

[Modelo de tareas elevado](elevated-task-model.md)
</dt> </dl>

 

 
