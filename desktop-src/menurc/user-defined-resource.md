---
title: User-Defined resource
description: Una instrucción de definición de recursos definida por el usuario define un recurso que contiene datos específicos de la aplicación.
ms.assetid: b1cfec71-5733-4900-97f6-c1cbb350c728
keywords:
- recurso definido por el usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b383b7c4d1f9acfc4ce6c9db24efa77f3bfed943c1f299186d42a1facee2b43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118472623"
---
# <a name="user-defined-resource"></a>User-Defined resource

Una instrucción de definición de recursos definida por el usuario define un recurso que contiene datos específicos de la aplicación. Los datos pueden tener cualquier formato y se pueden definir como el contenido de un archivo determinado (si se  especifica el parámetro *filename)* o como una serie de números y cadenas (si se especifica el bloque de datos sin formato).

``` syntax
nameID typeID filename
```

El *nombre* de archivo especifica el nombre de un archivo que contiene los datos binarios del recurso. El contenido del archivo se incluye como recurso. RC no interpreta los datos binarios de ninguna manera. Es responsabilidad del programador asegurarse de que los datos se alinean correctamente para la arquitectura del equipo de destino.

Un recurso definido por el usuario también se puede definir completamente en el script de recursos mediante la sintaxis siguiente:

``` syntax
nameID typeID  {  raw-data  }
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Nombre único o entero de 16 bits sin signo que identifica el recurso.

</dd> <dt>

<span id="typeID"></span><span id="typeid"></span><span id="TYPEID"></span>*typeID*
</dt> <dd>

Nombre único o entero de 16 bits sin signo que identifica el tipo de recurso. Si se da un número, debe ser mayor que 255. Los números del 1 al 255 están reservados para los tipos de recursos redefinidos existentes y futuros.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*Nombre*
</dt> <dd>

Nombre del archivo que contiene los datos del recurso. El parámetro debe ser un nombre de archivo válido; debe ser una ruta de acceso completa si el archivo no está en el directorio de trabajo actual.

</dd> <dt>

<span id="raw-data"></span><span id="RAW-DATA"></span>*datos sin procesar*
</dt> <dd>

Datos sin procesar que constan de uno o varios enteros o cadenas de caracteres. Los enteros se pueden especificar en formato decimal, octal o hexadecimal. Para que sean compatibles con los valores de 16 Windows bits, los enteros se almacenan como valores WORD. Puede almacenar un entero como un valor DWORD si califica el entero con el sufijo "L".

Las cadenas se incluyen entre comillas. RC no anexa automáticamente un carácter nulo de terminación a una cadena. Cada cadena es una secuencia de los caracteres ANSI especificados, a menos que la califique como una cadena de caracteres anchos con el prefijo "L".

El bloque de datos comienza en un **límite DWORD** y RC no realiza ningún relleno ni alineación de los datos dentro del *bloque de datos sin* procesar. Es responsabilidad del programador garantizar la alineación adecuada de los datos dentro del bloque.

</dd> </dl>

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestran varias instrucciones definidas por el usuario:

``` syntax
array   MYRES   data.res
14      300     custom.res
18 MYRES2
{
   "Here is an ANSI string\0",    // explicitly null-terminated 
   L"Here is a Unicode string\0", // explicitly null-terminated 
   1024,                          // integer, stored as WORD 
   7L,                            // integer, stored as DWORD 
   0x029a,                        // hex integer 
   0o733,                         // octal integer 
}
```

 

 




