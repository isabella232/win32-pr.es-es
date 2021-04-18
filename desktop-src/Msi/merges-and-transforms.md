---
description: El Windows Installer mantiene toda la información sobre la instalación en una base de datos relacional. Puede modificar esta base de datos y, por lo tanto, la instalación, mediante transformaciones y combinaciones.
ms.assetid: 32163e06-d03d-4b65-b744-62f306f2100d
title: Combinaciones y transformaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aec6314e81afb5afa9d74346b64fe3129ba5ed30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653039"
---
# <a name="merges-and-transforms"></a><span data-ttu-id="215a3-104">Combinaciones y transformaciones</span><span class="sxs-lookup"><span data-stu-id="215a3-104">Merges and Transforms</span></span>

<span data-ttu-id="215a3-105">El Windows Installer mantiene toda la información sobre la instalación en una base de datos relacional.</span><span class="sxs-lookup"><span data-stu-id="215a3-105">The Windows Installer keeps all information about the installation in a relational database.</span></span> <span data-ttu-id="215a3-106">Puede modificar esta base de datos y, por lo tanto, la instalación, mediante transformaciones y combinaciones.</span><span class="sxs-lookup"><span data-stu-id="215a3-106">You can modify this database, and therefore the installation, by using transforms and merges.</span></span>

## <a name="transforms"></a><span data-ttu-id="215a3-107">Transformaciones</span><span class="sxs-lookup"><span data-stu-id="215a3-107">Transforms</span></span>

<span data-ttu-id="215a3-108">Una [transformación de base de datos](database-transforms.md) agrega o reemplaza elementos en la base de datos original.</span><span class="sxs-lookup"><span data-stu-id="215a3-108">A [database transform](database-transforms.md) adds or replaces elements in the original database.</span></span> <span data-ttu-id="215a3-109">Por ejemplo, una transformación puede cambiar todo el texto de la interfaz de usuario de la aplicación de francés a Inglés.</span><span class="sxs-lookup"><span data-stu-id="215a3-109">For example, a transform can change all of the text in an application's user interface from French to English.</span></span>

<span data-ttu-id="215a3-110">Los usos principales de las transformaciones incluyen:</span><span class="sxs-lookup"><span data-stu-id="215a3-110">Primary uses for transforms include:</span></span>

-   <span data-ttu-id="215a3-111">Personalización de paquetes de instalación base para grupos de usuarios concretos.</span><span class="sxs-lookup"><span data-stu-id="215a3-111">Customization of base installation packages for particular groups of users.</span></span>

    <span data-ttu-id="215a3-112">Las transformaciones se pueden usar para encapsular las diferentes personalizaciones de un único paquete base que son necesarias para distintos grupos de usuarios.</span><span class="sxs-lookup"><span data-stu-id="215a3-112">Transforms can be used to encapsulate the various customizations of a single base package that are required by different groups of users.</span></span> <span data-ttu-id="215a3-113">Por ejemplo, esto es útil en organizaciones en las que los departamentos de soporte técnico y Finanzas requieren diferentes instalaciones de un producto determinado.</span><span class="sxs-lookup"><span data-stu-id="215a3-113">For example, this is useful in organizations where the finance and staff support departments require different installations of a particular product.</span></span> <span data-ttu-id="215a3-114">El paquete base de un producto puede estar disponible para todos los usuarios en un punto de instalación administrativa con las personalizaciones adecuadas distribuidas a cada grupo de usuarios por separado.</span><span class="sxs-lookup"><span data-stu-id="215a3-114">A product's base package can be available to everyone at one administrative installation point with appropriate customizations distributed to each group of users separately.</span></span>

