---
description: QueryAccept (Downstream)
ms.assetid: 3ca30f62-c320-40ea-9bf5-022abad912c4
title: QueryAccept (Downstream)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9015e0a246abb9fb996c0771e4bc935cccda054d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104556622"
---
# <a name="queryaccept-downstream"></a>QueryAccept (Downstream)

Este mecanismo permite a un PIN de salida proponer un nuevo formato a su par inferior. El nuevo formato no debe requerir un tamaño de búfer mayor. El PIN de salida hace lo siguiente:

1.  Llama a [**IPin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) o [**IPinConnection::D ynamicqueryaccept**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-dynamicqueryaccept) en el PIN de bajada, para comprobar si el otro pin puede aceptar el nuevo tipo de medio (vea la ilustración, paso A).
2.  Si el valor devuelto del paso 1 es S \_ correcto, el PIN asocia el tipo de medio al siguiente ejemplo. Para ello, primero llama a [**IMemAllocator:: getBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) para obtener el ejemplo (B). A continuación, llama a [**IMediaSample:: SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) para adjuntar el tipo de medio a ese ejemplo (C). Al adjuntar el tipo de archivo multimedia al ejemplo, el filtro indica que el formato ha cambiado, empezando por ese ejemplo.
3.  El PIN proporciona el ejemplo (D).
4.  Cuando el filtro de nivel inferior recibe el ejemplo, llama a [**IMediaSample:: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) para recuperar el nuevo tipo de archivo multimedia.

    ![queryaccept (Downstream)](images/dynformat3.png)

Todos los pin admiten el `QueryAccept` método. Sin embargo, este método es ligeramente ambiguo, ya que un valor devuelto de S \_ OK no garantiza siempre que se pueda cambiar el formato mientras el gráfico esté activo. Algunos filtros pueden devolver S \_ correcto, pero rechazar el cambio si el gráfico está activo. El método **DynamicQueryAccept** , que es compatible con algunos PIN de entrada, define explícitamente S \_ OK para indicar que el pin puede cambiar los formatos mientras está activo. Si un PIN de entrada es compatible con la interfaz **IPinConnection** , debe llamar a **DynamicQueryAccept** en lugar de `QueryAccept` .

En la mayoría de los casos, este mecanismo no permite cambios drásticos en el formato, como cambiar la profundidad de bits. Una situación en la que se puede usar es cuando un descodificador de vídeo cambia las paletas. Los detalles básicos del formato permanecen invariables, como las dimensiones de la imagen y la profundidad de bits, pero el nuevo tipo de medio tiene un conjunto diferente de entradas de la paleta.

**Nota de implementación**

En las clases base de DirectShow, [**CBasePin:: QueryAccept**](cbasepin-queryaccept.md) llama al método **CheckMediaType** , al que también se llama durante la conexión inicial del PIN. En el caso de un filtro de transformación, el método **CheckMediaType** del PIN de entrada siempre debe comprobar si el PIN de salida está conectado y, en caso afirmativo, si el tipo de medio de entrada es compatible con el tipo de medio de salida. Por lo tanto, es probable que esta implementación sea válida para `QueryAccept` . Si no es así, debe reemplazar `QueryAccept` para realizar cualquier comprobación adicional que sea necesaria. Además, tenga en cuenta que la clase [**CTransformFilter**](ctransformfilter.md) encapsula esta lógica dentro de los métodos **CheckInputType** y **CheckTransform** . La clase [**CTransInPlaceFilter**](ctransinplacefilter.md) , por otro lado, siempre llama a `QueryAccept` en el siguiente filtro ascendente o descendente.

El método [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) comprueba un tipo de medio en el ejemplo entrante y, si lo hay, llama a **CheckMediaType**. Sin embargo, no actualiza el miembro **m \_ MT** del PIN, que contiene el tipo de medio actual. Cuando el filtro procesa el ejemplo, debe comprobar si hay un tipo de medio en el ejemplo. Si hay un nuevo tipo, probablemente necesitará almacenarlo, ya sea llamando a **SetMediaType** en el código PIN o estableciendo el valor de **m \_ MT** directamente. Por otro lado, la clase [**CVideoTransformFilter**](cvideotransformfilter.md) , que está diseñada para los filtros de transformación de vídeo, almacena el tipo de medio cuando cambia. Para obtener más información, vea el código fuente de [**CVideoTransformFilter:: Receive**](cvideotransformfilter-receive.md) en la biblioteca de clases base de DirectShow.

En algunos casos, podría simplemente pasar la `QueryAccept` llamada de nivel inferior, adjuntar el tipo de medio al ejemplo de salida y dejar que el filtro de nivel inferior controle el cambio de formato.

 

 



