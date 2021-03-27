---
description: El sistema de carpetas conocido proporciona una manera de interactuar con determinadas carpetas de alto perfil que están presentes de forma predeterminada en Windows.
ms.assetid: 8b6163b5-e152-47c2-99f1-43e80cf0713e
title: Trabajar con carpetas conocidas en aplicaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0981d354e49f569dda229fab32308d8f4a79ff99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496757"
---
# <a name="working-with-known-folders-in-applications"></a>Trabajar con carpetas conocidas en aplicaciones

El sistema de carpetas conocido proporciona una manera de interactuar con determinadas carpetas de alto perfil que están presentes de forma predeterminada en Windows. También permite realizar las mismas interacciones con las carpetas instaladas y registradas con el sistema de carpetas conocidas por las aplicaciones. En este tema se describen esas posibles interacciones tal como las proporcionan las API de carpeta conocidas.

-   [Interfaces de carpeta conocidas](#known-folder-interfaces)
-   [Redireccionamiento](#redirection)
-   [Temas relacionados](#related-topics)

> [!IMPORTANT]
> Para redirigir los documentos, las imágenes o las carpetas de escritorio a OneDrive, use el traslado de carpetas conocidas de OneDrive en lugar del método de redireccionamiento que se describe en este artículo. Para obtener información, consulte [redirigir y trasladar carpetas conocidas de Windows a OneDrive](/onedrive/redirect-known-folders).  

## <a name="known-folder-interfaces"></a>Interfaces de carpeta conocidas

Hay dos interfaces de carpeta conocidas: [**IKnownFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder) y [**IKnownFolderManager**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager).

[**IKnownFolderManager**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager) proporciona muchas de las funciones más generales con respecto a estas carpetas. Sus métodos permiten:

-   Recupere un [**IKnownFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder) basado en el [**KNOWNFOLDERID**](knownfolderid.md)de la carpeta, su nombre canónico, su ruta de acceso expresada como una cadena o su ruta de acceso expresada como IDList.
-   Convierta un CSIDL en su equivalente de [**KNOWNFOLDERID**](knownfolderid.md) o convierta un **KNOWNFOLDERID** en su equivalente de CSIDL heredado.
-   Registrar o anular el registro de una carpeta conocida con el sistema.
-   Recupere todos los valores de [**KNOWNFOLDERID**](knownfolderid.md) registrados en ese sistema.
-   Redirigir una carpeta conocida a una nueva ubicación.

[**IKnownFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder) proporciona un método que permite que una carpeta se redirija a sí misma proporcionando una nueva ruta de acceso. Sus otros métodos obtienen información acerca de una carpeta conocida específica, entre las que se incluyen:

-   La categoría de la carpeta: virtual, fija, común o por usuario.
-   El tipo de la carpeta, como archivos comprimidos, documentos, imágenes o archivos de usuario.
-   [**KNOWNFOLDERID**](knownfolderid.md) de la carpeta.
-   La ruta de acceso completa de la carpeta como IDList o como una cadena. También es su ruta de acceso relativa a una carpeta principal.
-   Nombre canónico de la carpeta.
-   La información sobre herramientas mostrada para la carpeta.
-   El icono que se muestra para la carpeta.
-   Una descripción de la carpeta que explica su finalidad y uso.
-   Indica si la carpeta es capaz de redirigirse.

[**IKnownFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder) también proporciona un método para recuperar un [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) basado en la carpeta. Esto permite enlazar la carpeta a un controlador, comparar dos carpetas y recuperar los atributos de la carpeta, el nombre para mostrar y la carpeta principal.

## <a name="redirection"></a>Redireccionamiento

La redirección de carpetas es una característica importante del sistema de carpetas conocidas. Todas las carpetas conocidas de la categoría [ **Common** KF \_ Category \_ Common * * *](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category) * o [ **per-user** KF \_ categoría \_ peruser * *](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category) * * son redirigibles. No se puede redirigir la carpeta de la categoría KF virtual de categoría virtual [  \_ \_ * * *](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category) * o el KF de categoría [ **fija** \_ \_ * *](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category)* *.

Las carpetas se pueden redirigir a otra ubicación en el mismo equipo o a una ubicación de una red. En el caso de una redirección de red, la carpeta puede almacenarse en caché localmente a través del almacenamiento en caché del lado cliente para proporcionar acceso sin conexión. Sin embargo, incluso si existe una caché local, se debe tener acceso a la carpeta redirigida a través de la red.

La redirección de carpetas no es nueva en Windows Vista. Por ejemplo, en Windows XP algunas carpetas identificadas a través del sistema CSIDL se pueden redirigir a través de una llamada a [**SHSetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetfolderpatha) o modificando la entrada de CSIDL en el registro. En Windows Vista y versiones posteriores, el redireccionamiento debe realizarse a través de [**IKnownFolder:: SetPath**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-setpath) o [**SHSetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetknownfolderpath).

Para determinar si se puede redirigir una carpeta, llame a [**IKnownFolder:: GetRedirectionCapabilities**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getredirectioncapabilities). Si la carpeta no se puede redirigir, esta llamada puede dar una explicación.

Si una carpeta se redirige a una ubicación de red, todavía se pueden llamar correctamente a los métodos [**IKnownFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplo de carpetas conocidas](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))
</dt> </dl>

 

 
