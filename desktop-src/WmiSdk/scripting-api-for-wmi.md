---
description: La referencia de scripting de WMI contiene definiciones para WMI Scripting API.
ms.assetid: 83fc78fc-929d-4d32-940e-9147543a6324
ms.tgt_platform: multiple
title: API de scripting para WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6c43587fd8f40c2524bcabd79fe80e3d00d74b1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127358931"
---
# <a name="scripting-api-for-wmi"></a>API de scripting para WMI

La referencia de scripting de WMI contiene definiciones para WMI Scripting API. Use esta API si escribe aplicaciones con Microsoft Visual Basic, Visual Basic para Aplicaciones, Visual Basic Scripting Edition (VBScript) o cualquier otro lenguaje de scripting que admita tecnologías de scripting activas.

> [!Note]  
> PowerShell también está disponible para scripting con WMI. El cmdlet Get-WMI y los tres aceleradores de tipos \[ \] (wmi, \[ wmiclass \] y \[ wmisearcher) \] habilitan el acceso administrativo básico a WMI. Para obtener más información, vea [Scripting con Windows PowerShell](https://TechNet.Microsoft.Com/library/bb978526.aspx).

 

Los objetos de scripting WMI, excepto [**SWbemDateTime,**](swbemdatetime.md) no se marcan como seguros para scripts que se ejecutan en páginas HTML en Internet Explorer. Por lo tanto, a menos que el nivel de seguridad Internet Explorer se reduzca, se producirá un error en el script. **SWbemDateTime** se marca como seguro para inicialización y scripting. Sin embargo, use todos los objetos de scripting wmi **en llamadas GetObject** y **CreateObject** en el código del lado servidor en Active Server Pages (ASP).

-   [Modelo de objetos de LA API de scripting](scripting-api-object-model.md)
-   [Convenciones de documento para Scripting API](document-conventions-for-the-scripting-api.md)
-   [Objetos de API de scripting](scripting-api-objects.md)
-   [Constantes de API de scripting](scripting-api-constants.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de WMI](wmi-reference.md)
</dt> <dt>

[Códigos de retorno wmi](wmi-return-codes.md)
</dt> </dl>

 

 



