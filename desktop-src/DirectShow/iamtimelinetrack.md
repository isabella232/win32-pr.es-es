---
description: La interfaz IAMTimelineTrack proporciona métodos para manipular objetos de seguimiento en los servicios de edición de DirectShow (DES). Una pista contiene una lista de orígenes que se representan en la salida final.
ms.assetid: 42ac88f2-1361-413a-a9b0-95f5c32a7c3c
title: Interfaz IAMTimelineTrack (QEDIT. h)
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
ms.openlocfilehash: 71003694d33b33980fb262f06f6b2e7aa55a70d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691028"
---
# <a name="iamtimelinetrack-interface"></a>Interfaz IAMTimelineTrack

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

La `IAMTimelineTrack` interfaz proporciona métodos para manipular objetos de *seguimiento* en los [servicios de edición de DirectShow](directshow-editing-services.md) (des).

Una pista contiene una lista de orígenes que se representan en la salida final. Es posible que los orígenes dentro de la misma pista no se superpongan. Las pistas de vídeo pueden tener efectos y transiciones. El motor de representación aplica efectos antes de aplicar las transiciones. Las pistas de audio pueden tener efectos, pero no transiciones. Para obtener más información, vea [el modelo Timeline](the-timeline-model.md).

Para crear un objeto Track, llame a [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) con el valor de \_ tipo principal de la escala de tiempo \_ \_ . Puede consultar el puntero **IAMTimelineObj** devuelto para la `IAMTimelineTrack` interfaz.

## <a name="members"></a>Miembros

La interfaz **IAMTimelineTrack** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMTimelineTrack** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IAMTimelineTrack** tiene estos métodos.



| Método                                                          | Descripción                                                                                                                                          |
|:----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AreYouBlank**](iamtimelinetrack-areyoublank.md)             | Determina si la pista está en blanco (no contiene objetos de origen).<br/>                                                                       |
| [**GetNextSrc**](iamtimelinetrack-getnextsrc.md)               | Busca en la pista el siguiente origen que aparece en el momento especificado o en una versión posterior.<br/>                                                       |
| [**GetNextSrc2**](iamtimelinetrack-getnextsrc2.md)             | Busca en la pista el siguiente origen que aparece en el momento especificado o posterior, con la especificada como valor de [**REFTIME**](reftime.md) .<br/> |
| [**GetNextSrcEx**](iamtimelinetrack-getnextsrcex.md)           | Recupera el siguiente origen después del origen especificado.<br/>                                                                                     |
| [**GetSourcesCount**](iamtimelinetrack-getsourcescount.md)     | Recupera el número de orígenes de la pista.<br/>                                                                                             |
| [**GetSrcAtTime**](iamtimelinetrack-getsrcattime.md)           | Recupera el objeto de origen más cercano a la hora especificada, de acuerdo con las condiciones de límite especificadas.<br/>                                |
| [**GetSrcAtTime2**](iamtimelinetrack-getsrcattime2.md)         | Recupera el objeto de origen más cercano al tiempo especificado, dado como un valor [**REFTIME**](reftime.md) .<br/>                                   |
| [**InsertSpace**](iamtimelinetrack-insertspace.md)             | Divide los objetos que existen en el momento especificado e inserta espacio entre ellos.<br/>                                                       |
| [**InsertSpace2**](iamtimelinetrack-insertspace2.md)           | Divide los objetos que existen en el momento especificado e inserta espacio entre ellos, utilizando los valores de [**REFTIME**](reftime.md) .<br/>              |
| [**MoveEverythingBy**](iamtimelinetrack-moveeverythingby.md)   | No se admite.<br/>                                                                                                                            |
| [**MoveEverythingBy2**](iamtimelinetrack-moveeverythingby2.md) | No se admite.<br/>                                                                                                                            |
| [**SrcAdd**](iamtimelinetrack-srcadd.md)                       | Agrega un origen a la pista.<br/>                                                                                                               |
| [**ZeroBetween**](iamtimelinetrack-zerobetween.md)             | Quita todo de la pista entre las horas especificadas.<br/>                                                                            |
| [**ZeroBetween2**](iamtimelinetrack-zerobetween2.md)           | Quita todo de la pista entre las horas especificadas, dado como valores de [**REFTIME**](reftime.md) .<br/>                                |



 

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



 

 
