---
description: La interfaz IAMTimelineSrc proporciona métodos para manipular y establecer propiedades en objetos de origen en DirectShow Editing Services (DES).
ms.assetid: 39a64718-1fac-4d90-8340-b712d3bad2ec
title: Interfaz IAMTimelineSrc (Qedit.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126891929"
---
# <a name="iamtimelinesrc-interface"></a>Interfaz IAMTimelineSrc

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

La `IAMTimelineSrc` interfaz proporciona métodos para manipular y establecer propiedades en objetos de origen en DirectShow Editing [Services](directshow-editing-services.md) (DES). Un objeto de origen representa una secuencia de un origen multimedia.

Puede usar una parte de los datos dentro de un archivo de origen estableciendo los tiempos de inicio y de detención de medios. Estos valores especifican el principio y el final del objeto de origen, en relación con el origen multimedia original. Los tiempos multimedia pueden diferir de los tiempos de inicio y de detección del objeto en la escala de tiempo, lo que permite una reproducción en movimiento rápido o lento. (Con los orígenes de audio, se produce el cambio de tono).

Para crear un objeto de origen, llame a [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) con el valor TIMELINE \_ MAJOR TYPE \_ \_ SOURCE. Puede consultar el puntero [**IAMTimelineObj**](iamtimelineobj.md) devuelto para la **interfaz IAMTimelineSrc.** Para obtener más información, vea [Construir una escala de tiempo](constructing-a-timeline.md) y Trabajar con [orígenes.](working-with-sources.md)

## <a name="members"></a>Members

La **interfaz IAMTimelineSrc** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IAMTimelineSrc** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IAMTimelineSrc** tiene estos métodos.



| Método                                                    | Descripción                                                                                              |
|:----------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [**FixMediaTimes**](iamtimelinesrc-fixmediatimes.md)     | Redondea los valores de tiempo especificados al límite de marco más cercano.<br/>                               |
| [**FixMediaTimes2**](iamtimelinesrc-fixmediatimes2.md)   | Redondea los valores de tiempo especificados, dados **como valores REFTIME,** al límite de marco más cercano.<br/> |
| [**GetDefaultFPS**](iamtimelinesrc-getdefaultfps.md)     | Recupera la velocidad de fotogramas predeterminada del objeto de origen.<br/>                                             |
| [**GetMediaLength**](iamtimelinesrc-getmedialength.md)   | Recupera la longitud del medio de este objeto de origen.<br/>                                             |
| [**GetMediaLength2**](iamtimelinesrc-getmedialength2.md) | Recupera la longitud del medio de este objeto de origen, como un **valor REFTIME.**<br/>                     |
| [**GetMediaName**](iamtimelinesrc-getmedianame.md)       | Recupera el nombre del archivo de origen representado por este objeto de origen.<br/>                      |
| [**GetMediaTimes**](iamtimelinesrc-getmediatimes.md)     | Recupera las horas de inicio y de detenerse de los medios.<br/>                                                     |
| [**GetMediaTimes2**](iamtimelinesrc-getmediatimes2.md)   | Recupera las horas de inicio y de devolución de medios, como **valores REFTIME.**<br/>                              |
| [**GetStreamNumber**](iamtimelinesrc-getstreamnumber.md) | Recupera el número de secuencia actual para el objeto de origen.<br/>                                    |
| [**GetStretchMode**](iamtimelinesrc-getstretchmode.md)   | Recupera el modo de ajuste de un origen de vídeo.<br/>                                                 |
| [**IsNormalRate**](iamtimelinesrc-isnormalrate.md)       | Indica si el clip se reproducirá a la velocidad de reproducción normal.<br/>                             |
| [**ModifyStopTime**](iamtimelinesrc-modifystoptime.md)   | Establece la hora de detenerse, en relación con la escala de tiempo.<br/>                                                 |
| [**ModifyStopTime2**](iamtimelinesrc-modifystoptime2.md) | Establece la hora de devolución, como **un valor REFTIME.**<br/>                                                   |
| [**SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md)     | Establece la velocidad de fotogramas predeterminada del objeto de origen.<br/>                                                  |
| [**SetMediaLength**](iamtimelinesrc-setmedialength.md)   | Especifica la duración del archivo de origen.<br/>                                                    |
| [**SetMediaLength2**](iamtimelinesrc-setmedialength2.md) | Especifica la duración del archivo de origen, como un **valor REFTIME.**<br/>                            |
| [**SetMediaName**](iamtimelinesrc-setmedianame.md)       | Especifica el nombre del archivo de origen representado por este objeto de origen.<br/>                      |
| [**SetMediaTimes**](iamtimelinesrc-setmediatimes.md)     | Establece las horas de detención e inicio de los medios.<br/>                                                          |
| [**SetMediaTimes2**](iamtimelinesrc-setmediatimes2.md)   | Establece las horas de detención e inicio del medio, **como valores REFTIME.**<br/>                                   |
| [**SetStreamNumber**](iamtimelinesrc-setstreamnumber.md) | Especifica qué secuencia se va a leer del archivo de origen asociado a este objeto de origen.<br/>       |
| [**SetStretchMode**](iamtimelinesrc-setstretchmode.md)   | Establece el modo de ajuste de un origen de vídeo.<br/>                                                      |
| [**SpliceWithNext**](iamtimelinesrc-splicewithnext.md)   | Une este objeto de origen a otro objeto de origen.<br/>                                            |



 

## <a name="remarks"></a>Observaciones

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de Microsoft Windows para [Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



 

 
