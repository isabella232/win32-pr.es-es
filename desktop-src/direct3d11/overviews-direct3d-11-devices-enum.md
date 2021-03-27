---
title: Cómo enumerar adaptadores
description: En este tema se muestra cómo usar la infraestructura de gráficos de Microsoft DirectX (DXGI) para enumerar los adaptadores de gráficos disponibles en un equipo.
ms.assetid: f8ef981c-363e-4ac8-8734-69c68f346950
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af16aba0131d93a5f72732931a68f132126b5d48
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997108"
---
# <a name="how-to-enumerate-adapters"></a>Cómo: enumerar adaptadores

En este tema se muestra cómo usar la infraestructura de gráficos de Microsoft DirectX (DXGI) para enumerar los adaptadores de gráficos disponibles en un equipo. Direct3D 10 y 11 pueden usar DXGI para enumerar los adaptadores.

Por lo general, es necesario enumerar los adaptadores por estos motivos:

-   Para determinar el número de adaptadores de gráficos instalados en un equipo.
-   Para ayudarle a elegir el adaptador que se va a usar para crear un dispositivo Direct3D.
-   Para recuperar un objeto [**IDXGIAdapter**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter) que puede usar para recuperar funcionalidades del dispositivo.

**Para enumerar adaptadores**

1.  Cree un objeto [**IDXGIFactory**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory) mediante una llamada a la función [**CreateDXGIFactory**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory) . En el ejemplo de código siguiente se muestra cómo inicializar un objeto **IDXGIFactory** .
    ```
    IDXGIFactory * pFactory = NULL;

    CreateDXGIFactory(__uuidof(IDXGIFactory) ,(void**)&pFactory)
    ```

    

2.  Enumere cada adaptador llamando al método [**IDXGIFactory:: EnumAdapters**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-enumadapters) . El parámetro *Adapter* permite especificar un número de índice de base cero del adaptador que se va a enumerar. Si no hay ningún adaptador disponible en el índice especificado, el método devuelve el [**error de DXGI \_ \_ no \_ encontrado**](/windows/desktop/direct3ddxgi/dxgi-error).

    En el ejemplo de código siguiente se muestra cómo enumerar a través de los adaptadores de un equipo.

    ```
    for (UINT i = 0; 
         pFactory->EnumAdapters(i, &pAdapter) != DXGI_ERROR_NOT_FOUND; 
         ++i) 
    { ... }
    ```

    

En el ejemplo de código siguiente se muestra cómo enumerar todos los adaptadores de un equipo.

> [!Note]  
> En Direct3D 11,0 y versiones posteriores, se recomienda que las aplicaciones siempre usen [**IDXGIFactory1**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1) y [**CreateDXGIFactory1**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1) en su lugar.

 


```C++
std::vector <IDXGIAdapter*> EnumerateAdapters(void)
{
    IDXGIAdapter * pAdapter; 
    std::vector <IDXGIAdapter*> vAdapters; 
    IDXGIFactory* pFactory = NULL; 
    

    // Create a DXGIFactory object.
    if(FAILED(CreateDXGIFactory(__uuidof(IDXGIFactory) ,(void**)&pFactory)))
    {
        return vAdapters;
    }


    for ( UINT i = 0;
          pFactory->EnumAdapters(i, &pAdapter) != DXGI_ERROR_NOT_FOUND;
          ++i )
    {
        vAdapters.push_back(pAdapter); 
    } 


    if(pFactory)
    {
        pFactory->Release();
    }

    return vAdapters;

}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo usar Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 