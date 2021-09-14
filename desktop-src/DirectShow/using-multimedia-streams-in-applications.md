---
description: Uso de Secuencias multimedia en aplicaciones
ms.assetid: 73cfe89b-df46-445a-92c7-2f7323672441
title: Uso de Secuencias multimedia en aplicaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f30dab204bc7b0bddbdc293708daecbe0558e8f9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160109"
---
# <a name="using-multimedia-streams-in-applications"></a>Uso de Secuencias multimedia en aplicaciones

> [!Note]  
> Estas API están en desuso. Las aplicaciones deben usar el [**filtro Sample Grabber**](sample-grabber-filter.md) o implementar un filtro personalizado para obtener datos de un DirectShow gráfico de filtros.

 

Las interfaces de streaming multimedia simplifican en gran medida el proceso de manipulación de datos multimedia al eliminar la dependencia de características específicas del origen de hardware o software y proporcionar compatibilidad con todos los formatos multimedia de Microsoft DirectX®. Secuencias abstraer los datos a un nivel muy alto; Las aplicaciones incluso pueden mover datos de un flujo a otro sin saber nada sobre el formato de los datos.

Realice los pasos siguientes para crear una secuencia multimedia.

1.  Cree la secuencia multimedia. El método de creación e inicialización de la secuencia es específico de la arquitectura. DirectShow admite la [**interfaz IAMMultiMediaStream,**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream) que se usa para inicializar la secuencia. Otras implementaciones de servidor en proceso [**de IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) se crearán e inicializarán mediante distintos mecanismos.
2.  Una vez inicializado el objeto de secuencia multimedia, la aplicación usará **QueryInterface** para recuperar la **interfaz IMultiMediaStream** del objeto. Use esta interfaz para determinar las propiedades de la secuencia y enumerar las propias secuencias. Puede recuperar una secuencia específica llamando al [**método IMultiMediaStream::GetMediaStream**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-getmediastream) con un identificador de propósito específico. MSPID \_ PrimaryVideo y MSPID PrimaryAudio, que representan las secuencias de audio y vídeo principales, son los id. de uso más \_ usados.
3.  Llame **a IUnknown::QueryInterface para** obtener una interfaz específica del tipo de medio de la secuencia. Si quiere representar una secuencia de vídeo, por ejemplo, recupere su [**interfaz IDirectDrawMediaStream.**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream) Las interfaces específicas del medio definen métodos adicionales necesarios para aprovechar al máximo las funcionalidades de un formato.
4.  Cree uno o varios ejemplos a partir de los datos de flujo. Cada secuencia multimedia admite el [**método IMediaStream::CreateSharedSample**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imediastream-createsharedsample) para la creación de ejemplos. El ejemplo resultante admite la [**interfaz IStreamSample,**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample) que proporciona control sobre el ejemplo y sus características. Normalmente, la secuencia multimedia admite un método específico del formato de creación de muestras que es más eficaz que los métodos **IStreamSample mencionados** anteriormente. **IDirectDrawMediaStream,** por ejemplo, puede crear ejemplos adjuntos a una superficie y un rectángulo de recorte de DirectDraw deseados. Sin embargo, en algunas situaciones, debe controlar los datos sin conocer su formato de datos. Si desea transmitir datos independientemente de su formato, use el método **IMediaStream::CreateSharedSample** para crear los ejemplos de datos.
5.  Después de crear todos los ejemplos de flujo deseados, inicie la secuencia mediante una llamada al método [**IMultiMediaStream::SetState**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-setstate) y pase la marca STREAMSTATE \_ RUN como parámetro.
6.  Llame [**a IStreamSample::Update para**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) actualizar el ejemplo de secuencia. Cuando se **cierra el método IStreamSample::Update,** puede acceder a los datos del ejemplo. Si desea que un desencadenador llame a un evento o función específicos cuando se devuelva la actualización, pase los punteros adecuados al **método IStreamSample::Update.**

Para obtener más información sobre las interfaces de streaming multimedia, vea [Streaming multimedia.](multimedia-streaming.md)

 

 