-   <span data-ttu-id="215a3-115">Sincronización de aplicaciones entre lenguajes.</span><span class="sxs-lookup"><span data-stu-id="215a3-115">Synchronization of applications across languages.</span></span>

    <span data-ttu-id="215a3-116">Las transformaciones son útiles para mantener los paquetes creados en ubicaciones ampliamente separadas sincronizadas durante la creación.</span><span class="sxs-lookup"><span data-stu-id="215a3-116">Transforms are useful for keeping packages authored at widely separated locations synchronized during authoring.</span></span> <span data-ttu-id="215a3-117">Por ejemplo, si una actualización se desarrolla por primera vez para una versión en Inglés de una aplicación que existe en inglés y francés, se puede aplicar una transformación a la versión en inglés actualizada que la convierte en una versión en francés actualizada.</span><span class="sxs-lookup"><span data-stu-id="215a3-117">For example, if an upgrade is first developed for an English version of an application that exists in English and French, a transform can be applied to the upgraded English version that converts it into an upgraded French version.</span></span>

    <span data-ttu-id="215a3-118">Se pueden aplicar varias transformaciones a un paquete base y, a continuación, aplicar sobre la marcha durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="215a3-118">Multiple transforms can be applied to a base package and then applied on-the-fly during installation.</span></span> <span data-ttu-id="215a3-119">Esto amplía las capacidades del instalador para crear paquetes personalizados y proporciona un mecanismo para asignar eficazmente las instalaciones más adecuadas a distintos grupos de usuarios.</span><span class="sxs-lookup"><span data-stu-id="215a3-119">This extends the capabilities of the installer to create custom packages and provides a mechanism for efficiently assigning the most appropriate installations to different groups of users.</span></span>

-   <span data-ttu-id="215a3-120">Aplicación de revisiones.</span><span class="sxs-lookup"><span data-stu-id="215a3-120">Patching applications.</span></span>

    <span data-ttu-id="215a3-121">Las transformaciones se pueden usar para aplicar una corrección menor a una aplicación que no garantiza una actualización principal.</span><span class="sxs-lookup"><span data-stu-id="215a3-121">Transforms can be used to apply a minor fix to an application that does not warrant a major upgrade.</span></span> <span data-ttu-id="215a3-122">Para obtener más información acerca de las revisiones, consulte [paquetes de revisiones](patch-packages.md).</span><span class="sxs-lookup"><span data-stu-id="215a3-122">For more information about patches, see [Patch Packages](patch-packages.md).</span></span>

## <a name="merges"></a><span data-ttu-id="215a3-123">Combinaciones</span><span class="sxs-lookup"><span data-stu-id="215a3-123">Merges</span></span>

<span data-ttu-id="215a3-124">Una combinación combina dos bases de datos en una base de datos y agrega, en lugar de reemplazar, la información.</span><span class="sxs-lookup"><span data-stu-id="215a3-124">A merge combines two databases into one database, and adds, rather than replaces, information.</span></span> <span data-ttu-id="215a3-125">Si existe la misma información en ambas bases de datos, se produce un conflicto de fusión mediante combinación.</span><span class="sxs-lookup"><span data-stu-id="215a3-125">If the same information exists in both databases, a merge conflict occurs.</span></span> <span data-ttu-id="215a3-126">Las combinaciones son útiles para los equipos de desarrollo porque permiten que una aplicación grande se divida en partes que se pueden recombinar más adelante.</span><span class="sxs-lookup"><span data-stu-id="215a3-126">Merges are useful to development teams because they allow a large application to be divided into parts that can be recombined later.</span></span> <span data-ttu-id="215a3-127">Por ejemplo, los elementos de base de datos para la instalación de un componente nuevo se pueden desarrollar por separado y, posteriormente, combinarse en la base de datos de instalación principal.</span><span class="sxs-lookup"><span data-stu-id="215a3-127">For example, the database elements for the installation of a new component can be developed separately and later merged into the main installation database.</span></span> <span data-ttu-id="215a3-128">Para obtener más información, vea [módulos de combinación](merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="215a3-128">For more information, see [Merge Modules](merge-modules.md).</span></span>

<span data-ttu-id="215a3-129">Un equipo de desarrollo puede aplicar una operación de combinación de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="215a3-129">A development team might apply a merge operation in the following way:</span></span>

1.  <span data-ttu-id="215a3-130">Separar en grupos y trabajar simultáneamente en distintos componentes de una aplicación de gran tamaño.</span><span class="sxs-lookup"><span data-stu-id="215a3-130">Separate into groups and work simultaneously on different components of a large application.</span></span>
2.  <span data-ttu-id="215a3-131">A continuación, cada grupo de desarrollo rellena una base de datos con información de instalación para su propio componente, sin preocuparse por los demás componentes de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="215a3-131">Each development group then populates a database with installation information for its own component, without being concerned with the other components of the application.</span></span>
3.  <span data-ttu-id="215a3-132">Una vez completado el desarrollo de un componente, la base de datos de ese componente se puede combinar en la base de datos de instalación principal de toda la aplicación.</span><span class="sxs-lookup"><span data-stu-id="215a3-132">After the development of a component is complete, that component's database can be merged into the main installation database for the entire application.</span></span>

 

 



