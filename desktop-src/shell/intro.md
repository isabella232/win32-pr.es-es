---
description: La interfaz de usuario de Windows proporciona a los usuarios acceso a una gran variedad de objetos necesarios para ejecutar aplicaciones y administrar el sistema operativo.
title: Guía del desarrollador de Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 8f88ef25-3645-4f54-9453-41f919c0fc0a
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1be17ca90b7138294be3e1b34fa3fcb4dcb4227a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997293"
---
# <a name="shell-developers-guide"></a><span data-ttu-id="6c4cc-103">Guía del desarrollador de Shell</span><span class="sxs-lookup"><span data-stu-id="6c4cc-103">Shell Developer's Guide</span></span>

<span data-ttu-id="6c4cc-104">La interfaz de usuario de Windows proporciona a los usuarios acceso a una gran variedad de objetos necesarios para ejecutar aplicaciones y administrar el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="6c4cc-104">The Windows UI provides users with access to a wide variety of objects necessary to run applications and manage the operating system.</span></span> <span data-ttu-id="6c4cc-105">El más conocido de estos objetos son las carpetas y los archivos que residen en las unidades de disco del equipo.</span><span class="sxs-lookup"><span data-stu-id="6c4cc-105">The most numerous and familiar of these objects are the folders and files that reside on computer disk drives.</span></span> <span data-ttu-id="6c4cc-106">También hay una serie de objetos virtuales que permiten al usuario realizar tareas como el envío de archivos a las impresoras remotas o el acceso a la papelera de reciclaje.</span><span class="sxs-lookup"><span data-stu-id="6c4cc-106">There are also a number of virtual objects that allow the user to do tasks such as sending files to remote printers or accessing the Recycle Bin.</span></span> <span data-ttu-id="6c4cc-107">El shell organiza estos objetos en un espacio de nombres jerárquico y proporciona a los usuarios y las aplicaciones una manera coherente y eficaz de obtener acceso a los objetos y administrarlos.</span><span class="sxs-lookup"><span data-stu-id="6c4cc-107">The Shell organizes these objects into a hierarchical namespace, and provides users and applications with a consistent and efficient way to access and manage objects.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6c4cc-108">En esta sección</span><span class="sxs-lookup"><span data-stu-id="6c4cc-108">In this section</span></span>

-   [<span data-ttu-id="6c4cc-109">Consideraciones de seguridad: Shell de Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="6c4cc-109">Security Considerations: Microsoft Windows Shell</span></span>](sec-shell.md)
-   [<span data-ttu-id="6c4cc-110">Instrucciones para implementar extensiones de In-Process</span><span class="sxs-lookup"><span data-stu-id="6c4cc-110">Guidance for Implementing In-Process Extensions</span></span>](shell-and-managed-code.md)
-   [<span data-ttu-id="6c4cc-111">Versiones de Shell y controles comunes</span><span class="sxs-lookup"><span data-stu-id="6c4cc-111">Shell and Common Controls Versions</span></span>](versions.md)
-   [<span data-ttu-id="6c4cc-112">Implementar las interfaces de objeto de carpeta básicas</span><span class="sxs-lookup"><span data-stu-id="6c4cc-112">Implementing the Basic Folder Object Interfaces</span></span>](nse-implement.md)
-   [<span data-ttu-id="6c4cc-113">Implementar un formato de archivo personalizado</span><span class="sxs-lookup"><span data-stu-id="6c4cc-113">Implementing a Custom File Format</span></span>](customizing-file-types-bumper.md)
-   [<span data-ttu-id="6c4cc-114">Extensibilidad de Shell (creación de un origen de datos)</span><span class="sxs-lookup"><span data-stu-id="6c4cc-114">Shell Extensibility (Creating a Data Source)</span></span>](shell-extensibility-bumper.md)
-   [<span data-ttu-id="6c4cc-115">Implementar elementos del panel de control</span><span class="sxs-lookup"><span data-stu-id="6c4cc-115">Implementing Control Panel Items</span></span>](control-panel-applications.md)
-   [<span data-ttu-id="6c4cc-116">Compatibilidad con aplicaciones de Shell</span><span class="sxs-lookup"><span data-stu-id="6c4cc-116">Supporting Shell Applications</span></span>](application-support-bumper.md)
-   [<span data-ttu-id="6c4cc-117">Temas de Shell heredados</span><span class="sxs-lookup"><span data-stu-id="6c4cc-117">Legacy Shell Topics</span></span>](miscellaneous-topics-bumper.md)

## <a name="document-conventions"></a><span data-ttu-id="6c4cc-118">Convenciones del documento</span><span class="sxs-lookup"><span data-stu-id="6c4cc-118">Document Conventions</span></span>

<span data-ttu-id="6c4cc-119">La guía para desarrolladores de Shell sigue las convenciones de documentos habituales del kit de desarrollo de software (SDK) de Windows.</span><span class="sxs-lookup"><span data-stu-id="6c4cc-119">The Shell Developers's Guide follows the usual Windows Software Development Kit (SDK) document conventions.</span></span> <span data-ttu-id="6c4cc-120">Deben tenerse en cuentan dos convenciones en particular:</span><span class="sxs-lookup"><span data-stu-id="6c4cc-120">Two conventions in particular should be noted:</span></span>

-   <span data-ttu-id="6c4cc-121">El código de ejemplo omite el código normal de corrección de errores.</span><span class="sxs-lookup"><span data-stu-id="6c4cc-121">Sample code omits normal error-correction code.</span></span> <span data-ttu-id="6c4cc-122">Este código solo se ha quitado para que el código sea más legible.</span><span class="sxs-lookup"><span data-stu-id="6c4cc-122">This code has been removed only to make the code more readable.</span></span> <span data-ttu-id="6c4cc-123">Debe incluir todo el código de corrección de errores adecuado en sus propias aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="6c4cc-123">You should include all appropriate error-correction code in your own applications.</span></span>
-   <span data-ttu-id="6c4cc-124">Para que las entradas del registro de ejemplo sean claras, los nombres de clave, subclaves y entradas, así como los valores se muestran con una fuente estándar.</span><span class="sxs-lookup"><span data-stu-id="6c4cc-124">To make sample registry entries clear, key, subkey, and entry names as well as values are displayed with a standard font.</span></span> <span data-ttu-id="6c4cc-125">Los nombres de los elementos definidos por el usuario o por la aplicación están en cursiva.</span><span class="sxs-lookup"><span data-stu-id="6c4cc-125">User or application-defined item names are italicized.</span></span>

 

 



