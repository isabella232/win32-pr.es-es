---
title: Importación de archivos de encabezado del sistema
description: Aunque a menudo es posible usar la Directiva \ include para incluir archivos de encabezado en el archivo IDL, no se recomienda.
ms.assetid: ff524965-424d-416d-97cd-c2780ebf69ef
keywords:
- importar MIDL, archivos de encabezado del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c26df7ca983fa21ae8e604446f0221c302c73099
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103820474"
---
# <a name="importing-system-header-files"></a>Importación de archivos de encabezado del sistema

Aunque a menudo es posible usar la directiva **\# include** para incluir archivos de encabezado en el archivo IDL, no se recomienda. El compilador MIDL generará códigos auxiliares para todas las funciones definidas en el archivo IDL que se está compilando. Normalmente, un archivo de encabezado contiene una serie de prototipos que no necesita ni quiere incluir en los archivos de código auxiliar, y un **\# incluye** de forma eficaz todas esas definiciones en el archivo IDL principal. Además, si hay tipos no utilizables definidos en el archivo de encabezado, es posible que el archivo IDL no se compile.

Hay dos formas de incluir definiciones de tipos de archivos de encabezado en un archivo IDL:

-   Use la Directiva de [**importación**](import.md) para incluir tipos de datos definidos en un archivo de encabezado. A diferencia de la directiva **\# include** del lenguaje C, la directiva **Import** solo selecciona las definiciones de tipo y constante y omite los prototipos de procedimiento. Este enfoque funcionará siempre que el archivo IDL principal no haga referencia a ningún tipo de no utilizables definido en el archivo de encabezado.
-   Cree un archivo IDL auxiliar con una interfaz ficticia que incluya los archivos de encabezado. A continuación, use la Directiva de [**importación**](import.md) para incluir el archivo auxiliar. De este modo, solo los [**typedef**](typedef.md)aparecerán en el código auxiliar compilado. Por ejemplo:

```syntax
//in helper.idl:
interface dummy
{ 
   #include "kitchensink.h"
   #include "system.h"
}

//in main.idl:
import "helper.idl";
```
