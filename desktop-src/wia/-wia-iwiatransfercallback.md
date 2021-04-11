---
description: La interfaz IWiaTransferCallback recibe las devoluciones de llamada durante una transferencia de datos.
ms.assetid: 8fcaccf5-4d7b-4984-97ec-ec8c838a8360
title: Interfaz IWiaTransferCallback (WIA. h)
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
ms.openlocfilehash: 918482ebcb24f2638a006ab1bbc452ea28ff61e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154392"
---
# <a name="iwiatransfercallback-interface"></a>Interfaz IWiaTransferCallback

La interfaz **IWiaTransferCallback** recibe las devoluciones de llamada durante una transferencia de datos.

## <a name="members"></a>Miembros

La interfaz **IWiaTransferCallback** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IWiaTransferCallback** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IWiaTransferCallback** tiene estos métodos.



| Método                                                                 | Descripción                                                              |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md)       | Obtiene una nueva secuencia para el elemento especificado. <br/>                    |
| [**TransferCallback**](-wia-iwiatransfercallback-transfercallback.md) | Proporciona el progreso y otras notificaciones durante una transferencia. <br/> |



 

## <a name="remarks"></a>Observaciones

Los desarrolladores de filtros de procesamiento de imágenes deben implementar esta interfaz y la interfaz [**IWiaImageFilter**](-wia-iwiaimagefilter.md) .

La interfaz **IWiaTransferCallback** , al igual que todas las interfaces del modelo de objetos componentes (com), hereda los métodos de interfaz [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .



| Métodos IUnknown                                        | Descripción                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Devuelve punteros a las interfaces compatibles. |
| [IUnknown:: AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Incrementa el recuento de referencias.               |
| [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Reduce el recuento de referencias.               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 
