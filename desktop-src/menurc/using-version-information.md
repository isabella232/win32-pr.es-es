---
title: Uso de información de versión
description: En este tema se describe cómo usar las funciones de información de versión.
ms.assetid: 447b57c9-9e94-4a28-897e-f7b87d9cb25a
keywords:
- resources,version information
- información de versión
- información del archivo de instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a8785275f5aac69218989250d1c0f83e0a1ff9f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467203"
---
# <a name="using-version-information"></a>Uso de información de versión

Normalmente, un programa de instalación tiene los siguientes objetivos:

-   Para colocar los archivos en la ubicación correcta.
-   Para notificar al usuario si el programa de instalación está reemplazando un archivo existente por una versión significativamente diferente, por ejemplo, reemplazando un archivo en alemán por un archivo en inglés o reemplazando un archivo más reciente por un archivo anterior.

Al escribir el programa de instalación, debe tener la siguiente información para cada archivo:

-   Nombre y ubicación del archivo (denominado archivo de origen).
-   Nombre del archivo equivalente en el disco duro del usuario (denominado archivo de destino). Este nombre suele ser el mismo que el nombre de archivo del disco de instalación.
-   El estado de uso compartido del archivo, es decir, si el archivo es privado para la aplicación que se está instalando o si podría ser compartido por varias aplicaciones.

El programa de instalación puede usar la [**función VerFindFile**](/windows/desktop/api/Winver/nf-winver-verfindfilea) para determinar dónde se debe copiar el archivo en el disco. Esta función también se puede usar para especificar si el archivo es privado para la aplicación o se puede compartir. Si se produce un problema al buscar el archivo, **VerFindFile** devuelve un valor de error. Por ejemplo, si el sistema usa el archivo de destino, **VerFindFile** devuelve **VFF \_ FILEINUSE**. El programa de instalación debe notificar al usuario el problema y responder a la decisión del usuario de continuar o finalizar la instalación.

La [**función VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) copia el archivo de origen en un archivo temporal en el directorio especificado por [**VerFindFile**](/windows/desktop/api/Winver/nf-winver-verfindfilea). Si es necesario, **VerInstallFile** expande el archivo mediante las funciones de la biblioteca de descompresión de datos.

[**VerInstallFile compara**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) la información de versión del archivo temporal con la del archivo de destino. Si los dos difieren, **VerInstallFile** devuelve uno o varios valores de error. Por ejemplo, devuelve **VIF \_ SRCOLD** si el archivo temporal es anterior al archivo de destino y **VIF \_ DIFFLANG** si los archivos tienen identificadores de lenguaje o valores de página de códigos diferentes. El programa de instalación debe notificar al usuario el problema y responder a la decisión del usuario de continuar o finalizar la instalación.

Algunos [**errores de VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) son recuperables. Es decir, el programa de instalación puede volver a llamar a **VerInstallFile,** especificando la opción **\_ FORCEINSTALL de VIFF,** para instalar el archivo independientemente del conflicto de versión. Si **VerInstallFile devuelve** **VIF \_ TEMPFILE** y el usuario decide no forzar la instalación, el programa de instalación debe eliminar el archivo temporal.

[**VerInstallFile podría**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) encontrar un error irrecuperable al intentar forzar la instalación, aunque el error no existía anteriormente. Por ejemplo, otro usuario podría bloquear el archivo antes de que el programa de instalación intentara forzar la instalación. Si un programa de instalación intenta forzar la instalación después de un error no recuperable, se produce un error **en VerInstallFile.** El programa de instalación debe contener rutinas para recuperarse de este tipo de error.

La solución recomendada es mostrar un cuadro de diálogo con los botones **Instalar,** **Omitir** **e Instalar todo**. (Otra solución es un cuadro de diálogo con los botones **Sí,** Sí a **todo,** **Omitir** y **Cancelar).** El **botón Instalar todo** debe impedir que el programa de instalación pida al usuario errores similares mediante la inclusión de la opción **\_ FORCEINSTALL** de VIFF en todos los usos posteriores de [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea). En el caso de errores irrecuperables, **los** botones Instalar **e** Instalar todo deben estar deshabilitados.

Para mostrar un mensaje de error útil al usuario, el programa de instalación normalmente debe recuperar información de los recursos de versión de los archivos en conflicto. Hay cuatro funciones que el programa de instalación puede usar para este propósito:

-   [**GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea)
-   [**GetFileVersionInfo**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoa)
-   [**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea)
-   [**VerLanguageName**](/windows/desktop/api/Winver/nf-winver-verlanguagenamea)

[**GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea) devuelve el tamaño de la información de versión. [**GetFileVersionInfo usa**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoa) información recuperada por **GetFileVersionInfoSize** para recuperar una estructura que contiene la información de versión. [**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea) recupera un miembro específico de esa estructura.

Por ejemplo, si [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) devuelve el error **\_ DIFFTYPE de VIF,** el programa de instalación debe usar las funciones [**GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea), [**GetFileVersionInfo**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoa)y [**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea) en los archivos temporales y de destino para obtener el tipo general de cada archivo. Si los idiomas de los archivos están en conflicto, el programa de instalación también debe usar [**VerLanguageName**](/windows/desktop/api/Winver/nf-winver-verlanguagenamea) para traducir el identificador de idioma binario en una representación de texto del idioma. (Por ejemplo, 0x040C se traduce a la cadena "Francés").

Si [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) devuelve un error de archivo, como **VIF \_ ACCESSVIOLATION,** el programa de instalación debe usar la función [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para recuperar el valor de error más reciente. El programa debe traducir este valor en un mensaje informativo para mostrarlo al usuario. El programa no debe producir el control entre las llamadas a **VerInstallFile** y **GetLastError**.

 

 