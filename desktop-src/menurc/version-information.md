---
title: Información de versión
description: En esta sección se describe el recurso de información de versión.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\versioninformation.htm
keywords:
- recursos, información de versión
- información de versión
- números de versión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78e43de27f18f89a5f240242b63ade057f57ec92
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357135"
---
# <a name="version-information"></a>Información de versión

La información de versión facilita que las aplicaciones instalen archivos correctamente y permite que los programas de instalación analicen los archivos instalados actualmente. El recurso de información de versión contiene el número de versión del archivo, su sistema operativo deseado y el nombre de archivo original.

### <a name="in-this-section"></a>En esta sección



| Nombre                                                               | Descripción                                                        |
|--------------------------------------------------------------------|--------------------------------------------------------------------|
| [Información sobre la versión](about-version-information.md)         | Describe las funciones de información de versión.<br/>            |
| [Usar información de versión](using-version-information.md)         | Describe cómo utilizar las funciones de información de versión.<br/> |
| [Referencia de información de versión](version-information-reference.md) | Contiene la referencia de la API.<br/>                             |



 

### <a name="version-information-functions"></a>Funciones de información de versión



| Nombre                                                         | Descripción                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetFileVersionInfo**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoa)             | Recupera información de versión del archivo especificado. <br/>                                                                                                                                                                                                                                                                                                     |
| [**GetFileVersionInfoEx**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoexa)         | Recupera información de versión del archivo especificado.<br/>                                                                                                                                                                                                                                                                                                      |
| [**GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea)     | Determina si el sistema operativo puede recuperar información de versión de un archivo especificado. Si la información de versión está disponible, [**GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea) devuelve el tamaño, en bytes, de esa información. <br/>                                                                                                             |
| [**GetFileVersionInfoSizeEx**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizeexa) | Determina si el sistema operativo puede recuperar información de versión de un archivo especificado. Si la información de versión está disponible, [**GetFileVersionInfoSizeEx**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizeexa) devuelve el tamaño, en bytes, de esa información.<br/>                                                                                                          |
| [**VerFindFile**](/windows/desktop/api/Winver/nf-winver-verfindfilea)                           | Determina dónde se debe instalar un archivo basándose en si encuentra otra versión del archivo en el sistema. Los valores [**VerFindFile**](/windows/desktop/api/Winver/nf-winver-verfindfilea) devueltos en los búferes especificados se usan en una llamada subsiguiente a la función [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) . <br/>                                                                          |
| [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea)                     | Instala el archivo especificado en función de la información devuelta por la función [**VerFindFile**](/windows/desktop/api/Winver/nf-winver-verfindfilea) . [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) descomprime el archivo, si es necesario, asigna un nombre de archivo único y comprueba si hay errores, como archivos obsoletos. <br/>                                                                                   |
| [**VerLanguageName**](/windows/desktop/api/Winver/nf-winver-verlanguagenamea)                   | Recupera una cadena de Descripción del idioma asociado a un identificador de idioma de Microsoft binario especificado.<br/>                                                                                                                                                                                                                                          |
| [**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea)                       | Recupera la información de versión especificada del recurso de información de versión especificado. Para recuperar el recurso adecuado, antes de llamar a [**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea), primero debe llamar a la función [**GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea) y, a continuación, a la función [**GetFileVersionInfo**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoa) . <br/> |



 

### <a name="version-information-structures"></a>Estructuras de información de versión



| Nombre                                          | Descripción                                                                                                                                                                                                                      |
|-----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**String@**](string-str.md)                  | Describe la organización de los datos en un recurso de versión de archivo. Contiene una cadena que describe un aspecto específico de un archivo, por ejemplo, la versión de un archivo, sus avisos de propiedad intelectual o sus marcas comerciales.<br/>                |
| [**StringFileInfo**](stringfileinfo.md)      | Describe la organización de los datos en un recurso de versión de archivo. Contiene información de versión que se puede mostrar para un idioma y una página de códigos determinados.<br/>                                                           |
| [**StringTable**](stringtable.md)            | Describe la organización de los datos en un recurso de versión de archivo. Contiene información sobre el formato del idioma y la página de códigos para las cadenas especificadas por el miembro **secundario** . Una página de códigos es un juego de caracteres ordenado.<br/> |
| [**Distribuidor**](var-str.md)                        | Describe la organización de los datos en un recurso de versión de archivo. Normalmente contiene una lista de los pares de idioma y de identificador de página de códigos que admite la versión de la aplicación o DLL.<br/>                             |
| [**VarFileInfo**](varfileinfo.md)            | Describe la organización de los datos en un recurso de versión de archivo. Contiene información de versión que no depende de una combinación de idioma y página de códigos determinada.<br/>                                                        |
| [**VS \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) | Contiene información de versión sobre un archivo. Esta información es independiente del idioma y de la página de códigos. <br/>                                                                                                                   |
| [**VS \_ versionInfo**](vs-versioninfo.md)     | Describe la organización de los datos en un recurso de versión de archivo. Es la estructura raíz que contiene todas las demás estructuras de información de versión de archivo.<br/>                                                                    |



 

 

 





