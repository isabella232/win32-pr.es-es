---
description: Cree una textura de mapa de entorno cúbica llamando al método CreateCubeTexture. Las texturas del mapa del entorno cúbica deben ser cuadradas, con dimensiones que son una potencia de dos.
ms.assetid: 3879d215-064b-4d7d-afae-2ed46569c8bf
title: Crear superficies de mapa de entorno cúbica (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36be3067c6a5f21c39cfed7cab731ca875b70799
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539028"
---
# <a name="creating-cubic-environment-map-surfaces-direct3d-9"></a><span data-ttu-id="1ad73-104">Crear superficies de mapa de entorno cúbica (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1ad73-104">Creating Cubic Environment Map Surfaces (Direct3D 9)</span></span>

<span data-ttu-id="1ad73-105">Cree una textura de mapa de entorno cúbica llamando al método [**CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) .</span><span class="sxs-lookup"><span data-stu-id="1ad73-105">You create a cubic environment map texture by calling the [**CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) method.</span></span> <span data-ttu-id="1ad73-106">Las texturas del mapa del entorno cúbica deben ser cuadradas, con dimensiones que son una potencia de dos.</span><span class="sxs-lookup"><span data-stu-id="1ad73-106">Cubic environment map textures must be square, with dimensions that are a power of two.</span></span>

<span data-ttu-id="1ad73-107">En el ejemplo de código siguiente se muestra cómo la aplicación de C++ podría crear un mapa de entorno cúbico simple.</span><span class="sxs-lookup"><span data-stu-id="1ad73-107">The following code example shows how your C++ application might create a simple cubic environment map.</span></span>


```
// Init m_d3dDevice to point to an IDirect3DDevice9 interface

LPDIRECT3DCUBETEXTURE9 m_pCubeMap;

m_d3dDevice->CreateCubeTexture(256, 1, D3DUSAGE_RENDERTARGET, D3DFMT_R8G8B8,
                                D3DPOOL_DEFAULT, &m_pCubeMap);
```



## <a name="accessing-cubic-environment-map-faces"></a><span data-ttu-id="1ad73-108">Acceso a caras de mapas de entorno cúbicos</span><span class="sxs-lookup"><span data-stu-id="1ad73-108">Accessing Cubic Environment Map Faces</span></span>

<span data-ttu-id="1ad73-109">Puede navegar entre caras de un mapa de entorno cúbico mediante el método [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) .</span><span class="sxs-lookup"><span data-stu-id="1ad73-109">You can navigate between faces of a cubic environment map by using the [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) method.</span></span>

<span data-ttu-id="1ad73-110">En el ejemplo de código siguiente se usa [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) para recuperar la superficie del mapa de cubos usada para la cara y positiva (cara 2).</span><span class="sxs-lookup"><span data-stu-id="1ad73-110">The following code example uses [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) to retrieve the cube-map surface used for the positive y-face (face 2).</span></span>


```
// Init m_pCubeMap to point to an IDirect3DCubeTexture9 interface

LPDIRECT3DSURFACE9 pFace2;
m_pCubeMap->GetCubeMapSurface(D3DCUBEMAP_FACE_POSITIVE_Y, 0, &pFace2);
```



<span data-ttu-id="1ad73-111">El primer parámetro que [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) acepta es un valor enumerado de [**\_ caras D3DCUBEMAP**](./d3dcubemap-faces.md) que describe la superficie adjunta que el método debe recuperar.</span><span class="sxs-lookup"><span data-stu-id="1ad73-111">The first parameter that [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) accepts is a [**D3DCUBEMAP\_FACES**](./d3dcubemap-faces.md) enumerated value that describes the attached surface that the method should retrieve.</span></span> <span data-ttu-id="1ad73-112">El segundo parámetro indica a Direct3D el nivel de la textura de un cubo de mipmapped que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="1ad73-112">The second parameter tells Direct3D which level of a mipmapped cube texture to retrieve.</span></span> <span data-ttu-id="1ad73-113">El tercer parámetro aceptado es la dirección de la interfaz [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) , que representa la superficie de textura del cubo devuelta.</span><span class="sxs-lookup"><span data-stu-id="1ad73-113">The third parameter accepted is the address of the [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface, representing the returned cube texture surface.</span></span> <span data-ttu-id="1ad73-114">Dado que este mapa de cubo no es mipmapped, aquí se usa 0.</span><span class="sxs-lookup"><span data-stu-id="1ad73-114">Because this cube-map is not mipmapped, 0 is used here.</span></span>

> [!Note]
>
> <span data-ttu-id="1ad73-115">Después de llamar a este método, se aumenta el recuento de referencias internas en la interfaz [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) .</span><span class="sxs-lookup"><span data-stu-id="1ad73-115">After calling this method, the internal reference count on the [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface is increased.</span></span> <span data-ttu-id="1ad73-116">Cuando haya terminado de usar esta superficie, asegúrese de llamar al método [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) en esta interfaz **IDirect3DSurface9** o tendrá una pérdida de memoria.</span><span class="sxs-lookup"><span data-stu-id="1ad73-116">When you are done using this surface, be sure to call the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) method on this **IDirect3DSurface9** interface or you will have a memory leak.</span></span>

 

## <a name="rendering-to-cubic-environment-maps"></a><span data-ttu-id="1ad73-117">Representación en mapas de entorno cúbicos</span><span class="sxs-lookup"><span data-stu-id="1ad73-117">Rendering to Cubic Environment Maps</span></span>

<span data-ttu-id="1ad73-118">Puede copiar imágenes en las caras individuales del mapa de cubo de la misma manera que cualquier otro objeto de textura o superficie.</span><span class="sxs-lookup"><span data-stu-id="1ad73-118">You can copy images to the individual faces of the cube map just like you would any other texture or surface object.</span></span> <span data-ttu-id="1ad73-119">Lo más importante que hay que hacer antes de la representación en una esfera es establecer las matrices de transformación para que la cámara se coloque correctamente y apunte a la dirección adecuada para esa esfera: hacia delante (+ z), hacia atrás (-z), izquierda (-x), derecha (+ x), arriba (+ y) o hacia abajo (-y).</span><span class="sxs-lookup"><span data-stu-id="1ad73-119">The most important thing to do before rendering to a face is set the transformation matrices so that the camera is positioned properly and points in the proper direction for that face: forward (+z), backward (-z), left (-x), right (+x), up (+y), or down (-y).</span></span>

<span data-ttu-id="1ad73-120">En el siguiente ejemplo de código de C++ se prepara y establece una matriz de vistas según la superficie que se representa.</span><span class="sxs-lookup"><span data-stu-id="1ad73-120">The following C++ code example prepares and sets a view matrix according to the face being rendered.</span></span>


```
// Init pCubeMap to point to an IDirect3DCubeTexture9 interface
// Init d3dDevice to point to an IDirect3DDevice9 interface

void RenderFaces()
{
    // Save transformation matrices of the device
    D3DXMATRIX matProjSave, matViewSave;
    d3dDevice->GetTransform(D3DTS_VIEW,       &matViewSave ;
    d3dDevice->GetTransform(D3DTS_PROJECTION, &matProjSave);

    // Store the current back buffer and z-buffer
    LPDIRECT3DSURFACE9 pBackBuffer, pZBuffer;
    d3dDevice->GetRenderTarget(&pBackBuffer);
    d3dDevice->GetDepthStencilSurface(&pZBuffer);
```



<span data-ttu-id="1ad73-121">Recuerde que cada una de las caras de un mapa de entorno cúbico representa un campo de vista de 90 grados.</span><span class="sxs-lookup"><span data-stu-id="1ad73-121">Remember, each face of a cubic environment map represents a 90-degree field of view.</span></span> <span data-ttu-id="1ad73-122">A menos que la aplicación requiera un campo diferente del ángulo de vista, para los efectos especiales, por ejemplo, tenga cuidado para establecer la matriz de proyección en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="1ad73-122">Unless your application requires a different field of view angle - for special effects, for example - take care to set the projection matrix accordingly.</span></span>

<span data-ttu-id="1ad73-123">En este ejemplo de código se crea y establece una matriz de proyección para el caso más común.</span><span class="sxs-lookup"><span data-stu-id="1ad73-123">This code example creates and sets a projection matrix for the most common case.</span></span>


```
    // Use 90-degree field of view in the projection
    D3DMATRIX matProj;
    D3DXMatrixPerspectiveFovLH(matProj, D3DX_PI/2, 1.0f, 0.5f, 1000.0f);
    d3dDevice->SetTransform(D3DTS_PROJECTION, &matProj);

    // Loop through the six faces of the cube map
    for(DWORD i=0; i<6; i++)
    {
        // Standard view that will be overridden below
        D3DVECTOR vEnvEyePt = D3DVECTOR(0.0f, 0.0f, 0.0f);
        D3DVECTOR vLookatPt, vUpVec;

        switch(i)
        {
            case D3DCUBEMAP_FACE_POSITIVE_X:
                vLookatPt = D3DVECTOR(1.0f, 0.0f, 0.0f);
                vUpVec    = D3DVECTOR(0.0f, 1.0f, 0.0f);
                break;
            case D3DCUBEMAP_FACE_NEGATIVE_X:
                vLookatPt = D3DVECTOR(-1.0f, 0.0f, 0.0f);
                vUpVec    = D3DVECTOR( 0.0f, 1.0f, 0.0f);
                break;
            case D3DCUBEMAP_FACE_POSITIVE_Y:
                vLookatPt = D3DVECTOR(0.0f, 1.0f, 0.0f);
                vUpVec    = D3DVECTOR(0.0f, 0.0f,-1.0f);
                break;
            case D3DCUBEMAP_FACE_NEGATIVE_Y:
                vLookatPt = D3DVECTOR(0.0f,-1.0f, 0.0f);
                vUpVec    = D3DVECTOR(0.0f, 0.0f, 1.0f);
                break;
            case D3DCUBEMAP_FACE_POSITIVE_Z:
                vLookatPt = D3DVECTOR( 0.0f, 0.0f, 1.0f);
                vUpVec    = D3DVECTOR( 0.0f, 1.0f, 0.0f);
                break;
            case D3DCUBEMAP_FACE_NEGATIVE_Z:
                vLookatPt = D3DVECTOR(0.0f, 0.0f,-1.0f);
                vUpVec    = D3DVECTOR(0.0f, 1.0f, 0.0f);
                break;
        }

         D3DMATRIX matView;
         D3DXMatrixLookAtLH(matView, vEnvEyePt, vLookatPt, vUpVec);
         d3dDevice->SetTransform(D3DTS_VIEW, &matView);
```



<span data-ttu-id="1ad73-124">Cuando la cámara está en posición y el conjunto de matrices de proyección, puede representar la escena.</span><span class="sxs-lookup"><span data-stu-id="1ad73-124">When the camera is in position and the projection matrix set, you can render the scene.</span></span> <span data-ttu-id="1ad73-125">Cada objeto de la escena debe colocarse tal como lo haría normalmente.</span><span class="sxs-lookup"><span data-stu-id="1ad73-125">Each object in the scene should be positioned as you would normally position them.</span></span> <span data-ttu-id="1ad73-126">En el ejemplo de código siguiente, que se proporciona para la integridad, se describe esta tarea.</span><span class="sxs-lookup"><span data-stu-id="1ad73-126">The following code example, provided for completeness, outlines this task.</span></span>


```
        // Get pointer to surface in order to render to it
        LPDIRECT3DSURFACE9 pFace;
        pCubeMap->GetCubeMapSurface((D3DCUBEMAP_FACES)i, 0, &pFace);
        d3dDevice->SetRenderTarget (pFace , pZBuffer);
        SAFE_RELEASE(pFace);

        d3dDevice->BeginScene();
        // Render scene here
        ...
        d3dDevice->EndScene();
    }

    // Change the render target back to the main back buffer.
    d3dDevice->SetRenderTarget(pBackBuffer, pZBuffer);
    SAFE_RELEASE(pBackBuffer);
    SAFE_RELEASE(pZBuffer);

    // Restore the original transformation matrices
    d3dDevice->SetTransform(D3DTS_VIEW,       &matViewSave);
    d3dDevice->SetTransform(D3DTS_PROJECTION, &matProjSave);
}
```



<span data-ttu-id="1ad73-127">Observe la llamada al método [**SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) .</span><span class="sxs-lookup"><span data-stu-id="1ad73-127">Note the call to the [**SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) method.</span></span> <span data-ttu-id="1ad73-128">Al representar las caras del mapa de cubo, debe asignar la cara como la superficie de representación-destino actual.</span><span class="sxs-lookup"><span data-stu-id="1ad73-128">When rendering to the cube map faces, you must assign the face as the current render-target surface.</span></span> <span data-ttu-id="1ad73-129">Las aplicaciones que usan búferes de profundidad pueden crear explícitamente un búfer de profundidad para el destino de representación o reasignar un búfer de profundidad existente a la superficie de representación-destino.</span><span class="sxs-lookup"><span data-stu-id="1ad73-129">Applications that use depth buffers can explicitly create a depth-buffer for the render-target, or reassign an existing depth-buffer to the render-target surface.</span></span> <span data-ttu-id="1ad73-130">En el ejemplo de código anterior se usa el último enfoque.</span><span class="sxs-lookup"><span data-stu-id="1ad73-130">The code sample above uses the latter approach.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ad73-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1ad73-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ad73-132">Asignación de entorno cúbica</span><span class="sxs-lookup"><span data-stu-id="1ad73-132">Cubic Environment Mapping</span></span>](cubic-environment-mapping.md)
</dt> </dl>

 

 
