---
description: Teselación (Direct3D 9)
ms.assetid: ae39b0e1-d2ae-449e-89db-0a2b24171531
title: Teselación (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82378caac1218158ffc1834c9a9b56fb8cbd250e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806350"
---
# <a name="tessellation-direct3d-9"></a>Teselación (Direct3D 9)

## <a name="tessellator-unit"></a>Unidad del teselador

La unidad del teselador se ha mejorado. Ahora puede usarlo para:

-   Realiza una teselación adaptable de todos los primitivos de orden superior.
-   Buscar valores de desplazamiento por vértices de un mapa de desplazamiento y pasarlos a un sombreador de vértices.
-   Compatibilidad con rectángulo: teselación de revisiones. Esto se especifica mediante una declaración de vértice mediante D3DDECLMETHOD \_ PARTIALU o D3DDECLMETHOD \_ PARTIALV. Si se utiliza una declaración de vértice que contiene estos métodos para dibujar una revisión de triángulo, [**IDirect3DDevice9::D rawtripatch**](/windows/desktop/api) producirá un error. Para obtener más información sobre las declaraciones de vértices, vea [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).

En DirectX 8. x, lo que se llamaba orden era realmente el grado. En Direct3D 9, el grado se especifica ahora mediante [**D3DDEGREETYPE**](./d3ddegreetype.md).


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



Los controladores deben corregir los errores de compilación que serán el resultado de este cambio cuando se compilen con los nuevos encabezados. No es necesario cambiar ninguna funcionalidad.

## <a name="adaptive-tessellation"></a>Teselación adaptable

La teselación adaptable se puede aplicar a primitivas de orden superior, incluidas las revisiones N-patch, Rectangle patch y triángulos. Esta característica está habilitada por D3DRS \_ ENABLEADAPTIVETESSELLATION y adaptable tessellates a una revisión, en función del valor de profundidad del vértice de control en el espacio ocular.

Las coordenadas z (Zi) de los vértices de control (VI), que se transforman en el espacio de ojo (Zieye) mediante la ejecución de un producto de punto con un vector 4, se usan como valores de profundidad. La aplicación especifica el vector 4D (MDM) mediante cuatro Estados de representación (D3DRS \_ ADAPTIVETESS \_ X, D3DRS \_ ADAPTIVETESS \_ Y, D3DRS \_ ADAPTIVETESS \_ Z y D3DRS \_ ADAPTIVETESS \_ W). Este vector de 4 vectores podría ser la tercera columna del mundo concatenado y las matrices de vistas. También podría usarse para aplicar una escala a Zieye.

Se supone que la función para calcular un nivel de teselación de TI de Zieye es (MaxTessellationLevel/Zieye), lo que significa que MaxTessellationLevel es el nivel de teselación en Z = 1 en el espacio de ojo. MaxTessellationLevel es igual a un valor establecido por [**IDirect3DDevice9:: SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) para N-patches y, para RT-patches, es igual a pNumSegs. A continuación, el nivel de teselación se fija en valores, definidos por los dos Estados de representación adicionales D3DRS \_ MINTESSELLATIONLEVEL y D3DRS \_ MAXTESSELLATIONLEVEL, que definen los niveles de teselación mínimo y máximo que se van a fijar. La media de TI para cada vértice a lo largo de un borde de una revisión se calcula para obtener un nivel de teselación para ese borde. El algoritmo para calcular la TI para las revisiones de rectángulos, triángulos y N-patches difiere en lo que los vértices de control se usan para calcular el nivel de teselación.

En el caso de las revisiones de rectángulo con una spline B, se usan los cuatro vértices de control más extremos. Por ejemplo, con el \_ orden cúbico D3DORDER: vértices (1,1) y (1, width-2) se usan con pNumSegs \[ 0 \] , los vértices (1, ancho 2) y (height-2, height-2) se usan con pNumSegs \[ 1 \] , los vértices (height-2, width-2) y (1, width-2) se usan con pNumSegs \[ 2 \] , y los vértices (2, 1) y (1,1) se usan con pNumSegs \[ 3 \]

En el caso de las revisiones del triángulo, se usan los vértices del parche de la esquina. Con el \_ orden cúbico D3DORDER: los vértices (0) y (9) se usan con pNumSegs \[ 0 \] , los vértices (9) y (6) se usan con pNumSegs \[ 1 \] y los vértices (6) y (0) se usan con pNumSegs \[ 3 \] .

En el caso de N-patches se usan los vértices de triángulo.

En el caso de las revisiones de rectángulos y triángulos con Bézier, se usan los vértices de control de esquina.

Control de velocidad de teselación por vértices. Una aplicación puede proporcionar opcionalmente un valor de punto flotante positivo único por vértice, que se puede usar para controlar la velocidad de teselación. Esto se proporciona mediante D3DDECLUSAGE \_ TESSFACTOR, para el que el índice de uso debe ser 0 y el tipo de entrada debe ser D3DDECLTYPE \_ FLOAT1. Se multiplica por el nivel de teselación por vértices.

### <a name="math"></a>Matemáticas

El nivel de teselación (te) para un borde e, representado por dos vértices de control (Ve1, Ve2), se calcula como se muestra a continuación:


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



Cuando D3DRS \_ ENABLEADAPTIVETESSELLATION es **true**, los primitivos triangulares (listas de triángulos, ventiladores y tiras) se dibujan como N-patches, [**IDirect3DDevice9:: SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) tiene un valor establecido inferior a 1,0.

### <a name="api-changes"></a>Cambios de la API

Nuevos Estados de representación:


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



Nuevas Cap de hardware:


```
D3DDEVCAPS2_ADAPTIVETESSRTPATCH // Can adaptively tessellate RT-patches 
D3DDEVCAPS2_ADAPTIVETESSNPATCH  // Can adaptively tessellate N-patches 
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canalización de vértices](vertex-pipeline.md)
</dt> </dl>

 

 
