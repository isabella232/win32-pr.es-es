---
title: Información de versión
description: En esta sección se describe el recurso de información de versión.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\versioninformation.htm
keywords:
- resources,version information
- información de versión
- números de versión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac69601c593c51a5a15a0af0706a019f135d855875f6e1ecabdb414a8a100045
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118733100"
---
# <a name="version-information"></a>Información de versión

La información de versión facilita que las aplicaciones instalen archivos correctamente y permite que los programas de instalación analicen los archivos instalados actualmente. El recurso de información de versión contiene el número de versión del archivo, su sistema operativo previsto y el nombre de archivo original.

### <a name="in-this-section"></a>En esta sección



| Nombre                                                               | Descripción                                                        |
|--------------------------------------------------------------------|--------------------------------------------------------------------|
| [Acerca de la información de versión](about-version-information.md)         | Describe las funciones de información de versión.<br/>            |
| [Uso de información de versión](using-version-information.md)         | Describe cómo usar las funciones de información de versión.<br/> |
| [Referencia de información de versión](version-information-reference.md) | Contiene la referencia de API.<br/>                             |



 

### <a name="version-information-functions"></a>Funciones de información de versión



| Nombre                                                         | Descripción                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetFileVersionInfo**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoa)             | Recupera la información de versión del archivo especificado. <br/>                                                                                                                                                                                                                                                                                                     |
| [**GetFileVersionInfoEx**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoexa)         | Recupera la información de versión del archivo especificado.<br/>                                                                                                                                                                                                                                                                                                      |
| [**GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea)     | Determina si el sistema operativo puede recuperar la información de versión de un archivo especificado. Si la información de versión está disponible, [**GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea) devuelve el tamaño, en bytes, de esa información. <br/>                                                                                                             |
| [**GetFileVersionInfoSizeEx**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizeexa) | Determina si el sistema operativo puede recuperar la información de versión de un archivo especificado. Si la información de versión está disponible, [**GetFileVersionInfoSizeEx**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizeexa) devuelve el tamaño, en bytes, de esa información.<br/>                                                                                                          |
| [**VerFindFile**](/windows/desktop/api/Winver/nf-winver-verfindfilea)                           | Determina dónde instalar un archivo en función de si encuentra otra versión del archivo en el sistema. Los valores [**que Devuelve VerFindFile**](/windows/desktop/api/Winver/nf-winver-verfindfilea) en los búferes especificados se usan en una llamada posterior a la [**función VerInstallFile.**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) <br/>                                                                          |
| [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea)                     | Instala el archivo especificado en función de la información devuelta por la [**función VerFindFile.**](/windows/desktop/api/Winver/nf-winver-verfindfilea) [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) descomprime el archivo, si es necesario, asigna un nombre de archivo único y comprueba si hay errores, como archivos obsoletos. <br/>                                                                                   |
| [**VerLanguageName**](/windows/desktop/api/Winver/nf-winver-verlanguagenamea)                   | Recupera una cadena de descripción para el idioma asociado a un identificador de lenguaje binario de Microsoft especificado.<br/>                                                                                                                                                                                                                                          |
| [**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea)                       | Recupera la información de versión especificada del recurso de información de versión especificado. Para recuperar el recurso adecuado, antes de llamar a [**VerQueryValue,**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea)primero debe llamar a la función [**GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea) y, después, a la [**función GetFileVersionInfo.**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoa) <br/> |



 

### <a name="version-information-structures"></a>Estructuras de información de versión



| Nombre                                          | Descripción                                                                                                                                                                                                                      |
|-----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**String**](string-str.md)                  | Muestra la organización de los datos en un recurso de versión de archivo. Contiene una cadena que describe un aspecto específico de un archivo, por ejemplo, la versión de un archivo, sus avisos de copyright o sus marcas comerciales.<br/>                |
| [**StringFileInfo**](stringfileinfo.md)      | Muestra la organización de los datos en un recurso de versión de archivo. Contiene información de versión que se puede mostrar para un idioma y una página de códigos determinados.<br/>                                                           |
| [**StringTable**](stringtable.md)            | Muestra la organización de los datos en un recurso de versión de archivo. Contiene información de formato de página de códigos y lenguaje para las cadenas especificadas por el **miembro** Children. Una página de códigos es un juego de caracteres ordenado.<br/> |
| [**Var**](var-str.md)                        | Muestra la organización de los datos en un recurso de versión de archivo. Normalmente contiene una lista de pares de identificadores de idioma y de página de códigos que admite la versión de la aplicación o dll.<br/>                             |
| [**VarFileInfo**](varfileinfo.md)            | Muestra la organización de los datos en un recurso de versión de archivo. Contiene información de versión que no depende de una combinación de idioma y página de códigos determinada.<br/>                                                        |
| [**VS \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) | Contiene información de versión sobre un archivo. Esta información es independiente del idioma y de la página de códigos. <br/>                                                                                                                   |
| [**VS \_ VERSIONINFO**](vs-versioninfo.md)     | Muestra la organización de los datos en un recurso de versión de archivo. Es la estructura raíz que contiene todas las demás estructuras de información de versión de archivo.<br/>                                                                    |



 

 

 





