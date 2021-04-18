---
description: Las siguientes funciones administrativas permiten que un proveedor de red realice acciones específicas de la red para mostrar y manipular directorios específicos de la red, es decir, directorios asignados a protocolos que no son de Windows.
ms.assetid: df2f1bd6-5257-46e4-a4d4-ad2f5c0a1517
title: Funciones administrativas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b83cb5b7c515fe8e22dc5542a4d29e54e8b01329
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652939"
---
# <a name="administrative-functions"></a><span data-ttu-id="c42fa-103">Funciones administrativas</span><span class="sxs-lookup"><span data-stu-id="c42fa-103">Administrative Functions</span></span>

<span data-ttu-id="c42fa-104">Las siguientes funciones administrativas permiten que un proveedor de red realice acciones específicas de la red para mostrar y manipular directorios específicos de la red, es decir, directorios asignados a protocolos que no son de Windows.</span><span class="sxs-lookup"><span data-stu-id="c42fa-104">The following administrative functions enable a network provider to take network-specific action to display and manipulate network-specific directories, in other words, directories mapped to non-Windows protocols.</span></span>



| <span data-ttu-id="c42fa-105">Función</span><span class="sxs-lookup"><span data-stu-id="c42fa-105">Function</span></span>                                         | <span data-ttu-id="c42fa-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="c42fa-106">Description</span></span>                                                                                                                                                   |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c42fa-107">**NPGetDirectoryType**</span><span class="sxs-lookup"><span data-stu-id="c42fa-107">**NPGetDirectoryType**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetdirectorytype) | <span data-ttu-id="c42fa-108">Lo llama el administrador de archivos para determinar el tipo de un directorio de red.</span><span class="sxs-lookup"><span data-stu-id="c42fa-108">Called by File Manager to determine the type of a network directory.</span></span>                                                                                          |
| [<span data-ttu-id="c42fa-109">**NPDirectoryNotify**</span><span class="sxs-lookup"><span data-stu-id="c42fa-109">**NPDirectoryNotify**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npdirectorynotify)   | <span data-ttu-id="c42fa-110">Lo llama el administrador de archivos para notificar a la red el proveedor de operaciones de directorio.</span><span class="sxs-lookup"><span data-stu-id="c42fa-110">Called by File Manager to notify the network provider of directory operations.</span></span> <span data-ttu-id="c42fa-111">Esta función se puede utilizar para realizar un comportamiento especial en determinados directorios.</span><span class="sxs-lookup"><span data-stu-id="c42fa-111">This function can be used to perform special behavior for certain directories.</span></span> |



 

 

 



