---
description: Las acciones personalizadas de Nondeferred que llaman a las bibliotecas de vínculos dinámicos o scripts pueden tener acceso a una instalación en ejecución para consultar o modificar los atributos de la sesión de instalación actual.
ms.assetid: cf70b0b3-ac81-47ab-a4c8-4db53ed9dc84
title: Obtener acceso a la sesión del instalador actual desde una acción personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29a870247f70742d408c0f5d1d0e67f20cef65d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001769"
---
# <a name="accessing-the-current-installer-session-from-inside-a-custom-action"></a>Obtener acceso a la sesión del instalador actual desde una acción personalizada

Las acciones personalizadas de Nondeferred que llaman a las [bibliotecas de vínculos dinámicos](dynamic-link-libraries.md) o [scripts](scripts.md) pueden tener acceso a una instalación en ejecución para consultar o modificar los atributos de la sesión de instalación actual. Solo puede existir un objeto de **sesión** para cada proceso y los scripts de acción personalizados no deben intentar crear otra sesión.

Las acciones personalizadas solo pueden agregar, modificar o quitar filas, columnas o tablas temporales de una base de datos. Las acciones personalizadas no pueden modificar los datos persistentes en una base de datos, por ejemplo, los datos que forman parte de la base de datos almacenada en el disco.

[Bibliotecas de vínculos dinámicos](dynamic-link-libraries.md)

Para tener acceso a una instalación en ejecución, las acciones personalizadas que llaman a las bibliotecas de vínculos dinámicos (DLL) pasan un identificador del tipo MSIHANDLE para la sesión actual como el único argumento para el punto de entrada de DLL indicado en la columna de destino de la [tabla CustomAction](customaction-table.md). Dado que el instalador proporciona este identificador, la acción personalizada no debe cerrarlo, por ejemplo, para recibir el identificador *hInstall* desde el instalador, la función de acción personalizada se declara como sigue.


```C++
UINT __stdcall CustomAction(MSIHANDLE hInstall)
```



Para el acceso de solo lectura a la base de datos actual, obtenga el identificador de base de datos mediante una llamada a [**MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase). Para obtener más información, vea [obtener un identificador de base de datos](obtaining-a-database-handle.md).

[Scripts](scripts.md)

Las acciones personalizadas escritas en VBScript o JScript pueden tener acceso a la sesión de instalación actual mediante el [**objeto de sesión**](session-object.md). El instalador crea un objeto de **sesión** denominado "session" que hace referencia a la instalación actual. Para el acceso de solo lectura a la base de datos actual, use la propiedad de [**base de datos**](session-database.md) del objeto de **sesión** .

Dado que un script se ejecuta desde el contexto del objeto de [**sesión**](session-object.md) , no siempre es necesario calificar completamente las propiedades y los métodos. En el ejemplo siguiente, cuando se usa VBScript, la referencia me puede reemplazar el objeto de **sesión** ; por ejemplo, las tres líneas siguientes son equivalentes.


```VB
Session.SetInstallLevel 1
```




```VB
Me.SetInstallLevel 1
```




```VB
SetInstallLevel 1
```



[Archivos ejecutables](executable-files.md)

No se puede tener acceso a la sesión del instalador actual desde acciones personalizadas que llaman a los archivos ejecutables que se inician con una línea de comandos, por ejemplo, la [acción personalizada tipo 2](custom-action-type-2.md) y la [acción personalizada tipo 18](custom-action-type-18.md).

[Acciones personalizadas de ejecución aplazada](deferred-execution-custom-actions.md)

No se puede tener acceso a la sesión de instalador actual o a todos los datos de propiedad de una acción personalizada de ejecución aplazada. Para obtener más información, vea [obtener información de contexto para las acciones personalizadas de ejecución aplazada](obtaining-context-information-for-deferred-execution-custom-actions.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Obtener acceso a una base de datos o una sesión desde una acción personalizada](accessing-a-database-or-session-from-inside-a-custom-action.md)
</dt> </dl>

 

 



