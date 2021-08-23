---
title: Buscar archivos
description: De forma predeterminada, RC busca archivos de encabezado y archivos de recursos (como archivos de icono y cursor) primero en el directorio actual y, a continuación, en los directorios especificados por la variable de entorno INCLUDE.
ms.assetid: 6c8c905d-b0f6-4665-9a93-62617ff30137
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4fecaa3c20c9bedf498c30462d5e139da83f11d45a47c6d5e7554adb8ed325b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119601565"
---
# <a name="searching-for-files"></a>Buscar archivos

De forma predeterminada, RC busca archivos de encabezado y archivos de recursos (como archivos de icono y cursor) primero en el directorio actual y, a continuación, en los directorios especificados por la variable de entorno INCLUDE. (La variable de entorno PATH no tiene ningún efecto en los directorios que RC busca).

## <a name="adding-a-directory-to-search"></a>Agregar un directorio a la búsqueda

Puede usar la opción **/i** para agregar un directorio a la lista de directorios que RC busca. A continuación, el compilador busca en los directorios en el orden siguiente:

1.  Directorio actual
2.  El directorio o directorios que especifique mediante la **opción /i,** en el orden en que aparecen en la línea de comandos rc
3.  Lista de directorios especificados por la variable de entorno INCLUDE, en el orden en que la variable los enumera, a menos que especifique la **opción /x.**

En el ejemplo siguiente se compila el archivo de definición de recursos MyApp.rc:

**rc /i c: \\ source \\ stuff /i d: \\ resources myapp.rc**

Al compilar el script MyApp.rc, RC busca primero archivos de encabezado y archivos de recursos en el directorio actual, luego en C: Source Stuff y D: Resources y, a continuación, en los directorios especificados por la variable de entorno \\ \\ \\ INCLUDE.

## <a name="ignoring-the-include-environment-variable"></a>Omitir la variable de entorno INCLUDE

Puede evitar que RC use la variable de entorno INCLUDE al determinar los directorios en los que se va a buscar. Para ello, use la **opción /x.** A continuación, el compilador busca archivos solo en el directorio actual y en los directorios que especifique mediante **la opción /i.**

El comando siguiente compila el archivo de script MyApp.rc:

**rc /x /i c: \\ source \\ stuff myapp.rc**

Al compilar el script MyApp.rc, RC busca primero los archivos de encabezado y los archivos de recursos en el directorio actual y, a continuación, en C: \\ Source \\ Stuff. No busca en los directorios especificados por la variable de entorno INCLUDE.

 

 




