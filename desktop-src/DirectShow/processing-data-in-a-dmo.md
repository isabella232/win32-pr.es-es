---
description: Procesamiento de datos en una DMO
ms.assetid: 715482d9-23f4-40d0-9c09-7a81e148c543
title: Procesamiento de datos en una DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea9f5d5d820dc1467c25f9d411d46a9c66935e8b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906670"
---
# <a name="processing-data-in-a-dmo"></a>Procesamiento de datos en una DMO

En esta sección se explica cómo procesar un flujo de datos mediante DMO. Los pasos enumerados en esta sección son el comportamiento predeterminado; todos los DMOs deben admitir los métodos que se describen aquí. Estos métodos usan búferes independientes para la entrada y la salida. Algunos DMOs también admiten el procesamiento en contexto mediante un único búfer. Para obtener más información sobre el procesamiento en contexto, consulte [procesamiento en contexto](in-place-processing.md).

**Asignar búferes**

El cliente es responsable de toda la asignación de búfer. Después de establecer los tipos de medios en DMO, consulte en DMO los requisitos de búfer de cada secuencia. Estos pueden cambiar en función del tipo de medio. Para cada flujo, llame al método [**IMediaObject:: GetInputSizeInfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputsizeinfo) o [**IMediaObject:: GetOutputSizeInfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputsizeinfo) . Estos métodos devuelven la siguiente información:

-   Tamaño mínimo del búfer, en bytes.
-   Requisitos de alineación, si los hay. Un búfer se alinea si la dirección de inicio es un múltiplo de algún entero especificado.
-   La cantidad máxima de datos que DMO conservará para la búsqueda anticipada. Este número se aplica solo a los flujos de entrada. En el caso de algunos tipos de datos (por ejemplo, codificación MPEG), es posible que un DMO tenga que buscar hacia delante en la secuencia. El valor de búsqueda anticipada indica cuántos datos de entrada necesitará DMO antes de poder generar resultados.

El cliente debe asignar búferes que coincidan con estos requisitos. Además, DMO podría tener requisitos sobre cómo el cliente empaqueta los datos de entrada. Por ejemplo, DMO podría requerir que cada búfer contenga exactamente un ejemplo (o fotograma de vídeo). Para determinar estos requisitos, llame al método [**IMediaObject:: GetInputStreamInfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputstreaminfo) . El método [**IMediaObject:: GetOutputStreamInfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputstreaminfo) devuelve información similar sobre un flujo de salida.

En el modelo de streaming predeterminado, el cliente no pasa punteros de búfer sin formato a DMO. En su lugar, utiliza un objeto COM ligero que expone la interfaz [**IMediaBuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) . La interfaz **IMediaBuffer** actúa como un contenedor com para un bloque de memoria. Dado que se trata de un objeto COM, admite el recuento de referencias, lo que ayuda a garantizar que los búferes no se liberen mientras se siguen usando.

> [!Note]  
> La interfaz **IMediaBuffer** sirve para una función similar a la interfaz **IMediaSample** de DirectShow.

 

El cliente debe implementar el objeto **IMediaBuffer** . Para obtener más información, consulte [implementación de IMediaBuffer](implementing-imediabuffer.md).

**Procesar los datos**

Para procesar datos, haga lo siguiente:

1.  Para cada flujo de entrada, rellene un búfer con datos de entrada.
2.  Llame a [**IMediaObject::P rocessinput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processinput) para proporcionar cada búfer.
3.  Llame a [**IMediaObject::P rocessoutput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processoutput) para procesar los datos. Este método toma una matriz de búferes, uno para cada flujo de salida.
4.  Repita el procedimiento hasta que no haya más datos de entrada.

El método **ProcessInput** acepta la entrada de un flujo cada vez. Normalmente, el método vuelve inmediatamente y el DMO contiene un recuento de referencias en el objeto **IMediaBuffer** . Libera el objeto después de procesar todos los datos en el búfer, o cuando la aplicación vacía DMO. No vuelva a usar un búfer hasta que DMO lo haya liberado. Para determinar si un flujo de entrada puede aceptar más datos, llame al método [**IMediaObject:: GetInputStatus**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputstatus) . Este método devuelve la marca de datos de aceptación de STATUSF de entrada de DMO \_ \_ \_ \_ si la secuencia puede aceptar más entradas.

El método **ProcessOutput** genera una salida para todos los flujos de salida a la vez. La aplicación pasa una matriz de estructuras [**de \_ \_ \_ búfer de datos de salida de DMO**](/previous-versions/windows/desktop/api/Mediaobj/ns-mediaobj-dmo_output_data_buffer) , una para cada flujo de salida. Cada estructura de la matriz tiene un puntero a un objeto **IMediaBuffer** . DMO escribe tantos datos de salida como pueden en los búferes. También establece varias marcas para notificar el estado de la operación. La marca de datos de salida de DMO \_ \_ \_ BUFFERF \_ incompleta indica que DMO puede generar más resultados a partir de la entrada existente. En ese caso, el cliente puede volver a llamar a **ProcessOutput** . De lo contrario, debe llamar a **ProcessInput** con más datos de entrada. DMO nunca modifica los datos de los búferes de entrada; escribe solo en los búferes de salida.

Una vez que haya entregado todos los datos a un flujo de entrada, llame al método [**IMediaObject::D iscontinuity**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-discontinuity) . DMO no acepta ninguna entrada adicional a esa secuencia hasta que se procesa la salida restante (o se vacía el DMO).

En cualquier momento después del inicio del streaming, DMO puede recibir entradas o producir salidas, o ambas cosas. Por lo tanto, **GetInputStatus** devuelve los \_ datos de aceptación de \_ STATUSF de entrada de DMO \_ \_ o **ProcessOutput** devuelve datos de salida de DMO \_ \_ \_ BUFFERF \_ incompletos. La aplicación mantiene los datos en el flujo probando estas marcas y llamando a **ProcessInput** o **ProcessOutput** en consecuencia. Para interrumpir el flujo de datos, llame al método [**IMediaObject:: Flush**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-flush) . Este método hace que DMO descarte todos los búferes que contiene internamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Hospedar directamente un DMO](directly-hosting-a-dmo.md)
</dt> <dt>

[Procesamiento en contexto](in-place-processing.md)
</dt> </dl>

 

 



