---
description: Windows 7 incluye bibliotecas, que proporcionan a los usuarios una vista única y coherente de sus archivos, incluso cuando estos archivos se almacenan en ubicaciones diferentes.
title: Bibliotecas de Windows
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 19DA68B2-FCB6-443d-A3CD-0BF2F429B149
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ddb21b4678005d3def5812258a75f2e4fec4b9f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986127"
---
# <a name="windows-libraries"></a><span data-ttu-id="0bcc4-103">Bibliotecas de Windows</span><span class="sxs-lookup"><span data-stu-id="0bcc4-103">Windows Libraries</span></span>

<span data-ttu-id="0bcc4-104">Windows 7 incluye bibliotecas, que proporcionan a los usuarios una vista única y coherente de sus archivos, incluso cuando estos archivos se almacenan en ubicaciones diferentes.</span><span class="sxs-lookup"><span data-stu-id="0bcc4-104">Windows 7 introduces libraries, which provide users with a single, coherent view of their files even when those files are stored in different locations.</span></span> <span data-ttu-id="0bcc4-105">Las bibliotecas pueden ser configuradas y organizadas por un usuario, y una biblioteca puede contener carpetas que se encuentran en el equipo del usuario y también carpetas que se han compartido a través de una red.</span><span class="sxs-lookup"><span data-stu-id="0bcc4-105">Libraries can be configured and organized by a user and a library can contain folders that are found on the user's computer and also folders that have been shared over a network.</span></span> <span data-ttu-id="0bcc4-106">Las bibliotecas presentan una vista más sencilla del sistema de almacenamiento subyacente porque, para el usuario, los archivos y las carpetas de una biblioteca se muestran en una sola vista, independientemente de dónde se almacenen físicamente.</span><span class="sxs-lookup"><span data-stu-id="0bcc4-106">Libraries present a simpler view of the underlying storage system because, to the user, the files and folders in a library are displayed in single view, no matter where they are physically stored.</span></span>

<span data-ttu-id="0bcc4-107">Se recomienda a los desarrolladores que escriban nuevos programas en Windows 7 que usen las bibliotecas como medio para que los usuarios interactúen con los archivos utilizados por el programa.</span><span class="sxs-lookup"><span data-stu-id="0bcc4-107">Developers writing new programs in Windows 7 are encouraged to use libraries as the means through which the users interact with the files used by the program.</span></span> <span data-ttu-id="0bcc4-108">El uso de bibliotecas en el programa proporcionará a los usuarios una experiencia más limpia, más sencilla y más coherente en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0bcc4-108">Using libraries in your program will provide users with a cleaner, easier, and more consistent experience in Windows 7.</span></span>

<span data-ttu-id="0bcc4-109">Los desarrolladores también deben revisar sus programas existentes y actualizarlos si es necesario, para trabajar con las bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="0bcc4-109">Developers should also review their existing programs, and update them if necessary, to work with libraries.</span></span> <span data-ttu-id="0bcc4-110">Dado que las bibliotecas no forman parte del sistema de archivos, las API basadas en el sistema de archivos no tendrán acceso a las bibliotecas que el usuario podría haber configurado.</span><span class="sxs-lookup"><span data-stu-id="0bcc4-110">Because libraries are not a part of the file system, file system-based APIs will not have access to any libraries that the user might have configured.</span></span>

<span data-ttu-id="0bcc4-111">Los programas que actualmente permiten a los usuarios almacenar su contenido en carpetas diferentes o en equipos diferentes se beneficiarán de la mayor parte cuando agreguen compatibilidad con la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="0bcc4-111">Programs that currently allow users to store their content in different folders or on different computers will benefit most when they add library support.</span></span> <span data-ttu-id="0bcc4-112">Las bibliotecas simplifican la administración de contenido en diferentes ubicaciones de almacenamiento para el desarrollador y el usuario.</span><span class="sxs-lookup"><span data-stu-id="0bcc4-112">Libraries simplify the management of content in diverse storage locations for the developer and the user.</span></span>

<span data-ttu-id="0bcc4-113">En esta guía se describe más sobre qué son las bibliotecas, cómo se pueden hacer los programas para trabajar con las bibliotecas y algunas de las formas en que un programa puede usar las bibliotecas para mejorar la experiencia del usuario.</span><span class="sxs-lookup"><span data-stu-id="0bcc4-113">This guide describes more about what libraries are, how programs can be made to work with libraries, and some of the ways a program can use libraries to improve the user's experience.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0bcc4-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0bcc4-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0bcc4-115">Acerca de las bibliotecas</span><span class="sxs-lookup"><span data-stu-id="0bcc4-115">About Libraries</span></span>](library-leverage-to-manage-folders.md)
</dt> <dt>

[<span data-ttu-id="0bcc4-116">Usar bibliotecas en el programa</span><span class="sxs-lookup"><span data-stu-id="0bcc4-116">Using Libraries in your Program</span></span>](library-be-library-aware.md)
</dt> <dt>

[<span data-ttu-id="0bcc4-117">**IShellLibrary**</span><span class="sxs-lookup"><span data-stu-id="0bcc4-117">**IShellLibrary**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)
</dt> <dt>

[<span data-ttu-id="0bcc4-118">Vínculos de Shell</span><span class="sxs-lookup"><span data-stu-id="0bcc4-118">Shell Links</span></span>](./links.md)
</dt> <dt>

[<span data-ttu-id="0bcc4-119">Carpetas conocidas</span><span class="sxs-lookup"><span data-stu-id="0bcc4-119">Known Folders</span></span>](known-folders.md)
</dt> <dt>

[<span data-ttu-id="0bcc4-120">Esquema de descripción de biblioteca</span><span class="sxs-lookup"><span data-stu-id="0bcc4-120">Library Description Schema</span></span>](library-schema-entry.md)
</dt> </dl>

 

 
