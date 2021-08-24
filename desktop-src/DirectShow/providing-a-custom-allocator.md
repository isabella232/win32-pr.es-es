---
description: Proporcionar un asignador personalizado
ms.assetid: 4ce2db4b-c901-43a5-b905-7d6d923c940b
title: Proporcionar un asignador personalizado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79b2f36f269ff30545d648c5df22e3070ec5588bcc2fa8791852fe9b6a59215c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747915"
---
# <a name="providing-a-custom-allocator"></a>Proporcionar un asignador personalizado

En esta sección se describe cómo proporcionar un asignador personalizado para un filtro. Solo [**se describen las conexiones IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) pero los pasos para una [**conexión IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) son similares.

En primer lugar, defina una clase de C++ para el asignador. El asignador puede derivar de una de las clases de asignador estándar, [**CBaseAllocator**](cbaseallocator.md) o [**CMemAllocator,**](cmemallocator.md)o puede crear una clase de asignador completamente nueva. Si crea una nueva clase, debe exponer la [**interfaz IMemAllocator.**](/windows/desktop/api/Strmif/nn-strmif-imemallocator)

Los pasos restantes dependen de si el asignador pertenece a un pin de entrada o a un pin de salida en el filtro. Los pines de entrada desempeñan un rol diferente al de los pines de salida durante la fase de negociación del asignador, ya que el pin de salida selecciona en última instancia el asignador.

**Proporcionar un asignador personalizado para un pin de entrada**

Para proporcionar un asignador para un pin de entrada, invalide el método [**CBaseInputPin::GetAllocator del**](cbaseinputpin-getallocator.md) pin de entrada. Dentro de este método, compruebe la **variable \_ miembro m pAllocator.** Si esta variable no es **NULL,** significa que el asignador ya se ha seleccionado para esta conexión, por lo que el método **GetAllocator** debe devolver un puntero a ese asignador. Si **m \_ pAllocator** es **NULL,** significa que no se ha seleccionado el asignador, por lo que el método **GetAllocator** debe devolver un puntero al asignador preferido del pin de entrada. En ese caso, cree una instancia del asignador personalizado y devuelva su [**puntero IMemAllocator.**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) El código siguiente muestra cómo implementar el **método GetAllocator:**


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



Cuando el filtro ascendente selecciona un asignador, llama al método [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) del pin de entrada. Invalide [**el método CBaseInputPin::NotifyAllocator**](cbaseinputpin-notifyallocator.md) para comprobar las propiedades del asignador. En algunos casos, el pin de entrada podría rechazar el asignador si no es el asignador personalizado, aunque esto puede provocar un error en toda la conexión de pin.

**Proporcionar un asignador personalizado para un pin de salida**

Para proporcionar un asignador para un pin de salida, invalide el método [**CBaseOutputPin::InitAllocator**](cbaseoutputpin-initallocator.md) para crear una instancia del asignador:


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



De forma predeterminada, [**la clase CBaseOutputPin**](cbaseoutputpin.md) solicita primero un asignador del pin de entrada. Si ese asignador no es adecuado, el pin de salida crea su propio asignador. Para forzar que la conexión use el asignador personalizado, invalide el método [**CBaseOutputPin::D ecideAllocator.**](cbaseoutputpin-decideallocator.md) Sin embargo, tenga en cuenta que esto puede impedir que el pin de salida se conecte con determinados filtros, ya que el otro filtro también puede requerir su propio asignador personalizado. Una tercera opción es cambiar el orden: pruebe primero el asignador personalizado y, a continuación, vuelva al asignador del otro filtro.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asignadores de negociación](negotiating-allocators.md)
</dt> </dl>

 

 



