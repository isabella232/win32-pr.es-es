---
title: Usar BITS
description: Usar BITS
ms.assetid: 65b69ccb-b413-4690-ac0d-774d88608bdf
keywords:
- Servicio de transferencia inteligente en segundo plano
- Servicio de transferencia inteligente en segundo plano, tareas
- BITS de transferencia de archivos
- Uso de BITS bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5158e183ef7e7c142a481f1d89e329a9b04f422b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105656389"
---
# <a name="using-bits"></a>Usar BITS

En los pasos siguientes se muestra cómo realizar una transferencia de archivos mediante las  [interfaces](bits-interfaces.md)de servicio de transferencia inteligente en segundo plano (bits).

**Para realizar una transferencia de archivos**

1.  [Conectarse al servicio BITS](connecting-to-the-bits-service.md)
2.  [Crear un trabajo de transferencia](creating-a-job.md)
3.  [Agregar archivos al trabajo](adding-files-to-a-job.md)
4.  [Inicio del trabajo](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume)
5.  [Determinar si los BITS transfirieron correctamente los archivos](determining-the-status-of-a-job.md)
6.  [Completar el trabajo](completing-and-canceling-a-job.md)

En los pasos anteriores se muestra cómo transferir archivos con los valores de propiedad predeterminados de un trabajo. Puede cambiar el comportamiento predeterminado cambiando uno o varios de los valores de propiedad del trabajo. Por ejemplo, puede cambiar la prioridad con la que se procesa el trabajo en relación con otros trabajos de la cola, especificar su propia configuración de proxy y registrarse para recibir la notificación de eventos cuando BITS haya transferido los archivos. Para obtener más información, vea [establecer y recuperar las propiedades de un trabajo](setting-and-retrieving-the-properties-of-a-job.md).

Windows PowerShell proporciona un mecanismo sencillo para administrar muchas tareas de BITS. Esta sección contiene los siguientes temas que muestran cómo usar los cmdlets de Windows PowerShell con BITS:

-   [Uso de Windows PowerShell para crear trabajos de transferencia de BITS](using-windows-powershell-to-create-bits-transfer-jobs.md)
-   [Uso de los cmdlets de Windows PowerShell para WinRM para administrar trabajos de transferencia de BITS](using-winrm-windows-powershell-cmdlets-to-manage-bits-transfer-jobs.md)
-   [Usar cmdlets de WMI de Windows PowerShell para administrar el servidor de BITS Compact](using-wmi-windows-powershell-cmdlets-to-manage-the-bits-compact-server.md)

> [!Note]
>
> A partir de Windows 10, versión 1607, también puede ejecutar cmdlets de PowerShell y usar BITSAdmin u otras aplicaciones que usan las [interfaces](bits-interfaces.md) de bits desde una línea de comandos remota de PowerShell conectada a otra máquina (física o virtual). Esta funcionalidad no está disponible cuando se usa una línea de comandos de [PowerShell Direct](/virtualization/hyper-v-on-windows/user_guide/vmsession) para una máquina virtual en la misma máquina física y no está disponible cuando se usan los cmdlets de WinRM.
>
> Un trabajo de BITS creado a partir de una sesión remota de PowerShell se ejecutará en el contexto de la cuenta de usuario de la sesión y solo progresará cuando haya al menos una sesión de inicio de sesión local activa o una sesión de PowerShell remota asociada con esa cuenta de usuario. Para obtener más información, vea [para administrar sesiones remotas de PowerShell](using-windows-powershell-to-create-bits-transfer-jobs.md).

 

Esta sección también contiene los temas siguientes:

-   [Prácticas recomendadas al usar BITS](best-practices-when-using-bits.md)
-   [Enumerar trabajos en la cola de transferencia](enumerating-jobs-in-the-transfer-queue.md)
-   [Enumerar archivos en un trabajo](enumerating-files-in-a-job.md)
-   [Control de errores](handling-errors.md)
-   [Recuperar la respuesta de un trabajo de carga y respuesta](retrieving-the-reply-from-an-upload-reply-job.md)

Para ver el código de ejemplo que usa las interfaces de BITS, vea [ejemplos y herramientas de bits](bits-samples-and-tools.md).

 

 