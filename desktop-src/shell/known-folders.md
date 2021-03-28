---
description: Windows Vista presenta nuevos escenarios de almacenamiento y un nuevo espacio de nombres de Perfil de usuario.
title: Carpetas conocidas
ms.topic: article
ms.date: 05/31/2018
ms.assetid: d0c25eef-53ac-4dad-805a-b9ba4cd86be9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7527b7242c68f0d6c78cd0fae427626c182302f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985782"
---
# <a name="known-folders"></a>Carpetas conocidas

Windows Vista presenta nuevos escenarios de almacenamiento y un nuevo espacio de nombres de Perfil de usuario. Para abordar estos nuevos factores, se ha reemplazado el sistema anterior que hace referencia a las carpetas estándar mediante un valor [**CSIDL**](csidl.md) . A partir de Windows Vista, se hace referencia a esas carpetas mediante un nuevo conjunto de valores GUID denominados identificadores de carpeta conocidos.

El sistema de carpetas conocido proporciona estas ventajas:

-   Los fabricantes de software independientes (ISV) pueden extender el conjunto de identificadores de carpeta conocidos con los suyos propios. Pueden definir carpetas, asignarles identificadores y registrarlos en el sistema. No se pudieron extender los valores de CSIDL.
-   Todas las carpetas conocidas de un sistema se pueden enumerar. Ninguna API proporcionó esta funcionalidad para los valores CSIDL. Vea [**IKnownFolderManager:: GetFolderIds**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids) para obtener más información.
-   Una carpeta conocida agregada por un ISV puede Agregar propiedades personalizadas que le permitan explicar su finalidad y el uso previsto.
-   Muchas carpetas conocidas se pueden redirigir a nuevas ubicaciones, incluidas las ubicaciones de red. En el sistema CSIDL, solo se podría redirigir la carpeta **Mis documentos** .
-   Las carpetas conocidas pueden tener controladores personalizados para su uso durante la creación o la eliminación.

Todavía se admite el sistema CSIDL y las API que hacen uso de los valores de CSIDL por compatibilidad. Sin embargo, no se recomienda usarlas en ningún desarrollo nuevo.


En los temas siguientes se describen los detalles del sistema de carpetas conocidas.

-   [Trabajar con carpetas conocidas en aplicaciones](working-with-known-folders.md)
-   [Cómo extender carpetas conocidas con carpetas personalizadas](how-to-extend-known-folders-with-custom-folders.md)
-   [**KNOWNFOLDERID**](knownfolderid.md)

Las siguientes páginas de referencia explican las funciones de carpetas conocidas de Win32, que se pueden usar para recuperar la ubicación de carpetas conocidas o redirigirlas a una nueva ubicación. Estas funciones reemplazan a las funciones anteriores de Win32. Las nuevas funciones se proporcionan para proporcionar un comportamiento equivalente a las funciones anteriores, pero cada nueva función también se duplica mediante una API del modelo de objetos componentes (COM).



| Nueva función                                             | Reemplazo                                           | Equivalente de COM                                            |
|----------------------------------------------------------|----------------------------------------------------|-----------------------------------------------------------|
| [**SHGetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath)     | [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha)         | [**IKnownFolder::GetPath**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getpath)     |
| [**SHGetKnownFolderIDList**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist) | [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) | [**IKnownFolder::GetIDList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getidlist) |
| [**SHSetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetknownfolderpath)     | [**SHSetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetfolderpatha)         | [**IKnownFolder::SetPath**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-setpath)     |



 

Las siguientes páginas de referencia explican las API de carpetas conocidas de COM, que proporcionan toda la funcionalidad de las API de Win32 enumeradas anteriormente, además de agregar la capacidad de enumerar todas las carpetas conocidas, tener acceso a las propiedades de las carpetas conocidas y ampliar el conjunto estándar de carpetas conocidas.

-   [**IKnownFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder)
-   [**IKnownFolderManager**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager)

En el kit de desarrollo de software (SDK) de Windows se incluye un ejemplo de C++ que muestra las API de carpeta conocidas. Una vez que haya instalado el Windows SDK en el equipo, el ejemplo se puede encontrar en% ProgramFiles% \\ Microsoft SDKs \\ Windows \\ v 6.0 \\ Samples \\ WinUI \\ Shell \\ AppPlatform \\ KnownFolders.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplo de carpetas conocidas](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))
</dt> </dl>

 

 
