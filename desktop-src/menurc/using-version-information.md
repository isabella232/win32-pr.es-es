---
title: Usar información de versión
description: En este tema se describe cómo utilizar las funciones de información de versión.
ms.assetid: 447b57c9-9e94-4a28-897e-f7b87d9cb25a
keywords:
- recursos, información de versión
- información de versión
- información del archivo de instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a8785275f5aac69218989250d1c0f83e0a1ff9f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790240"
---
# <a name="using-version-information"></a>Usar información de versión

Un programa de instalación normalmente tiene los siguientes objetivos:

-   Para colocar los archivos en la ubicación correcta.
-   Para notificar al usuario si el programa de instalación está reemplazando un archivo existente por una versión que es significativamente diferente, por ejemplo, reemplazando un archivo de idioma alemán por un archivo de idioma inglés o reemplazando un archivo más reciente por un archivo más antiguo.

Al escribir el programa de instalación, debe tener la siguiente información para cada archivo:

-   El nombre y la ubicación del archivo (denominado archivo de código fuente).
-   El nombre del archivo equivalente en el disco duro del usuario (denominado archivo de destino). Este nombre suele ser el mismo que el nombre de archivo del disco de instalación.
-   El estado de uso compartido del archivo, es decir, si el archivo es privado para la aplicación que se está instalando o puede ser compartido por varias aplicaciones.

El programa de instalación puede usar la función [**VerFindFile**](/windows/desktop/api/Winver/nf-winver-verfindfilea) para determinar dónde se debe copiar el archivo en el disco. Esta función también se puede usar para especificar si el archivo es privado para la aplicación o se puede compartir. Si se produce un problema al buscar el archivo, **VerFindFile** devuelve un valor de error. Por ejemplo, si el sistema usa el archivo de destino, **VerFindFile** devuelve **VFF \_ FILEINUSE**. El programa de instalación debe notificar al usuario el problema y responder a la decisión del usuario de continuar o finalizar la instalación.

La función [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) copia el archivo de código fuente en un archivo temporal en el directorio especificado por [**VerFindFile**](/windows/desktop/api/Winver/nf-winver-verfindfilea). Si es necesario, **VerInstallFile** expande el archivo con las funciones de la biblioteca de descompresión de datos.

[**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) compara la información de versión del archivo temporal con la del archivo de destino. Si los dos son diferentes, **VerInstallFile** devuelve uno o varios valores de error. Por ejemplo, devuelve **VIF \_ SRCOLD** si el archivo temporal es más antiguo que el archivo de destino y **VIF \_ DIFFLANG** si los archivos tienen diferentes identificadores de idioma o valores de página de códigos. El programa de instalación debe notificar al usuario el problema y responder a la decisión del usuario de continuar o finalizar la instalación.

Algunos errores de [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) son recuperables. Es decir, el programa de instalación puede volver a llamar a **VerInstallFile** , especificando la opción **VIFF \_ FORCEINSTALL** , para instalar el archivo independientemente del conflicto de versiones. Si **VerInstallFile** devuelve **VIF \_ TEMPFILE** y el usuario decide no forzar la instalación, el programa de instalación debe eliminar el archivo temporal.

[**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) podría encontrar un error irrecuperable al intentar forzar la instalación, aunque el error no existía anteriormente. Por ejemplo, el archivo podría estar bloqueado por otro usuario antes de que el programa de instalación intentara forzar la instalación. Si un programa de instalación intenta forzar la instalación después de un error no recuperable, **VerInstallFile** produce un error. El programa de instalación debe contener rutinas para recuperarse de este tipo de error.

La solución recomendada es mostrar un cuadro de diálogo con los botones **instalar**, **omitir** e **instalar todo**. (Otra solución es un cuadro de diálogo con los botones **sí**, **sí a todo**, **omitir** y **Cancelar**). El botón **instalar todo** debe evitar que el programa de instalación solicite al usuario errores similares al incluir la opción **VIFF \_ FORCEINSTALL** en todos los usos subsiguientes de [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea). En el caso de los errores irrecuperables, se deben deshabilitar los botones **instalar** e **instalar todos** .

Para mostrar un mensaje de error útil al usuario, el programa de instalación normalmente debe recuperar información de los recursos de versión de los archivos en conflicto. Hay cuatro funciones que el programa de instalación puede usar para este propósito:

-   [**GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea)
-   [**GetFileVersionInfo**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoa)
-   [**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea)
-   [**VerLanguageName**](/windows/desktop/api/Winver/nf-winver-verlanguagenamea)

[**GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea) devuelve el tamaño de la información de versión. [**GetFileVersionInfo**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoa) usa la información recuperada por **GetFileVersionInfoSize** para recuperar una estructura que contiene la información de versión. [**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea) recupera un miembro específico de esa estructura.

Por ejemplo, si [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) devuelve el **error \_ VIF DIFFTYPE** , el programa de instalación debe usar las funciones [**GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea), [**GetFileVersionInfo**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoa)y [**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea) en los archivos temporales y de destino para obtener el tipo general de cada archivo. Si los idiomas de los archivos entran en conflicto, el programa de instalación también debe utilizar [**VerLanguageName**](/windows/desktop/api/Winver/nf-winver-verlanguagenamea) para traducir el identificador de idioma binario en una representación de texto del idioma. (Por ejemplo, 0x040C se convierte en la cadena "francés").

Si [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) devuelve un error de archivo, como **VIF \_ ACCESSVIOLATION**, el programa de instalación debe usar la función [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para recuperar el valor de error más reciente. El programa debe convertir este valor en un mensaje informativo para mostrar al usuario. El programa no debe proporcionar el control entre las llamadas a **VerInstallFile** y **GetLastError**.

 

 