---
description: Una acción personalizada puede llamar a una función definida en una biblioteca de vínculos dinámicos (DLL) escrita en C o C++.
ms.assetid: 605c7b97-70bd-467a-9438-47b05d8b6b5d
title: Dynamic-Link bibliotecas (Windows instalador)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5f9ff0113d97d219220a4f42030c1563f16ce7b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158513"
---
# <a name="dynamic-link-libraries-windows-installer"></a>Dynamic-Link bibliotecas (Windows instalador)

Una acción personalizada puede llamar a una función definida en una biblioteca de vínculos dinámicos (DLL) escrita en C o C++. El archivo DLL puede existir como un archivo instalado durante la instalación actual o como un flujo binario temporal que se origina en la [tabla Binaria](binary-table.md) de la base de datos de instalación.

Tenga en cuenta que las funciones llamadas, incluidas las acciones personalizadas en archivos DLL, deben especificar la \_ \_ convención de llamada stdcall. Por ejemplo, para llamar a CustomAction, use lo siguiente.


```C++
#include <windows.h>
#include <msi.h>
#include <Msiquery.h>
#pragma comment(lib, "msi.lib")

UINT __stdcall CustomAction(MSIHANDLE hInstall)
```



Para obtener más información, vea [Acceso a la sesión actual del instalador desde dentro de una acción personalizada.](accessing-the-current-installer-session-from-inside-a-custom-action.md)

Los siguientes tipos de acciones personalizadas llaman a una biblioteca de vínculos dinámicos.



| Tipo de acción personalizada                                 | Descripción                               |
|----------------------------------------------------|-------------------------------------------|
| [Tipo de acción personalizada 1](custom-action-type-1.md)   | Archivo DLL almacenado en una secuencia de tabla binaria. |
| [Tipo de acción personalizada 17](custom-action-type-17.md) | Archivo DLL instalado con un producto.        |



 

> [!Note]  
> Para usar COM, debe llamar a [**CoInitializeEx en**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) la acción personalizada. No salga si encuentra que el subproceso ya se ha inicializado. Por ejemplo, el subproceso se inicializa en una instalación por equipo, pero no en una instalación por usuario.

 

Vea [Lista de resumen de todos los tipos](summary-list-of-all-custom-action-types.md) de acciones personalizadas para obtener un resumen de todos los tipos de acciones personalizadas y cómo se codifican en la tabla [CustomAction](customaction-table.md).

 

 
