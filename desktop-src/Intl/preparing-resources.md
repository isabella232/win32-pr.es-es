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
# <a name="preparing-resources"></a>Preparación de recursos

La preparación de recursos para una aplicación de MUI es compatible con los modelos PE de Win32 y no Win32. Los recursos PE de Win32 se proporcionan en archivos basados en PE, como archivos. dll,. exe o. sys. Los recursos de PE que no son de Win32 se proporcionan en un módulo personalizado de su elección.

> [!Note]  
> Se recomienda encarecidamente usar recursos PE de Win32 para las aplicaciones de MUI de Win32, ya que estos recursos son totalmente compatibles con la tecnología de recursos de MUI. Los archivos de recursos no Win32 PE se pueden encontrar llamando a la función [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) , tal y como se describe en [localizar recursos de PE que no son de Win32](locating-non-win32-pe-resources.md), pero la aplicación debe proporcionar su propia funcionalidad para buscar y cargar los recursos necesarios.

 

Esta sección contiene los siguientes temas:

-   [Crear el archivo de recursos de idioma base](creating-the-base-language-resource-file.md)
-   [Usar el redireccionamiento de cadenas del registro](using-registry-string-redirection.md)
-   [Preparación de un archivo de configuración de recursos](preparing-a-resource-configuration-file.md)

 

 



