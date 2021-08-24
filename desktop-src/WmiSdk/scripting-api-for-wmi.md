---
description: La referencia de scripting de WMI contiene definiciones para WMI Scripting API.
ms.assetid: 83fc78fc-929d-4d32-940e-9147543a6324
ms.tgt_platform: multiple
title: API de scripting para WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35045aa8528c5a3c27475fff753478bd2202d9137cec6b019039aac52775f70a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640545"
---
# <a name="scripting-api-for-wmi"></a>API de scripting para WMI

La referencia de scripting de WMI contiene definiciones para WMI Scripting API. Use esta API si escribe aplicaciones con Microsoft Visual Basic, Visual Basic para Aplicaciones, Visual Basic Scripting Edition (VBScript) o cualquier otro lenguaje de scripting que admita tecnologías de scripting activas.

> [!Note]  
> PowerShell también está disponible para el scripting con WMI. El cmdlet Get-WMI y los tres aceleradores de tipos \[ \] (wmi, \[ wmiclass \] y \[ wmisearcher) \] permiten el acceso administrativo básico a WMI. Para obtener más información, vea [Scripting con Windows PowerShell](https://TechNet.Microsoft.Com/library/bb978526.aspx).

 

Los objetos de scripting WMI, excepto [**SWbemDateTime,**](swbemdatetime.md) no están marcados como seguros para scripts que se ejecutan en páginas HTML en Internet Explorer. Por lo tanto, a menos que se reduzca el nivel Internet Explorer seguridad dentro de la aplicación, se producirá un error en el script. **SWbemDateTime** está marcado como seguro para inicialización y scripting. Sin embargo, use todos los objetos de scripting WMI en las llamadas **GetObject** y **CreateObject** en el código del lado servidor Active Server Pages (ASP).

-   [Scripting API Object Model](scripting-api-object-model.md)
-   [Convenciones de documento para Scripting API](document-conventions-for-the-scripting-api.md)
-   [Objetos de API de scripting](scripting-api-objects.md)
-   [Constantes de API de scripting](scripting-api-constants.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de WMI](wmi-reference.md)
</dt> <dt>

[Códigos de retorno WMI](wmi-return-codes.md)
</dt> </dl>

 

 



