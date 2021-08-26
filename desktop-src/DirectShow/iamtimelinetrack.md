---
description: La interfaz IAMTimelineTrack proporciona métodos para manipular objetos de seguimiento en DirectShow Editing Services (DES). Una pista contiene una lista de orígenes que se representan en la salida final.
ms.assetid: 42ac88f2-1361-413a-a9b0-95f5c32a7c3c
title: Interfaz IAMTimelineTrack (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9cc33facc22023d6e93c8dcfa3804d111d9c99f49be16d8271b09a7bf938b49e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965085"
---
# <a name="iamtimelinetrack-interface"></a>Interfaz IAMTimelineTrack

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

La `IAMTimelineTrack` interfaz proporciona métodos para manipular objetos de *seguimiento* en DirectShow [Editing Services](directshow-editing-services.md) (DES).

Una pista contiene una lista de orígenes que se representan en la salida final. Es posible que los orígenes dentro de la misma pista no se superpongan. Las pistas de vídeo pueden tener efectos y transiciones. El motor de representación aplica efectos antes de aplicar transiciones. Las pistas de audio pueden tener efectos, pero no transiciones. Para obtener más información, vea [El modelo de escala de tiempo](the-timeline-model.md).

Para crear un objeto de seguimiento, llame a [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) con el valor TIMELINE \_ MAJOR TYPE \_ \_ TRACK. Puede consultar el puntero **IAMTimelineObj** devuelto para la `IAMTimelineTrack` interfaz .

## <a name="members"></a>Miembros

La **interfaz IAMTimelineTrack** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IAMTimelineTrack también** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IAMTimelineTrack** tiene estos métodos.



| Método                                                          | Descripción                                                                                                                                          |
|:----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AreYouBlank**](iamtimelinetrack-areyoublank.md)             | Determina si la pista está en blanco (no contiene objetos de origen).<br/>                                                                       |
| [**GetNextSrc**](iamtimelinetrack-getnextsrc.md)               | Busca en la pista el siguiente origen que aparece en el momento especificado o posterior.<br/>                                                       |
| [**GetNextSrc2**](iamtimelinetrack-getnextsrc2.md)             | Busca en la pista el siguiente origen que aparece en el momento especificado o posterior, con el especificado como [**valor REFTIME.**](reftime.md)<br/> |
| [**GetNextSrcEx**](iamtimelinetrack-getnextsrcex.md)           | Recupera el siguiente origen después del origen especificado.<br/>                                                                                     |
| [**GetSourcesCount**](iamtimelinetrack-getsourcescount.md)     | Recupera el número de orígenes de la pista.<br/>                                                                                             |
| [**GetSrcAtTime**](iamtimelinetrack-getsrcattime.md)           | Recupera el objeto de origen más cercano a la hora especificada, según las condiciones de límite especificadas.<br/>                                |
| [**GetSrcAtTime2**](iamtimelinetrack-getsrcattime2.md)         | Recupera el objeto de origen más cercano a la hora especificada, dado como un [**valor REFTIME.**](reftime.md)<br/>                                   |
| [**InsertSpace**](iamtimelinetrack-insertspace.md)             | Divide los objetos que existen en el momento especificado e inserta espacio entre ellos.<br/>                                                       |
| [**InsertSpace2**](iamtimelinetrack-insertspace2.md)           | Divide los objetos que existen en el momento especificado e inserta espacio entre ellos, utilizando [**valores REFTIME.**](reftime.md)<br/>              |
| [**MoveEverythingBy**](iamtimelinetrack-moveeverythingby.md)   | No compatible.<br/>                                                                                                                            |
| [**MoveEverythingBy2**](iamtimelinetrack-moveeverythingby2.md) | No compatible.<br/>                                                                                                                            |
| [**SrcAdd**](iamtimelinetrack-srcadd.md)                       | Agrega un origen a la pista.<br/>                                                                                                               |
| [**ZeroBetween**](iamtimelinetrack-zerobetween.md)             | Quita todo de la pista entre las horas especificadas.<br/>                                                                            |
| [**ZeroBetween2**](iamtimelinetrack-zerobetween2.md)           | Quita todo el elemento de la pista entre las horas especificadas, dados como [**valores REFTIME.**](reftime.md)<br/>                                |



 

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



 

 
