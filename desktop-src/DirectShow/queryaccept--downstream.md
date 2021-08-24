---
description: QueryAccept (bajada)
ms.assetid: 3ca30f62-c320-40ea-9bf5-022abad912c4
title: QueryAccept (bajada)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ec5c26209839f0dcd8351cc9a7ca84227faa2289d44d46c2c321fce0429e3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747744"
---
# <a name="queryaccept-downstream"></a>QueryAccept (bajada)

Este mecanismo permite que un pin de salida proponga un nuevo formato a su elemento del mismo nivel de bajada. El nuevo formato no debe requerir un tamaño de búfer mayor. El pin de salida hace lo siguiente:

1.  Llama [**a IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) o [**IPinConnection::D ynamicQueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-dynamicqueryaccept) en el pin de nivel inferior para comprobar si el otro pin puede aceptar el nuevo tipo de medio (consulte la ilustración, paso A).
2.  Si el valor devuelto del paso 1 es S OK, el pin asocia el \_ tipo de medio al ejemplo siguiente. Para ello, primero llama a [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) para obtener el ejemplo (B). A continuación, [**llama a IMediaSample::SetMediaType para**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) adjuntar el tipo de medio a ese ejemplo (C). Al adjuntar el tipo de medio al ejemplo, el filtro indica que el formato ha cambiado, empezando por ese ejemplo.
3.  El pin entrega el ejemplo (D).
4.  Cuando el filtro de bajada recibe el ejemplo, llama a [**IMediaSample::GetMediaType para**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) recuperar el nuevo tipo de medio.

    ![queryaccept (bajada)](images/dynformat3.png)

Todos los pines admiten el `QueryAccept` método . Sin embargo, este método es ligeramente ambiguo, ya que un valor devuelto de S OK no siempre garantiza que se pueda cambiar el formato mientras el gráfico \_ está activo. Algunos filtros pueden devolver S \_ OK pero rechazar el cambio si el gráfico está activo. El **método DynamicQueryAccept,** que es compatible con algunos pines de entrada, define explícitamente S OK para que el pin pueda cambiar los formatos \_ mientras está activo. Si un pin de entrada admite la **interfaz IPinConnection,** debe llamar a **DynamicQueryAccept en** lugar de `QueryAccept` a .

En la mayoría de los casos, este mecanismo no permite cambios drásticos en el formato, como cambiar la profundidad de bits. Una situación en la que se puede usar es cuando un descodificador de vídeo cambia las paletas. Los detalles básicos del formato permanecen iguales, como las dimensiones de la imagen y la profundidad de bits, pero el nuevo tipo de medio tiene un conjunto diferente de entradas de paleta.

**Nota de implementación**

En las DirectShow base, [**CBasePin::QueryAccept**](cbasepin-queryaccept.md) llama al método **CheckMediaType,** al que también se llama durante la conexión de pin inicial. En el caso de un filtro de transformación, el método **CheckMediaType** del pin de entrada siempre debe comprobar si el pin de salida está conectado y, si es así, si el tipo de medio de entrada es compatible con el tipo de medio de salida. Por lo tanto, es probable que esta implementación sea válida para `QueryAccept` . Si no es así, debe `QueryAccept` invalidar para realizar las comprobaciones adicionales que sean necesarias. Además, tenga en cuenta que [**la clase CTransformFilter**](ctransformfilter.md) encapsula esta lógica dentro de los **métodos CheckInputType** **y CheckTransform.** Por otro lado, la clase [**CTransInPlaceFilter**](ctransinplacefilter.md) siempre llama al siguiente filtro ascendente `QueryAccept` o descendente.

El [**método CBaseInputPin::Receive**](cbaseinputpin-receive.md) busca un tipo de medio en el ejemplo entrante y, si lo hay, llama a **CheckMediaType**. Sin embargo, no actualiza el miembro **m \_ mt** del pin, que contiene el tipo de medio actual. Cuando el filtro procese el ejemplo, debe comprobar si el ejemplo tiene un tipo de medio. Si hay un nuevo tipo, probablemente deba almacenarlo, ya sea llamando a **SetMediaType** en el pin o estableciendo el valor **de m \_ mt** directamente. Por otro lado, la clase [**CVideoTransformFilter,**](cvideotransformfilter.md) que está diseñada para filtros de transformación de vídeo, almacena el tipo de medio cuando cambia. Para obtener más información, vea el código fuente [**de CVideoTransformFilter::Receive**](cvideotransformfilter-receive.md) en DirectShow biblioteca de clases base.

En algunos casos, es posible que simplemente pase la llamada de nivel inferior y, a continuación, adjunte el tipo de medio al ejemplo de salida y deje que el filtro de nivel inferior `QueryAccept` controle el cambio de formato.

 

 



