---
description: La referencia de scripting de WMI contiene definiciones para la API de scripting de WMI.
ms.assetid: 83fc78fc-929d-4d32-940e-9147543a6324
ms.tgt_platform: multiple
title: API de scripting para WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6c43587fd8f40c2524bcabd79fe80e3d00d74b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908565"
---
# <a name="scripting-api-for-wmi"></a>API de scripting para WMI

La referencia de scripting de WMI contiene definiciones para la API de scripting de WMI. Use esta API si escribe aplicaciones con Microsoft Visual Basic, Visual Basic para Aplicaciones, Visual Basic Scripting Edition (VBScript) o cualquier otro lenguaje de scripting que admita tecnologías de Active Scripting.

> [!Note]  
> PowerShell también está disponible para scripting con WMI. El cmdlet Get-WMI y los tres aceleradores de tipos ( \[ WMI \] , \[ WMIClass \] y \[ wmisearcher \] ) permiten el acceso administrativo básico a WMI. Para obtener más información, vea [scripting con Windows PowerShell](https://TechNet.Microsoft.Com/library/bb978526.aspx).

 

Los objetos de scripting de WMI, a excepción de [**SWbemDateTime**](swbemdatetime.md) , no están marcados como seguros para scripts para scripts que se ejecutan en páginas HTML en Internet Explorer. Por lo tanto, a menos que se reduzca el nivel de seguridad de Internet Explorer, se producirá un error en el script. **SWbemDateTime** está marcado como Safe para la inicialización y el scripting. Sin embargo, use todos los objetos de scripting de WMI en las llamadas **GetObject** y **CreateObject** en el código del lado servidor en páginas de Active Server (ASP).

-   [Modelo de objetos de API de scripting](scripting-api-object-model.md)
-   [Convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md)
-   [Scripting de objetos de API](scripting-api-objects.md)
-   [Scripting de constantes de API](scripting-api-constants.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de WMI](wmi-reference.md)
</dt> <dt>

[Códigos de retorno de WMI](wmi-return-codes.md)
</dt> </dl>

 

 



