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
# <a name="locating-non-win32-pe-resources"></a>Ubicar recursos de PE que no son de Win32

Para ubicar recursos PE que no son de Win32, la aplicación debe llamar primero a la función [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) para buscar el archivo de recursos específico del lenguaje del que se van a cargar los recursos. Si la aplicación está siguiendo la configuración de idioma del sistema, debe llamar a la función con el \_ nombre de idioma mui \_ idiomas de \| \_ \_ interfaz de usuario preferidos \_ de MUI \_ especificados para *dwFlags* y **null** especificado para *pwszLanguage*. Si la aplicación sigue la configuración de lenguaje específico de la aplicación, usa **GetFileMUIPath** para determinar si existe un archivo específico del idioma especificando el idioma en el parámetro *pwszLanguage* .

Después de la llamada a [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath), la aplicación debe definir la funcionalidad personalizada para cargar el módulo de recursos y cargar recursos específicos desde él. Por ejemplo, si utiliza un archivo de recursos. txt o. XML, la aplicación debe utilizar un analizador TXT o XML para cargar el archivo y, a continuación, analizar el contenido del archivo para cada recurso necesario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de la interfaz de usuario multilingüe](using-multilingual-user-interface.md)
</dt> <dt>

[**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath)
</dt> </dl>

 

 



