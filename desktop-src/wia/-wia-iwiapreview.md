---
description: La interfaz IWiaPreview almacena en caché imágenes sin filtrar internamente y las pasa a través de filtros de procesamiento de imágenes.
ms.assetid: 8a51c42b-aa1d-4df0-aba3-6aeb8e1ca2cf
title: Interfaz IWiaPreview (Wia.h)
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
ms.openlocfilehash: e2672211e5c1a17fa360a6078069ae8260687dc896843ffb6bf572d9b7be8caa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119442075"
---
# <a name="iwiapreview-interface"></a>IWiaPreview (interfaz)

La **interfaz IWiaPreview** almacena en caché imágenes sin filtrar internamente y las pasa a través de filtros de procesamiento de imágenes.

## <a name="members"></a>Miembros

La **interfaz IWiaPreview** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IWiaPreview** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IWiaPreview** tiene estos métodos.



| Método                                                  | Descripción                                                                                                                                                                                 |
|:--------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Borrar**](-wia-iwiapreview-clear.md)                 | Libera la imagen sin filtrar almacenada en caché por el [**método IWiaPreview::GetNewPreview.**](-wia-iwiapreview-getnewpreview.md) También libera el filtro de procesamiento de imágenes. <br/>          |
| [**DetectRegions**](-wia-iwiapreview-detectregions.md) | Invoca el filtro de segmentación de controladores y pasa la imagen sin filtrar almacenada en caché por el método [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) al filtro. <br/> |
| [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md) | Almacena en caché internamente la imagen sin filtrar devuelta por el controlador. <br/>                                                                                                                |
| [**UpdatePreview**](-wia-iwiapreview-updatepreview.md) | Obtiene la imagen sin filtrar almacenada en caché por el [**método IWiaPreview::GetNewPreview.**](-wia-iwiapreview-getnewpreview.md) <br/>                                                            |



 

## <a name="remarks"></a>Observaciones

El método [**IWiaTransfer::D ownload**](-wia-iwiatransfer-download.md) llama automáticamente a este filtro.

La **interfaz IWiaPreview,** al igual que todas las interfaces del Modelo de objetos componentes (COM), hereda los métodos de [interfaz IUnknown.](/windows/win32/api/unknwn/nn-unknwn-iunknown)



| Métodos IUnknown                                        | Descripción                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Devuelve punteros a las interfaces compatibles. |
| [IUnknown::AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Incrementa el recuento de referencias.               |
| [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Reduce el recuento de referencias.               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
