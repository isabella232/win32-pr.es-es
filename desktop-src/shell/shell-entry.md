---
description: La interfaz de usuario de Windows proporciona a los usuarios acceso a una gran variedad de objetos necesarios para ejecutar aplicaciones y administrar el sistema operativo.
title: Shell de Windows
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 1d0d4ed7-9b85-4d70-bf1f-82567a1687fb
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 448e1d5265ec34ce1889ca36f234622e2b082553
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985611"
---
# <a name="windows-shell"></a><span data-ttu-id="6d2cd-103">Shell de Windows</span><span class="sxs-lookup"><span data-stu-id="6d2cd-103">Windows Shell</span></span>

<span data-ttu-id="6d2cd-104">La interfaz de usuario de Windows proporciona a los usuarios acceso a una gran variedad de objetos necesarios para ejecutar aplicaciones y administrar el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="6d2cd-104">The Windows UI provides users with access to a wide variety of objects necessary for running applications and managing the operating system.</span></span> <span data-ttu-id="6d2cd-105">El más conocido de estos objetos son las carpetas y los archivos que residen en las unidades de disco del equipo.</span><span class="sxs-lookup"><span data-stu-id="6d2cd-105">The most numerous and familiar of these objects are the folders and files that reside on computer disk drives.</span></span> <span data-ttu-id="6d2cd-106">También hay una serie de objetos virtuales que permiten al usuario realizar tareas como el envío de archivos a las impresoras remotas o el acceso a la papelera de reciclaje.</span><span class="sxs-lookup"><span data-stu-id="6d2cd-106">There are also a number of virtual objects that allow the user to perform tasks such as sending files to remote printers or accessing the Recycle Bin.</span></span> <span data-ttu-id="6d2cd-107">El shell organiza estos objetos en un espacio de nombres jerárquico y proporciona a los usuarios y las aplicaciones una manera coherente y eficaz de obtener acceso a los objetos y administrarlos.</span><span class="sxs-lookup"><span data-stu-id="6d2cd-107">The Shell organizes these objects into a hierarchical namespace and provides users and applications with a consistent and efficient way to access and manage objects.</span></span>

## <a name="shell-development-scenarios"></a><span data-ttu-id="6d2cd-108">Escenarios de desarrollo de Shell</span><span class="sxs-lookup"><span data-stu-id="6d2cd-108">Shell Development Scenarios</span></span>

<span data-ttu-id="6d2cd-109">Los siguientes escenarios de desarrollo se relacionan con el desarrollo de aplicaciones:</span><span class="sxs-lookup"><span data-stu-id="6d2cd-109">The following development scenarios relate to application development:</span></span>

-   <span data-ttu-id="6d2cd-110">Extender el Shell, que consiste en crear un origen de datos (en lugar de consumir el modelo de datos de Shell)</span><span class="sxs-lookup"><span data-stu-id="6d2cd-110">Extending the Shell, which consists of creating a data source (versus consuming the Shell data model)</span></span>
-   <span data-ttu-id="6d2cd-111">Implementar un subconjunto de las tareas de origen de datos de Shell</span><span class="sxs-lookup"><span data-stu-id="6d2cd-111">Implementing a subset of the Shell data source tasks</span></span>
-   <span data-ttu-id="6d2cd-112">Compatibilidad con bibliotecas y vistas de elementos en el explorador de Windows</span><span class="sxs-lookup"><span data-stu-id="6d2cd-112">Supporting libraries and item views in Windows Explorer</span></span>
-   <span data-ttu-id="6d2cd-113">Usar el cuadro de diálogo archivo común</span><span class="sxs-lookup"><span data-stu-id="6d2cd-113">Using the common file dialog</span></span>
-   <span data-ttu-id="6d2cd-114">Implementar elementos del panel de control</span><span class="sxs-lookup"><span data-stu-id="6d2cd-114">Implementing Control Panel items</span></span>
-   <span data-ttu-id="6d2cd-115">Administración de notificaciones</span><span class="sxs-lookup"><span data-stu-id="6d2cd-115">Managing notifications</span></span>

<span data-ttu-id="6d2cd-116">Los siguientes escenarios de desarrollo se refieren a la propiedad del formato de archivo:</span><span class="sxs-lookup"><span data-stu-id="6d2cd-116">The following development scenarios relate to file format ownership:</span></span>

-   <span data-ttu-id="6d2cd-117">Implementar un subconjunto de las tareas de origen de datos de Shell</span><span class="sxs-lookup"><span data-stu-id="6d2cd-117">Implementing a subset of the Shell data source tasks</span></span>
-   <span data-ttu-id="6d2cd-118">Implementar cualquier controlador</span><span class="sxs-lookup"><span data-stu-id="6d2cd-118">Implementing any handler</span></span>
-   <span data-ttu-id="6d2cd-119">Compatibilidad con la búsqueda en el escritorio</span><span class="sxs-lookup"><span data-stu-id="6d2cd-119">Supporting desktop search</span></span>

