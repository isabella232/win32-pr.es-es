---
description: Paso 4.
ms.assetid: c2fd6d8b-b239-45e4-9c02-41edafa58762
title: Paso 4. Establecer propiedades de asignador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a32d5e3affba32b96dc93cb97e1886322bc6f2c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688226"
---
# <a name="step-4-set-allocator-properties"></a>Paso 4. Establecer propiedades de asignador

Este es el paso 4 del tutorial de [escritura de filtros de transformación](writing-transform-filters.md).

> [!Note]  
> Este paso no es necesario para los filtros que derivan de **CTransInPlaceFilter**.

 

Una vez que dos clavijas coinciden con un tipo de medio, seleccionan un asignador para la conexión y negocian las propiedades del asignador, como el tamaño del búfer y el número de búferes.

En la clase **CTransformFilter** , hay dos asignadores, uno para la conexión de PIN de nivel superior y otro para la conexión de PIN de bajada. El filtro de nivel superior selecciona el asignador de nivel superior y también elige las propiedades de asignador. El PIN de entrada acepta lo que decida el filtro de nivel superior. Si necesita modificar este comportamiento, invalide el método [**CBaseInputPin:: NotifyAllocator**](cbaseinputpin-notifyallocator.md) .

El PIN de salida del filtro de transformación selecciona el asignador de nivel inferior. Realiza los pasos siguientes:

1.  Si el filtro de nivel inferior puede proporcionar un asignador, el PIN de salida utiliza ese. De lo contrario, el PIN de salida crea un nuevo asignador.
2.  El PIN de salida obtiene los requisitos de asignador del filtro de nivel inferior (si existen) mediante una llamada a [**IMemInputPin:: GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements).
3.  El PIN de salida llama al método [**CTransformFilter::D ecidebuffersize**](ctransformfilter-decidebuffersize.md) del filtro de transformación, que es virtual puro. Los parámetros de este método son un puntero al asignador y una estructura de [**\_ propiedades de asignador**](/windows/win32/api/strmif/ns-strmif-allocator_properties) con los requisitos del filtro de nivel inferior. Si el filtro de nivel inferior no tiene ningún requisito de asignador, la estructura se pone a cero.
4.  En el método **DecideBufferSize** , la clase derivada establece las propiedades de asignador llamando a [**IMemAllocator:: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties).

Por lo general, la clase derivada seleccionará las propiedades de asignador basadas en el formato de salida, los requisitos del filtro de nivel inferior y los propios requisitos del filtro. Intente seleccionar propiedades que sean compatibles con la solicitud del filtro de nivel inferior. De lo contrario, el filtro de nivel inferior podría rechazar la conexión.

En el ejemplo siguiente, el codificador RLE establece los valores mínimos para el tamaño de búfer, la alineación del búfer y el recuento de búferes. Para el prefijo, utiliza el valor que solicitó el filtro de nivel inferior. Normalmente, el prefijo es de cero bytes, pero algunos filtros lo requieren. Por ejemplo, el filtro de [AVI MUX](avi-mux-filter.md) usa el prefijo para escribir encabezados riff.


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



Es posible que el asignador no pueda coincidir exactamente con la solicitud. Por lo tanto, el método **SetProperties** devuelve el resultado real en una estructura de **\_ propiedades de asignador** independiente (el parámetro *real* , en el ejemplo anterior). Incluso cuando **SetProperties** se realiza correctamente, debe comprobar el resultado para asegurarse de que cumplen los requisitos mínimos del filtro.

**Asignadores personalizados**

De forma predeterminada, todas las clases de filtro usan la clase [**CMemAllocator**](cmemallocator.md) para sus asignadores. Esta clase asigna memoria del espacio de direcciones virtuales del proceso del cliente (mediante **VirtualAlloc**). Si el filtro necesita usar algún otro tipo de memoria, como superficies de DirectDraw, puede implementar un asignador personalizado. Puede usar la clase [**CBaseAllocator**](cbaseallocator.md) o escribir una clase de asignador completamente nueva. Si el filtro tiene un asignador personalizado, invalide los métodos siguientes, en función del PIN que use el asignador:

-   PIN de entrada: [**CBaseInputPin:: GetAllocator**](cbaseinputpin-getallocator.md) y [**CBaseInputPin:: NotifyAllocator**](cbaseinputpin-notifyallocator.md).
-   PIN de salida: [**CBaseOutputPin::D ecideallocator**](cbaseoutputpin-decideallocator.md).

Si el otro filtro se niega a conectar con el asignador personalizado, el filtro puede producir un error en la conexión o conectarse al otro asignador del filtro. En el último caso, es posible que tenga que establecer una marca interna que indique el tipo de asignador. Para obtener un ejemplo de este enfoque, consulte [**clase CDrawImage**](cdrawimage.md).

Siguiente: [paso 5. Transformar la imagen](step-5--transform-the-image.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escribir filtros de DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



