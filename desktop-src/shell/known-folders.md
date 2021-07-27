---
description: Windows Vista presenta nuevos escenarios de almacenamiento y un nuevo espacio de nombres de perfil de usuario.
title: Carpetas conocidas
ms.topic: article
ms.date: 05/31/2018
ms.assetid: d0c25eef-53ac-4dad-805a-b9ba4cd86be9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 3b5fbdaf0086f88fc4eed42ce47749a99ab07b40
ms.sourcegitcommit: 8bfe4f468ee5de7bbe096e5db81e427db53d977c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/26/2021
ms.locfileid: "114680318"
---
# <a name="known-folders"></a>Carpetas conocidas

Windows Vista presenta nuevos escenarios de almacenamiento y un nuevo espacio de nombres de perfil de usuario. Para abordar estos nuevos factores, se ha reemplazado el sistema anterior de hacer referencia a carpetas estándar por un [**valor CSIDL.**](csidl.md) A Windows Vista, se hace referencia a esas carpetas mediante un nuevo conjunto de valores GUID denominados identificadores de carpeta conocidos.

El sistema de carpetas conocidas proporciona estas ventajas:

-   Los proveedores de software independientes (ISV) pueden ampliar el conjunto de los propios iD de carpeta conocidos. Pueden definir carpetas, darles los iDs y registrarlos en el sistema. No se pudieron extender los valores CSIDL.
-   Se pueden enumerar todas las carpetas conocidas de un sistema. Ninguna API proporcionó esta funcionalidad para los valores CSIDL. Vea [**IKnownFolderManager::GetFolderIds para**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids) obtener más información.
-   Una carpeta conocida agregada por un ISV puede agregar propiedades personalizadas que le permitan explicar su propósito y su uso previsto.
-   Muchas carpetas conocidas se pueden redirigir a ubicaciones nuevas, incluidas las ubicaciones de red. En el sistema CSIDL, solo se **puede redirigir Mis documentos** carpeta principal.
-   Las carpetas conocidas pueden tener controladores personalizados para su uso durante la creación o eliminación.

El sistema CSIDL y las API que usan valores CSIDL siguen siendo compatibles. Sin embargo, no se recomienda usarlas en ningún desarrollo nuevo.


En los temas siguientes se tratan los detalles del sistema carpetas conocidas.

-   [Trabajar con carpetas conocidas en aplicaciones](working-with-known-folders.md)
-   [Cómo ampliar carpetas conocidas con carpetas personalizadas](how-to-extend-known-folders-with-custom-folders.md)
-   [**KNOWNFOLDERID**](knownfolderid.md)

En las siguientes páginas de referencia se explican las funciones carpetas conocidas de Win32, que se pueden usar para recuperar la ubicación de carpetas conocidas o redirigirlas a una nueva ubicación. Estas funciones reemplazan a las funciones anteriores de Win32. Las nuevas funciones se proporcionan para proporcionar un comportamiento equivalente a las funciones antiguas, pero cada función nueva también se duplica mediante una API de modelo de objetos componentes (COM).



| Nueva función                                             | Reemplaza                                           | EQUIVALENTE COM                                            |
|----------------------------------------------------------|----------------------------------------------------|-----------------------------------------------------------|
| [**SHGetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath)     | [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha)         | [**IKnownFolder::GetPath**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getpath)     |
| [**SHGetKnownFolderIDList**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist) | [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) | [**IKnownFolder::GetIDList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getidlist) |
| [**SHSetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetknownfolderpath)     | [**SHSetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetfolderpatha)         | [**IKnownFolder::SetPath**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-setpath)     |



 

En las siguientes páginas de referencia se explican las API de carpetas conocidas de COM, que proporcionan toda la funcionalidad de las API de Win32 enumeradas anteriormente, además de agregar la capacidad de enumerar todas las carpetas conocidas, acceder a las propiedades de carpetas conocidas y ampliar el conjunto estándar de carpetas conocidas.

-   [**IKnownFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder)
-   [**IKnownFolderManager**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager)

Un ejemplo de C++ que muestra las API de carpetas conocidas se incluye en Windows Software Development Kit (SDK). Una vez instalado el SDK de Windows en el equipo, el ejemplo se puede encontrar en %ProgramFiles% \\ Microsoft SDKs \\ Windows \\ v6.0 Samples WinUI Shell AppPlatform KnownFolders (Archivos de programa% SDK de Microsoft Windows ejemplos de \\ \\ WinUI Shell \\ \\ AppPlatform \\ KnownFolders).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplo de carpetas conocidas](/windows/win32/shell/samples-knownfolders)
</dt> </dl>
