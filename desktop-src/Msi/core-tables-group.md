---
description: Para obtener más información sobre el diagrama siguiente, vea la leyenda del diagrama de relaciones de entidades.
ms.assetid: ec4f585d-cbd5-4c25-aaf4-1c1333fd4587
title: Grupo de tablas principales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5a5cc87e80c60505025825353272699db574bd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002858"
---
# <a name="core-tables-group"></a><span data-ttu-id="3b68a-103">Grupo de tablas principales</span><span class="sxs-lookup"><span data-stu-id="3b68a-103">Core Tables Group</span></span>

<span data-ttu-id="3b68a-104">Para obtener más información sobre el diagrama siguiente, vea la [leyenda del diagrama de relaciones de entidades](entity-relationship-diagram-legend.md).</span><span class="sxs-lookup"><span data-stu-id="3b68a-104">For more information about the following diagram, see the [entity relationship diagram legend](entity-relationship-diagram-legend.md).</span></span>

![Grupo de tablas principales](images/core.png)

<span data-ttu-id="3b68a-106">El grupo principal consta de tablas que describen las características y los componentes fundamentales de la aplicación y el paquete del instalador.</span><span class="sxs-lookup"><span data-stu-id="3b68a-106">The core group consists of tables describing the fundamental features and components of the application and the installer package.</span></span> <span data-ttu-id="3b68a-107">Por lo tanto, los desarrolladores de paquetes de instalación deben considerar cómo rellenar estas tablas en primer lugar, ya que la organización de gran parte de la base de datos se verá patente del contenido de este grupo.</span><span class="sxs-lookup"><span data-stu-id="3b68a-107">Developers of install packages should therefore consider how to populate these tables first because the organization of much of the database will become apparent from the content of this group.</span></span>

-   <span data-ttu-id="3b68a-108">En la [tabla de características](feature-table.md) se enumeran todas las características que pertenecen a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3b68a-108">The [Feature table](feature-table.md) lists all features belonging to the application.</span></span>
-   <span data-ttu-id="3b68a-109">La [tabla de condiciones](condition-table.md) contiene las expresiones condicionales que determinan si se va a instalar una característica determinada.</span><span class="sxs-lookup"><span data-stu-id="3b68a-109">The [Condition table](condition-table.md) contains the conditional expressions that determine whether or not a particular feature will be installed.</span></span>
-   <span data-ttu-id="3b68a-110">En la [tabla FeatureComponents](featurecomponents-table.md) se describen los componentes que pertenecen a cada característica.</span><span class="sxs-lookup"><span data-stu-id="3b68a-110">The [FeatureComponents table](featurecomponents-table.md) describes which components belong to each feature.</span></span>
-   <span data-ttu-id="3b68a-111">En la [tabla componente](component-table.md) se enumeran todos los componentes que pertenecen a la instalación.</span><span class="sxs-lookup"><span data-stu-id="3b68a-111">The [Component table](component-table.md) lists all components belonging to the installation.</span></span>
-   <span data-ttu-id="3b68a-112">En la [tabla directorio](directory-table.md) se enumeran los directorios que son necesarios durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="3b68a-112">The [Directory table](directory-table.md) lists the directories that are needed during the installation.</span></span> <span data-ttu-id="3b68a-113">Dado que cada componente debe estar asociado a un solo directorio, la tabla de componentes está estrechamente relacionada con esta tabla y tiene una clave externa en la tabla de directorio.</span><span class="sxs-lookup"><span data-stu-id="3b68a-113">Because each component must be associated with one and only one directory, the Component table is closely related to this table and has an external key to the Directory table.</span></span>
-   <span data-ttu-id="3b68a-114">En la [tabla PublishComponent](publishcomponent-table.md) se enumeran las características y los componentes que se publican para su uso por parte de otras aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="3b68a-114">The [PublishComponent table](publishcomponent-table.md) lists the features and components that are published for use by other applications.</span></span> <span data-ttu-id="3b68a-115">Los [componentes y las características](components-and-features.md) son los dos tipos de anuncios de características.</span><span class="sxs-lookup"><span data-stu-id="3b68a-115">[Components and Features](components-and-features.md) are the two types of feature advertisement.</span></span>
-   <span data-ttu-id="3b68a-116">La [tabla MsiAssembly](msiassembly-table.md) especifica Windows Installer valores de .NET Framework ensamblados Common Language Runtime y ensamblados Win32.</span><span class="sxs-lookup"><span data-stu-id="3b68a-116">The [MsiAssembly table](msiassembly-table.md) specifies Windows Installer settings for .NET Framework common language runtime assemblies and Win32 assemblies.</span></span>
-   <span data-ttu-id="3b68a-117">La [tabla MsiAssemblyName](msiassemblyname-table.md) especifica el esquema de los elementos de un nombre de caché de ensamblados seguro para un ensamblado de Common Language Runtime o Win32.</span><span class="sxs-lookup"><span data-stu-id="3b68a-117">The [MsiAssemblyName table](msiassemblyname-table.md) specifies the schema for the elements of a strong assembly cache name for a common language runtime or Win32 assembly.</span></span>
-   <span data-ttu-id="3b68a-118">La [tabla ComPlus](complus-table.md) contiene información necesaria para instalar aplicaciones com+.</span><span class="sxs-lookup"><span data-stu-id="3b68a-118">The [Complus table](complus-table.md) contains information needed to install COM+ applications.</span></span>
-   <span data-ttu-id="3b68a-119">La [tabla IsolatedComponent](isolatedcomponent-table.md) asocia el componente especificado en la columna de aplicación de componentes \_ (normalmente un archivo. exe) con el componente especificado en la \_ columna compartida componente (normalmente, un archivo dll compartido).</span><span class="sxs-lookup"><span data-stu-id="3b68a-119">The [IsolatedComponent table](isolatedcomponent-table.md) associates the component specified in the Component\_Application column (commonly an .exe) with the component specified in the Component\_Shared column (commonly a shared DLL).</span></span>
-   <span data-ttu-id="3b68a-120">La [tabla de actualización](upgrade-table.md) contiene información necesaria durante las [actualizaciones principales](major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="3b68a-120">The [Upgrade table](upgrade-table.md) contains information required during [major upgrades](major-upgrades.md).</span></span>

 

 



