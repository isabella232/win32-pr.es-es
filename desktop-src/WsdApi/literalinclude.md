---
description: Coloca una instrucción include de C o IDL en el código generado.
ms.assetid: 7a7ffd54-09e9-412d-a637-5dc27597b46e
title: literalInclude, elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcfbd72300607dd2c6f3f21e4be3666083b559cb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473282"
---
# <a name="literalinclude-element"></a>literalInclude, elemento

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
<col  />
<col  />
<col  />
<col  />
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
<dt><strong>C</strong></dt> <dd> Incluya un archivo de encabezado de C.<br/> </dd> <dt><strong>IDL</strong></dt> <dd> Incluya un archivo IDL.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Local</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>Este atributo solo se usa cuando <strong>Language</strong> se establece en &quot; &quot; C.<br/> <br/>
<dt><strong>Verdad</strong></dt> <dd> Busca en el directorio actual el encabezado con nombre antes de buscar en los directorios del sistema.<br/> </dd> <dt><strong>Falso</strong></dt> <dd> Busque solo los directorios del sistema para el encabezado con nombre.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos secundarios

No hay elementos secundarios.

## <a name="parent-elements"></a>Elementos primarios



| Elemento                         | Descripción                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**Archivo**](file.md)<br/> | Genera un archivo desde el generador de código.<br/> <br/> |



## <a name="remarks"></a>Observaciones

En los ejemplos siguientes se muestra el código generado a partir de diferentes **elementos literalesInclude.**

### <a name="example-1---generating-a-c-include-statement"></a>Ejemplo 1: Generación de una instrucción include de C

XML de entrada:

``` syntax
<literalInclude Language="C" Local="False">wsdapi.h</literalInclude>
```

Código de salida:

``` syntax
#include <wsdapi.h>
```

### <a name="example-2---generating-a-c-include-statement"></a>Ejemplo 2: Generación de una instrucción include de C

XML de entrada:

``` syntax
<literalInclude Language="C" Local="True">wsdapi.h</literalInclude>
```

Código de salida:

``` syntax
#include "wsdapi.h"
```

### <a name="example-3---generating-an-idl-import-statement"></a>Ejemplo 3: Generación de una instrucción de importación de IDL

XML de entrada:

``` syntax
<literalInclude Language="IDL">wsdclient.idl</literalInclude>
```

Código de salida:

``` syntax
import wsdclient.idl;
```

## <a name="element-information"></a>Información de elemento



| Etiqueta | Value |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




