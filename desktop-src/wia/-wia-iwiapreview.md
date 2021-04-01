---
description: La interfaz IWiaPreview almacena en caché las imágenes sin filtrar internamente y las pasa a través de filtros de procesamiento de imágenes.
ms.assetid: 8a51c42b-aa1d-4df0-aba3-6aeb8e1ca2cf
title: Interfaz IWiaPreview (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 5e1c01daae4e86fa18c087b67bf902daaf6f8793
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275461"
---
# <a name="iwiapreview-interface"></a>Interfaz IWiaPreview

La interfaz **IWiaPreview** almacena en caché las imágenes sin filtrar internamente y las pasa a través de filtros de procesamiento de imágenes.

## <a name="members"></a>Miembros

La interfaz **IWiaPreview** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IWiaPreview** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IWiaPreview** tiene estos métodos.



| Método                                                  | Descripción                                                                                                                                                                                 |
|:--------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Claridad**](-wia-iwiapreview-clear.md)                 | Libera la imagen sin filtrar almacenada en memoria caché por el método [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) . También libera el filtro de procesamiento de imágenes. <br/>          |
| [**DetectRegions**](-wia-iwiapreview-detectregions.md) | Invoca el filtro de segmentación de controladores y pasa al filtro la imagen sin filtrar almacenada en memoria caché por el método [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) . <br/> |
| [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md) | Almacena en caché internamente la imagen sin filtrar devuelta por el controlador. <br/>                                                                                                                |
| [**UpdatePreview**](-wia-iwiapreview-updatepreview.md) | Obtiene la imagen sin filtrar almacenada en memoria caché por el método [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) . <br/>                                                            |



 

## <a name="remarks"></a>Observaciones

El método [**IWiaTransfer::D scargar**](-wia-iwiatransfer-download.md) llama automáticamente a este filtro.

La interfaz **IWiaPreview** , al igual que todas las interfaces del modelo de objetos componentes (com), hereda los métodos de interfaz [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .



| Métodos IUnknown                                        | Descripción                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Devuelve punteros a las interfaces compatibles. |
| [IUnknown:: AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Incrementa el recuento de referencias.               |
| [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Reduce el recuento de referencias.               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
