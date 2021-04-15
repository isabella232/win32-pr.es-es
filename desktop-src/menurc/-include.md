---
title: " include"
description: La Directiva \ include hace que el compilador de recursos procese el archivo especificado en el parámetro FILENAME.
ms.assetid: 9a3505c6-c19f-4c4f-85a4-94fbcfc0f9c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8d36f1d0ae24f3dc21d67eec57056872aabdbd
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421867"
---
# <a name="-include"></a>inclui

La directiva **\# include** hace que el compilador de recursos procese el archivo especificado en el parámetro *filename* . Este archivo debe ser un archivo de encabezado que defina las constantes que se usan en el archivo de definición de recursos. El archivo puede utilizar caracteres de un solo byte, de doble byte o Unicode.

``` syntax
#include filename
```

<dl> <dt>

<span id="filename"></span><span id="FILENAME"></span>*extensión*
</dt> <dd>

Nombre del archivo que se va a incluir. Si el archivo está en el directorio actual, la cadena debe ir entre comillas dobles. Si el archivo se encuentra en el directorio especificado por la variable de entorno INCLUDE, la cadena se debe incluir entre caracteres de menor que y mayor que (<>). Debe proporcionar una ruta de acceso completa entre comillas dobles (") si el archivo no está en el directorio actual o en el directorio especificado por la variable de entorno INCLUDE.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Use la siguiente instrucción en el archivo de encabezado para envolver las instrucciones que puede compilar un compilador de C pero no RC:

``` syntax
#ifndef RC_INVOKED
```

De este modo, puede usar los mismos archivos de inclusión en los archivos. c y. rc.

## <a name="example"></a>Ejemplo

En este ejemplo se procesan los archivos de encabezado Windows. h y MyDefs. h mientras se compila el archivo de definición de recursos:

``` syntax
#include <windows.h>
#include "headers\mydefs.h"
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Directivas de preprocesador](preprocessor-directives.md)
</dt> </dl>

 

 




