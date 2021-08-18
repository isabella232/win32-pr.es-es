---
description: En esta sección se describen las consideraciones para implementar la aplicación DEA para un uso óptimo por parte de la lógica de carga de aplicaciones y el cargador de recursos.
ms.assetid: 6c10b355-9bdd-4dba-8446-91034d4fe9b8
title: Implementación de aplicaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcb2d7605a2c6a39629749c00d175be4df8a3c66d8b0dc6c870926ec665d9ce6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041615"
---
# <a name="application-deployment"></a>Implementación de aplicaciones

En esta sección se describen las consideraciones para implementar la aplicación DEA para un uso óptimo por parte de la lógica de carga de aplicaciones y el cargador de recursos.

## <a name="packaging"></a>Packaging

El empaquetado de la aplicación depende del tipo de compatibilidad de idioma proporcionado, ya que Windows paquetes de idioma en función de las preferencias del usuario. Por ejemplo, si ha decidido admitir la configuración de idioma del sistema, es posible que desee proporcionar toda la compatibilidad con idiomas en un único paquete, independientemente del usuario previsto.

Si la aplicación y los recursos son grandes, debe usar un paquete por idioma admitido. Por ejemplo, puede usar este tipo de empaquetado si la aplicación presenta idiomas seleccionables por el usuario y el usuario necesita agregar y quitar recursos de idioma de forma dinámica.

## <a name="file-placement-on-windows-vista-and-later"></a>Selección de ubicación de Windows Vista y versiones posteriores

En esta sección se describe la selección de ubicación de archivos para una aplicación DE EXTENSIÓN dirigida solo a Windows Vista y versiones posteriores.

### <a name="place-the-ln-file"></a>Colocar el archivo LN

Un archivo LN típico para una aplicación de MUI es un archivo .exe o un archivo .dll, por ejemplo, BakerDelta.dll. Debe colocar este archivo en la carpeta raíz donde está instalada la aplicación, por ejemplo, X: \\ \\ <somepath> \\BakerDelta.dll.

### <a name="place-language-specific-resource-files"></a>Colocar Language-Specific archivos de recursos

Los archivos de recursos específicos del lenguaje deben tener nombres de predicción formados anexando ".mui" al nombre completo del archivo LN, por ejemplo, BakerDelta.dll.mui. Estos archivos deben colocarse en subcarpetas con el nombre de los nombres [de idioma adecuados.](language-names.md) En el ejemplo siguiente se muestra la ubicación de los recursos para el archivo LN de BakerDelta.dll, con archivos de recursos específicos del idioma para inglés (Reino Unido), inglés (Estados Unidos), inglés neutro, español (España), español (México) y español neutro:

-   X: \\ \\ <somepath> \\BakerDelta.dll
-   X: \\ \\ <somepath> \\ en-GB \\BakerDelta.dll.mui
-   X: \\ \\ <somepath> \\ en-US \\BakerDelta.dll.mui
-   X: \\ \\ <somepath> \\ en \\BakerDelta.dll.mui
-   X: \\ \\ <somepath> \\ es-ES \\BakerDelta.dll.mui
-   X: \\ \\ <somepath> \\ es-MX \\BakerDelta.dll.mui
-   X: \\ \\ <somepath> \\ es \\BakerDelta.dll.mui

Los archivos de recursos deben colocarse en sus ubicaciones correctas durante la instalación de la aplicación DEA o un paquete de idioma. Es importante colocar cada archivo en la carpeta correcta, ya que el cargador de recursos no puede funcionar correctamente de lo contrario. Con el ejemplo anterior, el cargador de recursos examina X: \\ <somepath> \\ en-USBakerDelta.dll.mui para los recursos \\ de inglés (Estados Unidos). Si el cargador busca en ese archivo y solo encuentra recursos en español, se produce un error.

## <a name="file-placement-on-a-pre-windows-vista-operating-system"></a>Selección de ubicación de archivos en un sistema operativo Windows Vista previo

Una aplicación que se ejecute en un sistema operativo Windows Vista puede usar la convención de Windows Vista de colocar archivos de recursos específicos del idioma en carpetas basadas en nombres de idioma. Como alternativa, la aplicación puede cumplir una convención anterior que forma rutas de acceso a partir de [identificadores de lenguaje](language-identifiers.md). En el caso de las aplicaciones que solo admiten un solo idioma, puede colocar el archivo de recursos específico del lenguaje en el directorio raíz con el archivo binario.

Por ejemplo, considere un archivo LN denominado BakerDelta.dll, con archivos de recursos específicos del idioma para inglés (Reino Unido), inglés (Estados Unidos), inglés neutro, español (España), español (México) y español neutro. Una instalación en un sistema operativo Windows Vista puede colocar estos archivos de la siguiente manera:

-   X: \\ \\ <somepath> \\BakerDelta.dll
-   X: \\ \\ <somepath>BakerDelta.dll.mui (archivo .csv opcional que contiene recursos en el idioma del sistema operativo \\ como reserva definitiva)
-   X: \\ \\ <somepath> \\ MUI \\ 0809 \\BakerDelta.dll.mui
-   X: \\ \\ <somepath> \\ MUI \\ 0409 \\BakerDelta.dll.mui
-   X: \\ \\ <somepath> \\ MUI \\ 0209 \\BakerDelta.dll.mui
-   X: \\ \\ <somepath> \\ MUI \\ 040a \\BakerDelta.dll.mui
-   X: \\ \\ <somepath> \\ MUI \\ 080a \\BakerDelta.dll.mui
-   X: \\ \\ <somepath> \\ MUI \\ 0209 \\BakerDelta.dll.mui

Además de estos archivos, la aplicación puede configurar un archivo de recursos específico del lenguaje de reserva final para residir en la misma carpeta que la propia aplicación. En el ejemplo anterior, este archivo es X: \\ <somepath> \\BakerDelta.dll.mui.

## <a name="installation"></a>Instalación

La lógica de instalación para copiar y configurar archivos de aplicación se basa en los idiomas admitidos y en la ubicación de los archivos de recursos de idioma en las ubicaciones de instalación correctas. Un instalador debe instalar y configurar la aplicación para que el usuario pueda agregar y quitar idiomas fácilmente.

Si la aplicación simplemente instala el idioma del sistema operativo de destino, el instalador debe detectar la interfaz de usuario del sistema operativo para determinar los recursos de aplicación que se instalarán. Para admitir la mejor experiencia del usuario, el instalador también debe detectar el idioma de la interfaz de usuario para presentar una interfaz de usuario localizada para la propia instalación.

Se recomienda usar el instalador Windows (MSI) para crear el software de instalación. Los recursos asociados deben incluirse en el archivo de recursos del lenguaje base, como se describe en [Creación del archivo de recursos de lenguaje base](creating-the-base-language-resource-file.md). Para obtener instrucciones sobre el uso de MSI para preparar el instalador de la aplicación, [consulte Windows Installer](../msi/windows-installer-portal.md).

## <a name="uninstall-program"></a>Desinstalar programa

Es posible que también quieras instalar un programa de desinstalación con tu aplicación DE INTERFAZ DE USUARIO. Msi también se recomienda para la creación de este programa. Para obtener instrucciones sobre el uso de MSI para preparar el software de desinstalación, [consulte Windows Installer](../msi/windows-installer-portal.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de Interfaz de usuario multilingüe](using-multilingual-user-interface.md)
</dt> </dl>

 

 
