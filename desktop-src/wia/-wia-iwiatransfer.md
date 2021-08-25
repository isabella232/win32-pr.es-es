---
description: La interfaz IWiaTransfer proporciona transferencia de datos basada en secuencias.
ms.assetid: 7bc6d3b8-9bf0-4b77-aa2b-b7c64c5730c0
title: Interfaz IWiaTransfer (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: ff19619b1f0ab46658d0876792248befd6940c525d5c7da1b3331f6ca1a8c12e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813905"
---
# <a name="iwiatransfer-interface"></a>Interfaz IWiaTransfer

La **interfaz IWiaTransfer** proporciona transferencia de datos basada en secuencias.

## <a name="members"></a>Miembros

La **interfaz IWiaTransfer** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IWiaTransfer también** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IWiaTransfer** tiene estos métodos.



| Método                                                                 | Descripción                                                                                 |
|:-----------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**Cancelar**](-wia-iwiatransfer-cancel.md)                             | Cancela la operación de transferencia actual. <br/>                                         |
| [**Descargar**](-wia-iwiatransfer-download.md)                         | Inicia una descarga de datos al autor de la llamada. <br/>                                        |
| [**Información de formato de EnumWIA \_ \_**](-wia-iwiatransfer-enumwia-format-info.md) | Crea un enumerador para los formatos de transferencia que admite el dispositivo WIA 2.0.<br/> |
| [**Cargar**](-wia-iwiatransfer-upload.md)                             | Inicia una carga de datos de un solo elemento desde el autor de la llamada. <br/>                       |



 

## <a name="remarks"></a>Comentarios

La **interfaz IWiaTransfer,** al igual que todas las interfaces del Modelo de objetos componentes (COM), hereda los métodos de [interfaz IUnknown.](/windows/win32/api/unknwn/nn-unknwn-iunknown)



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



 

 
