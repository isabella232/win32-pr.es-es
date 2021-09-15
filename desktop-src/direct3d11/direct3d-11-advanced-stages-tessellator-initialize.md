---
title: Cómo inicializar la fase del teselador
description: En este tema se muestra cómo inicializar la fase del teselador.
ms.assetid: 81f5461a-0938-4c46-b3e8-bef2bea125a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50cfe00a4d59396f0dc1b0157f84e57e9cabc4a0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566233"
---
# <a name="how-to-initialize-the-tessellator-stage"></a>Cómo: Inicializar la fase del teselador

En general, la teselación expande el modelo compacto, definido por el usuario, de una revisión en geometría que contiene una cantidad programable de detalles. La geometría suele ser un conjunto de triángulos que representa la geometría de superficie detallada. En este tema se muestra cómo inicializar la fase del teselador.

La fase del teselador es la segunda de tres fases que funcionan juntas para tesentar o mosaico una superficie. La primera fase es la fase del sombreador de casco; funciona una vez por revisión y configura cómo se comporta la siguiente fase (tessellator de función fija). Un sombreador de casco también genera salidas definidas por el usuario, como puntos de control de salida y constantes de revisión que se envían más allá del teselador directamente a la tercera fase, la fase de sombreador de dominio. Un sombreador de dominio se invoca una vez por cada punto de fase del teselador y evalúa las posiciones de la superficie.

La fase del teselador es una fase de función fija, no hay ningún sombreador que generar y ningún estado para establecer. Recibe todo su estado de configuración de la fase de sombreador de casco; Una vez inicializada la fase del sombreador de casco, la fase del teselador se inicializa automáticamente.

**Para inicializar la fase del teselador**

-   Inicialice la fase del sombreador de casco mediante [**ID3D11DeviceContext::HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader).

    ```
    void HSSetShader(
      ID3D11HullShader *pHullShader,  
      ID3D11ClassInstance *const *ppClassInstances,
      UINT NumClassInstances
    );
    ```

    

    *ppClassInstances* es un puntero a una matriz de interfaces de sombreador, representadas por punteros [**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance) y el número de interfaces, representadas *por NumClassInstances*. Si no se usan, estos parámetros se pueden establecer en **NULL** y 0, respectivamente.

Después de inicializar la fase del sombreador de casco, también debe inicializar la fase del sombreador de dominio.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Introducción a la teselación](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 




