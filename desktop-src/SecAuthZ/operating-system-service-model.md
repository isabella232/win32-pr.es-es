---
description: Una aplicación que se ejecuta como un usuario estándar se comunica con un servicio que se ejecuta como SYSTEM mediante la llamada a procedimiento remoto (RPC).
ms.assetid: c0bcebe3-f7eb-471f-a21d-5840d2e26729
title: Modelo de servicio de sistema operativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af797a7baad8390b1b4bc79fd7723a518c587ed58cc2dab27ab2898845335ca3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907805"
---
# <a name="operating-system-service-model"></a>Modelo de servicio de sistema operativo

En el modelo de servicio del sistema operativo, una aplicación que se ejecuta como un usuario estándar se comunica con un servicio que se ejecuta como **SYSTEM** mediante [llamada](/windows/desktop/Rpc/rpc-start-page) a procedimiento remoto (RPC).

La aplicación de usuario estándar se marca en el manifiesto de aplicación con **un requestedExecutionLevel** de **asInvoker**. Para realizar una operación que requiere privilegios de administrador, la aplicación de usuario estándar realiza una solicitud al servicio.

Un uso del modelo de servicio del sistema operativo es administrar aplicaciones que podrían afectar al sistema, como antivirus u otro software y spyware no deseados. La aplicación de usuario estándar permite al usuario que ha iniciado sesión controlar algunos aspectos del servicio. El servicio es responsable de determinar qué operaciones realiza para una aplicación de usuario estándar. Por ejemplo, un servicio antivirus podría permitir que un usuario estándar inicie un examen del sistema, pero podría no permitir que un usuario estándar deshabilite la comprobación de virus en tiempo real.

Una ventaja importante del uso del modelo de servicio del sistema operativo es que no se requiere ninguna solicitud de elevación.

Un inconveniente de usar el modelo de servicio del sistema operativo es que un servicio que se ejecuta en el sistema usa más recursos que una tarea y un usuario estándar no puede detener un servicio. Considere la posibilidad de [usar el modelo de tareas con privilegios](elevated-task-model.md) elevados si es suficiente.

Para implementar el modelo de servicio del sistema operativo, cree una aplicación cliente de usuario estándar y un servicio de sistema operativo. Instale el servicio en el sistema operativo durante el tiempo de instalación del producto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desarrollo de aplicaciones que requieren privilegios de administrador](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[Modelo de Agente de administrador](administrator-broker-model.md)
</dt> <dt>

[Modelo de objetos COM de administrador](administrator-com-object-model.md)
</dt> <dt>

[Modelo de tareas con privilegios elevados](elevated-task-model.md)
</dt> </dl>

 

 
