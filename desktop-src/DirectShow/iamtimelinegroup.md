---
description: La interfaz IAMTimelineGroup establece y recupera propiedades en grupos de DirectShow Editing Services (DES). Un grupo contiene una o varias pistas, y posiblemente una o varias composiciones, que a su vez contienen clips de origen de un tipo uniforme, como vídeo o audio. Los grupos son las composiciones más destacadas de una escala de tiempo y también exponen la interfaz IAMTimelineComp. Una escala de tiempo puede contener varios grupos. Cada grupo tiene los siguientes atributos. Tipo de medio asociado. Velocidad de fotogramas a la que se representa el grupo, en fotogramas por segundo (FPS). Todas las ediciones se producen a la vez redondeadas al límite del marco más cercano, tal y como se define en la configuración de FPS del grupo. Nivel de prioridad para escribir archivos con varias secuencias del mismo tipo de medio (por ejemplo, un archivo AVI de dos secuencias de vídeo). Para crear un objeto de grupo, llame a IAMTimeline::CreateEmptyNode con el valor TIMELINE \_ MAJOR \_ TYPE \_ GROUP. Puede consultar el puntero IAMTimelineObj devuelto para la interfaz IAMTimelineGroup.
ms.assetid: c24e5e0a-43a5-4ba7-ac28-6e2ebb341a38
title: Interfaz IAMTimelineGroup (Qedit.h)
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
ms.openlocfilehash: 9356e3edef0b61c119ec4cca774e9ec5976ac3732e0f0a508d103bc22bb0fef0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118155511"
---
# <a name="iamtimelinegroup-interface"></a>Interfaz IAMTimelineGroup

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

La interfaz establece y recupera propiedades en grupos de `IAMTimelineGroup` [DirectShow Editing Services](directshow-editing-services.md) (DES).

Un grupo contiene una o varias pistas, y posiblemente una o varias composiciones, que a su vez contienen clips de origen de un tipo uniforme, como vídeo o audio. Los grupos son las composiciones más destacadas de una escala de tiempo y también exponen la [**interfaz IAMTimelineComp.**](iamtimelinecomp.md) Una escala de tiempo puede contener varios grupos.

Cada grupo tiene los siguientes atributos.

-   Tipo de medio asociado.
-   Velocidad de fotogramas a la que se representa el grupo, en fotogramas por segundo (FPS). Todas las ediciones se producen a la vez redondeadas al límite del marco más cercano, tal y como se define en la configuración de FPS del grupo.
-   Nivel de prioridad para escribir archivos con varias secuencias del mismo tipo de medio (por ejemplo, un archivo AVI de dos secuencias de vídeo).

Para crear un objeto de grupo, llame [**a IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) con el valor TIMELINE \_ MAJOR TYPE \_ \_ GROUP. Puede consultar el puntero [**IAMTimelineObj devuelto**](iamtimelineobj.md) para la **interfaz IAMTimelineGroup.**

## <a name="members"></a>Miembros

La **interfaz IAMTimelineGroup** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IAMTimelineGroup** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IAMTimelineGroup** tiene estos métodos.



| Método                                                                            | Descripción                                                                                     |
|:----------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**ClearRecompressFormatDirty**](iamtimelinegroup-clearrecompressformatdirty.md) | No compatible.<br/>                                                                       |
| [**GetGroupName**](iamtimelinegroup-getgroupname.md)                             | Recupera el nombre definido por la aplicación del grupo.<br/>                                 |
| [**GetMediaType**](iamtimelinegroup-getmediatype.md)                             | Recupera el tipo de medio sin comprimir para el grupo.<br/>                                 |
| [**GetOutputBuffering**](iamtimelinegroup-getoutputbuffering.md)                 | Recupera el número de fotogramas representados de antemano durante la versión preliminar.<br/>                   |
| [**GetOutputFPS**](iamtimelinegroup-getoutputfps.md)                             | Recupera la velocidad de fotogramas de salida de este grupo.<br/>                                       |
| [**GetPreviewMode**](iamtimelinegroup-getpreviewmode.md)                         | Recupera el modo de vista previa del grupo.<br/>                                            |
| [**GetPriority**](iamtimelinegroup-getpriority.md)                               | Recupera la prioridad del grupo.<br/>                                                      |
| [**GetSmartRecompressFormat**](iamtimelinegroup-getsmartrecompressformat.md)     | Recupera el formato de compresión actual para la recompresión inteligente.<br/>                    |
| [**GetTimeline**](iamtimelinegroup-gettimeline.md)                               | Recupera la escala de tiempo a la que pertenece este grupo.<br/>                                  |
| [**IsRecompressFormatDirty**](iamtimelinegroup-isrecompressformatdirty.md)       | No compatible.<br/>                                                                       |
| [**IsSmartRecompressFormatSet**](iamtimelinegroup-issmartrecompressformatset.md) | Determina si se estableció un formato de compresión inteligente para el grupo.<br/>                 |
| [**SetGroupName**](iamtimelinegroup-setgroupname.md)                             | Establece el nombre definido por la aplicación del grupo.<br/>                                      |
| [**SetMediaType**](iamtimelinegroup-setmediatype.md)                             | Establece el tipo de medio sin comprimir para el grupo.<br/>                                      |
| [**SetMediaTypeForVB**](iamtimelinegroup-setmediatypeforvb.md)                   | Especifica el tipo de medio de grupo para los clientes de Automation.<br/>                              |
| [**SetOutputBuffering**](iamtimelinegroup-setoutputbuffering.md)                 | Especifica el número de fotogramas representados de antemano durante la versión preliminar.<br/>                   |
| [**SetOutputFPS**](iamtimelinegroup-setoutputfps.md)                             | Establece la velocidad de fotogramas de salida sin comprimir para este grupo.<br/>                              |
| [**SetPreviewMode**](iamtimelinegroup-setpreviewmode.md)                         | Establece el modo de vista previa del grupo.<br/>                                                 |
| [**SetRecompFormatFromSource**](iamtimelinegroup-setrecompformatfromsource.md)   | Establece el formato de recompresión de vídeo mediante el formato de compresión de un archivo de origen.<br/> |
| [**SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md)     | Especifica un formato de compresión que se usará para la recompresión inteligente.<br/>                       |
| [**SetTimeline**](iamtimelinegroup-settimeline.md)                               | No compatible.<br/>                                                                       |



 

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



 

 
