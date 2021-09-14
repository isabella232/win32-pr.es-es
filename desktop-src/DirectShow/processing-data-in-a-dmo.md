---
description: Procesamiento de datos en un DMO
ms.assetid: 715482d9-23f4-40d0-9c09-7a81e148c543
title: Procesamiento de datos en un DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea9f5d5d820dc1467c25f9d411d46a9c66935e8b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160130"
---
# <a name="processing-data-in-a-dmo"></a>Procesamiento de datos en un DMO

En esta sección se explica cómo procesar un flujo de datos mediante un DMO. Los pasos enumerados en esta sección son el comportamiento predeterminado; todas las DDO deben admitir los métodos descritos aquí. Estos métodos usan búferes independientes para la entrada y salida. Algunas DDO también admiten el procesamiento local, mediante un solo búfer. Para obtener más información sobre el procesamiento local, vea [Procesamiento en local.](in-place-processing.md)

**Asignación de búferes**

El cliente es responsable de toda la asignación del búfer. Después de establecer los tipos de medios en el DMO, consulte el DMO los requisitos de búfer de cada secuencia. Pueden cambiar en función del tipo de medio. Para cada secuencia, llame al [**método IMediaObject::GetInputSizeInfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputsizeinfo) [**o IMediaObject::GetOutputSizeInfo.**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputsizeinfo) Estos métodos devuelven la siguiente información:

-   Tamaño mínimo del búfer, en bytes.
-   Requisitos de alineación, si los hay. Un búfer se alinea si la dirección de inicio es un múltiplo de algún entero especificado.
-   La cantidad máxima de datos que DMO para buscar. Este número solo se aplica a los flujos de entrada. Para algunos tipos de datos (por ejemplo, la codificación MPEG), es posible DMO tener que mirar hacia delante en la secuencia. El valor de lookahead indica cuántos datos de entrada DMO necesitará antes de poder generar la salida.

El cliente debe asignar búferes que coincidan con estos requisitos. Además, el DMO puede tener requisitos sobre cómo el cliente empaqueta los datos de entrada. Por ejemplo, el DMO puede requerir que cada búfer contenga exactamente una muestra (o fotograma de vídeo). Para determinar estos requisitos, llame [**al método IMediaObject::GetInputStreamInfo.**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputstreaminfo) El [**método IMediaObject::GetOutputStreamInfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputstreaminfo) devuelve información similar sobre un flujo de salida.

En el modelo de streaming predeterminado, el cliente no pasa punteros de búfer sin procesar al DMO. En su lugar, usa un objeto COM ligero que expone la [**interfaz IMediaBuffer.**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) La **interfaz IMediaBuffer** actúa como un contenedor COM para un bloque de memoria. Dado que es un objeto COM, admite el recuento de referencias, lo que ayuda a garantizar que los búferes no se liberan mientras siguen en uso.

> [!Note]  
> La **interfaz IMediaBuffer** sirve una función similar a la **interfaz IMediaSample** en DirectShow.

 

El cliente debe implementar el **objeto IMediaBuffer.** Para obtener más información, [vea Implementing IMediaBuffer](implementing-imediabuffer.md).

**Procesamiento de los datos**

Para procesar datos, haga lo siguiente:

1.  Para cada flujo de entrada, rellene un búfer con datos de entrada.
2.  Llame [**a IMediaObject::P rocessInput para**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processinput) entregar cada búfer.
3.  Llame [**a IMediaObject::P rocessOutput para**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processoutput) procesar los datos. Este método toma una matriz de búferes, uno para cada flujo de salida.
4.  Repita la repetición hasta que no haya más datos de entrada.

El **método ProcessInput** acepta la entrada de una secuencia a la vez. Normalmente, el método devuelve inmediatamente y DMO contiene un recuento de referencias en el **objeto IMediaBuffer.** Libera el objeto después de que procese todos los datos del búfer o cuando la aplicación vacía el DMO. No vuelva a usar un búfer hasta que el DMO lo haya liberado. Para determinar si un flujo de entrada puede aceptar más datos, llame al [**método IMediaObject::GetInputStatus.**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputstatus) Este método devuelve la DMO \_ INPUT \_ STATUSF \_ ACCEPT DATA si la secuencia puede aceptar más \_ entradas.

El **método ProcessOutput** genera la salida de todos los flujos de salida a la vez. La aplicación pasa una matriz de estructuras DMO [**\_ OUTPUT DATA \_ \_ BUFFER,**](/previous-versions/windows/desktop/api/Mediaobj/ns-mediaobj-dmo_output_data_buffer) una para cada flujo de salida. Cada estructura de la matriz tiene un puntero a un **objeto IMediaBuffer.** El DMO escribe tantos datos de salida como sea posible en los búferes. También establece varias marcas para notificar el estado de la operación. La DMO OUTPUT DATA BUFFERF INCOMPLETE indica que el \_ DMO puede generar más salida a partir de la entrada \_ \_ \_ existente. En ese caso, el cliente puede volver a llamar a **ProcessOutput.** De lo contrario, debe llamar **a ProcessInput** con más datos de entrada. El DMO nunca modifica los datos de los búferes de entrada; solo escribe en los búferes de salida.

Después de haber entregado todos los datos a un flujo de entrada, llame al [**método IMediaObject::D iscontinuity.**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-discontinuity) El DMO no acepta más entradas en esa secuencia hasta que procese el resultado restante (o vacíe el DMO).

En cualquier momento después de comenzar el streaming, el DMO puede recibir entrada o generar salida, o ambos. Por lo tanto, **GetInputStatus** devuelve DMO \_ INPUT \_ STATUSF ACCEPT DATA o ProcessOutput devuelve DMO \_ OUTPUT DATA \_  \_ \_ \_ BUFFERF \_ INCOMPLETE. La aplicación mantiene el flujo de datos probando estas marcas y llamando a **ProcessInput** o **ProcessOutput** en consecuencia. Para interrumpir el flujo de datos, llame al [**método IMediaObject::Flush.**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-flush) Este método hace que el DMO descarte los búferes que mantiene internamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Hospedaje directo de un DMO](directly-hosting-a-dmo.md)
</dt> <dt>

[Procesamiento en local](in-place-processing.md)
</dt> </dl>

 

 



