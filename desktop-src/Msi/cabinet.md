---
description: El tipo de datos del archivo. cab debe usarse en la columna Cabinet de la tabla de medios.
ms.assetid: 149c74ea-4342-45dd-8da4-4dfa7f4317a0
title: Archiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4814473ef4d21d5445b5b5319278a5e25a7f5540
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909041"
---
# <a name="cabinet"></a><span data-ttu-id="e8473-103">Archiva</span><span class="sxs-lookup"><span data-stu-id="e8473-103">Cabinet</span></span>

<span data-ttu-id="e8473-104">El tipo de datos del archivo. cab debe usarse en la columna Cabinet de la [tabla de medios](media-table.md).</span><span class="sxs-lookup"><span data-stu-id="e8473-104">The Cabinet data type must be used in the Cabinet column of the [Media table](media-table.md).</span></span>

<span data-ttu-id="e8473-105">Si el nombre del archivo. cab va precedido del signo de número, el archivador se almacena como un flujo de datos dentro del paquete.</span><span class="sxs-lookup"><span data-stu-id="e8473-105">If the cabinet name is preceded by the number sign, the cabinet is stored as a data stream inside the package.</span></span> <span data-ttu-id="e8473-106">La cadena de caracteres que sigue \# a es un [identificador](identifier.md) de este flujo de datos.</span><span class="sxs-lookup"><span data-stu-id="e8473-106">The character string which follows the \# is an [Identifier](identifier.md) for this data stream.</span></span> <span data-ttu-id="e8473-107">Tenga en cuenta que si el archivo. cab se almacena como un flujo de datos, el nombre de un contenedor distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="e8473-107">Note that if the cabinet is stored as a data stream, the name of a cabinet is case-sensitive.</span></span>

<span data-ttu-id="e8473-108">Si el nombre del archivo. cab no está precedido por el signo de número \# , se almacena en un archivo independiente ubicado en la raíz del árbol de origen especificado por la [tabla de directorio](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="e8473-108">If the cabinet name is not preceded by the number sign \#, the cabinet is stored in a separate file located at the root of the source tree specified by the [Directory Table](directory-table.md).</span></span> <span data-ttu-id="e8473-109">El archivo. cab debe utilizar la sintaxis de nombre de archivo corto que consta de un nombre de ocho caracteres, un punto y una extensión de tres caracteres.</span><span class="sxs-lookup"><span data-stu-id="e8473-109">The cabinet file must use the short file name syntax consisting of an eight character name, a period, and a three character extension.</span></span> <span data-ttu-id="e8473-110">El tipo de datos del archivo. cab no puede usar la \| Sintaxis de longname breve para los nombres de archivo.</span><span class="sxs-lookup"><span data-stu-id="e8473-110">The Cabinet data type cannot use the short\|longname syntax for file names.</span></span> <span data-ttu-id="e8473-111">Si el archivo. cab se almacena como un archivo independiente, el nombre del archivo. cab no distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="e8473-111">If the cabinet file is stored as a separate file, the name of the cabinet file is not case-sensitive.</span></span>

<span data-ttu-id="e8473-112">Para conservar espacio en disco, el instalador quita todos los gabinetes incrustados en el archivo. msi antes de almacenar en caché el paquete de instalación en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="e8473-112">To conserve disk space, the installer removes any cabinets embedded in the .msi file before caching the installation package on the user's computer.</span></span>

<span data-ttu-id="e8473-113">Vea [incluir un archivo. cab en una instalación](including-a-cabinet-file-in-an-installation.md).</span><span class="sxs-lookup"><span data-stu-id="e8473-113">See [Including a Cabinet File in an Installation](including-a-cabinet-file-in-an-installation.md).</span></span>

 

 



