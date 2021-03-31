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
# <a name="tessellation-direct3d-9"></a><span data-ttu-id="3a27d-103">Teselación (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3a27d-103">Tessellation (Direct3D 9)</span></span>

## <a name="tessellator-unit"></a><span data-ttu-id="3a27d-104">Unidad del teselador</span><span class="sxs-lookup"><span data-stu-id="3a27d-104">Tessellator Unit</span></span>

<span data-ttu-id="3a27d-105">La unidad del teselador se ha mejorado.</span><span class="sxs-lookup"><span data-stu-id="3a27d-105">The tessellator unit has been enhanced.</span></span> <span data-ttu-id="3a27d-106">Ahora puede usarlo para:</span><span class="sxs-lookup"><span data-stu-id="3a27d-106">You can now use it to:</span></span>

-   <span data-ttu-id="3a27d-107">Realiza una teselación adaptable de todos los primitivos de orden superior.</span><span class="sxs-lookup"><span data-stu-id="3a27d-107">Perform adaptive tessellation of all higher-order primitives.</span></span>
-   <span data-ttu-id="3a27d-108">Buscar valores de desplazamiento por vértices de un mapa de desplazamiento y pasarlos a un sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="3a27d-108">Look up per-vertex displacement values from a displacement map and pass them on to a vertex shader.</span></span>
-   <span data-ttu-id="3a27d-109">Compatibilidad con rectángulo: teselación de revisiones.</span><span class="sxs-lookup"><span data-stu-id="3a27d-109">Support rectangle-patch tessellation.</span></span> <span data-ttu-id="3a27d-110">Esto se especifica mediante una declaración de vértice mediante D3DDECLMETHOD \_ PARTIALU o D3DDECLMETHOD \_ PARTIALV.</span><span class="sxs-lookup"><span data-stu-id="3a27d-110">This is specified through a vertex declaration using D3DDECLMETHOD\_PARTIALU or D3DDECLMETHOD\_PARTIALV.</span></span> <span data-ttu-id="3a27d-111">Si se utiliza una declaración de vértice que contiene estos métodos para dibujar una revisión de triángulo, [**IDirect3DDevice9::D rawtripatch**](/windows/desktop/api) producirá un error.</span><span class="sxs-lookup"><span data-stu-id="3a27d-111">If a vertex declaration containing these methods is used to draw a triangle patch, [**IDirect3DDevice9::DrawTriPatch**](/windows/desktop/api) will fail.</span></span> <span data-ttu-id="3a27d-112">Para obtener más información sobre las declaraciones de vértices, vea [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span><span class="sxs-lookup"><span data-stu-id="3a27d-112">For more information about vertex declarations, see [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

<span data-ttu-id="3a27d-113">En DirectX 8. x, lo que se llamaba orden era realmente el grado.</span><span class="sxs-lookup"><span data-stu-id="3a27d-113">In DirectX 8.x, what was called ORDER was really the degree.</span></span> <span data-ttu-id="3a27d-114">En Direct3D 9, el grado se especifica ahora mediante [**D3DDEGREETYPE**](./d3ddegreetype.md).</span><span class="sxs-lookup"><span data-stu-id="3a27d-114">In Direct3D 9, the degree is now specified by [**D3DDEGREETYPE**](./d3ddegreetype.md).</span></span>


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



<span data-ttu-id="3a27d-115">El cambio en el tipo de grado afectó a otras dos estructuras.</span><span class="sxs-lookup"><span data-stu-id="3a27d-115">The change in degree type affected two other structures.</span></span>


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



<span data-ttu-id="3a27d-116">Los controladores deben corregir los errores de compilación que serán el resultado de este cambio cuando se compilen con los nuevos encabezados.</span><span class="sxs-lookup"><span data-stu-id="3a27d-116">Drivers need to fix compilation errors that will result from this change when they compile with the new headers.</span></span> <span data-ttu-id="3a27d-117">No es necesario cambiar ninguna funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="3a27d-117">No functionality has to be changed.</span></span>

## <a name="adaptive-tessellation"></a><span data-ttu-id="3a27d-118">Teselación adaptable</span><span class="sxs-lookup"><span data-stu-id="3a27d-118">Adaptive Tessellation</span></span>

<span data-ttu-id="3a27d-119">La teselación adaptable se puede aplicar a primitivas de orden superior, incluidas las revisiones N-patch, Rectangle patch y triángulos.</span><span class="sxs-lookup"><span data-stu-id="3a27d-119">Adaptive tessellation can be applied to high-order primitives including N-patches, rectangle patches, and triangle patches.</span></span> <span data-ttu-id="3a27d-120">Esta característica está habilitada por D3DRS \_ ENABLEADAPTIVETESSELLATION y adaptable tessellates a una revisión, en función del valor de profundidad del vértice de control en el espacio ocular.</span><span class="sxs-lookup"><span data-stu-id="3a27d-120">This feature is enabled by the D3DRS\_ENABLEADAPTIVETESSELLATION and adaptively tessellates a patch, based on the depth value of the control vertex in eye space.</span></span>

<span data-ttu-id="3a27d-121">Las coordenadas z (Zi) de los vértices de control (VI), que se transforman en el espacio de ojo (Zieye) mediante la ejecución de un producto de punto con un vector 4, se usan como valores de profundidad.</span><span class="sxs-lookup"><span data-stu-id="3a27d-121">The z-coordinates (Zi) of control vertices (Vi), which are transformed into eye space (Zieye) by performing a dot product with a 4-vector, are used as the depth values.</span></span> <span data-ttu-id="3a27d-122">La aplicación especifica el vector 4D (MDM) mediante cuatro Estados de representación (D3DRS \_ ADAPTIVETESS \_ X, D3DRS \_ ADAPTIVETESS \_ Y, D3DRS \_ ADAPTIVETESS \_ Z y D3DRS \_ ADAPTIVETESS \_ W).</span><span class="sxs-lookup"><span data-stu-id="3a27d-122">The 4D vector (Mdm) is specified by the application using four render states (D3DRS\_ADAPTIVETESS\_X, D3DRS\_ADAPTIVETESS\_Y, D3DRS\_ADAPTIVETESS\_Z, and D3DRS\_ADAPTIVETESS\_W).</span></span> <span data-ttu-id="3a27d-123">Este vector de 4 vectores podría ser la tercera columna del mundo concatenado y las matrices de vistas.</span><span class="sxs-lookup"><span data-stu-id="3a27d-123">This 4-vector could be the third column of the concatenated world and view matrices.</span></span> <span data-ttu-id="3a27d-124">También podría usarse para aplicar una escala a Zieye.</span><span class="sxs-lookup"><span data-stu-id="3a27d-124">It also could be used to apply a scale to Zieye.</span></span>

<span data-ttu-id="3a27d-125">Se supone que la función para calcular un nivel de teselación de TI de Zieye es (MaxTessellationLevel/Zieye), lo que significa que MaxTessellationLevel es el nivel de teselación en Z = 1 en el espacio de ojo.</span><span class="sxs-lookup"><span data-stu-id="3a27d-125">The function to compute a tessellation level Ti from Zieye is assumed to be (MaxTessellationLevel/Zieye), which means that the MaxTessellationLevel is the tessellation level at Z = 1 in eye space.</span></span> <span data-ttu-id="3a27d-126">MaxTessellationLevel es igual a un valor establecido por [**IDirect3DDevice9:: SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) para N-patches y, para RT-patches, es igual a pNumSegs.</span><span class="sxs-lookup"><span data-stu-id="3a27d-126">The MaxTessellationLevel is equal to a value set by [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) for N-patches and, for RT-patches, it is equal to pNumSegs.</span></span> <span data-ttu-id="3a27d-127">A continuación, el nivel de teselación se fija en valores, definidos por los dos Estados de representación adicionales D3DRS \_ MINTESSELLATIONLEVEL y D3DRS \_ MAXTESSELLATIONLEVEL, que definen los niveles de teselación mínimo y máximo que se van a fijar.</span><span class="sxs-lookup"><span data-stu-id="3a27d-127">The tessellation level is then clamped to values, defined by the two additional render states D3DRS\_MINTESSELLATIONLEVEL and D3DRS\_MAXTESSELLATIONLEVEL, which define the minimum and maximum tessellation levels to be clamped to.</span></span> <span data-ttu-id="3a27d-128">La media de TI para cada vértice a lo largo de un borde de una revisión se calcula para obtener un nivel de teselación para ese borde.</span><span class="sxs-lookup"><span data-stu-id="3a27d-128">The Ti's for each vertex along an edge of a patch are averaged to obtain a tessellation level for that edge.</span></span> <span data-ttu-id="3a27d-129">El algoritmo para calcular la TI para las revisiones de rectángulos, triángulos y N-patches difiere en lo que los vértices de control se usan para calcular el nivel de teselación.</span><span class="sxs-lookup"><span data-stu-id="3a27d-129">The algorithm for computing Ti for rectangle patches, triangle patches, and N-patches differs in what control vertices are used to compute the tessellation level.</span></span>

<span data-ttu-id="3a27d-130">En el caso de las revisiones de rectángulo con una spline B, se usan los cuatro vértices de control más extremos.</span><span class="sxs-lookup"><span data-stu-id="3a27d-130">For the rectangle patches with a B-spline basis, the four outermost control vertices are used.</span></span> <span data-ttu-id="3a27d-131">Por ejemplo, con el \_ orden cúbico D3DORDER: vértices (1,1) y (1, width-2) se usan con pNumSegs \[ 0 \] , los vértices (1, ancho 2) y (height-2, height-2) se usan con pNumSegs \[ 1 \] , los vértices (height-2, width-2) y (1, width-2) se usan con pNumSegs \[ 2 \] , y los vértices (2, 1) y (1,1) se usan con pNumSegs \[ 3 \]</span><span class="sxs-lookup"><span data-stu-id="3a27d-131">For example, with D3DORDER\_CUBIC order: vertices (1,1) and (1,width-2) are used with pNumSegs\[0\], vertices (1,width-2) and (height-2,height-2) are used with pNumSegs\[1\], vertices (height-2,width-2) and (1,width-2) are used with pNumSegs\[2\], and vertices (2,1) and (1,1) are used with pNumSegs\[3\].</span></span>

<span data-ttu-id="3a27d-132">En el caso de las revisiones del triángulo, se usan los vértices del parche de la esquina.</span><span class="sxs-lookup"><span data-stu-id="3a27d-132">For the triangle patches, the corner patch vertices are used.</span></span> <span data-ttu-id="3a27d-133">Con el \_ orden cúbico D3DORDER: los vértices (0) y (9) se usan con pNumSegs \[ 0 \] , los vértices (9) y (6) se usan con pNumSegs \[ 1 \] y los vértices (6) y (0) se usan con pNumSegs \[ 3 \] .</span><span class="sxs-lookup"><span data-stu-id="3a27d-133">With D3DORDER\_CUBIC order: vertices (0) and (9) are used with pNumSegs\[0\], vertices (9) and (6) are used with pNumSegs\[1\] and vertices (6) and (0) are used with pNumSegs\[3\].</span></span>

<span data-ttu-id="3a27d-134">En el caso de N-patches se usan los vértices de triángulo.</span><span class="sxs-lookup"><span data-stu-id="3a27d-134">For N-patches the triangle vertices are used.</span></span>

<span data-ttu-id="3a27d-135">En el caso de las revisiones de rectángulos y triángulos con Bézier, se usan los vértices de control de esquina.</span><span class="sxs-lookup"><span data-stu-id="3a27d-135">For the rectangle and triangle patches with a Bezier basis, the corner-control vertices are used.</span></span>

<span data-ttu-id="3a27d-136">Control de velocidad de teselación por vértices.</span><span class="sxs-lookup"><span data-stu-id="3a27d-136">Per-vertex tessellation rate control.</span></span> <span data-ttu-id="3a27d-137">Una aplicación puede proporcionar opcionalmente un valor de punto flotante positivo único por vértice, que se puede usar para controlar la velocidad de teselación.</span><span class="sxs-lookup"><span data-stu-id="3a27d-137">An application can optionally supply a single positive floating-point value per vertex, which can be used to control the rate of tessellation.</span></span> <span data-ttu-id="3a27d-138">Esto se proporciona mediante D3DDECLUSAGE \_ TESSFACTOR, para el que el índice de uso debe ser 0 y el tipo de entrada debe ser D3DDECLTYPE \_ FLOAT1.</span><span class="sxs-lookup"><span data-stu-id="3a27d-138">This is supplied using the D3DDECLUSAGE\_TESSFACTOR, for which usage index must be 0 and input type must be D3DDECLTYPE\_FLOAT1.</span></span> <span data-ttu-id="3a27d-139">Se multiplica por el nivel de teselación por vértices.</span><span class="sxs-lookup"><span data-stu-id="3a27d-139">This is multiplied to the per-vertex tessellation level.</span></span>

### <a name="math"></a><span data-ttu-id="3a27d-140">Matemáticas</span><span class="sxs-lookup"><span data-stu-id="3a27d-140">Math</span></span>

<span data-ttu-id="3a27d-141">El nivel de teselación (te) para un borde e, representado por dos vértices de control (Ve1, Ve2), se calcula como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="3a27d-141">The tessellation level (Te) for an edge e, represented by two control vertices (Ve1, Ve2), is computed as shown below :</span></span>


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



<span data-ttu-id="3a27d-142">Cuando D3DRS \_ ENABLEADAPTIVETESSELLATION es **true**, los primitivos triangulares (listas de triángulos, ventiladores y tiras) se dibujan como N-patches, [**IDirect3DDevice9:: SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) tiene un valor establecido inferior a 1,0.</span><span class="sxs-lookup"><span data-stu-id="3a27d-142">When D3DRS\_ENABLEADAPTIVETESSELLATION is **TRUE**, triangle primitives (triangle lists, fans, strips) are drawn as N-patches, [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) has set value less than 1.0.</span></span>

### <a name="api-changes"></a><span data-ttu-id="3a27d-143">Cambios de la API</span><span class="sxs-lookup"><span data-stu-id="3a27d-143">API Changes</span></span>

<span data-ttu-id="3a27d-144">Nuevos Estados de representación:</span><span class="sxs-lookup"><span data-stu-id="3a27d-144">New render states:</span></span>


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



<span data-ttu-id="3a27d-145">Y sus valores predeterminados:</span><span class="sxs-lookup"><span data-stu-id="3a27d-145">And their default values:</span></span>


```
D3DRS_MAXTESSELLATIONLEVEL = 1.0f 
D3DRS_MINTESSELLATIONLEVEL = 1.0f 
D3DRS_ADAPTIVETESS_X = 0.0f 
D3DRS_ADAPTIVETESS_Y = 0.0f 
D3DRS_ADAPTIVETESS_Z = 1.0f 
D3DRS_ADAPTIVETESS_W = 0.0f 
D3DRS_ENABLEADAPTIVETESSELLATION = FALSE 
```



<span data-ttu-id="3a27d-146">Nuevas Cap de hardware:</span><span class="sxs-lookup"><span data-stu-id="3a27d-146">New hardware caps:</span></span>


```
D3DDEVCAPS2_ADAPTIVETESSRTPATCH // Can adaptively tessellate RT-patches 
D3DDEVCAPS2_ADAPTIVETESSNPATCH  // Can adaptively tessellate N-patches 
```



## <a name="related-topics"></a><span data-ttu-id="3a27d-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3a27d-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a27d-148">Canalización de vértices</span><span class="sxs-lookup"><span data-stu-id="3a27d-148">Vertex Pipeline</span></span>](vertex-pipeline.md)
</dt> </dl>

 

 