<span data-ttu-id="6d2cd-120">Los siguientes escenarios de desarrollo se refieren a la propiedad del almacenamiento de datos:</span><span class="sxs-lookup"><span data-stu-id="6d2cd-120">The following development scenarios relate to data storage ownership:</span></span>

-   <span data-ttu-id="6d2cd-121">Compatibilidad con la búsqueda de escritorio y OpenSearch</span><span class="sxs-lookup"><span data-stu-id="6d2cd-121">Supporting desktop search and OpenSearch</span></span>
-   <span data-ttu-id="6d2cd-122">Implementar un subconjunto de las tareas de origen de datos de Shell (carpetas virtuales)</span><span class="sxs-lookup"><span data-stu-id="6d2cd-122">Implementing a subset of the Shell data source tasks (virtual folders)</span></span>
-   <span data-ttu-id="6d2cd-123">Bibliotecas auxiliares en el explorador de Windows</span><span class="sxs-lookup"><span data-stu-id="6d2cd-123">Supporting libraries in Windows Explorer</span></span>

<span data-ttu-id="6d2cd-124">El siguiente escenario de desarrollo está relacionado con la compatibilidad de dispositivos:</span><span class="sxs-lookup"><span data-stu-id="6d2cd-124">The following development scenario relates to device support:</span></span>

-   <span data-ttu-id="6d2cd-125">Ejecución automática y reproducción automática</span><span class="sxs-lookup"><span data-stu-id="6d2cd-125">Auto run and auto play</span></span>

## <a name="windows-shell-sdk-documentation"></a><span data-ttu-id="6d2cd-126">Documentación del SDK de Windows Shell</span><span class="sxs-lookup"><span data-stu-id="6d2cd-126">Windows Shell SDK Documentation</span></span>

<span data-ttu-id="6d2cd-127">Esta documentación se divide en tres secciones principales:</span><span class="sxs-lookup"><span data-stu-id="6d2cd-127">This documentation is broken into three major sections:</span></span>

-   <span data-ttu-id="6d2cd-128">La [Guía del desarrollador de Shell](intro.md) proporciona material conceptual sobre cómo funciona el Shell y cómo usar la API del shell en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6d2cd-128">The [Shell Developer's Guide](intro.md) provides conceptual material about how the Shell works and how to use the Shell's API in your application.</span></span>
-   <span data-ttu-id="6d2cd-129">La sección de [Referencia del shell](shell-reference-bumper.md) documenta los elementos de programación que componen las distintas API de Shell.</span><span class="sxs-lookup"><span data-stu-id="6d2cd-129">The [Shell Reference](shell-reference-bumper.md) section documents programming elements that make up the various Shell APIs.</span></span>
-   <span data-ttu-id="6d2cd-130">[Ejemplos de Shell](samples-entry.md) proporciona vínculos a ejemplos de código relacionados.</span><span class="sxs-lookup"><span data-stu-id="6d2cd-130">[Shell Samples](samples-entry.md) provides links to related code samples.</span></span>

<span data-ttu-id="6d2cd-131">En la tabla siguiente se proporciona un esquema de la sección de referencia de Shell.</span><span class="sxs-lookup"><span data-stu-id="6d2cd-131">The following table provides an outline of the Shell Reference section.</span></span> <span data-ttu-id="6d2cd-132">A menos que se indique lo contrario, todos los elementos de programación están documentados en C++ no administrado.</span><span class="sxs-lookup"><span data-stu-id="6d2cd-132">Unless otherwise noted, all programming elements are documented in unmanaged C++.</span></span>



