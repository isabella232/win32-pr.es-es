---
title: " include (Directiva)"
description: Directiva de preprocesador que inserta el contenido del archivo especificado en el programa de origen en el punto donde aparece la Directiva.
ms.assetid: 24796d89-5690-469b-950e-df56783aa05a
keywords:
- incluir la Directiva HLSL
topic_type:
- apiref
api_name:
- include Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a844459234200ca99233eb3f64a2a1c30449cdcc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997085"
---
# <a name="include-directive"></a>\#include (Directiva)

Directiva de preprocesador que inserta el contenido del archivo especificado en el programa de origen en el punto donde aparece la Directiva.


| \#incluir "*filename*"       |
|------------------------------|
| \#incluir <*nombre de archivo*> |

## <a name="parameters"></a>Parámetros

| Elemento | Descripción |
|------|-------------|
| *filename* | Nombre del archivo que se va a incluir, opcionalmente precedido por una especificación de directorio. El nombre de archivo debe especificar un archivo existente. |

## <a name="remarks"></a>Observaciones

La \# directiva Include provoca el reemplazo de la Directiva por todo el contenido del archivo especificado. El preprocesador detiene la búsqueda en cuanto encuentra un archivo con el nombre especificado; Si especifica una especificación de ruta de acceso completa y no ambigua para el archivo, el preprocesador busca solo la ruta de acceso especificada.

> [!NOTE]
> La [herramienta de compilador de efecto](/windows/desktop/direct3dtools/fxc) tiene un controlador de inclusión integrado mediante el modificador/i. Sin embargo, al ejecutar el compilador desde la API, puede proporcionar un controlador de inclusión personalizado implementando la interfaz ID3DXInclude.

La diferencia entre las dos formas de sintaxis es el orden en el que el preprocesador busca los archivos de encabezado cuando la ruta de acceso se especifica incompletamente, como se muestra en la tabla siguiente.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Forma de sintaxis</th>
<th>Patrón de búsqueda del preprocesador</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>#incluir <b>&quot;</b> <em>nombre de archivo</em><b>&quot;</b></td>
<td>Busca el archivo de inclusión:
<ol>
<li>en el mismo directorio que el archivo que contiene la Directiva #include.</li>
<li>en los directorios de los archivos que contienen una directiva #include para el archivo que contiene la Directiva #include.</li>
<li>en las rutas de acceso especificadas por la opción del compilador/I, en el orden en que aparecen.</li>
<li><p>en las rutas de acceso especificadas por la variable de entorno INCLUDE, en el orden en que aparecen en la lista.</p>
<blockquote>
[!NOTE]<br />
La variable de entorno INCLUDE se omite en un entorno de desarrollo. Consulte la documentación del entorno de desarrollo para obtener información sobre cómo establecer las rutas de acceso de inclusión para el proyecto.
</blockquote>
<p><br/></p></li>
</ol></td>
</tr>
<tr class="even">
<td>#incluir <b><</b> <em>nombre de archivo</em><b>></b></td>
<td>Busca el archivo de inclusión:
<ol>
<li>en las rutas de acceso especificadas por la opción del compilador/I, en el orden en que aparecen.</li>
<li><p>en las rutas de acceso especificadas por la variable de entorno INCLUDE, en el orden en que aparecen en la lista.</p>
<blockquote>
[!NOTE]<br />
La variable de entorno INCLUDE se omite en un entorno de desarrollo. Consulte la documentación del entorno de desarrollo para obtener información sobre cómo establecer las rutas de acceso de inclusión para el proyecto.
</blockquote>
<p><br/></p></li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se hace que el preprocesador Reemplace la \# directiva Include por el contenido de stdio. h. Dado que en el ejemplo se usa el formato de corchete angular, el preprocesador buscará el archivo solo en los directorios enumerados por la opción del compilador/I y la variable de entorno INCLUDE.

```cpp
#include <stdio.h>
```

## <a name="see-also"></a>Vea también

- [Directivas de preprocesador (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)

- [Interfaz ID3D10Include](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))

- [Efecto: herramienta de compilador](/windows/desktop/direct3dtools/fxc)