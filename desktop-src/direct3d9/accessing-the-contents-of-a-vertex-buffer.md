---
description: Los objetos de búfer de vértices permiten a las aplicaciones acceder directamente a la memoria asignada para los datos de vértices.
ms.assetid: 63d255b7-fa7d-411b-9cdb-52113f30c933
title: Acceso al contenido de un búfer de vértices (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1b5e4a4986e064d3736f83567f5dd6d479d0dbc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072837"
---
# <a name="accessing-the-contents-of-a-vertex-buffer-direct3d-9"></a>Acceso al contenido de un búfer de vértices (Direct3D 9)

Los objetos de búfer de vértices permiten a las aplicaciones acceder directamente a la memoria asignada para los datos de vértices. Puede recuperar un puntero a la memoria del búfer de vértices llamando al método [**IDirect3DVertexBuffer9::Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock) y, a continuación, accediendo a la memoria según sea necesario para rellenar el búfer con nuevos datos de vértices o para leer los datos que ya contiene. El **método IDirect3DVertexBuffer9::Lock** acepta cuatro parámetros. El primero, *OffsetToLock*, es el desplazamiento en los datos del vértice. El segundo parámetro es el tamaño, medido en bytes, de los datos del vértice. El tercer parámetro aceptado es la dirección de un puntero que apunta a los datos del vértice, si la llamada se realiza correctamente.

El último parámetro, *Flags*, indica al sistema cómo se debe bloquear la memoria. Especifique constantes para el *parámetro Flags según* la forma en que se accederá a los datos del vértice. Asegúrese de que el valor elegido para [**D3DUSAGE**](d3dusage.md) coincide con el valor elegido para [D3DLOCK](d3dlock.md). Por ejemplo, si va a crear un búfer de vértices solo con acceso de escritura, no tiene sentido intentar leer los datos especificando D3DLOCK \_ READONLY. El uso inteligente de estas marcas permite al controlador bloquear la memoria y proporcionar el mejor rendimiento, dado el tipo de acceso solicitado.

Cuando termine de rellenar o leer los datos del vértice, llame al método [**IDirect3DVertexBuffer9::Unlock,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-unlock) como se muestra en el ejemplo de código siguiente.


```
// This code example assumes the g_pVB is a variable of type 
//   LPDIRECT3DVERTEXBUFFER9 and that g_Vertices has been  
//   properly initialized with vertices

// Lock the buffer to gain access to the vertices 
VOID* pVertices;

if(FAILED(g_pVB->Lock(0, sizeof(g_Vertices), 
        (BYTE**)&pVertices, 0 ) ) ) 
    return E_FAIL;

memcpy(pVertices, g_Vertices, sizeof(g_Vertices));
g_pVB->Unlock();
```



Si crea un búfer de vértices con la marca WRITEONLY D3DUSAGE, no use la marca de bloqueo \_ D3DLOCK \_ READONLY. Use la marca D3DLOCK READONLY si la aplicación \_ solo leerá desde la memoria del búfer de vértices. La inclusión de esta marca permite a Direct3D optimizar sus procedimientos internos para mejorar la eficacia, dado que el acceso a la memoria será de solo lectura.

Vea Using [Dynamic Vertex and Index Buffers](performance-optimizations.md) (Uso de búferes dinámicos de vértices e índices) para obtener información sobre el uso de D3DLOCK DISCARD o \_ D3DLOCK NOOVERWRITE para el parámetro Flags de \_ [**IDirect3DVertexBuffer9::Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock).

En C++, dado que accede directamente a la memoria asignada para el búfer de vértices, asegúrese de que la aplicación tiene acceso correctamente a la memoria asignada. De lo contrario, corre el riesgo de representar esa memoria como no válida. Use el paso del formato de vértice que usa la aplicación para pasar de un vértice del búfer asignado a otro. La memoria del búfer de vértices es una matriz simple de vértices especificados en FVF. Use el paso de cualquier estructura de formato de vértice que defina. Puede calcular el paso de cada vértice en tiempo de ejecución examinando la [D3DFVF](d3dfvf.md) contenida en la descripción del búfer de vértices. En la tabla siguiente se muestra el tamaño de cada componente de vértice.



| Marca de formato de vértice | Size              |
|--------------------|-------------------|
| D3DFVF \_ DIFUSO    | sizeof(DWORD)     |
| D3DFVF \_ NORMAL     | sizeof(float) x 3 |
| D3DFVF \_ SPECULAR   | sizeof(DWORD)     |
| D3DFVF \_ TEXn       | sizeof(float) x n |
| D3DFVF \_ XYZ        | sizeof(float) x 3 |
| D3DFVF \_ XYZRHW     | sizeof(float) x 4 |



 

El número de coordenadas de textura presentes en el formato de vértice se describe mediante las marcas n de D3DFVF TEXAS (donde n es un valor de \_ 0 a 8). Multiplique el número de conjuntos de coordenadas de textura por el tamaño de un conjunto de coordenadas de textura, que puede oscilar entre uno y cuatro flotantes, para calcular la memoria necesaria para ese número de coordenadas de textura.

Use el intervalo de vértice total para incrementar y disminuir el puntero de memoria según sea necesario para acceder a vértices concretos.

## <a name="retrieving-vertex-buffer-descriptions"></a>Recuperar descripciones del búfer de vértices

Puede recuperar información sobre un búfer de vértices llamando al [**método IDirect3DVertexBuffer9::GetDesc.**](/windows/desktop/api) Este método rellena los miembros de la estructura [**D3DVERTEXBUFFER \_ DESC**](d3dvertexbuffer-desc.md) con información sobre el búfer de vértices.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búferes de vértices](vertex-buffers.md)
</dt> </dl>

 

 
