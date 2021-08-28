---
title: " include (Directiva)"
description: Directiva de preprocesador que inserta el contenido del archivo especificado en el programa de origen en el punto donde aparece la directiva.
ms.assetid: 24796d89-5690-469b-950e-df56783aa05a
keywords:
- directiva include HLSL
topic_type:
- apiref
api_name:
- include Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 079ae2680a2610993c3cd54ac64afdfcbafa25c9
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627471"
---
# <a name="include-directive"></a>\#include (Directiva)

Directiva de preprocesador que inserta el contenido del archivo especificado en el programa de origen en el punto donde aparece la directiva.


| \#include "*filename*"       |
|------------------------------|
| \#include <*filename*> |

## <a name="parameters"></a>Parámetros

| Elemento | Descripción |
|------|-------------|
| *filename* | Nombre de archivo del archivo que se incluirá, precedido opcionalmente por una especificación de directorio. El nombre de archivo debe especificar un archivo existente. |

## <a name="remarks"></a>Comentarios

La directiva include provoca el reemplazo de la directiva por todo el \# contenido del archivo especificado. El preprocesador deja de buscar en cuanto encuentra un archivo con el nombre especificado; Si especifica una especificación de ruta de acceso completa e inequívoca para el archivo, el preprocesador busca solo la ruta de acceso especificada.

> [!NOTE]
> La [herramienta Effect-Compiler tiene](/windows/desktop/direct3dtools/fxc) un controlador de incluir integrado mediante el modificador /I. Sin embargo, al ejecutar el compilador desde la API, puede proporcionar un controlador de include personalizado implementando la interfaz ID3DXInclude.

La diferencia entre los dos formularios de sintaxis es el orden en el que el preprocesador busca archivos de encabezado cuando la ruta de acceso está incompleta, como se muestra en la tabla siguiente.

<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Forma de sintaxis</th>
<th>Patrón de búsqueda de preprocesador</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>#incluir nombre <b>&quot;</b> <em>de archivo</em><b>&quot;</b></td>
<td>Busca el archivo include:
<ol>
<li>en el mismo directorio que el archivo que contiene la #include directiva.</li>
<li>en los directorios de los archivos que contienen una #include directiva para el archivo que contiene la #include directiva.</li>
<li>en las rutas de acceso especificadas por la opción del compilador /I, en el orden en que se enumeran.</li>
<li><p>en las rutas de acceso especificadas por la variable de entorno INCLUDE, en el orden en que se enumeran.</p>
<blockquote>
[!NOTE]<br />
La variable de entorno INCLUDE se omite en un entorno de desarrollo. Consulte la documentación del entorno de desarrollo para obtener información sobre cómo establecer las rutas de acceso de include para el proyecto.
</blockquote>
<p><br/></p></li>
</ol></td>
</tr>
<tr class="even">
<td>#incluir nombre <b><</b> <em>de archivo</em><b>></b></td>
<td>Busca el archivo include:
<ol>
<li>en las rutas de acceso especificadas por la opción del compilador /I, en el orden en que se enumeran.</li>
<li><p>en las rutas de acceso especificadas por la variable de entorno INCLUDE, en el orden en que se enumeran.</p>
<blockquote>
[!NOTE]<br />
La variable de entorno INCLUDE se omite en un entorno de desarrollo. Consulte la documentación del entorno de desarrollo para obtener información sobre cómo establecer las rutas de acceso de include para el proyecto.
</blockquote>
<p><br/></p></li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente, el preprocesador reemplaza la \# directiva include por el contenido de stdio.h. Dado que en el ejemplo se usa el formato de corchete angular, el preprocesador buscará el archivo solo en los directorios enumerados por la opción del compilador /I y la variable de entorno INCLUDE.

```cpp
#include <stdio.h>
```

## <a name="see-also"></a>Vea también

- [Directivas de preprocesador (HLSL de DirectX)](dx-graphics-hlsl-appendix-preprocessor.md)

- [Interfaz ID3D10Include](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))

- [Herramienta Effect-Compiler](/windows/desktop/direct3dtools/fxc)
