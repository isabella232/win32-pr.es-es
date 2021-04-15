---
description: Proporcionar un asignador personalizado
ms.assetid: 4ce2db4b-c901-43a5-b905-7d6d923c940b
title: Proporcionar un asignador personalizado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e85a8d133ee5b686e25bc0d7d4a3e2444cb2791
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422848"
---
# <a name="providing-a-custom-allocator"></a>Proporcionar un asignador personalizado

En esta sección se describe cómo proporcionar un asignador personalizado para un filtro. Solo se describen las conexiones [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) , pero los pasos para una conexión [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) son similares.

En primer lugar, defina una clase de C++ para el asignador. Su asignador puede derivar de una de las clases de asignador estándar, [**CBaseAllocator**](cbaseallocator.md) o [**CMemAllocator**](cmemallocator.md), o puede crear una clase de asignador completamente nueva. Si crea una nueva clase, debe exponer la interfaz [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .

Los pasos restantes dependen de si el asignador pertenece a un terminal de entrada o a un terminal de salida en el filtro. Los pin de entrada juegan un rol diferente que los pin de salida durante la fase de negociación del asignador, porque el PIN de salida selecciona en última instancia el asignador.

**Proporcionar un asignador personalizado para un PIN de entrada**

Para proporcionar un asignador para un PIN de entrada, invalide el método [**CBaseInputPin:: GetAllocator**](cbaseinputpin-getallocator.md) del PIN de entrada. En este método, Compruebe la variable de miembro **m \_ pAllocator** . Si esta variable no es **null**, significa que el asignador ya se ha seleccionado para esta conexión, por lo que el método **GetAllocator** debe devolver un puntero a ese asignador. Si **m \_ PAllocator** es **null**, significa que no se ha seleccionado el asignador, por lo que el método **GetAllocator** debe devolver un puntero al asignador preferido del PIN de entrada. En ese caso, cree una instancia de su asignador personalizado y devuelva su puntero [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) . En el código siguiente se muestra cómo implementar el método **GetAllocator** :


```C++
STDMETHODIMP CMyInputPin::GetAllocator(IMemAllocator **ppAllocator)
{
    CheckPointer(ppAllocator, E_POINTER);
    if (m_pAllocator)  
    {
        // We already have an allocator, so return that one.
        *ppAllocator = m_pAllocator;
        (*ppAllocator)->AddRef();
        return S_OK;
    }

    // No allocator yet, so propose our custom allocator. The exact code
    // here will depend on your custom allocator class definition.
    HRESULT hr = S_OK;
    CMyAllocator *pAlloc = new CMyAllocator(&hr);
    if (!pAlloc)
    {
        return E_OUTOFMEMORY;
    }
    if (FAILED(hr))
    {
        delete pAlloc;
        return hr;
    }

    // Return the IMemAllocator interface to the caller.
    return pAlloc->QueryInterface(IID_IMemAllocator, (void**)ppAllocator);
}
```



Cuando el filtro de nivel superior selecciona un asignador, llama al método [**IMemInputPin:: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) del PIN de entrada. Invalide el método [**CBaseInputPin:: NotifyAllocator**](cbaseinputpin-notifyallocator.md) para comprobar las propiedades de asignador. En algunos casos, el PIN de entrada podría rechazar el asignador si no es el asignador personalizado, aunque esto puede hacer que se produzca un error en toda la conexión del PIN.

**Proporcionar un asignador personalizado para un PIN de salida**

Para proporcionar un asignador para un PIN de salida, invalide el método [**CBaseOutputPin:: InitAllocator**](cbaseoutputpin-initallocator.md) para crear una instancia del asignador:


```C++
HRESULT MyOutputPin::InitAllocator(IMemAllocator **ppAllocator)
{
    HRESULT hr = S_OK;
    CMyAllocator *pAlloc = new CMyAllocator(&hr);
    if (!pAlloc)
    {
        return E_OUTOFMEMORY;
    }

    if (FAILED(hr))
    {
        delete pAlloc;
        return hr;
    }

    // Return the IMemAllocator interface.
    return pAlloc->QueryInterface(IID_IMemAllocator, (void**)ppAllocator);
}
```



De forma predeterminada, la clase [**CBaseOutputPin**](cbaseoutputpin.md) solicita primero un asignador del PIN de entrada. Si ese asignador no es adecuado, el PIN de salida crea su propio asignador. Para forzar que la conexión use el asignador personalizado, invalide el método [**CBaseOutputPin::D ecideallocator**](cbaseoutputpin-decideallocator.md) . Sin embargo, tenga en cuenta que esto puede impedir que la clavija de salida se conecte con determinados filtros, porque el otro filtro también puede requerir su propio asignador personalizado. Una tercera opción es cambiar el orden: Pruebe el asignador personalizado primero y, a continuación, revierta al asignador del otro filtro.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Negociar asignadores](negotiating-allocators.md)
</dt> </dl>

 

 



