---
description: Una acción personalizada puede llamar a una función definida en una biblioteca de vínculos dinámicos (DLL) escrita en C o C++.
ms.assetid: 605c7b97-70bd-467a-9438-47b05d8b6b5d
title: Bibliotecas de Dynamic-Link (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5f9ff0113d97d219220a4f42030c1563f16ce7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082781"
---
# <a name="dynamic-link-libraries-windows-installer"></a>Bibliotecas de Dynamic-Link (Windows Installer)

Una acción personalizada puede llamar a una función definida en una biblioteca de vínculos dinámicos (DLL) escrita en C o C++. La DLL puede existir como un archivo instalado durante la instalación actual o como una secuencia binaria temporal que se origina en la [tabla binaria](binary-table.md) de la base de datos de instalación.

Tenga en cuenta que todas las funciones llamadas, incluidas las acciones personalizadas en archivos dll, deben especificar la \_ \_ Convención de llamada Stdcall. Por ejemplo, para llamar a CustomAction, use lo siguiente.


```C++
#include <windows.h>
#include <msi.h>
#include <Msiquery.h>
#pragma comment(lib, "msi.lib")

UINT __stdcall CustomAction(MSIHANDLE hInstall)
```



Para obtener más información, vea [obtener acceso a la sesión del instalador actual desde una acción personalizada](accessing-the-current-installer-session-from-inside-a-custom-action.md) .

Los siguientes tipos de acciones personalizadas llaman a una biblioteca de vínculos dinámicos.



| Tipo de acción personalizada                                 | Descripción                               |
|----------------------------------------------------|-------------------------------------------|
| [Tipo de acción personalizada 1](custom-action-type-1.md)   | Archivo DLL almacenado en un flujo de tabla binaria. |
| [Tipo de acción personalizada 17](custom-action-type-17.md) | Archivo DLL instalado con un producto.        |



 

> [!Note]  
> Para utilizar COM, debe llamar a [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) en la acción personalizada. No salga si observa que el subproceso ya se ha inicializado. Por ejemplo, el subproceso se inicializa en una instalación por equipo, pero no en una instalación por usuario.

 

Vea [lista de Resumen de todos los tipos de acciones personalizadas](summary-list-of-all-custom-action-types.md) para obtener un resumen de todos los tipos de acciones personalizadas y cómo se codifican en la [tabla CustomAction](customaction-table.md).

 

 