| <span data-ttu-id="6d2cd-133">Sección</span><span class="sxs-lookup"><span data-stu-id="6d2cd-133">Section</span></span>                                                               | <span data-ttu-id="6d2cd-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="6d2cd-134">Description</span></span>                                                                                                          |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6d2cd-135">Clases de Shell</span><span class="sxs-lookup"><span data-stu-id="6d2cd-135">Shell Classes</span></span>](classes.md)                                          | <span data-ttu-id="6d2cd-136">En esta sección se describen las clases de Shell de Windows.</span><span class="sxs-lookup"><span data-stu-id="6d2cd-136">This section describes select Windows Shell classes.</span></span>                                                                 |
| [<span data-ttu-id="6d2cd-137">Interfaces de Shell</span><span class="sxs-lookup"><span data-stu-id="6d2cd-137">Shell Interfaces</span></span>](interfaces.md)                                    | <span data-ttu-id="6d2cd-138">En esta sección se describen las interfaces del modelo de objetos componentes (COM) del shell de Windows.</span><span class="sxs-lookup"><span data-stu-id="6d2cd-138">This section describes the Windows Shell Component Object Model (COM) interfaces.</span></span>                                    |
| [<span data-ttu-id="6d2cd-139">Funciones de Shell</span><span class="sxs-lookup"><span data-stu-id="6d2cd-139">Shell Functions</span></span>](functions.md)                                      | <span data-ttu-id="6d2cd-140">En esta sección se describen las funciones del shell de Windows.</span><span class="sxs-lookup"><span data-stu-id="6d2cd-140">This section describes the Windows Shell functions.</span></span>                                                                  |
| [<span data-ttu-id="6d2cd-141">Funciones de devolución de llamada de Shell</span><span class="sxs-lookup"><span data-stu-id="6d2cd-141">Shell Callback Functions</span></span>](callbacks.md)                             | <span data-ttu-id="6d2cd-142">En esta sección se describen las plantillas de funciones de devolución de llamada del shell de Windows.</span><span class="sxs-lookup"><span data-stu-id="6d2cd-142">This section describes the Windows Shell callback functions templates.</span></span>                                               |
| [<span data-ttu-id="6d2cd-143">Constantes, enumeraciones y marcas de Shell</span><span class="sxs-lookup"><span data-stu-id="6d2cd-143">Shell Constants, Enumerations, and Flags</span></span>](consts-enums-flags.md)    | <span data-ttu-id="6d2cd-144">En esta sección se describen las constantes, enumeraciones y marcas del shell de Windows que se usan en las API de Shell.</span><span class="sxs-lookup"><span data-stu-id="6d2cd-144">This section describes the Windows Shell constants, enumerations, and flags used in the Shell APIs.</span></span>                  |
| [<span data-ttu-id="6d2cd-145">Funciones de la utilidad ligera de Shell</span><span class="sxs-lookup"><span data-stu-id="6d2cd-145">Shell Lightweight Utility Functions</span></span>](shlwapi.md)                    | <span data-ttu-id="6d2cd-146">En esta sección se describen las funciones de utilidad ligera de Shell de Windows proporcionadas en Shlwapi.dll.</span><span class="sxs-lookup"><span data-stu-id="6d2cd-146">This section describes the Windows Shell lightweight utility functions provided in Shlwapi.dll.</span></span>                      |
| [<span data-ttu-id="6d2cd-147">Macros de Shell</span><span class="sxs-lookup"><span data-stu-id="6d2cd-147">Shell Macros</span></span>](macros.md)                                            | <span data-ttu-id="6d2cd-148">En esta sección se describen las macros de la utilidad Shell de Windows.</span><span class="sxs-lookup"><span data-stu-id="6d2cd-148">This section describes the Windows Shell utility macros.</span></span>                                                             |
| [<span data-ttu-id="6d2cd-149">Notificaciones y mensajes de Shell</span><span class="sxs-lookup"><span data-stu-id="6d2cd-149">Shell Messages and Notifications</span></span>](messages.md)                      | <span data-ttu-id="6d2cd-150">En esta sección se describen los mensajes y las notificaciones enviados por elementos del shell de Windows.</span><span class="sxs-lookup"><span data-stu-id="6d2cd-150">This section describes the messages and notifications sent by elements of the Windows Shell.</span></span>                         |
| [<span data-ttu-id="6d2cd-151">Objetos de Shell para scripting y Microsoft Visual Basic</span><span class="sxs-lookup"><span data-stu-id="6d2cd-151">Shell Objects for Scripting and Microsoft Visual Basic</span></span>](objects.md) | <span data-ttu-id="6d2cd-152">En esta sección se describen los objetos de Windows implementados por el shell para su uso en scripting y Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="6d2cd-152">This section describes the Windows objects implemented by the Shell for use in scripting and Microsoft Visual Basic.</span></span> |
| [<span data-ttu-id="6d2cd-153">Objetos de Shell para C++</span><span class="sxs-lookup"><span data-stu-id="6d2cd-153">Shell Objects for C++</span></span>](objects-cpp.md)                              | <span data-ttu-id="6d2cd-154">En esta sección se describen los objetos de Windows de C++ implementados por el shell.</span><span class="sxs-lookup"><span data-stu-id="6d2cd-154">This section describes the C++ Windows objects implemented by the Shell.</span></span>                                             |
| [<span data-ttu-id="6d2cd-155">Esquemas de Shell</span><span class="sxs-lookup"><span data-stu-id="6d2cd-155">Shell Schemas</span></span>](schemas.md)                                          | <span data-ttu-id="6d2cd-156">En esta sección se describen los esquemas de manifiesto de biblioteca, propiedad y transferencia utilizados por el shell de Windows.</span><span class="sxs-lookup"><span data-stu-id="6d2cd-156">This section describes library, property, and transfer manifest schemas used by the Windows Shell.</span></span>                   |
| [<span data-ttu-id="6d2cd-157">Estructuras de Shell</span><span class="sxs-lookup"><span data-stu-id="6d2cd-157">Shell Structures</span></span>](structures.md)                                    | <span data-ttu-id="6d2cd-158">En esta sección se describen las estructuras de Shell de Windows que se usan en las API de Shell.</span><span class="sxs-lookup"><span data-stu-id="6d2cd-158">This section describes the Windows Shell structures used in the Shell APIs.</span></span>                                          |



 

 

 



