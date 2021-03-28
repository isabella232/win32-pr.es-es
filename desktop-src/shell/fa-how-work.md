---
description: Las asociaciones de archivo definen cómo el shell trata un tipo de archivo en el sistema.
ms.assetid: A1C05857-26F8-4d4a-977B-4782E8AFA317
title: Cómo funcionan las asociaciones de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cf307e40bb6165da4a2547fb8dafc1791a11ee6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276767"
---
# <a name="how-file-associations-work"></a><span data-ttu-id="65d84-103">Cómo funcionan las asociaciones de archivos</span><span class="sxs-lookup"><span data-stu-id="65d84-103">How File Associations Work</span></span>

<span data-ttu-id="65d84-104">Las asociaciones de archivo definen cómo el shell trata un [tipo de archivo](fa-file-types.md) en el sistema.</span><span class="sxs-lookup"><span data-stu-id="65d84-104">File associations define how the Shell treats a [file type](fa-file-types.md) on the system.</span></span>

<span data-ttu-id="65d84-105">Este tema se organiza de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="65d84-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="65d84-106">Acerca de las asociaciones de archivos</span><span class="sxs-lookup"><span data-stu-id="65d84-106">About File Associations</span></span>](#about-file-associations)
-   [<span data-ttu-id="65d84-107">Cuándo debe implementar o modificar las asociaciones de archivos</span><span class="sxs-lookup"><span data-stu-id="65d84-107">When You Should Implement or Modify File Associations</span></span>](#when-you-should-implement-or-modify-file-associations)
-   [<span data-ttu-id="65d84-108">Cómo funcionan las asociaciones de archivos</span><span class="sxs-lookup"><span data-stu-id="65d84-108">How File Associations Work</span></span>](#how-file-associations-work)
-   [<span data-ttu-id="65d84-109">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="65d84-109">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="65d84-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="65d84-110">Related topics</span></span>](#related-topics)

## <a name="about-file-associations"></a><span data-ttu-id="65d84-111">Acerca de las asociaciones de archivos</span><span class="sxs-lookup"><span data-stu-id="65d84-111">About File Associations</span></span>

<span data-ttu-id="65d84-112">Las asociaciones de archivos controlan la siguiente funcionalidad:</span><span class="sxs-lookup"><span data-stu-id="65d84-112">File associations control the following functionality:</span></span>

-   <span data-ttu-id="65d84-113">La aplicación que se inicia cuando un usuario hace doble clic en un archivo.</span><span class="sxs-lookup"><span data-stu-id="65d84-113">Which application launches when a user double-clicks a file.</span></span>
-   <span data-ttu-id="65d84-114">El icono que aparece para un archivo de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="65d84-114">Which icon appears for a file by default.</span></span>
-   <span data-ttu-id="65d84-115">Cómo aparece el tipo de archivo cuando se ve en el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="65d84-115">How the file type appears when viewed in Windows Explorer.</span></span>
-   <span data-ttu-id="65d84-116">Qué comandos aparecen en el menú contextual de un archivo.</span><span class="sxs-lookup"><span data-stu-id="65d84-116">Which commands appear in a file's shortcut menu.</span></span>
-   <span data-ttu-id="65d84-117">Otras características de la interfaz de usuario, como información sobre herramientas, información de mosaico y el panel de detalles.</span><span class="sxs-lookup"><span data-stu-id="65d84-117">Other UI features, such as tooltips, tile info, and the details pane.</span></span>

<span data-ttu-id="65d84-118">Los desarrolladores de aplicaciones pueden usar asociaciones de archivos para controlar el modo en que el shell trata los tipos de archivo personalizados o para asociar una aplicación a los tipos de archivo existentes.</span><span class="sxs-lookup"><span data-stu-id="65d84-118">Application developers can use file associations to control how the Shell treats custom file types, or to associate an application with existing file types.</span></span> <span data-ttu-id="65d84-119">Por ejemplo, cuando se instala una aplicación, la aplicación puede comprobar la presencia de las asociaciones de archivos existentes y crear o invalidar esas asociaciones de archivo.</span><span class="sxs-lookup"><span data-stu-id="65d84-119">For example, when an application is installed, the application can check for the presence of existing file associations, and either create or override those file associations.</span></span>

<span data-ttu-id="65d84-120">Los usuarios pueden controlar algunos aspectos de las asociaciones de archivos para personalizar el modo en que el shell trata un tipo de archivo mediante la interfaz de usuario **abrir con** o editando el registro.</span><span class="sxs-lookup"><span data-stu-id="65d84-120">Users can control some aspects of file associations to customize how the Shell treats a file type either by using the **Open With** UI, or editing the registry.</span></span>

<span data-ttu-id="65d84-121">En la ventana del explorador de Windows que se muestra en la captura de pantalla siguiente, el shell muestra iconos diferentes para cada archivo, en función del icono asociado al tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="65d84-121">In the Windows Explorer window shown in the screen shot below, the Shell displays different icons for each file, based on the icon associated with the file type.</span></span> <span data-ttu-id="65d84-122">Si el usuario hace doble clic en la **imagen de mapa de bits de ejemplo** de archivo, el shell inicia Paint y lo usa para abrir el archivo porque en este sistema, Paint está asociado a archivos. bmp.</span><span class="sxs-lookup"><span data-stu-id="65d84-122">If the user double-clicks the file **Sample Bitmap Image**, the Shell launches Paint and uses it to open the file because on this system, Paint is associated with .bmp files.</span></span> <span data-ttu-id="65d84-123">Las personas pueden controlar estas acciones mediante asociaciones de archivo.</span><span class="sxs-lookup"><span data-stu-id="65d84-123">People can control these actions using file associations.</span></span>

![Ilustración de cómo funcionan las asociaciones de archivos en la práctica](images/file-assoc/fileassoc-icons.png)

## <a name="when-you-should-implement-or-modify-file-associations"></a><span data-ttu-id="65d84-125">Cuándo debe implementar o modificar las asociaciones de archivos</span><span class="sxs-lookup"><span data-stu-id="65d84-125">When You Should Implement or Modify File Associations</span></span>

<span data-ttu-id="65d84-126">Las aplicaciones pueden usar archivos para varios propósitos: algunos archivos se usan exclusivamente en la aplicación y no suelen tener acceso a ellos los usuarios, mientras que otros archivos son creados por el usuario y se suelen abrir, buscar y ver desde el shell.</span><span class="sxs-lookup"><span data-stu-id="65d84-126">Applications can use files for various purposes: some files are used exclusively by the application, and are not typically accessed by users, while other files are created by the user and are often opened, searched for, and viewed from the Shell.</span></span>

<span data-ttu-id="65d84-127">A menos que la aplicación use exclusivamente el tipo de archivo personalizado, debe implementar las asociaciones de archivo para él.</span><span class="sxs-lookup"><span data-stu-id="65d84-127">Unless your custom file type is used exclusively by the application, you should implement file associations for it.</span></span> <span data-ttu-id="65d84-128">Como norma general, implemente asociaciones de archivo para el tipo de archivo personalizado si espera que el usuario interactúe directamente con estos archivos de cualquier manera.</span><span class="sxs-lookup"><span data-stu-id="65d84-128">As a general rule, implement file associations for your custom file type if you expect the user to interact directly with these files in any way.</span></span> <span data-ttu-id="65d84-129">Esto incluye el uso del shell para examinar y abrir los archivos, buscar el contenido o las propiedades de los archivos y obtener una vista previa de los archivos.</span><span class="sxs-lookup"><span data-stu-id="65d84-129">That includes using the Shell to browse and open the files, searching the content or properties of the files, and previewing the files.</span></span>

<span data-ttu-id="65d84-130">Si la aplicación controla un tipo de archivo existente, no modifique la Asociación de archivo a menos que desee modificar la forma en que el shell controla todos los archivos de este tipo.</span><span class="sxs-lookup"><span data-stu-id="65d84-130">If your application is handling an existing file type, do not modify the file association unless you want to modify the way the Shell handles all files of this type.</span></span>

## <a name="how-file-associations-work"></a><span data-ttu-id="65d84-131">Cómo funcionan las asociaciones de archivos</span><span class="sxs-lookup"><span data-stu-id="65d84-131">How File Associations Work</span></span>

<span data-ttu-id="65d84-132">Los archivos se exponen en el shell como elementos de Shell.</span><span class="sxs-lookup"><span data-stu-id="65d84-132">Files are exposed in the Shell as Shell items.</span></span> <span data-ttu-id="65d84-133">Para controlar las asociaciones de archivos, los desarrolladores de aplicaciones pueden registrar una asignación entre el tipo de archivo y los controladores (objetos COM que proporcionan funcionalidad para los elementos de Shell del tipo de archivo).</span><span class="sxs-lookup"><span data-stu-id="65d84-133">To control file associations, application developers can register a mapping between the file type and the handlers (COM objects that provide functionality for the file type's Shell items).</span></span> <span data-ttu-id="65d84-134">Cuando el shell necesita consultar las asociaciones de archivo de un tipo de archivo, crea una matriz de claves del registro que contienen las asociaciones para el tipo de archivo y comprueba estas claves para que las asociaciones de archivos correspondientes las utilicen.</span><span class="sxs-lookup"><span data-stu-id="65d84-134">When the Shell needs to query for the file associations of a file type, it creates an array of registry keys containing the associations for the file type, and checks these keys for the appropriate file associations to use.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="65d84-135">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="65d84-135">Additional Resources</span></span>

-   <span data-ttu-id="65d84-136">Para obtener información conceptual sobre las asociaciones de archivos, vea [información general sobre verbos y asociaciones de archivo](fa-verbs.md).</span><span class="sxs-lookup"><span data-stu-id="65d84-136">For conceptual background on file associations, see [Overview of Verbs and File Associations](fa-verbs.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="65d84-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="65d84-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65d84-138">Registro de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="65d84-138">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="65d84-139">Tipos de archivo</span><span class="sxs-lookup"><span data-stu-id="65d84-139">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="65d84-140">Vista de contenido por tipo de archivo o tipo</span><span class="sxs-lookup"><span data-stu-id="65d84-140">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="65d84-141">Comprobador de tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="65d84-141">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="65d84-142">Controladores de tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="65d84-142">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="65d84-143">Identificadores de programación</span><span class="sxs-lookup"><span data-stu-id="65d84-143">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="65d84-144">Tipos percibidos</span><span class="sxs-lookup"><span data-stu-id="65d84-144">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="65d84-145">Matrices de asociación</span><span class="sxs-lookup"><span data-stu-id="65d84-145">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 



