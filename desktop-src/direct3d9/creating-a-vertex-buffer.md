---
description: 'Cree un objeto de búfer de vértices llamando al método IDirect3DDevice9:: CreateVertexBuffer, que acepta cinco parámetros.'
ms.assetid: 95116ef5-af88-47e7-abf7-1ade9735e2a7
title: Crear un búfer de vértices (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ffc831ab508f14d61b8e42861f75422ff6a04bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714877"
---
# <a name="creating-a-vertex-buffer-direct3d-9"></a>Crear un búfer de vértices (Direct3D 9)

Cree un objeto de búfer de vértices llamando al método [**IDirect3DDevice9:: CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) , que acepta cinco parámetros. El primer parámetro especifica la longitud del búfer de vértices, en bytes. Use el operador sizeof para determinar el tamaño de un formato de vértice, en bytes. Tenga en cuenta el siguiente formato de vértice personalizado.


```
struct CUSTOMVERTEX {
        FLOAT x, y, z;
        FLOAT rhw;
        DWORD color;
        FLOAT tu, tv;   // Texture coordinates
};

// Custom flexible vertex format (FVF) describing the custom vertex structure
#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZRHW | D3DFVF_DIFFUSE | D3DFVF_TEX1)
```



Para crear un búfer de vértices que contenga cuatro estructuras CUSTOMVERTEX, especifique \[ 4 \* SIZEOF (CUSTOMVERTEX) \] para el parámetro de *longitud* .

El segundo parámetro es un conjunto de controles de uso. Entre otras cosas, su valor determina si el búfer de vértices es capaz de contener información de recorte, en forma de marcas de recorte, para los vértices que existen fuera del área de visualización. Para crear un búfer de vértices que no puede contener marcas de recorte, incluya la \_ marca D3DUSAGE DONOTCLIP para el parámetro *Usage* . La \_ marca D3DUSAGE DONOTCLIP solo se aplica si también indica que el búfer de vértice contendrá vértices transformados \_ . la marca D3DFVF XYZRHW se incluye en el parámetro *FVF* . El método [**IDirect3DDevice9:: CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) omite la marca D3DUSAGE \_ DONOTCLIP si indica que el búfer contendrá vértices sin transformar (la marca de D3DFVF \_ XYZ). Las marcas de recorte ocupan memoria adicional, lo que permite que un búfer de vértice compatible con el recorte sea ligeramente mayor que un búfer de vértices que no puede contener marcas de recorte. Dado que estos recursos se asignan al crear el búfer de vértices, debe solicitar un búfer de vértice compatible con el recorte con anterioridad.

El tercer parámetro, *FVF*, es una combinación de [D3DFVF](d3dfvf.md) que describe el formato de vértices del búfer de vértices. Si especifica 0 para este parámetro, el búfer de vértices es un búfer de vértices que no es FVF. Para obtener más información, vea [búferes de vértices de FVF (Direct3D 9)](fvf-vertex-buffers.md). El cuarto parámetro describe la clase de memoria en la que se coloca el búfer de vértices.

El último parámetro que [**IDirect3DDevice9:: CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) acepta es la dirección de una variable que se rellenará con un puntero a la nueva interfaz [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) del objeto de búfer de vértices si la llamada se realiza correctamente.

No se pueden generar marcas de recorte para un búfer de vértice creado sin su compatibilidad.

En el ejemplo de código de C++ siguiente se muestra cómo la creación de un búfer de vértices podría ser similar en el código.


```
   
// d3dDevice contains the address of an IDirect3DDevice9 interface
// g_pVB is a variable of type LPDIRECT3DVERTEXBUFFER9 

// The custom vertex type
struct CUSTOMVERTEX {
    FLOAT x, y, z;
    FLOAT rhw;
    DWORD color;
    FLOAT tu, tv;   // The texture coordinates
};

#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZRHW | D3DFVF_DIFFUSE | D3DFVF_TEX1)

// Create a clipping-capable vertex buffer. Allocate enough memory 
// in the default memory pool to hold three CUSTOMVERTEX 
// structures

    if( FAILED( d3dDevice->CreateVertexBuffer( 3*sizeof(CUSTOMVERTEX),
            0 /*Usage*/, D3DFVF_CUSTOMVERTEX, D3DPOOL_DEFAULT, &g_pVB, NULL ) ) )
        return E_FAIL;
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búferes de vértices](vertex-buffers.md)
</dt> </dl>

 

 
