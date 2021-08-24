---
description: Asignadores de negociación
ms.assetid: fe13477c-1a7b-4098-9d0f-c54783102bc9
title: Asignadores de negociación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 710b8315bfd44371a82d995afa56483414623136a6ce5c510babd5ea07b4b8bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790945"
---
# <a name="negotiating-allocators"></a>Asignadores de negociación

Cuando se conectan dos pines, necesitan un mecanismo para intercambiar datos multimedia. Este mecanismo se denomina *transporte*. En general, la arquitectura DirectShow es neutra con respecto a los transportes. Dos filtros pueden aceptar la conexión mediante cualquier transporte que ambos admitan.

El transporte más común es el *transporte de memoria local,* en el que los datos multimedia residen en la memoria principal. Existen dos tipos de transporte de memoria local: el *modelo de inserción* y el *modelo de extracción*. En el modelo de inserción, el filtro de origen inserta datos en el filtro de nivel inferior, mediante la interfaz [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) en el pin de entrada del filtro de bajada. En el modelo de extracción, el filtro de bajada solicita datos del filtro de origen, mediante la interfaz [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) en el pin de salida del filtro de origen. Para obtener más información sobre estos dos modelos de flujo de datos, vea [Data Flow en filter Graph](data-flow-in-the-filter-graph.md).

En el transporte de memoria local, el objeto responsable de asignar búferes de memoria se denomina *asignador*. Un asignador admite la [**interfaz IMemAllocator.**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) Ambos pines comparten un solo asignador. Cualquiera de las anclar puede proporcionar un asignador, pero el pin de salida selecciona el asignador que se va a usar.

El pin de salida también establece las propiedades del asignador, que determinan cuántos búferes crea el asignador, el tamaño de cada búfer y la alineación de la memoria. El pin de salida puede diferir al pin de entrada para los requisitos del búfer.

En una **conexión IMemInputPin,** la negociación del asignador funciona de la siguiente manera:

1.  Opcionalmente, el pin de salida llama [**a IMemInputPin::GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements). Este método recupera los requisitos de búfer del pin de entrada, como la alineación de memoria. En general, el pin de salida debe respetar la solicitud del pin de entrada, a menos que haya una buena razón para no hacerlo.
2.  Opcionalmente, el pin de salida llama [**a IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator). Este método solicita un asignador del pin de entrada. El pin de entrada proporciona uno o devuelve un código de error.
3.  El pin de salida selecciona un asignador. Puede usar uno proporcionado por el pin de entrada o crear el suyo propio.
4.  El pin de salida llama [**a IMemAllocator::SetProperties para**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) establecer las propiedades del asignador. Sin embargo, es posible que el asignador no respeta las propiedades solicitadas. (Por ejemplo, esto puede ocurrir si el pin de entrada proporciona el asignador). El asignador devuelve las propiedades reales como un parámetro de salida en el **método SetProperties.**
5.  El saliente llama a [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) para informar al pin de entrada de la selección.
6.  El pin de entrada debe llamar [**a IMemAllocator::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getproperties) para comprobar si las propiedades del asignador son aceptables.
7.  El pin de salida es responsable de confirmar y desasignar el asignador. Esto sucede cuando el streaming se inicia y se detiene.

En una **conexión IAsyncReader,** la negociación del asignador funciona de la siguiente manera:

1.  El pin de entrada [**llama a IAsyncReader::RequestAllocator**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) en el pin de salida. El pin de entrada especifica sus requisitos de búfer y, opcionalmente, proporciona un asignador.
2.  El pin de salida selecciona un asignador. Puede usar el proporcionado por el pin de entrada, si lo hay, o crear el suyo propio.
3.  El pin de salida devuelve el asignador como un parámetro saliente en el **método RequestAllocator.** El pin de entrada debe comprobar las propiedades del asignador.
4.  El pin de entrada es responsable de confirmar y desasignar el asignador.
5.  En cualquier momento durante el proceso de negociación del asignador, cualquier pin puede producir un error en la conexión.
6.  Si el pin de salida usa el asignador del pin de entrada, solo puede usar ese asignador para entregar muestras a ese pin de entrada. El filtro propietario no debe usar el asignador para entregar muestras a otros pines.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Proporcionar un asignador personalizado](providing-a-custom-allocator.md)
</dt> </dl>

 

 



