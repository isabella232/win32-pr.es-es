---
description: 'Libera la imagen sin filtrar almacenada en memoria caché por el método IWiaPreview:: GetNewPreview. También libera el filtro de procesamiento de imágenes.'
ms.assetid: af94d27f-9d93-40e1-8d1a-e5546531a176
title: 'IWiaPreview:: CLEAR (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview.Clear
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 1ac2cc1f12cf6fd59111d0159684459c2500a854
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705691"
---
# <a name="iwiapreviewclear-method"></a>IWiaPreview:: CLEAR (método)

Libera la imagen sin filtrar almacenada en memoria caché por el método [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) . También libera el filtro de procesamiento de imágenes.

## <a name="syntax"></a>Sintaxis


```C++
void Clear();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

En **IWiaPreview:: Desactive** el componente Windows Image Acquisition (WIA) 2,0 Preview libera todos los punteros de interfaz que almacena. El componente de vista previa de WIA 2,0 mantiene las referencias a *pWiaItem2* y *pWiaTransferCallback* que se pasan a [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md). Para ser precisos, el componente de vista previa de WIA 2,0 mantiene una referencia a *pWiaItem2* y el filtro de procesamiento de imágenes del controlador, que a su vez mantiene una referencia a *pWiaTransferCallback*. En **IWiaPreview:: Clear**, el componente de vista previa de WIA 2,0 también libera su referencia a *pWiaItem2* y al filtro de procesamiento de imágenes, que a su vez libera su referencia a *pWiaTransferCallback*. El componente de vista previa de WIA 2,0 elimina la imagen almacenada en memoria caché y sin filtrar que almacena internamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




