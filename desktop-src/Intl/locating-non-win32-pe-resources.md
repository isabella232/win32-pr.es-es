---
description: Buscar recursos de PE que no son win32
ms.assetid: 12f0b78e-ca85-443a-94ea-6bec5aa40c06
title: Buscar recursos de PE que no son win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf706712b2e1be2dd8fb1598c1404a829251bb24db83db7c7d6deaa87a13d24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147178"
---
# <a name="locating-non-win32-pe-resources"></a>Buscar recursos de PE que no son win32

Para buscar recursos que no son de Win32 PE, la aplicación debe llamar primero a la función [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) para buscar el archivo de recursos específico del lenguaje desde el que se cargan los recursos. Si la aplicación está siguiendo la configuración del lenguaje del sistema, debe llamar a la función con EL NOMBRE DE LENGUAJE DE LA INTERFAZ DE USUARIO DE MUI USER PREFERRED LANGUAGES especificado para dwFlags y NULL especificados para \_ \_ \| \_ \_ \_ \_ *pwszLanguage.*   Si la aplicación sigue la configuración de lenguaje específica de la aplicación, usa **GetFileMUIPath** para determinar si existe un archivo específico del lenguaje especificando el idioma en el parámetro *pwszLanguage.*

Después de llamar a [**GetFileMUIPath,**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath)la aplicación debe definir la funcionalidad personalizada para cargar el módulo de recursos y cargar recursos específicos desde él. Por ejemplo, si usa un archivo de recursos .txt o .xml, la aplicación debe usar un analizador TXT o XML para cargar el archivo y, a continuación, analizar el contenido del archivo para cada recurso necesario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de Interfaz de usuario multilingüe](using-multilingual-user-interface.md)
</dt> <dt>

[**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath)
</dt> </dl>

 

 



