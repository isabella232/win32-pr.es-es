---
description: El sistema de carpetas conocidas proporciona una manera de interactuar con determinadas carpetas de alto perfil que están presentes de forma predeterminada en Windows.
ms.assetid: 8b6163b5-e152-47c2-99f1-43e80cf0713e
title: Trabajar con carpetas conocidas en aplicaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0981d354e49f569dda229fab32308d8f4a79ff99
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127262479"
---
# <a name="working-with-known-folders-in-applications"></a>Trabajar con carpetas conocidas en aplicaciones

El sistema de carpetas conocidas proporciona una manera de interactuar con determinadas carpetas de alto perfil que están presentes de forma predeterminada en Windows. También permite esas mismas interacciones con carpetas instaladas y registradas con el sistema de carpetas conocidas por las aplicaciones. En este tema se de abordan las posibles interacciones que proporcionan las API de carpetas conocidas.

-   [Interfaces de carpeta conocidas](#known-folder-interfaces)
-   [Redireccionamiento](#redirection)
-   [Temas relacionados](#related-topics)

> [!IMPORTANT]
> Para redirigir las carpetas Documentos, Imágenes o Escritorio a OneDrive, use OneDrive mover carpetas conocidas en lugar del método de redirección descrito en este artículo. Para obtener información, vea [Redirigir y mover Windows carpetas conocidas a OneDrive](/onedrive/redirect-known-folders).  

## <a name="known-folder-interfaces"></a>Interfaces de carpeta conocidas

Hay dos interfaces de carpeta conocida: [**IKnownFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder) e [**IKnownFolderManager.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager)

[**IKnownFolderManager proporciona**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager) muchas de las funciones más generales con respecto a estas carpetas. Sus métodos permiten:

-   Recupere un [**IKnownFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder) en función de [**KNOWNFOLDERID**](knownfolderid.md)de esa carpeta, su nombre canónico, su ruta de acceso expresada como una cadena o su ruta de acceso expresada como IDList.
-   Convierta un CSIDL en su [**equivalente KNOWNFOLDERID**](knownfolderid.md) o convierta **un VALOR KNOWNFOLDERID** en su equivalente de CSIDL heredado.
-   Registrar o anular el registro de una carpeta conocida con el sistema.
-   Recupere todos [**los valores KNOWNFOLDERID**](knownfolderid.md) registrados en ese sistema.
-   Redirigir una carpeta conocida a una nueva ubicación.

[**IKnownFolder proporciona**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder) un método que permite que una carpeta se redirija a sí misma proporcionando una nueva ruta de acceso. Sus otros métodos obtienen información sobre una carpeta conocida específica, como:

-   Categoría de la carpeta: virtual, fija, común o por usuario.
-   Tipo de la carpeta, como archivos comprimidos, documentos, imágenes o archivos de usuario.
-   [**KNOWNFOLDERID de**](knownfolderid.md) la carpeta.
-   Ruta de acceso completa de la carpeta como IDList o como una cadena. También su ruta de acceso relativa a una carpeta primaria.
-   Nombre canónico de la carpeta.
-   Información sobre herramientas que se muestra para la carpeta.
-   Icono que se muestra para la carpeta.
-   Descripción de la carpeta que explica su propósito y uso.
-   Si la carpeta es capaz de redirigirse.

[**IKnownFolder también**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder) proporciona un método para recuperar un [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) basado en la carpeta . Esto le permite enlazar la carpeta a un controlador, comparar dos carpetas y recuperar los atributos, el nombre para mostrar y la carpeta primaria de la carpeta.

## <a name="redirection"></a>Redireccionamiento

El redireccionamiento de carpetas es una característica importante del sistema de carpetas conocido. Todas las carpetas conocidas de categoría [ común CATEGORY \_ \_ COMMON**](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category) o [  \_ \_ PERUSER CATEGORY PERUSER*](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category) por usuario se pueden redirigir. Sin embargo, no se puede redirigir la carpeta de la categoría [ **virtual** DE CATEGORÍA \_ VIRTUAL** \_](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category) o [ fijar CATEGORY \_ \_ FIXED**..](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category)

Las carpetas se pueden redirigir a otra ubicación en el mismo equipo o a una ubicación de una red. En el caso de un redireccionamiento de red, la carpeta se puede almacenar en caché localmente a través del almacenamiento en caché del lado cliente para proporcionar acceso sin conexión. Sin embargo, incluso si existe una caché local, se debe tener acceso a la propia carpeta redirigida a través de la red.

La redirección de carpetas no es nueva para Windows Vista. Por ejemplo, en Windows XP, algunas carpetas identificadas a través del sistema CSIDL se podrían redirigir mediante una llamada a [**SHSetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetfolderpatha) o modificando la entrada del CSIDL en el Registro. En Windows Vista y versiones posteriores, el redireccionamiento debe realizarse a través [**de IKnownFolder::SetPath**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-setpath) o [**SHSetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetknownfolderpath).

Para determinar si se puede redirigir una carpeta, llame a [**IKnownFolder::GetRedirectionCapabilities**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getredirectioncapabilities). Si no se puede redirigir la carpeta, esta llamada puede dar una explicación.

Si se redirige una carpeta a una ubicación de red, todavía se puede llamar correctamente a los métodos [**IKnownFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder) en ella.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplo de carpetas conocidas](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))
</dt> </dl>

 

 
