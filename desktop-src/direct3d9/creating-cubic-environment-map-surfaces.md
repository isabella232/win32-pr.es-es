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
# <a name="creating-cubic-environment-map-surfaces-direct3d-9"></a>Crear superficies de mapa de entorno cúbica (Direct3D 9)

Cree una textura de mapa de entorno cúbica llamando al método [**CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) . Las texturas del mapa del entorno cúbica deben ser cuadradas, con dimensiones que son una potencia de dos.

En el ejemplo de código siguiente se muestra cómo la aplicación de C++ podría crear un mapa de entorno cúbico simple.


```
// Init m_d3dDevice to point to an IDirect3DDevice9 interface

LPDIRECT3DCUBETEXTURE9 m_pCubeMap;

m_d3dDevice->CreateCubeTexture(256, 1, D3DUSAGE_RENDERTARGET, D3DFMT_R8G8B8,
                                D3DPOOL_DEFAULT, &m_pCubeMap);
```



## <a name="accessing-cubic-environment-map-faces"></a>Acceso a caras de mapas de entorno cúbicos

Puede navegar entre caras de un mapa de entorno cúbico mediante el método [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) .

En el ejemplo de código siguiente se usa [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) para recuperar la superficie del mapa de cubos usada para la cara y positiva (cara 2).


```
// Init m_pCubeMap to point to an IDirect3DCubeTexture9 interface

LPDIRECT3DSURFACE9 pFace2;
m_pCubeMap->GetCubeMapSurface(D3DCUBEMAP_FACE_POSITIVE_Y, 0, &pFace2);
```



El primer parámetro que [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) acepta es un valor enumerado de [**\_ caras D3DCUBEMAP**](./d3dcubemap-faces.md) que describe la superficie adjunta que el método debe recuperar. El segundo parámetro indica a Direct3D el nivel de la textura de un cubo de mipmapped que se va a recuperar. El tercer parámetro aceptado es la dirección de la interfaz [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) , que representa la superficie de textura del cubo devuelta. Dado que este mapa de cubo no es mipmapped, aquí se usa 0.

> [!Note]
>
> Después de llamar a este método, se aumenta el recuento de referencias internas en la interfaz [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) . Cuando haya terminado de usar esta superficie, asegúrese de llamar al método [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) en esta interfaz **IDirect3DSurface9** o tendrá una pérdida de memoria.

 

## <a name="rendering-to-cubic-environment-maps"></a>Representación en mapas de entorno cúbicos

Puede copiar imágenes en las caras individuales del mapa de cubo de la misma manera que cualquier otro objeto de textura o superficie. Lo más importante que hay que hacer antes de la representación en una esfera es establecer las matrices de transformación para que la cámara se coloque correctamente y apunte a la dirección adecuada para esa esfera: hacia delante (+ z), hacia atrás (-z), izquierda (-x), derecha (+ x), arriba (+ y) o hacia abajo (-y).

En el siguiente ejemplo de código de C++ se prepara y establece una matriz de vistas según la superficie que se representa.


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



Recuerde que cada una de las caras de un mapa de entorno cúbico representa un campo de vista de 90 grados. A menos que la aplicación requiera un campo diferente del ángulo de vista, para los efectos especiales, por ejemplo, tenga cuidado para establecer la matriz de proyección en consecuencia.

En este ejemplo de código se crea y establece una matriz de proyección para el caso más común.


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



Cuando la cámara está en posición y el conjunto de matrices de proyección, puede representar la escena. Cada objeto de la escena debe colocarse tal como lo haría normalmente. En el ejemplo de código siguiente, que se proporciona para la integridad, se describe esta tarea.


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



Observe la llamada al método [**SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) . Al representar las caras del mapa de cubo, debe asignar la cara como la superficie de representación-destino actual. Las aplicaciones que usan búferes de profundidad pueden crear explícitamente un búfer de profundidad para el destino de representación o reasignar un búfer de profundidad existente a la superficie de representación-destino. En el ejemplo de código anterior se usa el último enfoque.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asignación de entorno cúbica](cubic-environment-mapping.md)
</dt> </dl>

 

 
