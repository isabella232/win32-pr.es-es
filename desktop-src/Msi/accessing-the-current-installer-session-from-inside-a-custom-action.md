---
description: Las acciones personalizadas no deducidas que llaman a scripts o bibliotecas de vínculos dinámicos pueden acceder a una instalación en ejecución para consultar o modificar los atributos de la sesión de instalación actual.
ms.assetid: cf70b0b3-ac81-47ab-a4c8-4db53ed9dc84
title: Acceso a la sesión actual del instalador desde dentro de una acción personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3ee3214b8f8664b57f5216b28a7f5d5269d76049fe5c4dd24f7ab8d130d89a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118640194"
---
# <a name="accessing-the-current-installer-session-from-inside-a-custom-action"></a>Acceso a la sesión actual del instalador desde dentro de una acción personalizada

Las acciones personalizadas no deducidas [](scripts.md) que llaman a scripts o bibliotecas de [vínculos dinámicos](dynamic-link-libraries.md) pueden tener acceso a una instalación en ejecución para consultar o modificar los atributos de la sesión de instalación actual. Solo puede **existir un objeto Session** para cada proceso y los scripts de acción personalizados no deben intentar crear otra sesión.

Las acciones personalizadas solo pueden agregar, modificar o quitar filas, columnas o tablas temporales de una base de datos. Las acciones personalizadas no pueden modificar los datos persistentes de una base de datos, por ejemplo, los datos que forman parte de la base de datos almacenada en disco.

[Bibliotecas de vínculos dinámicos](dynamic-link-libraries.md)

Para tener acceso a una instalación en ejecución, las acciones personalizadas que llaman a bibliotecas de vínculos dinámicos (DLL) se pasan un identificador del tipo MSIHANDLE para la sesión actual como único argumento al punto de entrada dll denominado en la columna Target de la [tabla CustomAction](customaction-table.md). Dado que el instalador proporciona este identificador, la acción personalizada no debe cerrarlo, por ejemplo, para recibir el identificador *hInstall* del instalador, la función de acción personalizada se declara como sigue.


```C++
UINT __stdcall CustomAction(MSIHANDLE hInstall)
```



Para obtener acceso de solo lectura a la base de datos actual, obtenga el identificador de base de datos mediante una [**llamada a MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase). Para obtener más información, vea [Obtener un identificador de base de datos](obtaining-a-database-handle.md).

[Scripts](scripts.md)

Las acciones personalizadas escritas en VBScript JScript pueden acceder a la sesión de instalación actual mediante el [**objeto session**](session-object.md). El instalador crea un **objeto Session** denominado "Session" que hace referencia a la instalación actual. Para obtener acceso de solo lectura a la base de datos actual, use [**la propiedad Database**](session-database.md) del objeto **Session.**

Dado que un script se ejecuta desde el contexto del [**objeto Session,**](session-object.md) no siempre es necesario calificar completamente las propiedades y los métodos. En el ejemplo siguiente, al usar VBScript, la referencia Me puede reemplazar el objeto **Session,** por ejemplo, las tres líneas siguientes son equivalentes.


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

No se puede acceder a la sesión del instalador actual desde acciones personalizadas que llaman a archivos ejecutables iniciados con una línea de comandos, por ejemplo, Custom [Action Type 2](custom-action-type-2.md) y [Custom Action Type 18](custom-action-type-18.md).

[Acciones personalizadas de ejecución aplazada](deferred-execution-custom-actions.md)

No se puede acceder a la sesión actual del instalador ni a todos los datos de propiedad desde una acción personalizada de ejecución aplazada. Para obtener más información, vea Obtener información de contexto para acciones personalizadas [de ejecución aplazada.](obtaining-context-information-for-deferred-execution-custom-actions.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acceso a una base de datos o una sesión desde dentro de una acción personalizada](accessing-a-database-or-session-from-inside-a-custom-action.md)
</dt> </dl>

 

 



