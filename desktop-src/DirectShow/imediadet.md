---
description: La interfaz IMediaDet recupera información sobre un archivo multimedia, como el número de flujos y el tipo de medio, la duración y la velocidad de fotogramas de cada flujo.
ms.assetid: 596fc84e-a88a-4e1b-aa48-b6dc9031db31
title: Interfaz IMediaDet (QEDIT. h)
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
ms.openlocfilehash: ca5c87a1424872491aba5dcf4e01011872e9ff36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679071"
---
# <a name="imediadet-interface"></a>Interfaz IMediaDet

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

La `IMediaDet` interfaz recupera información sobre un archivo multimedia, como el número de flujos y el tipo de medio, la duración y la velocidad de fotogramas de cada flujo. También contiene métodos para recuperar fotogramas individuales de una secuencia de vídeo. El objeto de [detección de medios (MediaDet)](media-detector--mediadet.md) expone esta interfaz.

Para obtener información acerca de un archivo mediante esta interfaz, realice los pasos siguientes:

1.  Cree una instancia del objeto MediaDet llamando a **CoCreateInstance**. El identificador de clase es CLSID \_ MediaDet.
2.  Llame a [**IMediaDet::p \_ nombre**](imediadet-put-filename.md) de archivo UT para especificar el nombre del archivo de código fuente.
3.  Llame a [**IMediaDet:: get \_ OutputStreams**](imediadet-get-outputstreams.md) para obtener el número de flujos de salida en el origen.
4.  Llame a [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md) para especificar una secuencia determinada.
5.  Llame a cualquiera de los métodos siguientes:
    -   [**IMediaDet:: get \_ velocidad de fotogramas**](imediadet-get-framerate.md)
    -   [**IMediaDet:: get \_ StreamLength**](imediadet-get-streamlength.md)
    -   [**IMediaDet:: get \_ StreamMediaType**](imediadet-get-streammediatype.md)
    -   [**IMediaDet:: get \_ StreamType**](imediadet-get-streamtype.md)

Para recuperar un fotograma de vídeo, llame a [**IMediaDet:: GetBitmapBits**](imediadet-getbitmapbits.md) o [**IMediaDet:: WriteBitmapBits**](imediadet-writebitmapbits.md). El marco devuelto siempre tiene el formato RGB de 24 bits.

> [!Note]  
> No use el mismo objeto MediaDet con varios archivos. Para obtener información o fotogramas de vídeo de más de un archivo, use instancias de MediaDet independientes.

 

La interfaz **IMediaDet** no admite formatos [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) , por lo que no puede usar esta interfaz para obtener campos entrelazados o información sobre el entrelazado. Además, si el descodificador de nivel superior solo admite **VIDEOINFOHEADER2**, no puede usar `IMediaDet` . Este es el caso de un descodificador MPEG-2, por ejemplo. Además, la `IMediaDet` interfaz omite cualquier flujo del archivo que no sea de vídeo o audio. Por ejemplo, si el archivo contiene una secuencia de audio, un flujo de datos y una secuencia de vídeo, el método **Get \_ OutputStreams** informará solo de dos flujos (audio y vídeo).

## <a name="members"></a>Miembros

La interfaz **IMediaDet** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IMediaDet** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IMediaDet** tiene estos métodos.



| Método                                                        | Descripción                                                                                                |
|:--------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md)  | Cambia el detector de medios al modo de agarre de mapa de bits y busca el gráfico de filtro en un tiempo especificado.<br/> |
| [**obtener \_ CurrentStream**](imediadet-get-currentstream.md)     | Recupera el número de secuencia utilizado actualmente por el detector de medios.<br/>                               |
| [**obtener \_ nombre de archivo**](imediadet-get-filename.md)               | Recupera el nombre del archivo de código fuente utilizado actualmente por el detector de medios.<br/>                     |
| [**obtener \_ filtro**](imediadet-get-filter.md)                   | Recupera un puntero al filtro de origen utilizado actualmente por el detector de medios.<br/>                  |
| [**obtener \_ velocidad de fotogramas**](imediadet-get-framerate.md)             | Recupera la velocidad de fotogramas de la secuencia actual.<br/>                                                 |
| [**obtener \_ OutputStreams**](imediadet-get-outputstreams.md)     | Recupera el número de secuencias de audio y vídeo contenidas en el origen de medios.<br/>                  |
| [**obtener \_ StreamLength**](imediadet-get-streamlength.md)       | Recupera la duración de la secuencia actual.<br/>                                                   |
| [**obtener \_ StreamMediaType**](imediadet-get-streammediatype.md) | Recupera el tipo de medio de la secuencia actual.<br/>                                                 |
| [**obtener \_ StreamType**](imediadet-get-streamtype.md)           | Recupera el identificador único global (GUID) para el tipo de medio de la secuencia actual.<br/>       |
| [**obtener \_ StreamTypeB**](imediadet-get-streamtypeb.md)         | Recupera una cadena que representa el GUID del tipo de medio para la secuencia actual.<br/>              |
| [**GetBitmapBits**](imediadet-getbitmapbits.md)              | Recupera un fotograma de vídeo en el tiempo medio especificado.<br/>                                            |
| [**GetSampleGrabber**](imediadet-getsamplegrabber.md)        | Recupera un puntero a la interfaz [**ISampleGrabber**](isamplegrabber.md) .<br/>                  |
| [**Put \_ CurrentStream**](imediadet-put-currentstream.md)     | Especifica el número de secuencia que va a usar el detector de medios.<br/>                                      |
| [**Put \_ FILENAME**](imediadet-put-filename.md)               | Especifica el nombre del archivo de origen para el detector de medios que se va a usar.<br/>                            |
| [**colocar \_ filtro**](imediadet-put-filter.md)                   | Especifica un filtro de origen para que lo use el detector de medios.<br/>                                        |
| [**WriteBitmapBits**](imediadet-writebitmapbits.md)          | Recupera un fotograma de vídeo en el tiempo medio especificado y lo escribe en un archivo.<br/>                    |



 

## <a name="remarks"></a>Observaciones

> [!Note]  
> El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>QEDIT. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



 

 
