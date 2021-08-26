---
description: La preparación de recursos para una aplicación DE INTERFAZ de usuario es compatible con los modelos Win32 PE y no Win32 PE.
ms.assetid: e528dac7-c157-42d7-808d-709a4ae84f1e
title: Preparación de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ef40453ca6db40bed1c07bad80f7e21cb7adaa7ea48ae8ee5ce2a2a5c657ba2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040675"
---
# <a name="preparing-resources"></a>Preparación de recursos

La preparación de recursos para una aplicación DE INTERFAZ de usuario es compatible con los modelos Win32 PE y no Win32 PE. Los recursos de Win32 PE se proporcionan en archivos basados en PE, como archivos .dll, .exe o .sys archivos. Los recursos que no son de Win32 PE se disponen en un módulo personalizado de su elección.

> [!Note]  
> Se recomienda encarecidamente usar los recursos de Win32 PE para las aplicaciones DE WIN32 DE WIN32, ya que estos recursos son totalmente compatibles con la tecnología de recursos DE MOMENTO. Los archivos de recursos pe que no son win32 se pueden encontrar llamando a la función [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) como se describe en Localización de recursos pe que no son [win32,](locating-non-win32-pe-resources.md)pero la aplicación debe proporcionar su propia funcionalidad para buscar y cargar los recursos necesarios.

 

Esta sección contiene los siguientes temas:

-   [Creación del archivo de recursos del lenguaje base](creating-the-base-language-resource-file.md)
-   [Uso del redireccionamiento de cadenas del Registro](using-registry-string-redirection.md)
-   [Preparación de un archivo de configuración de recursos](preparing-a-resource-configuration-file.md)

 

 



