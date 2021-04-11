---
description: La interfaz IWiaTransfer proporciona transferencia de datos basada en secuencias.
ms.assetid: 7bc6d3b8-9bf0-4b77-aa2b-b7c64c5730c0
title: Interfaz IWiaTransfer (WIA. h)
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
ms.openlocfilehash: 623cc21591289f4c1fff33cabe1d504b3682708c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275457"
---
# <a name="iwiatransfer-interface"></a>Interfaz IWiaTransfer

La interfaz **IWiaTransfer** proporciona transferencia de datos basada en secuencias.

## <a name="members"></a>Miembros

La interfaz **IWiaTransfer** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IWiaTransfer** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IWiaTransfer** tiene estos métodos.



| Método                                                                 | Descripción                                                                                 |
|:-----------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**Cancelar**](-wia-iwiatransfer-cancel.md)                             | Cancela la operación de transferencia actual. <br/>                                         |
| [**Descargar**](-wia-iwiatransfer-download.md)                         | Inicia una descarga de datos en el autor de la llamada. <br/>                                        |
| [**\_Información de formato de EnumWIA \_**](-wia-iwiatransfer-enumwia-format-info.md) | Crea un enumerador para los formatos de transferencia que admite el dispositivo WIA 2,0.<br/> |
| [**Cargar**](-wia-iwiatransfer-upload.md)                             | Inicia una carga de datos de un único elemento del llamador. <br/>                       |



 

## <a name="remarks"></a>Observaciones

La interfaz **IWiaTransfer** , al igual que todas las interfaces del modelo de objetos componentes (com), hereda los métodos de interfaz [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .



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



 

 
