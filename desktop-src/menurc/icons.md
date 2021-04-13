---
title: Iconos (menús y otros recursos)
description: En esta sección se describen los iconos que son imágenes de mapa de bits combinados con una máscara para crear áreas transparentes en la imagen.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\icons.htm
keywords:
- recursos, iconos
- iconos, acerca de
- RT_ICON recurso
- RT_GROUP_ICON recurso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22c96e740c23bb61cfdaa6cfbcbf6d0ce7538586
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421858"
---
# <a name="icons-menus-and-other-resources"></a>Iconos (menús y otros recursos)

Un *icono* es una imagen que consta de una imagen de mapa de bits combinada con una máscara para crear áreas transparentes en la imagen. El icono de término puede hacer referencia a cualquiera de las siguientes opciones:

-   Imagen de un solo icono. Este es un recurso de tipo **RT \_ Icon**.
-   Un grupo de imágenes, desde el que el sistema o una aplicación puede elegir el icono más adecuado en función del tamaño y la profundidad de color. Se trata de un recurso del tipo de **\_ \_ icono de grupo RT**.

### <a name="in-this-section"></a>En esta sección



| Nombre                                 | Descripción                                                 |
|--------------------------------------|-------------------------------------------------------------|
| [Acerca de los iconos](about-icons.md)       | Describe los iconos.<br/>                                 |
| [Usar iconos](using-icons.md)       | Describe cómo realizar tareas relacionadas con los iconos.<br/> |
| [Referencia de icono](icon-reference.md) | Contiene la referencia de la API.<br/>                      |



 

### <a name="icon-functions"></a>Funciones de icono



| Nombre                                                               | Descripción                                                                                                                                                                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CopyIcon**](/windows/desktop/api/Winuser/nf-winuser-copyicon)                                       | Copia el icono especificado de otro módulo en el módulo actual. <br/>                                                                                                                                      |
| [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon)                                   | Crea un icono que tiene el tamaño, los colores y los patrones de bits especificados. <br/>                                                                                                                                    |
| [**CreateIconFromResource**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresource)           | Crea un icono o un cursor a partir de bits de recursos que describen el icono.<br/>                                                                                                                                          |
| [**CreateIconFromResourceEx**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex)       | Crea un icono o un cursor a partir de bits de recursos que describen el icono. <br/>                                                                                                                                         |
| [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect)                   | Crea un icono o un cursor a partir de una estructura [**ICONINFO**](/windows/desktop/api/Winuser/ns-winuser-iconinfo) . <br/>                                                                                                                                 |
| [**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon)                                 | Destruye un icono y libera la memoria que ocupa el icono. <br/>                                                                                                                                                  |
| [**DrawIcon**](/windows/desktop/api/Winuser/nf-winuser-drawicon)                                       | Dibuja un icono o un cursor en el contexto de dispositivo especificado.<br/>                                                                                                                                                 |
| [**DrawIconEx**](/windows/desktop/api/Winuser/nf-winuser-drawiconex)                                   | Dibuja un icono o un cursor en el contexto de dispositivo especificado, realiza las operaciones de trama especificadas y ajusta o comprime el icono o el cursor según lo especificado. <br/>                                     |
| [**DuplicateIcon**](/windows/desktop/api/Shellapi/nf-shellapi-duplicateicon)                             | Crea un duplicado de un icono especificado.<br/>                                                                                                                                                                   |
| [**ExtractAssociatedIcon**](/windows/desktop/api/Shellapi/nf-shellapi-extractassociatedicona)             | Recupera un identificador de un icono indizado encontrado en un archivo o un icono que se encuentra en un archivo ejecutable asociado. <br/>                                                                                                  |
| [**ExtractIcon**](/windows/desktop/api/Shellapi/nf-shellapi-extracticona)                                 | Recupera un identificador de un icono del archivo ejecutable, el archivo DLL o el archivo de icono especificado.<br/>                                                                                                                        |
| [**ExtractIconEx**](/windows/desktop/api/Shellapi/nf-shellapi-extracticonexa)                             | Crea una matriz de identificadores para los iconos grandes o pequeños extraídos del archivo ejecutable, el archivo DLL o el archivo de icono especificado. <br/>                                                                                      |
| [**GetIconInfo**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo)                                 | Recupera información sobre el icono o el cursor especificado. <br/>                                                                                                                                                 |
| [**GetIconInfoEx**](/windows/desktop/api/Winuser/nf-winuser-geticoninfoexa)                             | Recupera información sobre el icono o el cursor especificado. [**GetIconInfoEx**](/windows/desktop/api/Winuser/nf-winuser-geticoninfoexa) extiende [**GetIconInfo**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo) mediante la estructura [**ICONINFOEX**](/windows/desktop/api/Winuser/ns-winuser-iconinfoexa) más reciente.<br/> |
| [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona)                                       | Carga el recurso de icono especificado a partir del archivo ejecutable (. exe) asociado a una instancia de la aplicación.<br/>                                                                                                 |
| [**LookupIconIdFromDirectory**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectory)     | Busca el icono o el cursor que mejor se adapte al dispositivo de pantalla actual.<br/>                                                                                                     |
| [**LookupIconIdFromDirectoryEx**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectoryex) | Busca el icono o el cursor que mejor se adapte al dispositivo de pantalla actual. <br/>                                                                                                    |
| [**PrivateExtractIcons**](/windows/desktop/api/Winuser/nf-winuser-privateextracticonsa)                 | Crea una matriz de identificadores para los iconos que se extraen de un archivo especificado.<br/>                                                                                                                             |



 

### <a name="icon-structures"></a>Estructuras de iconos



| Nombre                               | Descripción                                                                                                                                                                                                                                     |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICONINFO**](/windows/desktop/api/Winuser/ns-winuser-iconinfo)       | Contiene información sobre un icono o un cursor. <br/>                                                                                                                                                                                     |
| [**ICONINFOEX**](/windows/desktop/api/Winuser/ns-winuser-iconinfoexa)   | Contiene información sobre un icono o un cursor. Extiende [**ICONINFO**](/windows/desktop/api/Winuser/ns-winuser-iconinfo). Usado por [**GetIconInfoEx**](/windows/desktop/api/Winuser/nf-winuser-geticoninfoexa).<br/>                                                                                                |
| [**ICONMETRICS**](/windows/win32/api/winuser/ns-winuser-iconmetricsa) | Contiene las métricas escalables asociadas a los iconos. Esta estructura se usa con la función [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) cuando se especifica la acción **SPI \_ GETICONMETRICS** o **SPI \_ SETICONMETRICS** .<br/> |



 

 

