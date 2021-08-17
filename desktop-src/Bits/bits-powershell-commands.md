---
title: Referencia administrada para comandos PowerShell de BITS
description: Servicio de transferencia inteligente en segundo plano (BITS) 4.0 puede usar cmdlets Windows PowerShell para administrar trabajos de transferencia.
ms.assetid: 2c151dfe-4f89-41ea-a533-21ffcf0aa39e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7acc88c557209ed2958d06766215278e75223a1b297bd2704ca1dcba062cfed6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118173861"
---
# <a name="managed-reference-for-bits-powershell-commands"></a>Referencia administrada para comandos PowerShell de BITS

Servicio de transferencia inteligente en segundo plano (BITS) 4.0 puede usar cmdlets Windows PowerShell para crear y administrar trabajos de transferencia de descarga y carga de archivos.

```PowerShell
Import-Module BitsTransfer
mkdir -force c:\temp\BITSFILES
Start-BitsTransfer -Source https://aka.ms/WinServ16/StndPDF -Destination c:\temp\BITSFILES\WindowsServer2016.pdf
```

Windows PowerShell cmdlets para BITS proporcionan gran parte de la misma funcionalidad que la utilidad de línea de comandos bitsadmin. Sin embargo, Windows PowerShell también hace lo siguiente:

-   Automatiza las tareas de BITS en un lenguaje de scripting extensible y orientado a la administración.
-   Proporciona una única herramienta para todas las tareas relacionadas con el trabajo.

> [!Note]  
> Para usar estos comandos, primero debe importar el módulo bits de PowerShell mediante el `Import-Module BitsTransfer` comando . Para obtener más información, consulte el siguiente [artículo de TechNet](/previous-versions/technet-magazine/ff382721(v=msdn.10)).

 

Para obtener más información sobre el uso Windows PowerShell, [vea Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx).

## <a name="bits-powershell-classes"></a>Clases de PowerShell bits

**Espacio de** nombres : Microsoft.BackgroundIntelligentTransfer.Management

**Ensamblado:** System.Management.Automation

Estas clases de comandos bits se implementan mediante Windows PowerShell. Estas clases se incluyen en este kit de desarrollo de software (SDK) solo para integridad. Los miembros de estas clases no se pueden usar directamente, ni deben usarse para derivar otras clases.



| Clase                           | Descripción                                                                                                                                                                                                                                         |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **AddBitsFileCommand**          | Agrega uno o varios archivos a un trabajo de transferencia de BITS existente.<br/> Consulte el cmdlet [Add-BitsFile](/previous-versions//dd347701(v=technet.10)) para obtener información detallada sobre los parámetros y para obtener ejemplos.<br/>                       |
| **ClearBitsTransferCommand**    | Cancela un trabajo de transferencia de BITS.<br/> Consulte el cmdlet [Clear-BitsTransfer]( /previous-versions//dd347701(v=technet.10)) para obtener información detallada sobre los parámetros y para obtener ejemplos.<br/>                                          |
| **CompleteBitsTransferCommand** | Completa un trabajo de transferencia de BITS.<br/> Consulte el cmdlet [Complete-BitsTransfer]( /previous-versions//dd347701(v=technet.10)) para obtener información detallada sobre los parámetros y para obtener ejemplos.<br/>                                     |
| **GetBitsTransferCommand**      | Recupera el objeto BitsJob asociado para un trabajo de transferencia de BITS existente.<br/> Consulte el cmdlet [Get-BitsTransfer](/previous-versions//dd347701(v=technet.10)) para obtener información detallada sobre los parámetros y para obtener ejemplos.<br/> |
| **NewBitsTransferCommand**      | Crea un nuevo trabajo de transferencia de BITS.<br/> Consulte el cmdlet [New-BitsTransfer](/previous-versions//dd347701(v=technet.10)) para obtener información detallada sobre los parámetros y para obtener ejemplos.<br/>                                           |
| **ResumeBitsTransferCommand**   | Reanuda un trabajo de transferencia de BITS.<br/> Consulte el cmdlet [Resume-BitsTransfer](/previous-versions//dd347701(v=technet.10)) para obtener información detallada sobre los parámetros y para obtener ejemplos.<br/>                                            |
| **SetBitsTransferCommand**      | Modifica las propiedades de un trabajo de transferencia de BITS existente.<br/> Consulte el cmdlet [Set-BitsTransfer](/previous-versions//dd347701(v=technet.10)) para obtener información detallada sobre los parámetros y para obtener ejemplos.<br/>                  |
| **SuspendBitsTransferCommand**  | Suspende un trabajo de transferencia de BITS.<br/> Consulte el cmdlet [Suspend-BitsTransfer](/previous-versions//dd347701(v=technet.10)) para obtener información detallada sobre los parámetros y para obtener ejemplos.<br/>                                          |



 

 

