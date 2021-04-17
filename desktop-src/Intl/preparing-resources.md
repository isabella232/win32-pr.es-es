---
description: La preparación de recursos para una aplicación de MUI es compatible con los modelos PE de Win32 y no Win32.
ms.assetid: e528dac7-c157-42d7-808d-709a4ae84f1e
title: Preparación de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4ca7655535318fa7a385993e6a55f9e7b6110ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688335"
---
# <a name="preparing-resources"></a><span data-ttu-id="65ef6-103">Preparación de recursos</span><span class="sxs-lookup"><span data-stu-id="65ef6-103">Preparing Resources</span></span>

<span data-ttu-id="65ef6-104">La preparación de recursos para una aplicación de MUI es compatible con los modelos PE de Win32 y no Win32.</span><span class="sxs-lookup"><span data-stu-id="65ef6-104">Resource preparation for a MUI application supports both Win32 PE and non-Win32 PE models.</span></span> <span data-ttu-id="65ef6-105">Los recursos PE de Win32 se proporcionan en archivos basados en PE, como archivos. dll,. exe o. sys.</span><span class="sxs-lookup"><span data-stu-id="65ef6-105">Win32 PE resources are provided in PE-based files, such as .dll, .exe, or .sys files.</span></span> <span data-ttu-id="65ef6-106">Los recursos de PE que no son de Win32 se proporcionan en un módulo personalizado de su elección.</span><span class="sxs-lookup"><span data-stu-id="65ef6-106">Non-Win32 PE resources are furnished in a customized module of your choosing.</span></span>

> [!Note]  
> <span data-ttu-id="65ef6-107">Se recomienda encarecidamente usar recursos PE de Win32 para las aplicaciones de MUI de Win32, ya que estos recursos son totalmente compatibles con la tecnología de recursos de MUI.</span><span class="sxs-lookup"><span data-stu-id="65ef6-107">It is highly recommended for you to use Win32 PE resources for Win32 MUI applications, as these resources are completely supported by the MUI resource technology.</span></span> <span data-ttu-id="65ef6-108">Los archivos de recursos no Win32 PE se pueden encontrar llamando a la función [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) , tal y como se describe en [localizar recursos de PE que no son de Win32](locating-non-win32-pe-resources.md), pero la aplicación debe proporcionar su propia funcionalidad para buscar y cargar los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="65ef6-108">Non-Win32 PE resource files can be located by calling the [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) function as described in [Locating Non-Win32 PE Resources](locating-non-win32-pe-resources.md), but the application must provide its own functionality to find and load the required resources.</span></span>

 

<span data-ttu-id="65ef6-109">Esta sección contiene los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="65ef6-109">This section contains the following topics:</span></span>

-   [<span data-ttu-id="65ef6-110">Crear el archivo de recursos de idioma base</span><span class="sxs-lookup"><span data-stu-id="65ef6-110">Creating the Base Language Resource File</span></span>](creating-the-base-language-resource-file.md)
-   [<span data-ttu-id="65ef6-111">Usar el redireccionamiento de cadenas del registro</span><span class="sxs-lookup"><span data-stu-id="65ef6-111">Using Registry String Redirection</span></span>](using-registry-string-redirection.md)
-   [<span data-ttu-id="65ef6-112">Preparación de un archivo de configuración de recursos</span><span class="sxs-lookup"><span data-stu-id="65ef6-112">Preparing a Resource Configuration File</span></span>](preparing-a-resource-configuration-file.md)

 

 



