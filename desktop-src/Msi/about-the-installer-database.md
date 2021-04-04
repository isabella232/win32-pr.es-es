---
description: La base de datos de Windows Installer se compone de muchas tablas interrelacionadas que forman una base de datos relacional de la información necesaria para instalar un grupo de aplicaciones.
ms.assetid: 3352dd8f-c082-4c4b-98be-5823c8b28f07
title: Acerca de la base de datos del instalador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7f0ee2cc326f85d964ac3d845b97751a48fbb91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909153"
---
# <a name="about-the-installer-database"></a><span data-ttu-id="9a9d7-103">Acerca de la base de datos del instalador</span><span class="sxs-lookup"><span data-stu-id="9a9d7-103">About the Installer Database</span></span>

<span data-ttu-id="9a9d7-104">La base de datos de Windows Installer se compone de muchas tablas interrelacionadas que forman una base de datos relacional de la información necesaria para instalar un grupo de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="9a9d7-104">The Windows Installer database consists of many interrelated tables that together comprise a relational database of the information necessary to install a group of applications.</span></span> <span data-ttu-id="9a9d7-105">Dado que la base de datos es relacional, las tablas se vinculan a través de los datos de los valores de clave principal y de clave externa.</span><span class="sxs-lookup"><span data-stu-id="9a9d7-105">Because the database is relational, the tables are linked through the data in the primary and foreign key values.</span></span> <span data-ttu-id="9a9d7-106">Esto proporciona un método eficaz para cambiar el proceso de instalación y significa que los usuarios pueden personalizar más fácilmente una aplicación grande o un grupo de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="9a9d7-106">This provides an efficient method for changing the installation process and means that users can more easily customize a large application or group of applications.</span></span> <span data-ttu-id="9a9d7-107">Las tablas de base de datos reflejan el diseño general de todo el grupo de aplicaciones, entre las que se incluyen:</span><span class="sxs-lookup"><span data-stu-id="9a9d7-107">The database tables reflect the general layout of the entire group of applications, including:</span></span>

-   <span data-ttu-id="9a9d7-108">Características disponibles</span><span class="sxs-lookup"><span data-stu-id="9a9d7-108">Available features</span></span>
-   <span data-ttu-id="9a9d7-109">Componentes</span><span class="sxs-lookup"><span data-stu-id="9a9d7-109">Components</span></span>
-   <span data-ttu-id="9a9d7-110">Relación entre características y componentes</span><span class="sxs-lookup"><span data-stu-id="9a9d7-110">Relationship between features and components</span></span>
-   <span data-ttu-id="9a9d7-111">Configuración necesaria del registro</span><span class="sxs-lookup"><span data-stu-id="9a9d7-111">Necessary registry settings</span></span>
-   <span data-ttu-id="9a9d7-112">Interfaz de usuario para la aplicación</span><span class="sxs-lookup"><span data-stu-id="9a9d7-112">User interface for the application</span></span>

<span data-ttu-id="9a9d7-113">Para crear una base de datos de instalación, debe rellenar las tablas con toda la información sobre las aplicaciones y el proceso de instalación.</span><span class="sxs-lookup"><span data-stu-id="9a9d7-113">To create an installation database, you must populate the tables with all the information about the applications and the installation process.</span></span> <span data-ttu-id="9a9d7-114">La creación manual de todas estas tablas se convierte en una tarea grande incluso para una instalación de tamaño moderado. por lo tanto, algunas herramientas de terceros están disponibles para ayudar a crear la base de datos del instalador.</span><span class="sxs-lookup"><span data-stu-id="9a9d7-114">Manually authoring all these tables becomes a large task even for a moderate size installation; therefore some third-party tools are available to assist with building the installer database.</span></span> <span data-ttu-id="9a9d7-115">En las secciones siguientes se describen los grupos de tablas de bases de datos relacionadas.</span><span class="sxs-lookup"><span data-stu-id="9a9d7-115">The following sections describe groups of related database tables.</span></span>

[<span data-ttu-id="9a9d7-116">Grupo de tablas principales</span><span class="sxs-lookup"><span data-stu-id="9a9d7-116">Core Tables Group</span></span>](core-tables-group.md)

[<span data-ttu-id="9a9d7-117">Grupo de tablas de archivos</span><span class="sxs-lookup"><span data-stu-id="9a9d7-117">File Tables Group</span></span>](file-tables-group.md)

[<span data-ttu-id="9a9d7-118">Grupo de tablas del registro</span><span class="sxs-lookup"><span data-stu-id="9a9d7-118">Registry Tables Group</span></span>](registry-tables-group.md)

[<span data-ttu-id="9a9d7-119">Grupo tablas del sistema</span><span class="sxs-lookup"><span data-stu-id="9a9d7-119">System Tables Group</span></span>](system-tables-group.md)

[<span data-ttu-id="9a9d7-120">Grupo de tablas de localizador</span><span class="sxs-lookup"><span data-stu-id="9a9d7-120">Locator Tables Group</span></span>](locator-tables-group.md)

[<span data-ttu-id="9a9d7-121">Grupo de tablas de información de programas</span><span class="sxs-lookup"><span data-stu-id="9a9d7-121">Program Information Tables Group</span></span>](program-information-tables-group.md)

[<span data-ttu-id="9a9d7-122">Grupo de tablas de procedimientos de instalación</span><span class="sxs-lookup"><span data-stu-id="9a9d7-122">Installation Procedure Tables Group</span></span>](installation-procedure-tables-group.md)

[<span data-ttu-id="9a9d7-123">Leyenda de diagrama de relación de entidades</span><span class="sxs-lookup"><span data-stu-id="9a9d7-123">Entity Relationship Diagram Legend</span></span>](entity-relationship-diagram-legend.md)

[<span data-ttu-id="9a9d7-124">Archivos de archivo de texto</span><span class="sxs-lookup"><span data-stu-id="9a9d7-124">Text Archive Files</span></span>](text-archive-files.md)

<span data-ttu-id="9a9d7-125">Para obtener una lista completa de todas las tablas de una base de datos de instalación, vea [tablas de base de datos](database-tables.md).</span><span class="sxs-lookup"><span data-stu-id="9a9d7-125">For a complete list of all tables in an installation database, see [Database Tables](database-tables.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a9d7-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9a9d7-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a9d7-127">Versiones publicadas, herramientas y redistribuibles</span><span class="sxs-lookup"><span data-stu-id="9a9d7-127">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



