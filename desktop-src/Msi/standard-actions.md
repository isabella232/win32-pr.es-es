---
description: Una acción encapsula una función típica realizada durante la instalación o el mantenimiento de una aplicación. Windows Installer tiene muchas acciones estándar integradas. Los desarrolladores de paquetes de instalación también pueden crear sus propias acciones personalizadas.
ms.assetid: 33651988-e371-4258-96a7-bcd7d6762161
title: Acciones estándar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ed4f9c2a7fc6671442f6b72cd10889e2fcf5e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276368"
---
# <a name="standard-actions"></a><span data-ttu-id="57793-105">Acciones estándar</span><span class="sxs-lookup"><span data-stu-id="57793-105">Standard Actions</span></span>

<span data-ttu-id="57793-106">Una acción encapsula una función típica realizada durante la instalación o el mantenimiento de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="57793-106">An action encapsulates a typical function performed during the installation or maintenance of an application.</span></span> <span data-ttu-id="57793-107">Windows Installer tiene muchas acciones estándar integradas.</span><span class="sxs-lookup"><span data-stu-id="57793-107">Windows Installer has many built-in standard actions.</span></span> <span data-ttu-id="57793-108">Los desarrolladores de paquetes de instalación también pueden crear sus propias [acciones personalizadas](custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="57793-108">Developers of installation packages can also author their own [custom actions](custom-actions.md).</span></span>

<span data-ttu-id="57793-109">Algunos ejemplos de acciones estándar del instalador son:</span><span class="sxs-lookup"><span data-stu-id="57793-109">Examples of installer standard actions include:</span></span>

-   <span data-ttu-id="57793-110">[Acción CreateShortcuts](createshortcuts-action.md): administra la creación de accesos directos a los archivos que se instalan con la aplicación actual.</span><span class="sxs-lookup"><span data-stu-id="57793-110">[CreateShortcuts action](createshortcuts-action.md): Manages the creation of shortcuts to files installed with the current application.</span></span> <span data-ttu-id="57793-111">Esta acción usa la [tabla de acceso directo](shortcut-table.md) para sus datos.</span><span class="sxs-lookup"><span data-stu-id="57793-111">This action uses the [Shortcut table](shortcut-table.md) for its data.</span></span>
-   <span data-ttu-id="57793-112">[InstallFiles Action](installfiles-action.md): copia los archivos seleccionados desde el directorio de origen en el directorio de destino.</span><span class="sxs-lookup"><span data-stu-id="57793-112">[InstallFiles action](installfiles-action.md): Copies selected files from the source directory to the destination directory.</span></span> <span data-ttu-id="57793-113">Esta acción utiliza la [tabla de archivos](file-table.md) para sus datos.</span><span class="sxs-lookup"><span data-stu-id="57793-113">This action uses the [File table](file-table.md) for its data.</span></span>
-   <span data-ttu-id="57793-114">[Acción WriteRegistryValues](writeregistryvalues-action.md): configura la información del registro que la aplicación requiere en el registro.</span><span class="sxs-lookup"><span data-stu-id="57793-114">[WriteRegistryValues action](writeregistryvalues-action.md): Sets up registry information the application requires in the registry.</span></span> <span data-ttu-id="57793-115">Esta acción utiliza la [tabla del registro](registry-table.md) para sus datos.</span><span class="sxs-lookup"><span data-stu-id="57793-115">This action uses the [Registry table](registry-table.md) for its data.</span></span>

<span data-ttu-id="57793-116">En las secciones siguientes se describen las acciones estándar.</span><span class="sxs-lookup"><span data-stu-id="57793-116">The following sections discuss standard actions.</span></span>

-   [<span data-ttu-id="57793-117">Acerca de las acciones estándar</span><span class="sxs-lookup"><span data-stu-id="57793-117">About Standard Actions</span></span>](about-standard-actions.md)
-   [<span data-ttu-id="57793-118">Uso de acciones estándar</span><span class="sxs-lookup"><span data-stu-id="57793-118">Using Standard Actions</span></span>](using-standard-actions.md)
-   [<span data-ttu-id="57793-119">Referencia de acciones estándar</span><span class="sxs-lookup"><span data-stu-id="57793-119">Standard Actions Reference</span></span>](standard-actions-reference.md)

 

 



