---
description: La interfaz IAMTimelineSrc proporciona métodos para manipular y establecer las propiedades de los objetos de origen en los servicios de edición de DirectShow (DES).
ms.assetid: 39a64718-1fac-4d90-8340-b712d3bad2ec
title: Interfaz IAMTimelineSrc (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 25733b1353bc0cbd92c40335a8d342473b03a806
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679053"
---
# <a name="iamtimelinesrc-interface"></a>Interfaz IAMTimelineSrc

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

La `IAMTimelineSrc` interfaz proporciona métodos para manipular y establecer las propiedades de los objetos de origen en los [servicios de edición de DirectShow](directshow-editing-services.md) (des). Un objeto de origen representa una secuencia de un origen de multimedia.

Puede usar una parte de los datos de un archivo de código fuente estableciendo las horas de inicio y detención del medio. Estos valores especifican el principio y el final del objeto de origen, en relación con el origen del medio original. Los tiempos de los medios pueden diferir de los tiempos de inicio y detención del objeto en la escala de tiempo, lo que permite la reproducción rápida o lenta. (Con orígenes de audio, se produce el cambio de tono).

Para crear un objeto de origen, llame a [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) con el valor de origen de tipo principal de la escala de tiempo \_ \_ \_ . Puede consultar el puntero [**IAMTimelineObj**](iamtimelineobj.md) devuelto para la interfaz **IAMTimelineSrc** . Para obtener más información, vea [crear una escala de tiempo](constructing-a-timeline.md) y [trabajar con orígenes](working-with-sources.md).

## <a name="members"></a>Miembros

La interfaz **IAMTimelineSrc** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMTimelineSrc** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IAMTimelineSrc** tiene estos métodos.



| Método                                                    | Descripción                                                                                              |
|:----------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [**FixMediaTimes**](iamtimelinesrc-fixmediatimes.md)     | Redondea los valores de hora especificados al límite de fotogramas más cercano.<br/>                               |
| [**FixMediaTimes2**](iamtimelinesrc-fixmediatimes2.md)   | Redondea los valores de hora especificados, dados como valores de **REFTIME** , al límite de fotogramas más cercano.<br/> |
| [**GetDefaultFPS**](iamtimelinesrc-getdefaultfps.md)     | Recupera la velocidad de fotogramas predeterminada del objeto de origen.<br/>                                             |
| [**GetMediaLength**](iamtimelinesrc-getmedialength.md)   | Recupera la longitud del medio de este objeto de origen.<br/>                                             |
| [**GetMediaLength2**](iamtimelinesrc-getmedialength2.md) | Recupera la longitud del medio de este objeto de origen, como un valor de **REFTIME** .<br/>                     |
| [**GetMediaName**](iamtimelinesrc-getmedianame.md)       | Recupera el nombre del archivo de código fuente representado por este objeto de origen.<br/>                      |
| [**GetMediaTimes**](iamtimelinesrc-getmediatimes.md)     | Recupera las horas de inicio y detención del medio.<br/>                                                     |
| [**GetMediaTimes2**](iamtimelinesrc-getmediatimes2.md)   | Recupera las horas de inicio y detención del medio, como valores de **REFTIME** .<br/>                              |
| [**GetStreamNumber**](iamtimelinesrc-getstreamnumber.md) | Recupera el número de secuencia actual para el objeto de origen.<br/>                                    |
| [**GetStretchMode**](iamtimelinesrc-getstretchmode.md)   | Recupera el modo de ajuste de una fuente de vídeo.<br/>                                                 |
| [**IsNormalRate**](iamtimelinesrc-isnormalrate.md)       | Indica si el clip se reproducirá a la velocidad de reproducción normal.<br/>                             |
| [**ModifyStopTime**](iamtimelinesrc-modifystoptime.md)   | Establece la hora de detención, relativa a la escala de tiempo.<br/>                                                 |
| [**ModifyStopTime2**](iamtimelinesrc-modifystoptime2.md) | Establece la hora de detención, como un valor de **REFTIME** .<br/>                                                   |
| [**SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md)     | Establece la velocidad de fotogramas predeterminada del objeto de origen.<br/>                                                  |
| [**SetMediaLength**](iamtimelinesrc-setmedialength.md)   | Especifica la duración del archivo de código fuente.<br/>                                                    |
| [**SetMediaLength2**](iamtimelinesrc-setmedialength2.md) | Especifica la duración del archivo de código fuente, como un valor de **REFTIME** .<br/>                            |
| [**SetMediaName**](iamtimelinesrc-setmedianame.md)       | Especifica el nombre del archivo de origen representado por este objeto de origen.<br/>                      |
| [**SetMediaTimes**](iamtimelinesrc-setmediatimes.md)     | Establece las horas de detención e inicio del medio.<br/>                                                          |
| [**SetMediaTimes2**](iamtimelinesrc-setmediatimes2.md)   | Establece las horas de detención e inicio del medio, como valores de **REFTIME** .<br/>                                   |
| [**SetStreamNumber**](iamtimelinesrc-setstreamnumber.md) | Especifica la secuencia que se va a leer del archivo de código fuente asociado a este objeto de origen.<br/>       |
| [**SetStretchMode**](iamtimelinesrc-setstretchmode.md)   | Establece el modo de stretch de un origen de vídeo.<br/>                                                      |
| [**SpliceWithNext**](iamtimelinesrc-splicewithnext.md)   | Une este objeto de origen a otro objeto de origen.<br/>                                            |



 

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



 

 
