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
# <a name="accessing-the-current-installer-session-from-inside-a-custom-action"></a><span data-ttu-id="eac85-103">Obtener acceso a la sesión del instalador actual desde una acción personalizada</span><span class="sxs-lookup"><span data-stu-id="eac85-103">Accessing the Current Installer Session from Inside a Custom Action</span></span>

<span data-ttu-id="eac85-104">Las acciones personalizadas de Nondeferred que llaman a las [bibliotecas de vínculos dinámicos](dynamic-link-libraries.md) o [scripts](scripts.md) pueden tener acceso a una instalación en ejecución para consultar o modificar los atributos de la sesión de instalación actual.</span><span class="sxs-lookup"><span data-stu-id="eac85-104">Nondeferred custom actions that call [dynamic-link libraries](dynamic-link-libraries.md) or [scripts](scripts.md) may access a running installation to query or modify the attributes of the current installation session.</span></span> <span data-ttu-id="eac85-105">Solo puede existir un objeto de **sesión** para cada proceso y los scripts de acción personalizados no deben intentar crear otra sesión.</span><span class="sxs-lookup"><span data-stu-id="eac85-105">Only one **Session** object can exist for each process, and custom action scripts must not attempt to create another session.</span></span>

<span data-ttu-id="eac85-106">Las acciones personalizadas solo pueden agregar, modificar o quitar filas, columnas o tablas temporales de una base de datos.</span><span class="sxs-lookup"><span data-stu-id="eac85-106">Custom actions can only add, modify, or remove temporary rows, columns, or tables from a database.</span></span> <span data-ttu-id="eac85-107">Las acciones personalizadas no pueden modificar los datos persistentes en una base de datos, por ejemplo, los datos que forman parte de la base de datos almacenada en el disco.</span><span class="sxs-lookup"><span data-stu-id="eac85-107">Custom actions cannot modify persistent data in a database, for example, data that is a part of the database stored on disk.</span></span>

[<span data-ttu-id="eac85-108">Bibliotecas de vínculos dinámicos</span><span class="sxs-lookup"><span data-stu-id="eac85-108">Dynamic-Link Libraries</span></span>](dynamic-link-libraries.md)

