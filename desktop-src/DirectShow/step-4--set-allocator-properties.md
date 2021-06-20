---
description: Establezca las propiedades del asignador como parte de la escritura de un filtro de transformación. El pin de salida del filtro de transformación selecciona el asignador de nivel inferior.
ms.assetid: c2fd6d8b-b239-45e4-9c02-41edafa58762
title: Paso 4. Establecer propiedades de asignador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ee7d9ecdc85b63ec6bd774a3a47e0e9399dcf3
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406828"
---
# <a name="step-4-set-allocator-properties"></a>Paso 4. Establecer propiedades de asignador

Este es el paso 4 del tutorial Escribir [filtros de transformación](writing-transform-filters.md).

> [!Note]  
> Este paso no es necesario para los filtros que derivan de **CTransInPlaceFilter.**

 

Una vez que dos pines coinciden en un tipo de medio, seleccionan un asignador para la conexión y negocian las propiedades del asignador, como el tamaño del búfer y el número de búferes.

En la **clase CTransformFilter,** hay dos asignadores, uno para la conexión de pin ascendente y otro para la conexión de pin de nivel inferior. El filtro ascendente selecciona el asignador ascendente y también elige las propiedades del asignador. El pin de entrada acepta lo que decida el filtro ascendente. Si necesita modificar este comportamiento, invalide el [**método CBaseInputPin::NotifyAllocator.**](cbaseinputpin-notifyallocator.md)

El pin de salida del filtro de transformación selecciona el asignador de nivel inferior. Realiza los pasos siguientes:

1.  Si el filtro de nivel inferior puede proporcionar un asignador, el pin de salida usa ese. De lo contrario, la patilla de salida crea un nuevo asignador.
2.  El pin de salida obtiene los requisitos de asignador del filtro de bajada (si los hay) llamando a [**IMemInputPin::GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements).
3.  El pin de salida llama al método [**CTransformFilter::D ecideBufferSize**](ctransformfilter-decidebuffersize.md) del filtro de transformación, que es virtual puro. Los parámetros de este método son un puntero al asignador y una estructura [**ALLOCATOR \_ PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) con los requisitos del filtro de nivel inferior. Si el filtro de nivel inferior no tiene requisitos de asignador, la estructura se abate a cero.
4.  En el **método DecideBufferSize,** la clase derivada establece las propiedades del asignador llamando a [**IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties).

Por lo general, la clase derivada seleccionará las propiedades del asignador en función del formato de salida, los requisitos del filtro de nivel inferior y los propios requisitos del filtro. Intente seleccionar las propiedades que son compatibles con la solicitud del filtro de nivel inferior. De lo contrario, el filtro de nivel inferior podría rechazar la conexión.

En el ejemplo siguiente, el codificador RLE establece los valores mínimos para el tamaño del búfer, la alineación del búfer y el recuento de búferes. Para el prefijo, usa cualquier valor que solicite el filtro de bajada. El prefijo suele ser de cero bytes, pero algunos filtros lo requieren. Por ejemplo, el [filtro AVI Mux](avi-mux-filter.md) usa el prefijo para escribir encabezados RIFF.


```C++
HRESULT CRleFilter::DecideBufferSize(
    IMemAllocator *pAlloc, ALLOCATOR_PROPERTIES *pProp)
{
    AM_MEDIA_TYPE mt;
    HRESULT hr = m_pOutput->ConnectionMediaType(&mt);
    if (FAILED(hr))
    {
        return hr;
    }

    ASSERT(mt.formattype == FORMAT_VideoInfo);
    BITMAPINFOHEADER *pbmi = HEADER(mt.pbFormat);
    pProp->cbBuffer = DIBSIZE(*pbmi) * 2; 
    if (pProp->cbAlign == 0)
    {
        pProp->cbAlign = 1;
    }
    if (pProp->cBuffers == 0)
    {
        pProp->cBuffers = 1;
    }
    // Release the format block.
    FreeMediaType(mt);

    // Set allocator properties.
    ALLOCATOR_PROPERTIES Actual;
    hr = pAlloc->SetProperties(pProp, &Actual);
    if (FAILED(hr)) 
    {
        return hr;
    }
    // Even when it succeeds, check the actual result.
    if (pProp->cbBuffer > Actual.cbBuffer) 
    {
        return E_FAIL;
    }
    return S_OK;
}
```



Es posible que el asignador no pueda coincidir exactamente con la solicitud. Por lo tanto, **el método SetProperties** devuelve el resultado real en una estructura **ALLOCATOR \_ PROPERTIES** independiente (el *parámetro Real,* en el ejemplo anterior). Incluso cuando **SetProperties se** realiza correctamente, debe comprobar el resultado para asegurarse de que cumplen los requisitos mínimos del filtro.

**Asignadores personalizados**

De forma predeterminada, todas las clases de filtro usan [**la clase CMemAllocator**](cmemallocator.md) para sus asignadores. Esta clase asigna memoria desde el espacio de direcciones virtuales del proceso de cliente (mediante **VirtualAlloc**). Si el filtro necesita usar algún otro tipo de memoria, como las superficies de DirectDraw, puede implementar un asignador personalizado. Puede usar la [**clase CBaseAllocator**](cbaseallocator.md) o escribir una clase de asignador completamente nueva. Si el filtro tiene un asignador personalizado, invalide los métodos siguientes, en función de qué pin use el asignador:

-   Pin de entrada: [**CBaseInputPin::GetAllocator**](cbaseinputpin-getallocator.md) y [**CBaseInputPin::NotifyAllocator**](cbaseinputpin-notifyallocator.md).
-   Pin de salida: [**CBaseOutputPin::D ecideAllocator**](cbaseoutputpin-decideallocator.md).

Si el otro filtro rechaza la conexión mediante el asignador personalizado, el filtro puede producir un error en la conexión o conectarse con el asignador del otro filtro. En el último caso, es posible que tenga que establecer una marca interna que indique el tipo de asignador. Para obtener un ejemplo de este enfoque, vea [**CDrawImage (clase).**](cdrawimage.md)

Siguiente: [Paso 5. Transforme la imagen](step-5--transform-the-image.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escribir filtros de DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



