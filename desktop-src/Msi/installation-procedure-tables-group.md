---
description: Las tablas del grupo procedimiento de instalación controlan las tareas realizadas durante la instalación por acciones estándar y acciones personalizadas.
ms.assetid: dff7cf4a-89a2-47b0-9038-93b79c0d915a
title: Grupo de tablas de procedimientos de instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbb3c5eb0306941d3cdd02bf7f994270ca0d6490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361550"
---
# <a name="installation-procedure-tables-group"></a><span data-ttu-id="ccfd4-103">Grupo de tablas de procedimientos de instalación</span><span class="sxs-lookup"><span data-stu-id="ccfd4-103">Installation Procedure Tables Group</span></span>

<span data-ttu-id="ccfd4-104">Las tablas del grupo procedimiento de instalación controlan las tareas realizadas durante la instalación por [acciones estándar](standard-actions.md) y [acciones personalizadas](custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="ccfd4-104">The tables in the Installation Procedure group control tasks performed during the installation by [standard actions](standard-actions.md) and [custom actions](custom-actions.md).</span></span>

<span data-ttu-id="ccfd4-105">Algunas de las tablas de este grupo controlan una acción de alto nivel proporcionando una secuencia de acciones.</span><span class="sxs-lookup"><span data-stu-id="ccfd4-105">Some of the tables in this group control a high level action by providing a sequence of actions.</span></span> <span data-ttu-id="ccfd4-106">Cada una de las tablas de secuencia siguientes controla una parte de una acción de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="ccfd4-106">Each of the following sequence tables controls a portion of a high level action.</span></span>

-   [<span data-ttu-id="ccfd4-107">Tabla InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="ccfd4-107">InstallUISequence table</span></span>](installuisequence-table.md)
-   [<span data-ttu-id="ccfd4-108">Tabla InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="ccfd4-108">InstallExecuteSequence table</span></span>](installexecutesequence-table.md)
-   [<span data-ttu-id="ccfd4-109">Tabla AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="ccfd4-109">AdminUISequence table</span></span>](adminuisequence-table.md)
-   [<span data-ttu-id="ccfd4-110">Tabla AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="ccfd4-110">AdminExecuteSequence table</span></span>](adminexecutesequence-table.md)
-   [<span data-ttu-id="ccfd4-111">Tabla AdvtUISequence</span><span class="sxs-lookup"><span data-stu-id="ccfd4-111">AdvtUISequence table</span></span>](advtuisequence-table.md)
-   [<span data-ttu-id="ccfd4-112">Tabla AdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="ccfd4-112">AdvtExecuteSequence table</span></span>](advtexecutesequence-table.md)

<span data-ttu-id="ccfd4-113">Puede haber situaciones en las que una instalación tenga que hacer algo que no sea posible mediante el uso de [acciones estándar](standard-actions.md)únicamente.</span><span class="sxs-lookup"><span data-stu-id="ccfd4-113">There may be situations in which an installation needs to do something that is not possible using only [standard actions](standard-actions.md).</span></span> <span data-ttu-id="ccfd4-114">Para proporcionar el mayor grado de flexibilidad, el instalador proporciona a los autores de la instalación la capacidad de crear sus propias acciones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="ccfd4-114">To provide the greatest degree of flexibility, the installer provides setup authors the ability to create their own custom actions.</span></span> <span data-ttu-id="ccfd4-115">Si tiene alguna acción personalizada, debe registrarla con el instalador rellenando la tabla CustomAction.</span><span class="sxs-lookup"><span data-stu-id="ccfd4-115">If you have any custom actions, you should register them with the installer by populating the CustomAction Table.</span></span>

<span data-ttu-id="ccfd4-116">La [tabla CustomAction](customaction-table.md) proporciona los medios para integrar el código personalizado y los datos en el proceso de instalación.</span><span class="sxs-lookup"><span data-stu-id="ccfd4-116">The [CustomAction table](customaction-table.md) provides the means of integrating custom code and data into the installation process.</span></span> <span data-ttu-id="ccfd4-117">El código que se ejecuta puede ser una secuencia contenida en la base de datos, un archivo instalado recientemente o un ejecutable existente.</span><span class="sxs-lookup"><span data-stu-id="ccfd4-117">The code that is executed can be a stream contained within the database, a recently installed file, or an existing executable.</span></span>

<span data-ttu-id="ccfd4-118">En las tablas siguientes se amplían las capacidades del instalador para manipular archivos y carpetas durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="ccfd4-118">The following tables extend the installer's capabilities to manipulate files and folders during the installation.</span></span>

-   <span data-ttu-id="ccfd4-119">La [tabla RemoveFile](removefile-table.md) contiene una lista de archivos que se quitan durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="ccfd4-119">The [RemoveFile table](removefile-table.md) contains a list of files that are removed during the installation.</span></span>
-   <span data-ttu-id="ccfd4-120">La [tabla RemoveIniFile](removeinifile-table.md) contiene la información que necesita una aplicación para quitarse de los archivos. ini.</span><span class="sxs-lookup"><span data-stu-id="ccfd4-120">The [RemoveIniFile table](removeinifile-table.md) contains the information an application needs to remove from .ini files.</span></span>
-   <span data-ttu-id="ccfd4-121">La [tabla RemoveRegistry](removeregistry-table.md) contiene la información que se elimina del registro del sistema cuando se selecciona el componente correspondiente para instalarse.</span><span class="sxs-lookup"><span data-stu-id="ccfd4-121">The [RemoveRegistry table](removeregistry-table.md) contains the information which is deleted from the system registry when the corresponding component is selected to be installed.</span></span>
-   <span data-ttu-id="ccfd4-122">En la [tabla CreateFolder](createfolder-table.md) se enumeran las carpetas que se deben crear durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="ccfd4-122">The [CreateFolder table](createfolder-table.md) lists the folders that must be created during the installation.</span></span> <span data-ttu-id="ccfd4-123">Aunque el instalador crea carpetas a medida que se necesitan, se quitan tan pronto como están vacías.</span><span class="sxs-lookup"><span data-stu-id="ccfd4-123">Although the installer creates folders as they are needed, these are removed as soon as they are empty.</span></span> <span data-ttu-id="ccfd4-124">La lista de carpetas de la tabla CreateFolder no se elimina hasta que se desinstale el componente.</span><span class="sxs-lookup"><span data-stu-id="ccfd4-124">Folders list in the CreateFolder table are not deleted until the component is uninstalled.</span></span>
-   <span data-ttu-id="ccfd4-125">La [tabla MoveFile](movefile-table.md) contiene una lista de archivos que se mueven o copian desde un directorio de origen especificado en el equipo del usuario a un directorio de destino.</span><span class="sxs-lookup"><span data-stu-id="ccfd4-125">The [MoveFile table](movefile-table.md) contains a list of files to be moved or copied from a specified source directory on the user's computer to a destination directory.</span></span> <span data-ttu-id="ccfd4-126">No es necesario usar la tabla MoveFile para describir los archivos asociados a los componentes que se van a instalar.</span><span class="sxs-lookup"><span data-stu-id="ccfd4-126">It is not necessary to use the MoveFile table to describe the files associated with the components you are installing.</span></span>

<span data-ttu-id="ccfd4-127">Para configurar las condiciones necesarias que se deben cumplir para iniciar la instalación, rellene la tabla LaunchCondition.</span><span class="sxs-lookup"><span data-stu-id="ccfd4-127">To set up necessary conditions that must be met to initiate the installation, populate the LaunchCondition table.</span></span>

<span data-ttu-id="ccfd4-128">La [tabla LaunchCondition](launchcondition-table.md) contiene una lista de condiciones que se deben satisfacer para que la acción se realice correctamente.</span><span class="sxs-lookup"><span data-stu-id="ccfd4-128">The [LaunchCondition table](launchcondition-table.md) contains a list of conditions, all of which must be satisfied for the action to succeed.</span></span>

 

 



