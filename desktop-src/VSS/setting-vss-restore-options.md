---
description: Las opciones de restauración permiten a los solicitantes comunicar opciones de restauración personalizadas a escritores.
ms.assetid: 364550a1-070a-4f7e-bd62-84672959dc21
title: Establecer opciones de restauración de VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c814ffb94f25229e7f3e17f592c631f13b6717e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696969"
---
# <a name="setting-vss-restore-options"></a><span data-ttu-id="9d6f8-103">Establecer opciones de restauración de VSS</span><span class="sxs-lookup"><span data-stu-id="9d6f8-103">Setting VSS Restore Options</span></span>

<span data-ttu-id="9d6f8-104">Las opciones de restauración permiten a los solicitantes comunicar opciones de restauración personalizadas a escritores.</span><span class="sxs-lookup"><span data-stu-id="9d6f8-104">Restore options allow requesters to communicate customized restore options to writers.</span></span>

## <a name="restore-options"></a><span data-ttu-id="9d6f8-105">Opciones de restauración</span><span class="sxs-lookup"><span data-stu-id="9d6f8-105">Restore Options</span></span>

<span data-ttu-id="9d6f8-106">La estandarización del formato de las opciones de restauración permite que escritores y solicitantes controlen las solicitudes personalizadas comunes.</span><span class="sxs-lookup"><span data-stu-id="9d6f8-106">Standardizing the format of the restore options allow writers and requesters to handle common custom requests.</span></span> <span data-ttu-id="9d6f8-107">Las opciones de restauración las establece el solicitante llamando al método [**ivssbackupcomponents:: SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) hasta una vez por cada componente de copia de seguridad seleccionado antes de llamar al método [**ivssbackupcomponents::P rerestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) .</span><span class="sxs-lookup"><span data-stu-id="9d6f8-107">Restore options are set by the requester by calling the [**IVssBackupComponents::SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) method up to once per selected-for-backup component before calling the [**IVssBackupComponents::PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) method.</span></span> <span data-ttu-id="9d6f8-108">La cadena que se pasa en el parámetro *wszRestoreOptions* al método **SetRestoreOptions** puede contener varios valores, tal y como se describe a continuación.</span><span class="sxs-lookup"><span data-stu-id="9d6f8-108">The string passed in the *wszRestoreOptions* parameter to the **SetRestoreOptions** method can contain multiple values, as described below.</span></span>

## <a name="format"></a><span data-ttu-id="9d6f8-109">Formato</span><span class="sxs-lookup"><span data-stu-id="9d6f8-109">Format</span></span>

<span data-ttu-id="9d6f8-110">El formato de las opciones de restauración, es uno o varios pares de nombre/valor separados por comas, y el nombre se antepone opcionalmente al nombre del subcomponente al que se aplica.</span><span class="sxs-lookup"><span data-stu-id="9d6f8-110">The format of restore options, is one or more comma-separated name/value pairs, and the name is optionally prefixed with the name of the subcomponent to which it applies.</span></span> <span data-ttu-id="9d6f8-111">Los nombres de componente y de opción no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="9d6f8-111">The component names and option names are case-insensitive.</span></span> <span data-ttu-id="9d6f8-112">El escritor determina la distinción de mayúsculas y minúsculas de los valores.</span><span class="sxs-lookup"><span data-stu-id="9d6f8-112">The case-sensitivity of the values is determined by the writer.</span></span> <span data-ttu-id="9d6f8-113">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="9d6f8-113">For example:</span></span>

``` syntax
"Child1":"Option1"="Value1","Option2"="Value2","Child2\Grandchild3":"Option3"="Value3"
```

<span data-ttu-id="9d6f8-114">En este ejemplo, "Opción1" solo se aplica al subcomponente "Child1" y a sus descendientes, "opción2" se aplica a todos los componentes y sus descendientes, y "Option3" solo se aplica a los \\ subcomponentes "Child2 Grandchild3" y a sus descendientes.</span><span class="sxs-lookup"><span data-stu-id="9d6f8-114">In this example, "Option1" only applies to the "Child1" subcomponent and its descendants, "Option2" applies to all components and their descendants, and "Option3" applies only to the "Child2\\Grandchild3" subcomponents and its descendants.</span></span>

<span data-ttu-id="9d6f8-115">Solo se puede llamar al método [**SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) en los componentes que se pueden seleccionar para la copia de seguridad, mientras que los nodos descendientes no se pueden seleccionar para la copia de seguridad, pueden seleccionarse para la restauración.</span><span class="sxs-lookup"><span data-stu-id="9d6f8-115">The [**SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) method can only be called on components that are selectable for backup, while descendant nodes may not be selectable for backup, they may be selectable for restore.</span></span>

## <a name="common-restore-options"></a><span data-ttu-id="9d6f8-116">Opciones de restauración comunes</span><span class="sxs-lookup"><span data-stu-id="9d6f8-116">Common Restore Options</span></span>

