---
description: Ubicar recursos de PE que no son de Win32
ms.assetid: 12f0b78e-ca85-443a-94ea-6bec5aa40c06
title: Ubicar recursos de PE que no son de Win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 079288cd6200eb64289f474636cbc8dc046c1e47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687095"
---
# <a name="locating-non-win32-pe-resources"></a><span data-ttu-id="44ac7-103">Ubicar recursos de PE que no son de Win32</span><span class="sxs-lookup"><span data-stu-id="44ac7-103">Locating Non-Win32 PE Resources</span></span>

<span data-ttu-id="44ac7-104">Para ubicar recursos PE que no son de Win32, la aplicación debe llamar primero a la función [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) para buscar el archivo de recursos específico del lenguaje del que se van a cargar los recursos.</span><span class="sxs-lookup"><span data-stu-id="44ac7-104">To locate non-Win32 PE resources, your application should first call the [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) function to locate the language-specific resource file from which to load resources.</span></span> <span data-ttu-id="44ac7-105">Si la aplicación está siguiendo la configuración de idioma del sistema, debe llamar a la función con el \_ nombre de idioma mui \_ idiomas de \| \_ \_ interfaz de usuario preferidos \_ de MUI \_ especificados para *dwFlags* y **null** especificado para *pwszLanguage*.</span><span class="sxs-lookup"><span data-stu-id="44ac7-105">If the application is following system language settings, it must call the function with MUI\_LANGUAGE\_NAME \| MUI\_USER\_PREFERRED\_UI\_LANGUAGES specified for *dwFlags* and **NULL** specified for *pwszLanguage*.</span></span> <span data-ttu-id="44ac7-106">Si la aplicación sigue la configuración de lenguaje específico de la aplicación, usa **GetFileMUIPath** para determinar si existe un archivo específico del idioma especificando el idioma en el parámetro *pwszLanguage* .</span><span class="sxs-lookup"><span data-stu-id="44ac7-106">If the application is following application-specific language settings, it uses **GetFileMUIPath** to determine if a language-specific file exists by specifying the language in the *pwszLanguage* parameter.</span></span>

<span data-ttu-id="44ac7-107">Después de la llamada a [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath), la aplicación debe definir la funcionalidad personalizada para cargar el módulo de recursos y cargar recursos específicos desde él.</span><span class="sxs-lookup"><span data-stu-id="44ac7-107">After the call to [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath), the application must define custom functionality to load the resource module and load specific resources from it.</span></span> <span data-ttu-id="44ac7-108">Por ejemplo, si utiliza un archivo de recursos. txt o. XML, la aplicación debe utilizar un analizador TXT o XML para cargar el archivo y, a continuación, analizar el contenido del archivo para cada recurso necesario.</span><span class="sxs-lookup"><span data-stu-id="44ac7-108">For example, if you are using a .txt or .xml resource file, the application must use a TXT or XML parser to load the file and then parse the contents of the file for each required resource.</span></span>

## <a name="related-topics"></a><span data-ttu-id="44ac7-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="44ac7-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44ac7-110">Uso de la interfaz de usuario multilingüe</span><span class="sxs-lookup"><span data-stu-id="44ac7-110">Using Multilingual User Interface</span></span>](using-multilingual-user-interface.md)
</dt> <dt>

[<span data-ttu-id="44ac7-111">**GetFileMUIPath**</span><span class="sxs-lookup"><span data-stu-id="44ac7-111">**GetFileMUIPath**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath)
</dt> </dl>

 

 



