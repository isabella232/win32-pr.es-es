---
description: En esta sección se describen las consideraciones para implementar la aplicación MUI para un uso óptimo de la lógica de carga de la aplicación y del cargador de recursos.
ms.assetid: 6c10b355-9bdd-4dba-8446-91034d4fe9b8
title: Implementación de aplicaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2023e5fc2dbde51a6ef996126e7557c9ffce8d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105670012"
---
# <a name="application-deployment"></a>Implementación de aplicaciones

En esta sección se describen las consideraciones para implementar la aplicación MUI para un uso óptimo de la lógica de carga de la aplicación y del cargador de recursos.

## <a name="packaging"></a>Packaging

El empaquetado de la aplicación depende del tipo de compatibilidad de idioma proporcionado, ya que Windows instala paquetes de idioma según las preferencias del usuario. Por ejemplo, si decidió admitir la configuración de idioma del sistema, es posible que desee proporcionar compatibilidad con todos los idiomas en un único paquete, independientemente del usuario previsto.

Si la aplicación y los recursos son grandes, debe usar un paquete por cada idioma admitido. Por ejemplo, puede usar este tipo de empaquetado si la aplicación presenta lenguajes seleccionables por el usuario y el usuario necesita la adición y eliminación dinámica de recursos de idioma.

## <a name="file-placement-on-windows-vista-and-later"></a>Ubicación de los archivos en Windows Vista y versiones posteriores

En esta sección se describe la ubicación de los archivos de una aplicación de MUI destinada únicamente a Windows Vista y versiones posteriores.

### <a name="place-the-ln-file"></a>Colocar el archivo LN

Un archivo LN típico para una aplicación MUI es un archivo. exe o. dll, por ejemplo, BakerDelta.dll. Debe colocar este archivo en la carpeta raíz donde está instalada la aplicación, por ejemplo, X: \\ \\ <somepath> \\BakerDelta.dll.

### <a name="place-language-specific-resource-files"></a>Colocar Language-Specific archivos de recursos

Los archivos de recursos específicos del lenguaje deben tener nombres predecibles que se hayan formado anexando ". mui" al nombre completo del archivo LN, por ejemplo, BakerDelta.dll. MUI. Estos archivos deben colocarse en subcarpetas con el nombre de los [nombres de idioma](language-names.md)adecuados. En el ejemplo siguiente se muestra la ubicación de los recursos para el archivo BakerDelta.dll LN, con archivos de recursos específicos del idioma para inglés (Reino Unido), Inglés (Estados Unidos), Inglés neutro, español (España), español (México) y español neutro:

-   X: \\ \\ <somepath> \\BakerDelta.dll
-   X: \\ \\ <somepath> \\ en-GB \\BakerDelta.dll. MUI
-   X: \\ \\ <somepath> \\ en-US \\BakerDelta.dll. MUI
-   X: \\ \\ <somepath> \\ en \\BakerDelta.dll. MUI
-   X: \\ \\ <somepath> \\ es-es \\BakerDelta.dll. MUI
-   X: \\ \\ <somepath> \\ es-mx \\BakerDelta.dll. MUI
-   X: \\ \\ <somepath> \\ es \\BakerDelta.dll. MUI

Los archivos de recursos se deben colocar en sus ubicaciones correctas durante la instalación de la aplicación MUI o de un paquete de idioma. Es importante colocar cada archivo en la carpeta correcta, ya que el cargador de recursos no puede funcionar correctamente en caso contrario. Con el ejemplo anterior, el cargador de recursos examina X: \\ <somepath> \\ en-US \\BakerDelta.dll. MUI para los recursos de inglés (Estados Unidos). Si el cargador busca en ese archivo y encuentra solo los recursos de idioma español, se produce un error.

## <a name="file-placement-on-a-pre-windows-vista-operating-system"></a>Ubicación de los archivos en un sistema operativo anterior a Windows Vista

Una aplicación para ejecutarse en un sistema operativo anterior a Windows Vista puede utilizar la Convención de Windows Vista para colocar archivos de recursos específicos del idioma en carpetas basadas en nombres de idioma. Como alternativa, la aplicación puede ajustarse a una Convención anterior que forma las rutas de acceso de los [identificadores de idioma](language-identifiers.md). En el caso de las aplicaciones que solo admiten un único idioma, puede simplemente colocar el archivo de recursos específico del idioma en el directorio raíz con el archivo binario.

Por ejemplo, considere un archivo LN denominado BakerDelta.dll, con archivos de recursos específicos del idioma para inglés (Reino Unido), Inglés (Estados Unidos), Inglés neutro, español (España), español (México) y español neutro. Una instalación en un sistema operativo anterior a Windows Vista podría colocar estos archivos de la siguiente manera:

-   X: \\ \\ <somepath> \\BakerDelta.dll
-   X: \\ \\ <somepath> \\BakerDelta.dll. MUI (archivo opcional. mui que contiene recursos en el idioma del sistema operativo como reserva definitiva)
-   X: \\ \\ <somepath> \\ mui \\ 0809 \\BakerDelta.dll. MUI
-   X: \\ \\ <somepath> \\ mui \\ 0409 \\BakerDelta.dll. MUI
-   X: \\ \\ <somepath> \\ mui \\ 0209 \\BakerDelta.dll. MUI
-   X: \\ \\ <somepath> \\ mui \\ 040a \\BakerDelta.dll. MUI
-   X: \\ \\ <somepath> \\ mui \\ 080a \\BakerDelta.dll. MUI
-   X: \\ \\ <somepath> \\ mui \\ 0209 \\BakerDelta.dll. MUI

Además de estos archivos, la aplicación puede configurar un archivo de recursos específico del lenguaje de reserva final para que resida en la misma carpeta que la propia aplicación. En el ejemplo anterior, este archivo es X: \\ <somepath> \\BakerDelta.dll. MUI.

## <a name="installation"></a>Instalación

La lógica de instalación para copiar y configurar archivos de aplicación se basa en los idiomas admitidos y la ubicación de los archivos de recursos de idioma en las ubicaciones de instalación correctas. Un instalador debe instalar y configurar la aplicación para que el usuario pueda agregar y quitar idiomas fácilmente.

Si la aplicación simplemente instala el idioma del sistema operativo de destino, el instalador debe detectar la interfaz de usuario del sistema operativo para determinar los recursos de la aplicación que se van a instalar. Para admitir la mejor experiencia de usuario, el instalador también debe detectar el idioma de la interfaz de usuario para presentar una interfaz de usuario localizada para la instalación propiamente dicha.

Se recomienda usar Windows Installer (MSI) para crear el software de instalación. Los recursos asociados deben incluirse en el archivo de recursos de idioma base, tal como se describe en [crear el archivo de recursos de idioma base](creating-the-base-language-resource-file.md). Para obtener instrucciones sobre el uso de MSI para preparar el instalador de la aplicación, consulte [Windows Installer](../msi/windows-installer-portal.md).

## <a name="uninstall-program"></a>Desinstalar programa

También es posible que desee proporcionar un programa de desinstalación con la aplicación MUI. MSI también se recomienda para la creación de este programa. Para obtener instrucciones sobre el uso de MSI para preparar el software de desinstalación, consulte [Windows Installer](../msi/windows-installer-portal.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de la interfaz de usuario multilingüe](using-multilingual-user-interface.md)
</dt> </dl>

 

 
