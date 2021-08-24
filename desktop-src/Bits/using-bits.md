---
title: Uso de BITS
description: Uso de BITS
ms.assetid: 65b69ccb-b413-4690-ac0d-774d88608bdf
keywords:
- Servicio de transferencia inteligente en segundo plano
- Servicio de transferencia inteligente en segundo plano,tasks
- BITS de transferencia de archivos
- Uso de BITS BITS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b301c1d96956bca924d99ef41ade3032f58dc4e194b420069cbae1071c916b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801165"
---
# <a name="using-bits"></a>Uso de BITS

Los pasos siguientes muestran cómo realizar una transferencia de archivos mediante las  [interfaces](bits-interfaces.md)Servicio de transferencia inteligente en segundo plano (BITS).

**Para realizar una transferencia de archivos**

1.  [Conectar al servicio BITS](connecting-to-the-bits-service.md)
2.  [Creación de un trabajo de transferencia](creating-a-job.md)
3.  [Agregar archivos al trabajo](adding-files-to-a-job.md)
4.  [Inicio del trabajo](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume)
5.  [Determinar si BITS ha transferido correctamente los archivos](determining-the-status-of-a-job.md)
6.  [Completar el trabajo](completing-and-canceling-a-job.md)

Los pasos anteriores muestran cómo transferir archivos mediante los valores de propiedad predeterminados para un trabajo. Puede cambiar el comportamiento predeterminado cambiando uno o varios de los valores de propiedad del trabajo. Por ejemplo, puede cambiar la prioridad de que el trabajo se procese con respecto a otros trabajos de la cola, especificar su propia configuración de proxy y registrarse para recibir una notificación de eventos cuando BITS haya transferido los archivos. Para obtener más información, [vea Establecer y recuperar las propiedades de un trabajo.](setting-and-retrieving-the-properties-of-a-job.md)

Windows PowerShell proporciona un mecanismo sencillo para administrar muchas tareas de BITS. Esta sección contiene los temas siguientes que muestran cómo usar Windows PowerShell cmdlets con BITS:

-   [Uso de Windows PowerShell para crear trabajos de transferencia de BITS](using-windows-powershell-to-create-bits-transfer-jobs.md)
-   [Uso de los cmdlets de Windows PowerShell para WinRM para administrar trabajos de transferencia de BITS](using-winrm-windows-powershell-cmdlets-to-manage-bits-transfer-jobs.md)
-   [Uso de cmdlets Windows PowerShell WMI para administrar el servidor de BITS Compact](using-wmi-windows-powershell-cmdlets-to-manage-the-bits-compact-server.md)

> [!Note]
>
> A partir de Windows 10, versión 1607, también puede ejecutar cmdlets de PowerShell y usar BITSAdmin u otras aplicaciones que usan las [interfaces](bits-interfaces.md) BITS desde una línea de comandos remota de PowerShell conectada a otra máquina (física o virtual). Esta funcionalidad no está disponible cuando se usa una línea de [comandos de PowerShell Direct](/virtualization/hyper-v-on-windows/user_guide/vmsession) para una máquina virtual en la misma máquina física y no está disponible cuando se usan cmdlets de WinRM.
>
> Un trabajo bits creado a partir de una sesión remota de PowerShell se ejecutará en el contexto de la cuenta de usuario de esa sesión y solo avanzará cuando haya al menos una sesión de inicio de sesión local activa o una sesión remota de PowerShell asociada a esa cuenta de usuario. Para obtener más información, vea [Para administrar sesiones remotas de PowerShell.](using-windows-powershell-to-create-bits-transfer-jobs.md)

 

Esta sección también contiene los temas siguientes:

-   [Procedimientos recomendados al usar BITS](best-practices-when-using-bits.md)
-   [Enumeración de trabajos en la cola de transferencia](enumerating-jobs-in-the-transfer-queue.md)
-   [Enumeración de archivos en un trabajo](enumerating-files-in-a-job.md)
-   [Control de errores](handling-errors.md)
-   [Recuperación de la respuesta de un trabajo de carga y respuesta](retrieving-the-reply-from-an-upload-reply-job.md)

Para obtener código de ejemplo que usa las interfaces bits, vea [Ejemplos y herramientas de BITS.](bits-samples-and-tools.md)

 

 