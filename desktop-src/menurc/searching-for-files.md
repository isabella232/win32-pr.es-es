---
title: Búsqueda de archivos
description: De forma predeterminada, RC busca archivos de encabezado y archivos de recursos (como archivos de icono y cursor) primero en el directorio actual y, a continuación, en los directorios especificados por la variable de entorno INCLUDE.
ms.assetid: 6c8c905d-b0f6-4665-9a93-62617ff30137
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 078a04a4cf2f3461d03c7026e0f1d73d8fd38665
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360068"
---
# <a name="searching-for-files"></a>Búsqueda de archivos

De forma predeterminada, RC busca archivos de encabezado y archivos de recursos (como archivos de icono y cursor) primero en el directorio actual y, a continuación, en los directorios especificados por la variable de entorno INCLUDE. (La variable de entorno PATH no tiene ningún efecto en qué directorios busca RC).

## <a name="adding-a-directory-to-search"></a>Agregar un directorio a la búsqueda

Puede usar la opción **/i** para agregar un directorio a la lista de directorios rc busca. A continuación, el compilador busca en los directorios en el orden siguiente:

1.  El directorio actual
2.  Directorio o directorios que especifique mediante la **opción /i,** en el orden en que aparecen en la línea de comandos RC.
3.  Lista de directorios especificados por la variable de entorno INCLUDE, en el orden en que la variable los enumera, a menos que especifique la **opción /x.**

En el ejemplo siguiente se compila el archivo de definición de recursos MyApp.rc:

**rc /i c: \\ source \\ stuff /i d: \\ resources myapp.rc**

Al compilar el script MyApp.rc, RC busca primero los archivos de encabezado y los archivos de recursos en el directorio actual, luego en C: \\ Source Stuff y D: Resources y, a continuación, en los directorios especificados por la variable de entorno \\ \\ INCLUDE.

## <a name="ignoring-the-include-environment-variable"></a>Omitir la variable de entorno INCLUDE

Puede evitar que RC use la variable de entorno INCLUDE al determinar los directorios en los que se va a buscar. Para ello, use la **opción /x.** A continuación, el compilador busca archivos solo en el directorio actual y en los directorios que especifique mediante **la opción /i.**

El comando siguiente compila el archivo de script MyApp.rc:

**rc /x /i c: \\ source \\ stuff myapp.rc**

Al compilar el script MyApp.rc, RC busca primero los archivos de encabezado y los archivos de recursos en el directorio actual y, a continuación, en C: \\ Source \\ Stuff. No busca en los directorios especificados por la variable de entorno INCLUDE.

 

 




