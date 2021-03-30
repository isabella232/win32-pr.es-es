---
description: ICE88 valida que el directorio al que se hace referencia en la columna DirProperty de la tabla IniFile existe en el paquete de Windows Installer.
ms.assetid: 9bb253fd-e231-4016-807d-3b1068ecff68
title: ICE88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f59197259f8e5e1831c055618a85854d9f7c427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912305"
---
# <a name="ice88"></a><span data-ttu-id="731c9-103">ICE88</span><span class="sxs-lookup"><span data-stu-id="731c9-103">ICE88</span></span>

<span data-ttu-id="731c9-104">ICE88 valida que el directorio al que se hace referencia en la columna DirProperty de la [tabla inifile](inifile-table.md) existe en el paquete de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="731c9-104">ICE88 validates that the directory referenced in the DirProperty column of the [IniFile table](inifile-table.md) exists in the Windows Installer package.</span></span> <span data-ttu-id="731c9-105">ICE88 emite una advertencia si el valor de DirProperty no representa una propiedad en el directorio, AppSearch o las tablas de propiedades, ciertas [propiedades de carpeta del sistema](property-reference.md)o una propiedad establecida por una acción personalizada Type 51.</span><span class="sxs-lookup"><span data-stu-id="731c9-105">ICE88 issues a warning if the DirProperty value does not represent a property in the Directory, AppSearch, or Property tables, certain [system folder properties](property-reference.md), or a property set by a type 51 custom action.</span></span>

<span data-ttu-id="731c9-106">ICE88 examina las siguientes tablas y propiedades.</span><span class="sxs-lookup"><span data-stu-id="731c9-106">ICE88 scans the following tables and properties.</span></span>

-   [<span data-ttu-id="731c9-107">Tabla de directorio</span><span class="sxs-lookup"><span data-stu-id="731c9-107">Directory Table</span></span>](directory-table.md)
-   [<span data-ttu-id="731c9-108">Tabla AppSearch</span><span class="sxs-lookup"><span data-stu-id="731c9-108">AppSearch Table</span></span>](appsearch-table.md)
-   [<span data-ttu-id="731c9-109">Tabla de propiedades</span><span class="sxs-lookup"><span data-stu-id="731c9-109">Property Table</span></span>](property-table.md)
-   <span data-ttu-id="731c9-110">[Tabla CustomAction](customaction-table.md) , donde la acción personalizada es un [tipo de acción personalizada 51](custom-action-type-51.md)</span><span class="sxs-lookup"><span data-stu-id="731c9-110">[CustomAction Table](customaction-table.md) , where the custom action is a [Custom Action Type 51](custom-action-type-51.md)</span></span>
-   [<span data-ttu-id="731c9-111">**ProgramFilesFolder (propiedad)**</span><span class="sxs-lookup"><span data-stu-id="731c9-111">**ProgramFilesFolder Property**</span></span>](programfilesfolder.md)
-   [<span data-ttu-id="731c9-112">**Propiedad CommonFilesFolder**</span><span class="sxs-lookup"><span data-stu-id="731c9-112">**CommonFilesFolder Property**</span></span>](commonfilesfolder.md)
-   [<span data-ttu-id="731c9-113">**Propiedad Carpetadelsistema**</span><span class="sxs-lookup"><span data-stu-id="731c9-113">**SystemFolder Property**</span></span>](systemfolder.md)
-   [<span data-ttu-id="731c9-114">**Propiedad ProgramFiles64Folder**</span><span class="sxs-lookup"><span data-stu-id="731c9-114">**ProgramFiles64Folder Property**</span></span>](programfiles64folder.md)
-   [<span data-ttu-id="731c9-115">**Propiedad CommonFiles64Folder**</span><span class="sxs-lookup"><span data-stu-id="731c9-115">**CommonFiles64Folder Property**</span></span>](commonfiles64folder.md)
-   [<span data-ttu-id="731c9-116">**Propiedad System64Folder**</span><span class="sxs-lookup"><span data-stu-id="731c9-116">**System64Folder Property**</span></span>](system64folder.md)

## <a name="result"></a><span data-ttu-id="731c9-117">Resultado</span><span class="sxs-lookup"><span data-stu-id="731c9-117">Result</span></span>

<span data-ttu-id="731c9-118">ICE88 envía la siguiente advertencia.</span><span class="sxs-lookup"><span data-stu-id="731c9-118">ICE88 posts the following warning.</span></span>



| <span data-ttu-id="731c9-119">ADVERTENCIA de ICE88</span><span class="sxs-lookup"><span data-stu-id="731c9-119">ICE88 Warning</span></span>                                                                                                                                                                  | <span data-ttu-id="731c9-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="731c9-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="731c9-121">En la entrada de tabla IniFile (IniFile =) \[ 3, \] DirProperty = \[ 1 \] no se encuentra en las tablas Directory/Property/AppSearch/CA-Type51 y no es una de las propiedades del instalador.</span><span class="sxs-lookup"><span data-stu-id="731c9-121">In the IniFile table entry (IniFile=) \[3\] the DirProperty=\[1\] is not found in Directory/Property/AppSearch/CA-Type51 tables and it is not one of the installer properties.</span></span> | <span data-ttu-id="731c9-122">Para cada registro de la tabla IniFile, ICE88 lee el valor de la columna DirProperty.</span><span class="sxs-lookup"><span data-stu-id="731c9-122">For each record in the IniFile table, ICE88 reads the value in the DirProperty column.</span></span> <span data-ttu-id="731c9-123">ICE88 busca el valor en la tabla de [directorios](directory-table.md), la [tabla AppSearch](appsearch-table.md)y la [tabla de propiedades](property-table.md) , además de examinar la lista de propiedades establecida por el instalador.</span><span class="sxs-lookup"><span data-stu-id="731c9-123">ICE88 scans for the value in the [Directory Table](directory-table.md), [AppSearch Table](appsearch-table.md), and [Property Table](property-table.md) and also scans the list of properties set by the installer.</span></span> <span data-ttu-id="731c9-124">ICE88 envía esta advertencia si el valor no se encuentra en el examen.</span><span class="sxs-lookup"><span data-stu-id="731c9-124">ICE88 posts this warning if the value cannot be found in the scan.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="731c9-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="731c9-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="731c9-126">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="731c9-126">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