<span data-ttu-id="9d6f8-117">Estas opciones de restauración comunes se han definido para aumentar la interoperabilidad entre escritores y solicitantes.</span><span class="sxs-lookup"><span data-stu-id="9d6f8-117">These common restore options have been defined to increase interoperability between writers and requesters.</span></span>

-   <span data-ttu-id="9d6f8-118">Restaur</span><span class="sxs-lookup"><span data-stu-id="9d6f8-118">Authoritative</span></span>

    <span data-ttu-id="9d6f8-119">La opción "autoritativa" admite varios valores "Item", pero solo un valor "All".</span><span class="sxs-lookup"><span data-stu-id="9d6f8-119">The "Authoritative" option supports multiple "Item" values, but only one "All" value.</span></span>

    <span data-ttu-id="9d6f8-120">Todo este componente es autoritativo.</span><span class="sxs-lookup"><span data-stu-id="9d6f8-120">This entire component is authoritative.</span></span>

    ``` syntax
    "Authoritative"="All"
    ```

    <span data-ttu-id="9d6f8-121">Solo el elemento especificado es autoritativo.</span><span class="sxs-lookup"><span data-stu-id="9d6f8-121">Only the specified item is authoritative.</span></span> <span data-ttu-id="9d6f8-122">El escritor define el formato del elemento con nombre.</span><span class="sxs-lookup"><span data-stu-id="9d6f8-122">The format of the named item is defined by the writer.</span></span> <span data-ttu-id="9d6f8-123">Las designaciones comunes son " \* " para indicar todos los archivos, "..." para indicar todos los archivos y subdirectorios del componente especificado.</span><span class="sxs-lookup"><span data-stu-id="9d6f8-123">Common designations are "\*" to indicate all files, "..." to indicate all files and subdirectories of the specified component.</span></span>

    ``` syntax
    "Authoritative"="Item:XXX"
    ```

-   <span data-ttu-id="9d6f8-124">Puesta al día</span><span class="sxs-lookup"><span data-stu-id="9d6f8-124">Roll Forward</span></span>

    <span data-ttu-id="9d6f8-125">Después de restaurar una base de datos, los escritores normalmente se ponen al día a través de los registros para actualizar la base de datos.</span><span class="sxs-lookup"><span data-stu-id="9d6f8-125">After a database is restored, writers usually roll forward through logs to bring the database up to date.</span></span> <span data-ttu-id="9d6f8-126">En el caso de las restauraciones incrementales o diferenciales, el solicitante usa el método [**IVssBackupComponents:: SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores) para controlar parcialmente el comportamiento de control de registros: esta opción de restauración permite un control más granular.</span><span class="sxs-lookup"><span data-stu-id="9d6f8-126">In the case of incremental or differential restores, the requester uses the [**IVssBackupComponents::SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores) method to partially control the log-handling behavior - this restore option allows more granular control.</span></span>

    <span data-ttu-id="9d6f8-127">No revierta los registros.</span><span class="sxs-lookup"><span data-stu-id="9d6f8-127">Do not roll through logs.</span></span>

    ``` syntax
    "Roll Forward"="None"
    ```

    <span data-ttu-id="9d6f8-128">Revertir todos los registros.</span><span class="sxs-lookup"><span data-stu-id="9d6f8-128">Roll through all logs.</span></span>

    ``` syntax
    "Roll Forward"="All"
    ```

    <span data-ttu-id="9d6f8-129">Desplazarse por los registros hasta el punto especificado.</span><span class="sxs-lookup"><span data-stu-id="9d6f8-129">Roll through logs up to specified point.</span></span> <span data-ttu-id="9d6f8-130">El escritor define el formato del punto especificado.</span><span class="sxs-lookup"><span data-stu-id="9d6f8-130">The format of the specified point is defined by the writer.</span></span>

    ``` syntax
    "Roll Forward"="Partial:XXX"
    ```

-   <span data-ttu-id="9d6f8-131">Nuevo nombre de componente</span><span class="sxs-lookup"><span data-stu-id="9d6f8-131">New Component Name</span></span>

    <span data-ttu-id="9d6f8-132">Es posible que un escritor desee restaurar un componente a un nuevo nombre.</span><span class="sxs-lookup"><span data-stu-id="9d6f8-132">A writer may want to restore a component to a new name.</span></span> <span data-ttu-id="9d6f8-133">Por ejemplo, restaurar una base de datos a un nombre diferente para restaurar un elemento individual; al restaurar al mismo nombre, todos los datos recomendamos que los escritores acepten una ruta de acceso lógica y un nombre de componente válidos como valor de esta opción.</span><span class="sxs-lookup"><span data-stu-id="9d6f8-133">For example, restoring a database to a different name to restore an individual item; restoring to the same name would please all data We recommend that writers accept a valid logical path and component name as this options' value.</span></span> <span data-ttu-id="9d6f8-134">Esto se suele usar con un [*destino dirigido*](vssgloss-d.md).</span><span class="sxs-lookup"><span data-stu-id="9d6f8-134">This will often be used with a [*directed target*](vssgloss-d.md).</span></span>

    ``` syntax
    "New Component Name"="Logical Path\Component Name"
    ```

 

 



