---
description: 'La interfaz IAMTimelineGroup establece y recupera propiedades en grupos en los servicios de edición de DirectShow (DES). Un grupo contiene una o más pistas y, posiblemente, una o más composiciones, que a su vez contienen clips de origen de un tipo uniforme, como vídeo o audio. Los grupos son las composiciones más arriba en una escala de tiempo y también exponen la interfaz IAMTimelineComp. Una escala de tiempo puede contener varios grupos. Cada grupo tiene los siguientes atributos. Un tipo de medio asociado. Velocidad de fotogramas en la que se representa el grupo, en fotogramas por segundo (FPS). Todas las ediciones se producen en un momento redondeado al límite de fotogramas más cercano, según se define en la configuración de FPS del grupo. Un nivel de prioridad, para escribir archivos con varias secuencias del mismo tipo de medio (por ejemplo, un archivo AVI de dos secuencias de vídeo). Para crear un objeto de grupo, llame a IAMTimeline:: CreateEmptyNode con el grupo de tipo de escala de tiempo de valor \_ principal \_ \_ . Puede consultar el puntero IAMTimelineObj devuelto para la interfaz IAMTimelineGroup.'
ms.assetid: c24e5e0a-43a5-4ba7-ac28-6e2ebb341a38
title: Interfaz IAMTimelineGroup (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e82a11db65183e343048f594a7457c0a8febf8bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691063"
---
# <a name="iamtimelinegroup-interface"></a>Interfaz IAMTimelineGroup

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

La `IAMTimelineGroup` interfaz establece y recupera propiedades en grupos en los [servicios de edición de DirectShow](directshow-editing-services.md) (des).

Un grupo contiene una o más pistas y, posiblemente, una o más composiciones, que a su vez contienen clips de origen de un tipo uniforme, como vídeo o audio. Los grupos son las composiciones más arriba en una escala de tiempo y también exponen la interfaz [**IAMTimelineComp**](iamtimelinecomp.md) . Una escala de tiempo puede contener varios grupos.

Cada grupo tiene los siguientes atributos.

-   Un tipo de medio asociado.
-   Velocidad de fotogramas en la que se representa el grupo, en fotogramas por segundo (FPS). Todas las ediciones se producen en un momento redondeado al límite de fotogramas más cercano, según se define en la configuración de FPS del grupo.
-   Un nivel de prioridad, para escribir archivos con varias secuencias del mismo tipo de medio (por ejemplo, un archivo AVI de dos secuencias de vídeo).

Para crear un objeto de grupo, llame a [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) con el grupo de tipo de escala de tiempo de valor \_ principal \_ \_ . Puede consultar el puntero [**IAMTimelineObj**](iamtimelineobj.md) devuelto para la interfaz **IAMTimelineGroup** .

## <a name="members"></a>Miembros

La interfaz **IAMTimelineGroup** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMTimelineGroup** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IAMTimelineGroup** tiene estos métodos.



| Método                                                                            | Descripción                                                                                     |
|:----------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**ClearRecompressFormatDirty**](iamtimelinegroup-clearrecompressformatdirty.md) | No se admite.<br/>                                                                       |
| [**GetGroupName**](iamtimelinegroup-getgroupname.md)                             | Recupera el nombre definido por la aplicación del grupo.<br/>                                 |
| [**GetMediaType**](iamtimelinegroup-getmediatype.md)                             | Recupera el tipo de medio sin comprimir para el grupo.<br/>                                 |
| [**GetOutputBuffering**](iamtimelinegroup-getoutputbuffering.md)                 | Recupera el número de fotogramas representados de antemano durante la vista previa.<br/>                   |
| [**GetOutputFPS**](iamtimelinegroup-getoutputfps.md)                             | Recupera la velocidad de fotogramas de salida de este grupo.<br/>                                       |
| [**GetPreviewMode**](iamtimelinegroup-getpreviewmode.md)                         | Recupera el modo de vista previa para el grupo.<br/>                                            |
| [**GetPriority (**](iamtimelinegroup-getpriority.md)                               | Recupera la prioridad del grupo.<br/>                                                      |
| [**GetSmartRecompressFormat**](iamtimelinegroup-getsmartrecompressformat.md)     | Recupera el formato de compresión actual para la recompresión inteligente.<br/>                    |
| [**GetTimeline**](iamtimelinegroup-gettimeline.md)                               | Recupera la escala de tiempo a la que pertenece este grupo.<br/>                                  |
| [**IsRecompressFormatDirty**](iamtimelinegroup-isrecompressformatdirty.md)       | No se admite.<br/>                                                                       |
| [**IsSmartRecompressFormatSet**](iamtimelinegroup-issmartrecompressformatset.md) | Determina si se ha establecido un formato de compresión inteligente para el grupo.<br/>                 |
| [**SetGroupName**](iamtimelinegroup-setgroupname.md)                             | Establece el nombre definido por la aplicación del grupo.<br/>                                      |
| [**SetMediaType**](iamtimelinegroup-setmediatype.md)                             | Establece el tipo de medio sin comprimir para el grupo.<br/>                                      |
| [**SetMediaTypeForVB**](iamtimelinegroup-setmediatypeforvb.md)                   | Especifica el tipo de medio de grupo para los clientes de automatización.<br/>                              |
| [**SetOutputBuffering**](iamtimelinegroup-setoutputbuffering.md)                 | Especifica el número de fotogramas representados de antemano durante la vista previa.<br/>                   |
| [**SetOutputFPS**](iamtimelinegroup-setoutputfps.md)                             | Establece la velocidad de fotogramas de salida sin comprimir para este grupo.<br/>                              |
| [**SetPreviewMode**](iamtimelinegroup-setpreviewmode.md)                         | Establece el modo de vista previa para el grupo.<br/>                                                 |
| [**SetRecompFormatFromSource**](iamtimelinegroup-setrecompformatfromsource.md)   | Establece el formato de recompresión de vídeo con el formato de compresión de un archivo de código fuente.<br/> |
| [**SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md)     | Especifica un formato de compresión que se va a utilizar para la recompresión inteligente.<br/>                       |
| [**SetTimeline**](iamtimelinegroup-settimeline.md)                               | No se admite.<br/>                                                                       |



 

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



 

 