<span data-ttu-id="eac85-109">Para tener acceso a una instalación en ejecución, las acciones personalizadas que llaman a las bibliotecas de vínculos dinámicos (DLL) pasan un identificador del tipo MSIHANDLE para la sesión actual como el único argumento para el punto de entrada de DLL indicado en la columna de destino de la [tabla CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="eac85-109">To access a running installation, custom actions that call dynamic-link libraries (DLL) are passed a handle of the type MSIHANDLE for the current session as the only argument to the DLL entry point named in the Target column of the [CustomAction Table](customaction-table.md).</span></span> <span data-ttu-id="eac85-110">Dado que el instalador proporciona este identificador, la acción personalizada no debe cerrarlo, por ejemplo, para recibir el identificador *hInstall* desde el instalador, la función de acción personalizada se declara como sigue.</span><span class="sxs-lookup"><span data-stu-id="eac85-110">Because the installer provides this handle, the custom action should not close it, for example, to receive the handle *hInstall* from the installer, the custom action function is declared as follows.</span></span>


```C++
UINT __stdcall CustomAction(MSIHANDLE hInstall)
```



<span data-ttu-id="eac85-111">Para el acceso de solo lectura a la base de datos actual, obtenga el identificador de base de datos mediante una llamada a [**MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase).</span><span class="sxs-lookup"><span data-stu-id="eac85-111">For read-only access to the current database obtain the database handle by calling [**MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase).</span></span> <span data-ttu-id="eac85-112">Para obtener más información, vea [obtener un identificador de base de datos](obtaining-a-database-handle.md).</span><span class="sxs-lookup"><span data-stu-id="eac85-112">For more information, see [Obtaining a Database Handle](obtaining-a-database-handle.md).</span></span>

[<span data-ttu-id="eac85-113">Scripts</span><span class="sxs-lookup"><span data-stu-id="eac85-113">Scripts</span></span>](scripts.md)

<span data-ttu-id="eac85-114">Las acciones personalizadas escritas en VBScript o JScript pueden tener acceso a la sesión de instalación actual mediante el [**objeto de sesión**](session-object.md).</span><span class="sxs-lookup"><span data-stu-id="eac85-114">Custom actions written in VBScript or JScript can access the current installation session by using the [**Session Object**](session-object.md).</span></span> <span data-ttu-id="eac85-115">El instalador crea un objeto de **sesión** denominado "session" que hace referencia a la instalación actual.</span><span class="sxs-lookup"><span data-stu-id="eac85-115">The installer creates a **Session** object named "Session" that references the current installation.</span></span> <span data-ttu-id="eac85-116">Para el acceso de solo lectura a la base de datos actual, use la propiedad de [**base de datos**](session-database.md) del objeto de **sesión** .</span><span class="sxs-lookup"><span data-stu-id="eac85-116">For read-only access to the current database use the [**Database**](session-database.md) property of the **Session** object.</span></span>

<span data-ttu-id="eac85-117">Dado que un script se ejecuta desde el contexto del objeto de [**sesión**](session-object.md) , no siempre es necesario calificar completamente las propiedades y los métodos.</span><span class="sxs-lookup"><span data-stu-id="eac85-117">Because a script is run from the context of the [**Session**](session-object.md) object, it is not always necessary to fully qualify properties and methods.</span></span> <span data-ttu-id="eac85-118">En el ejemplo siguiente, cuando se usa VBScript, la referencia me puede reemplazar el objeto de **sesión** ; por ejemplo, las tres líneas siguientes son equivalentes.</span><span class="sxs-lookup"><span data-stu-id="eac85-118">In the following example, when using VBScript, the Me reference can replace the **Session** object, for example, the following three lines are equivalent.</span></span>


```VB
Session.SetInstallLevel 1
```




```VB
Me.SetInstallLevel 1
```




```VB
SetInstallLevel 1
```



[<span data-ttu-id="eac85-119">Archivos ejecutables</span><span class="sxs-lookup"><span data-stu-id="eac85-119">Executable Files</span></span>](executable-files.md)

<span data-ttu-id="eac85-120">No se puede tener acceso a la sesión del instalador actual desde acciones personalizadas que llaman a los archivos ejecutables que se inician con una línea de comandos, por ejemplo, la [acción personalizada tipo 2](custom-action-type-2.md) y la [acción personalizada tipo 18](custom-action-type-18.md).</span><span class="sxs-lookup"><span data-stu-id="eac85-120">You cannot access the current installer session from custom actions that call executable files launched with a command-line, for example, [Custom Action Type 2](custom-action-type-2.md) and [Custom Action Type 18](custom-action-type-18.md).</span></span>

[<span data-ttu-id="eac85-121">Acciones personalizadas de ejecución aplazada</span><span class="sxs-lookup"><span data-stu-id="eac85-121">Deferred Execution Custom Actions</span></span>](deferred-execution-custom-actions.md)

<span data-ttu-id="eac85-122">No se puede tener acceso a la sesión de instalador actual o a todos los datos de propiedad de una acción personalizada de ejecución aplazada.</span><span class="sxs-lookup"><span data-stu-id="eac85-122">You cannot access the current installer session or all property data from a deferred execution custom action.</span></span> <span data-ttu-id="eac85-123">Para obtener más información, vea [obtener información de contexto para las acciones personalizadas de ejecución aplazada](obtaining-context-information-for-deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="eac85-123">For more information, see [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="eac85-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="eac85-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eac85-125">Obtener acceso a una base de datos o una sesión desde una acción personalizada</span><span class="sxs-lookup"><span data-stu-id="eac85-125">Accessing a Database or Session from Inside a Custom Action</span></span>](accessing-a-database-or-session-from-inside-a-custom-action.md)
</dt> </dl>

 

 



