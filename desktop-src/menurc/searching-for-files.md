---
title: Buscar archivos
description: De forma predeterminada, RC busca en primer lugar los archivos de encabezado y los archivos de recursos (como los archivos de icono y de cursor) en el directorio actual y, después, en los directorios especificados por la variable de entorno INCLUDE.
ms.assetid: 6c8c905d-b0f6-4665-9a93-62617ff30137
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 078a04a4cf2f3461d03c7026e0f1d73d8fd38665
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704737"
---
# <a name="searching-for-files"></a>Buscar archivos

De forma predeterminada, RC busca en primer lugar los archivos de encabezado y los archivos de recursos (como los archivos de icono y de cursor) en el directorio actual y, después, en los directorios especificados por la variable de entorno INCLUDE. (La variable de entorno PATH no tiene ningún efecto en qué directorios busca en RC).

## <a name="adding-a-directory-to-search"></a>Agregar un directorio para buscar

Puede usar la opción **/i** para agregar un directorio a la lista de directorios de búsquedas RC. Después, el compilador busca en los directorios en el siguiente orden:

1.  Directorio actual
2.  Directorio o directorios que se especifican mediante la opción **/i** , en el orden en que aparecen en la línea de comandos de RC
3.  La lista de directorios especificados por la variable de entorno INCLUDE, en el orden en que la variable los muestra, a menos que especifique la opción **/x**

En el ejemplo siguiente se compila el archivo de definición de recursos MyApp. RC:

**rc/i c: \\ contenido de origen \\ /i d: \\ Resources MyApp. RC**

Al compilar el script MyApp. rc, RC busca primero los archivos de encabezado y los archivos de recursos en el directorio actual, en C: \\ source \\ Materials and D: \\ Resources y, a continuación, en los directorios especificados por la variable de entorno include.

## <a name="ignoring-the-include-environment-variable"></a>Omitir la variable de entorno INCLUDE

Puede evitar que RC use la variable de entorno INCLUDE al determinar los directorios en los que buscar. Para ello, use la opción **/x** . A continuación, el compilador busca los archivos solo en el directorio actual y en los directorios especificados mediante la opción **/i** .

El siguiente comando compila el archivo de script MyApp. RC:

**RC/x/i c: \\ código fuente \\ MyApp. RC**

Al compilar el script MyApp. rc, RC busca primero los archivos de encabezado y los archivos de recursos en el directorio actual y, después, en C: \\ source \\ materials. No busca en los directorios especificados por la variable de entorno INCLUDE.

 

 




