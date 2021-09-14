---
title: " include"
description: La directiva \ include hace que el compilador de recursos procese el archivo especificado en el parámetro filename.
ms.assetid: 9a3505c6-c19f-4c4f-85a4-94fbcfc0f9c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8d36f1d0ae24f3dc21d67eec57056872aabdbd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127252446"
---
# <a name="-include"></a>'include'

La **\# directiva include** hace que el compilador de recursos procese el archivo especificado en el parámetro *filename.* Este archivo debe ser un archivo de encabezado que defina las constantes usadas en el archivo de definición de recursos. El archivo puede usar caracteres Unicode, de un solo byte o de doble byte.

``` syntax
#include filename
```

<dl> <dt>

<span id="filename"></span><span id="FILENAME"></span>*Nombre*
</dt> <dd>

Nombre del archivo que se va a incluir. Si el archivo está en el directorio actual, la cadena debe incluirse entre comillas dobles; Si el archivo está en el directorio especificado por la variable de entorno INCLUDE, la cadena debe incluirse entre caracteres menores y mayores que (<>). Debe proporcionar una ruta de acceso completa entre comillas dobles (") si el archivo no está en el directorio actual o en el directorio especificado por la variable de entorno INCLUDE.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Use la siguiente instrucción en el archivo de encabezado para rodear instrucciones que un compilador de C puede compilar, pero no RC:

``` syntax
#ifndef RC_INVOKED
```

De este modo, puede usar los mismos archivos de include en los archivos .c y .rc.

## <a name="example"></a>Ejemplo

Este ejemplo procesa los archivos de encabezado Windows.h y MyDefs.h al compilar el archivo de definición de recursos:

``` syntax
#include <windows.h>
#include "headers\mydefs.h"
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Directivas de preprocesador](preprocessor-directives.md)
</dt> </dl>

 

 




