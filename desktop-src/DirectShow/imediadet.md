---
description: La interfaz IMediaDet recupera información sobre un archivo multimedia, como el número de secuencias, y el tipo de medio, la duración y la velocidad de fotogramas de cada secuencia.
ms.assetid: 596fc84e-a88a-4e1b-aa48-b6dc9031db31
title: Interfaz IMediaDet (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: abdf913ab74e6f0f988449a14b84b5be109b9380ebbfb2473edd4a9980f3c577
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819038"
---
# <a name="imediadet-interface"></a>Interfaz IMediaDet

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

La interfaz recupera información sobre un archivo multimedia, como el número de secuencias y el tipo de medio, la duración y la velocidad de `IMediaDet` fotogramas de cada secuencia. También contiene métodos para recuperar fotogramas individuales de una secuencia de vídeo. El [objeto Media Detector (MediaDet)](media-detector--mediadet.md) expone esta interfaz.

Para obtener información sobre un archivo mediante esta interfaz, realice los pasos siguientes:

1.  Cree una instancia del objeto MediaDet llamando a **CoCreateInstance.** El identificador de clase es CLSID \_ MediaDet.
2.  Llame [**a IMediaDet::p ut \_ Filename**](imediadet-put-filename.md) para especificar el nombre del archivo de origen.
3.  Llame [**a IMediaDet::get \_ OutputStreams**](imediadet-get-outputstreams.md) para obtener el número de flujos de salida en el origen.
4.  Llame [**a IMediaDet::p ut \_ CurrentStream**](imediadet-put-currentstream.md) para especificar una secuencia determinada.
5.  Llame a cualquiera de los métodos siguientes:
    -   [**IMediaDet::get \_ FrameRate**](imediadet-get-framerate.md)
    -   [**IMediaDet::get \_ StreamLength**](imediadet-get-streamlength.md)
    -   [**IMediaDet::get \_ StreamMediaType**](imediadet-get-streammediatype.md)
    -   [**IMediaDet::get \_ StreamType**](imediadet-get-streamtype.md)

Para recuperar un fotograma de vídeo, llame a [**IMediaDet::GetBitmapBits**](imediadet-getbitmapbits.md) o [**IMediaDet::WriteBitmapBits**](imediadet-writebitmapbits.md). El marco devuelto siempre está en formato RGB de 24 bits.

> [!Note]  
> No use el mismo objeto MediaDet con varios archivos. Para obtener información o fotogramas de vídeo de más de un archivo, use instancias de MediaDet independientes.

 

La **interfaz IMediaDet** no admite formatos [**VIDEOINFOHEADER2,**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) por lo que no puede usar esta interfaz para obtener campos entrelazados o información sobre el entrelazado. Además, si el descodificador ascendente solo admite **VIDEOINFOHEADER2**, no puede usar `IMediaDet` . Este podría ser el caso de un descodificador MPEG-2, por ejemplo. Además, la `IMediaDet` interfaz omite las secuencias del archivo que no son de vídeo o audio. Por ejemplo, si el archivo contiene una secuencia de audio, una secuencia de datos y una secuencia de vídeo, el método **\_ get OutputStreams** solo mostrará dos secuencias (el audio y el vídeo).

## <a name="members"></a>Miembros

La **interfaz IMediaDet** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IMediaDet** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IMediaDet** tiene estos métodos.



| Método                                                        | Descripción                                                                                                |
|:--------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md)  | Cambia el detector de medios al modo de captura de mapa de bits y busca el gráfico de filtro a una hora especificada.<br/> |
| [**get \_ CurrentStream**](imediadet-get-currentstream.md)     | Recupera el número de secuencia utilizado actualmente por el detector de medios.<br/>                               |
| [**get \_ Filename**](imediadet-get-filename.md)               | Recupera el nombre del archivo de origen utilizado actualmente por el detector de medios.<br/>                     |
| [**get \_ Filter**](imediadet-get-filter.md)                   | Recupera un puntero al filtro de origen utilizado actualmente por el detector de medios.<br/>                  |
| [**get \_ FrameRate**](imediadet-get-framerate.md)             | Recupera la velocidad de fotogramas de la secuencia actual.<br/>                                                 |
| [**get \_ OutputStreams**](imediadet-get-outputstreams.md)     | Recupera el número de secuencias de audio y vídeo contenidas en el origen multimedia.<br/>                  |
| [**get \_ StreamLength**](imediadet-get-streamlength.md)       | Recupera la duración de la secuencia actual.<br/>                                                   |
| [**get \_ StreamMediaType**](imediadet-get-streammediatype.md) | Recupera el tipo de medio de la secuencia actual.<br/>                                                 |
| [**get \_ StreamType**](imediadet-get-streamtype.md)           | Recupera el identificador único global (GUID) para el tipo de medio de la secuencia actual.<br/>       |
| [**get \_ StreamTypeB**](imediadet-get-streamtypeb.md)         | Recupera una cadena que representa el GUID del tipo de medio para la secuencia actual.<br/>              |
| [**GetBitmapBits**](imediadet-getbitmapbits.md)              | Recupera un fotograma de vídeo en el tiempo de medios especificado.<br/>                                            |
| [**GetSampleGrabber**](imediadet-getsamplegrabber.md)        | Recupera un puntero a la [**interfaz ISampleGrabber.**](isamplegrabber.md)<br/>                  |
| [**put \_ CurrentStream**](imediadet-put-currentstream.md)     | Especifica el número de secuencia que debe usar el detector de medios.<br/>                                      |
| [**put \_ Filename**](imediadet-put-filename.md)               | Especifica el nombre del archivo de origen que debe usar el detector de medios.<br/>                            |
| [**put \_ Filter**](imediadet-put-filter.md)                   | Especifica un filtro de origen para el detector de medios que se usará.<br/>                                        |
| [**WriteBitmapBits**](imediadet-writebitmapbits.md)          | Recupera un fotograma de vídeo en el momento del medio especificado y lo escribe en un archivo.<br/>                    |



 

## <a name="remarks"></a>Comentarios

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



 

 
