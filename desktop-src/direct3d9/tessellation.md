---
description: Teselación (Direct3D 9)
ms.assetid: ae39b0e1-d2ae-449e-89db-0a2b24171531
title: Teselación (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82378caac1218158ffc1834c9a9b56fb8cbd250e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127358879"
---
# <a name="tessellation-direct3d-9"></a>Teselación (Direct3D 9)

## <a name="tessellator-unit"></a>Unidad de teselador

Se ha mejorado la unidad de teselador. Ahora puede usarlo para:

-   Realice la teselación adaptable de todas las primitivas de orden superior.
-   Busque los valores de desplazamiento por vértice de un mapa de desplazamiento y pásenlos a un sombreador de vértices.
-   Admite la teselación de revisión de rectángulos. Esto se especifica mediante una declaración de vértice mediante D3DDECLMETHOD \_ PARTIALU o D3DDECLMETHOD \_ PARTIALV. Si se usa una declaración de vértice que contiene estos métodos para dibujar una revisión de triángulo, se producirá un error [**en IDirect3DDevice9::D rawTriPatch.**](/windows/desktop/api) Para obtener más información sobre las declaraciones de vértices, [**vea D3DVERTEXELEMENT9**](d3dvertexelement9.md).

En DirectX 8.x, lo que se llamaba ORDER era realmente el grado. En Direct3D 9, [**D3DDEGREETYPE**](./d3ddegreetype.md)especifica ahora el grado.


```
 // This used to be D3DORDERTYPE and D3DORDER* 
 typedef enum _D3DDEGREETYPE 
 { 
 D3DDEGREE_LINEAR = 1, 
 D3DDEGREE_QUADRATIC = 2, 
 D3DDEGREE_CUBIC = 3, 
 D3DDEGREE_QUINTIC = 5, 
 D3DDEGREE_FORCE_DWORD = 0x7fffffff, 
 } D3DDEGREETYPE; 
```



El cambio en el tipo de grado afectó a otras dos estructuras.


```
typedef struct _D3DRECTPATCH_INFO 
 { 
 UINT StartVertexOffsetWidth; 
 UINT StartVertexOffsetHeight; 
 UINT Width; 
 UINT Height; 
 UINT Stride; 
 D3DBASISTYPE Basis; 
 D3DDEGREETYPE Degree; 
 } D3DRECTPATCH_INFO; 
```




```
 typedef struct _D3DTRIPATCH_INFO 
 { 
 UINT StartVertexOffset; 
 UINT NumVertices; 
 D3DBASISTYPE Basis; 
 D3DDEGREETYPE Degree; 
 } D3DTRIPATCH_INFO; 
```



Los controladores deben corregir los errores de compilación que se producen a partir de este cambio cuando se compilan con los nuevos encabezados. No es necesaria ninguna funcionalidad.

## <a name="adaptive-tessellation"></a>Teselación adaptable

La teselación adaptable se puede aplicar a primitivas de orden alto, incluidas N revisiones, revisiones de rectángulo y revisiones de triángulo. Esta característica está habilitada por D3DRS ENABLEADAPTIVETESSELLATION y presenta una revisión de forma adaptable, en función del valor de profundidad del vértice de control en el espacio de los \_ ojos.

Las coordenadas z (Zi) de los vértices de control (Vi), que se transforman en espacio de los ojos (Zieye) mediante la realización de un producto de puntos con un vector 4, se usan como valores de profundidad. La aplicación especifica el vector 4D (Mdm) mediante cuatro estados de representación \_ (D3DRS ADAPTIVETESS \_ X, D3DRS \_ ADAPTIVETESS \_ Y, D3DRS \_ ADAPTIVETESS \_ Z y D3DRS \_ ADAPTIVETESS \_ W). Este vector 4 podría ser la tercera columna del mundo concatenado y ver matrices. También se puede usar para aplicar una escala a Zieye.

Se supone que la función para calcular un nivel de teselación Ti de Zieye es (MaxTessellationLevel/Zieye), lo que significa que MaxTessellationLevel es el nivel de teselación en Z = 1 en el espacio de los ojos. MaxTessellationLevel es igual a un valor establecido por [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) para N revisiones y, en el caso de las revisiones RT, es igual a pNumSegs. A continuación, el nivel de teselación se fija en valores, definidos por los dos estados de representación adicionales D3DRS \_ MINTESSELLATIONLEVEL y D3DRS MAXTESSELLATIONLEVEL, que definen los niveles de teselación mínimo y máximo a los que se va a \_ fijar. Las ti de cada vértice a lo largo de un borde de una revisión se promedian para obtener un nivel de teselación para ese borde. El algoritmo para calcular Ti para revisiones de rectángulos, revisiones de triángulos y N revisiones difiere en qué vértices de control se usan para calcular el nivel de teselación.

Para las revisiones de rectángulo con una base B-spline, se usan los cuatro vértices de control más externos. Por ejemplo, con orden CUBIC de D3DORDER: los \_ vértices (1,1) y (1,width-2) se usan con pNumSegs 0, los vértices \[ \] (1,width-2) y (height-2,height-2) se usan con pNumSeg 1 , los \[ \] vértices (height-2, width-2) y (1,width-2) se usan con pNumSegs 2 y los \[ \] vértices (2,1) y (1,1) se usan con pNumSegs \[ \] 3.

Para las revisiones de triángulo, se usan los vértices de revisión de esquina. Con el orden CUBIC de D3DORDER: los vértices (0) y (9) se usan con \_ pNumSegs 0, los vértices (9) y (6) se usan con \[ \] pNumSegs 1 y los vértices \[ \] (6) y (0) se usan con pNumSegs \[ \] 3.

En el caso de las N revisiones, se usan los vértices del triángulo.

Para las revisiones de rectángulo y triángulo con una base Bézier, se usan los vértices de control de esquina.

Control de velocidad de teselación por vértice. Opcionalmente, una aplicación puede proporcionar un único valor de punto flotante positivo por vértice, que se puede usar para controlar la velocidad de teselación. Esto se proporciona mediante D3DDECLUSAGE TESSFACTOR, para el que el índice de uso debe ser 0 y el tipo de entrada debe ser \_ D3DDECLTYPE \_ FLOAT1. Esto se multiplica al nivel de teselación por vértice.

### <a name="math"></a>Matemáticas

El nivel de teselación (Te) de un borde e, representado por dos vértices de control (Ve1, Ve2), se calcula como se muestra a continuación:


```
Vertex Vi: (Xi, Yi, Zi, TFactori (optional)). 
Ze1eye = Ve1 . Mdm 
Ze2eye = Ve2 . Mdm 
Te1 = MaxTessellationLevel * TFactore1 / Ze1eye 
Te2 = MaxTessellationLevel * TFactore2 / Ze2eye 
Te = ( Te1 + Te2 ) / 2; 
if Te > D3DRS_MAXTESSELLATIONLEVEL || Te < 0, then Te = D3DRS_MAXTESSELLATIONLEVEL 
if Te < D3DRS_MINTESSELLATIONLEVEL, then Te = D3DRS_MINTESSELLATIONLEVEL 
```



Cuando D3DRS \_ ENABLEADAPTIVETESSELLATION es **TRUE,** las primitivas de triángulo (listas de triángulos, ventiladores, franjas) se dibujan como N revisiones, [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) tiene un valor establecido menor que 1,0.

### <a name="api-changes"></a>Cambios de API

Nuevos estados de representación:


```
 D3DRS_ENABLEADAPTIVETESSELLATION // BOOL 
 D3DRS_MAXTESSELLATIONLEVEL       // Float 
 D3DRS_MINTESSELLATIONLEVEL       // Float 
 D3DRS_ADAPTIVETESS_X             // Float 
 D3DRS_ADAPTIVETESS_Y             // Float 
 D3DRS_ADAPTIVETESS_Z             // Float 
 D3DRS_ADAPTIVETESS_W             // Float 
 
 // D3DRS_MINTESSELLATIONLEVEL and D3DRS_MAXTESSELLATIONLEVEL 
 // cannot be less than 1 
```



Y sus valores predeterminados:


```
D3DRS_MAXTESSELLATIONLEVEL = 1.0f 
D3DRS_MINTESSELLATIONLEVEL = 1.0f 
D3DRS_ADAPTIVETESS_X = 0.0f 
D3DRS_ADAPTIVETESS_Y = 0.0f 
D3DRS_ADAPTIVETESS_Z = 1.0f 
D3DRS_ADAPTIVETESS_W = 0.0f 
D3DRS_ENABLEADAPTIVETESSELLATION = FALSE 
```



Nuevos límites de hardware:


```
D3DDEVCAPS2_ADAPTIVETESSRTPATCH // Can adaptively tessellate RT-patches 
D3DDEVCAPS2_ADAPTIVETESSNPATCH  // Can adaptively tessellate N-patches 
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canalización de vértices](vertex-pipeline.md)
</dt> </dl>

 

 
