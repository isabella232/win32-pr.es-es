---
description: Coloca una instrucción include de C o IDL en el código generado.
ms.assetid: 7a7ffd54-09e9-412d-a637-5dc27597b46e
title: elemento literalInclude
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2701b2b21d14b629d5d9b61dcbc73e11371f54e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706455"
---
# <a name="literalinclude-element"></a>elemento literalInclude

Coloca una instrucción include de C o IDL en el código generado.

## <a name="usage"></a>Uso

``` syntax
<literalInclude
  Language = "language string"
  Local = "Boolean"/>
```

## <a name="attributes"></a>Atributos



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Tipo</th>
<th>Obligatorio</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Lenguaje</strong><br/></td>
<td>cadena de idioma<br/></td>
<td>No<br/></td>
<td>Tipo de archivo de encabezado que se va a incluir. <br/> <br/>
<dt><strong>Unidad</strong></dt> <dd> Incluya un archivo de encabezado de C.<br/> </dd> <dt><strong>IDL</strong></dt> <dd> Incluya un archivo IDL.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Local</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>Este atributo solo se utiliza cuando el <strong>idioma</strong> está establecido en &quot; C &quot; .<br/> <br/>
<dt><strong>Reales</strong></dt> <dd> Busca el encabezado con nombre en el directorio actual antes de buscar en los directorios del sistema.<br/> </dd> <dt><strong>Es</strong></dt> <dd> Solo busca en los directorios de sistema del encabezado con nombre.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos secundarios

No hay elementos secundarios.

## <a name="parent-elements"></a>Elementos primarios



| Elemento                         | Descripción                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**archivo**](file.md)<br/> | Genera un archivo desde el generador de código.<br/> <br/> |



## <a name="remarks"></a>Observaciones

En los siguientes ejemplos se muestra el código generado a partir de distintos elementos **literalInclude** .

### <a name="example-1---generating-a-c-include-statement"></a>Ejemplo 1: generar una instrucción include de C

XML de entrada:

``` syntax
<literalInclude Language="C" Local="False">wsdapi.h</literalInclude>
```

Código de salida:

``` syntax
#include <wsdapi.h>
```

### <a name="example-2---generating-a-c-include-statement"></a>Ejemplo 2: generar una instrucción include de C

XML de entrada:

``` syntax
<literalInclude Language="C" Local="True">wsdapi.h</literalInclude>
```

Código de salida:

``` syntax
#include "wsdapi.h"
```

### <a name="example-3---generating-an-idl-import-statement"></a>Ejemplo 3: generación de una instrucción de importación IDL

XML de entrada:

``` syntax
<literalInclude Language="IDL">wsdclient.idl</literalInclude>
```

Código de salida:

``` syntax
import wsdclient.idl;
```

## <a name="element-information"></a>Información de elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




