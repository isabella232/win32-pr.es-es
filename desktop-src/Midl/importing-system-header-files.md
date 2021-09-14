---
title: Importación de archivos de encabezado del sistema
description: Aunque a menudo es posible usar la directiva \ include para incluir archivos de encabezado en el archivo IDL, no se recomienda.
ms.assetid: ff524965-424d-416d-97cd-c2780ebf69ef
keywords:
- importar MIDL, archivos de encabezado del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c26df7ca983fa21ae8e604446f0221c302c73099
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159537"
---
# <a name="importing-system-header-files"></a>Importación de archivos de encabezado del sistema

Aunque a menudo es posible usar la directiva **\# include** para incluir archivos de encabezado en el archivo IDL, no se recomienda. El compilador midl generará códigos auxiliares para todas las funciones definidas en el archivo IDL que se está compilando. Normalmente, un archivo de encabezado contiene una serie de prototipos que no necesita ni desea incluir en los archivos de código auxiliar, y un archivo **\# include** coloca eficazmente todas esas definiciones en el archivo IDL principal. Además, si hay tipos no actualizables definidos en el archivo de encabezado, es posible que el archivo IDL no se compile.

Hay dos maneras de incluir definiciones de tipos de archivos de encabezado en un archivo IDL:

-   Use la [**directiva import**](import.md) para incluir los tipos de datos definidos en un archivo de encabezado. A diferencia de la directiva **\# include** del lenguaje C, la **directiva import** solo recoge definiciones de tipo y constantes y omite los prototipos de procedimiento. Este enfoque funcionará siempre que el archivo IDL principal no haga referencia a ningún tipo no actualizable definido en el archivo de encabezado.
-   Cree un archivo IDL auxiliar con una interfaz ficticia que incluya los archivos de encabezado. A continuación, use [**la directiva import**](import.md) para incluir el archivo auxiliar. De este modo, solo [**aparecerán las definiciones**](typedef.md)de tipo en los códigos auxiliares compilados. Por ejemplo:

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
