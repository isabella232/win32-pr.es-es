---
description: Negociar asignadores
ms.assetid: fe13477c-1a7b-4098-9d0f-c54783102bc9
title: Negociar asignadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2faa393ba9fcd8585d68947cec172d4cfca6decf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686279"
---
# <a name="negotiating-allocators"></a>Negociar asignadores

Cuando dos patillas se conectan, necesitan un mecanismo para intercambiar datos multimedia. Este mecanismo se denomina *transporte*. En general, la arquitectura de DirectShow es neutra sobre los transportes. Dos filtros pueden aceptar la conexión mediante cualquier transporte que admitan ambos.

El transporte más común es el transporte de *memoria local* , en el que los datos multimedia residen en la memoria principal. Existen dos tipos de transporte de memoria local, el *modelo de inserción* y el modelo de *extracción*. En el modelo de entrada, el filtro de origen envía datos al filtro de bajada, utilizando la interfaz [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) en el PIN de entrada del filtro de nivel inferior. En el modelo de extracción, el filtro de nivel inferior solicita datos del filtro de origen mediante la interfaz [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) en el PIN de salida del filtro de origen. Para obtener más información sobre estos dos modelos de flujo de datos, vea [flujo de datos en el gráfico de filtros](data-flow-in-the-filter-graph.md).

En el transporte de memoria local, el objeto responsable de la asignación de búferes de memoria se denomina *asignador*. Un asignador admite la interfaz [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) . Ambos PIN comparten un único asignador. Cualquier pin puede proporcionar un asignador, pero el PIN de salida selecciona el asignador que se va a usar.

El PIN de salida también establece las propiedades de asignador, que determinan el número de búferes que crea el asignador, el tamaño de cada búfer y la alineación de memoria. El PIN de salida podría diferir en el PIN de entrada para los requisitos de búfer.

En una conexión **IMemInputPin** , la negociación de asignador funciona de la siguiente manera:

1.  Opcionalmente, el PIN de salida llama a [**IMemInputPin:: GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements). Este método recupera los requisitos de búfer del PIN de entrada, como la alineación de memoria. En general, el PIN de salida debe respetar la solicitud del PIN de entrada, a menos que haya una buena razón para no hacerlo.
2.  Opcionalmente, el PIN de salida llama a [**IMemInputPin:: GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator). Este método solicita un asignador del PIN de entrada. El PIN de entrada proporciona uno o devuelve un código de error.
3.  El PIN de salida selecciona un asignador. Puede usar uno proporcionado por el PIN de entrada o crear el suyo propio.
4.  El PIN de salida llama a [**IMemAllocator:: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) para establecer las propiedades de asignador. Sin embargo, es posible que el asignador no respete las propiedades solicitadas. (Por ejemplo, esto puede ocurrir si el PIN de entrada proporciona el asignador). El asignador devuelve las propiedades reales como parámetro de salida en el método **SetProperties** .
5.  Outpin llama a [**IMemInputPin:: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) para informar al pin de entrada de la selección.
6.  El PIN de entrada debe llamar a [**IMemAllocator:: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getproperties) para comprobar si las propiedades de asignador son aceptables.
7.  El PIN de salida es responsable de confirmar y confirmar el asignador. Esto sucede cuando se inicia y se detiene el streaming.

En una conexión **IAsyncReader** , la negociación de asignador funciona de la siguiente manera:

1.  El PIN de entrada llama a [**IAsyncReader:: RequestAllocator**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) en el terminal de salida. El PIN de entrada especifica sus requisitos de búfer y, opcionalmente, proporciona un asignador.
2.  El PIN de salida selecciona un asignador. Puede usar el que proporciona el PIN de entrada, si existe, o crear uno propio.
3.  El PIN de salida devuelve el asignador como un parámetro saliente en el método **RequestAllocator** . El PIN de entrada debe comprobar las propiedades de asignador.
4.  El PIN de entrada es responsable de confirmar y confirmar el asignador.
5.  En cualquier momento durante el proceso de negociación del asignador, el pin puede producir un error en la conexión.
6.  Si el PIN de salida usa el asignador del PIN de entrada, puede usar ese asignador solo para proporcionar muestras a ese pin de entrada. El filtro propietario no debe utilizar el asignador para proporcionar ejemplos a otros PIN.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Proporcionar un asignador personalizado](providing-a-custom-allocator.md)
</dt> </dl>

 

 



