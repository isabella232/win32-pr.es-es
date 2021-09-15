---
description: Libera la imagen sin filtrar almacenada en caché por el método IWiaPreview::GetNewPreview. También libera el filtro de procesamiento de imágenes.
ms.assetid: af94d27f-9d93-40e1-8d1a-e5546531a176
title: Método IWiaPreview::Clear (Wia.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360619"
---
# <a name="iwiapreviewclear-method"></a>IWiaPreview::Clear (Método)

Libera la imagen sin filtrar almacenada en caché por el [**método IWiaPreview::GetNewPreview.**](-wia-iwiapreview-getnewpreview.md) También libera el filtro de procesamiento de imágenes.

## <a name="syntax"></a>Sintaxis


```C++
void Clear();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

En **IWiaPreview::Clear** the Windows Image Acquisition (WIA) 2.0 Preview Component libera todos los punteros de interfaz que almacena. El componente de versión preliminar de WIA 2.0 mantiene las referencias a *pWiaItem2* y *pWiaTransferCallback* pasados a [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md). Para ser precisos, el componente de versión preliminar de WIA 2.0 mantiene una referencia a *pWiaItem2* y el filtro de procesamiento de imágenes del controlador, que a su vez mantiene una referencia a *pWiaTransferCallback*. En **IWiaPreview::Clear**, el componente de versión preliminar de WIA 2.0 también publica su referencia a *pWiaItem2* y al filtro de procesamiento de imágenes, que a su vez libera su referencia a *pWiaTransferCallback*. El componente de versión preliminar de WIA 2.0 elimina la imagen almacenada en caché sin filtrar que almacena internamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 




