---
description: Usar secuencias multimedia en aplicaciones
ms.assetid: 73cfe89b-df46-445a-92c7-2f7323672441
title: Usar secuencias multimedia en aplicaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f30dab204bc7b0bddbdc293708daecbe0558e8f9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104003377"
---
# <a name="using-multimedia-streams-in-applications"></a>Usar secuencias multimedia en aplicaciones

> [!Note]  
> Estas API están en desuso. Las aplicaciones deben usar el filtro de [**enganche de ejemplo**](sample-grabber-filter.md) o implementar un filtro personalizado para obtener datos de un gráfico de filtros de DirectShow.

 

Las interfaces de transmisión por secuencias de multimedia simplifican considerablemente el proceso de manipulación de datos multimedia mediante la eliminación de la dependencia de características específicas del origen de hardware o software y la compatibilidad con todos los formatos multimedia de Microsoft DirectX®. Los flujos abstraen los datos a un nivel muy alto; las aplicaciones pueden incluso trasladar los datos de un flujo a otro sin tener que saber nada sobre el formato de los datos.

Realice los pasos siguientes para crear una secuencia multimedia.

1.  Cree la secuencia multimedia. El método de creación e inicialización de la secuencia es específico de la arquitectura. DirectShow admite la interfaz [**IAMMultiMediaStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream) , que se usa para inicializar la secuencia. Otras implementaciones de servidor en proceso de [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) se crearán e inicializarán usando mecanismos diferentes.
2.  Una vez inicializado el objeto de secuencia multimedia, la aplicación usará **QueryInterface** para recuperar la interfaz **IMultiMediaStream** para el objeto. Use esta interfaz para determinar las propiedades de la secuencia y enumerar las propias secuencias. Puede recuperar una secuencia específica llamando al método [**IMultiMediaStream:: GetMediaStream**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-getmediastream) con un identificador de propósito específico. MSPID \_ PrimaryVideo y MSPID \_ PrimaryAudio, que representan las secuencias de audio y vídeo principales, son los identificadores de propósito más usados.
3.  Llame a **IUnknown:: QueryInterface** para una interfaz específica del tipo de archivo multimedia de la secuencia. Si desea representar una secuencia de vídeo, por ejemplo, recupere su interfaz [**IDirectDrawMediaStream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream) . Las interfaces específicas del medio definen métodos adicionales necesarios para sacar el máximo partido de las capacidades de un formato.
4.  Cree uno o más ejemplos a partir de los datos de la secuencia. Cada flujo multimedia admite el método [**IMediaStream:: CreateSharedSample**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imediastream-createsharedsample) para la creación de un ejemplo. El ejemplo resultante es compatible con la interfaz [**IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample) , que proporciona control sobre el ejemplo y sus características. Normalmente, la secuencia de medios admite un método específico del formato de creación de ejemplo que es más eficaz que los métodos **IStreamSample** antes mencionados. Por ejemplo, **IDirectDrawMediaStream** puede crear muestras adjuntas a una superficie DirectDraw deseada y a un rectángulo de recorte. En algunas situaciones, sin embargo, debe controlar los datos sin tener que conocer su formato de datos. Si desea transmitir datos independientemente de su formato, use el método **IMediaStream:: CreateSharedSample** para crear los ejemplos de datos.
5.  Después de crear todos los ejemplos de secuencias deseados, inicie la secuencia llamando al método [**IMultiMediaStream:: SetState**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-setstate) y pase la \_ marca de ejecución STREAMSTATE como su parámetro.
6.  Llame a [**IStreamSample:: Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) para actualizar el ejemplo de secuencia. Cuando el método **IStreamSample:: Update** se cierra, puede tener acceso a los datos del ejemplo. Si desea que un desencadenador sea una llamada de función o un evento específico cuando se devuelva la actualización, pase los punteros adecuados al método **IStreamSample:: Update** .

Para obtener más información sobre las interfaces de streaming multimedia, consulte [streaming multimedia](multimedia-streaming.md).

 

 



