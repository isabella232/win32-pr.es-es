---
description: La interfaz IWiaTransferCallback recibe devoluciones de llamada durante una transferencia de datos.
ms.assetid: 8fcaccf5-4d7b-4984-97ec-ec8c838a8360
title: Interfaz IWiaTransferCallback (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransferCallback
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 20c577530785de3e05d00d4674556fbcd03cb69832b164e12dc703108d23c58a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119549645"
---
# <a name="iwiatransfercallback-interface"></a>Interfaz IWiaTransferCallback

La **interfaz IWiaTransferCallback recibe** devoluciones de llamada durante una transferencia de datos.

## <a name="members"></a>Miembros

La **interfaz IWiaTransferCallback** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IWiaTransferCallback** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IWiaTransferCallback** tiene estos métodos.



| Método                                                                 | Descripción                                                              |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md)       | Obtiene una nueva secuencia para el elemento especificado. <br/>                    |
| [**TransferCallback**](-wia-iwiatransfercallback-transfercallback.md) | Proporciona el progreso y otras notificaciones durante una transferencia. <br/> |



 

## <a name="remarks"></a>Comentarios

Los desarrolladores de filtros de procesamiento de imágenes deben implementar esta interfaz y [**la interfaz IWiaImageFilter.**](-wia-iwiaimagefilter.md)

La **interfaz IWiaTransferCallback,** al igual que todas las interfaces del Modelo de objetos componentes (COM), hereda los métodos de [interfaz IUnknown.](/windows/win32/api/unknwn/nn-unknwn-iunknown)



| Métodos IUnknown                                        | Descripción                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Devuelve punteros a las interfaces compatibles. |
| [IUnknown::AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Incrementa el recuento de referencias.               |
| [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Reduce el recuento de referencias.               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>       |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



 

 
