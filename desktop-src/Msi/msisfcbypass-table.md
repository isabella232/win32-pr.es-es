---
description: La tabla MsiSFCBypass contiene una lista de archivos que deben omitir la protección de archivos de Windows cuando los archivos se instalan en Microsoft Windows me.
ms.assetid: 86de0dc1-ed8f-410c-a411-6c44c8e5c9fd
title: Tabla MsiSFCBypass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 707294e9461aaf321add8a3959682a0db555cc2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361066"
---
# <a name="msisfcbypass-table"></a><span data-ttu-id="203c9-103">Tabla MsiSFCBypass</span><span class="sxs-lookup"><span data-stu-id="203c9-103">MsiSFCBypass Table</span></span>

<span data-ttu-id="203c9-104">La tabla MsiSFCBypass contiene una lista de archivos que deben omitir la protección de archivos de Windows cuando los archivos se instalan en Microsoft Windows me.</span><span class="sxs-lookup"><span data-stu-id="203c9-104">The MsiSFCBypass Table contains a list of files that should bypass Windows File Protection when the files are installed on Microsoft Windows Me.</span></span>

<span data-ttu-id="203c9-105">La tabla MsiSFCBypass tiene la siguiente columna.</span><span class="sxs-lookup"><span data-stu-id="203c9-105">The MsiSFCBypass Table has the following column.</span></span>



| <span data-ttu-id="203c9-106">Columna</span><span class="sxs-lookup"><span data-stu-id="203c9-106">Column</span></span> | <span data-ttu-id="203c9-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="203c9-107">Type</span></span>                         | <span data-ttu-id="203c9-108">Clave</span><span class="sxs-lookup"><span data-stu-id="203c9-108">Key</span></span> | <span data-ttu-id="203c9-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="203c9-109">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="203c9-110">Archivo\_</span><span class="sxs-lookup"><span data-stu-id="203c9-110">File\_</span></span> | [<span data-ttu-id="203c9-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="203c9-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="203c9-112">Y</span><span class="sxs-lookup"><span data-stu-id="203c9-112">Y</span></span>   | <span data-ttu-id="203c9-113">N</span><span class="sxs-lookup"><span data-stu-id="203c9-113">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="203c9-114">Columnas</span><span class="sxs-lookup"><span data-stu-id="203c9-114">Columns</span></span>

<dl> <dt>

<span data-ttu-id="203c9-115"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Filesystem\_</span><span class="sxs-lookup"><span data-stu-id="203c9-115"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="203c9-116">La clave externa de la [tabla de archivos](file-table.md) que especifica el archivo que debe omitir la protección de archivos de Windows cuando el archivo está instalado en Windows me.</span><span class="sxs-lookup"><span data-stu-id="203c9-116">The foreign key to the [File Table](file-table.md) that specifies the file that should bypass Windows File Protection when the file is installed on Windows Me.</span></span>

</dd> </dl>

 

 



