---
description: La interfaz IWiaErrorHandler proporciona métodos para controlar los errores que pueden producirse cuando una aplicación solicita datos de imagen, ya sea para los bits de vista previa o final.
ms.assetid: 33d8ccc5-6856-4a54-b1f0-d015933d63ab
title: Interfaz IWiaErrorHandler (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaErrorHandler
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 7b3ea9f5556f1f919336e4abb4085f9e0c32d81d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154857"
---
# <a name="iwiaerrorhandler-interface"></a>Interfaz IWiaErrorHandler

La interfaz **IWiaErrorHandler** proporciona métodos para controlar los errores que pueden producirse cuando una aplicación solicita datos de imagen, ya sea para los bits de vista previa o final.

## <a name="members"></a>Miembros

La interfaz **IWiaErrorHandler** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IWiaErrorHandler** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IWiaErrorHandler** tiene estos métodos.



| Método                                                                     | Descripción                                                                                             |
|:---------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**GetStatusDescription**](-wia-iwiaerrorhandler-getstatusdescription.md) | Devuelve una cadena que describe el código de estado.<br/>                                             |
| [**ReportStatus**](-wia-iwiaerrorhandler-reportstatus.md)                 | Controla el estado y los mensajes de error durante las transferencias de datos de imagen y los muestra al usuario.<br/> |



 

## <a name="remarks"></a>Observaciones

El objeto de devolución de llamada de la aplicación puede implementar **IWiaErrorHandler**.

Esta interfaz no está diseñada para controlar los errores detectados fuera de las transferencias de datos de la imagen, por ejemplo, errores al obtener o establecer las propiedades del dispositivo o las devoluciones de llamada no devueltas en un controlador.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 
