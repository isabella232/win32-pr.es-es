---
description: La interfaz IWiaErrorHandler proporciona métodos para controlar los errores que pueden producirse cuando una aplicación solicita datos de imagen, ya sea para la versión preliminar o los bits finales.
ms.assetid: 33d8ccc5-6856-4a54-b1f0-d015933d63ab
title: Interfaz IWiaErrorHandler (Wia.h)
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
ms.openlocfilehash: 6e97c5a146c23ce1ecdb2ba77cde5d37cd9091fc9d77e288042f02fc118816e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965594"
---
# <a name="iwiaerrorhandler-interface"></a>Interfaz IWiaErrorHandler

La **interfaz IWiaErrorHandler proporciona métodos** para controlar los errores que pueden producirse cuando una aplicación solicita datos de imagen, ya sea para la versión preliminar o los bits finales.

## <a name="members"></a>Miembros

La **interfaz IWiaErrorHandler** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IWiaErrorHandler** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IWiaErrorHandler** tiene estos métodos.



| Método                                                                     | Descripción                                                                                             |
|:---------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**GetStatusDescription**](-wia-iwiaerrorhandler-getstatusdescription.md) | Devuelve una cadena que describe el código de estado.<br/>                                             |
| [**ReportStatus**](-wia-iwiaerrorhandler-reportstatus.md)                 | Controla los mensajes de estado y error durante las transferencias de datos de imagen y los muestra al usuario.<br/> |



 

## <a name="remarks"></a>Comentarios

El objeto de devolución de llamada de aplicación puede implementar **IWiaErrorHandler**.

Esta interfaz no está diseñada para controlar los errores detectados fuera de las transferencias de datos de imagen, por ejemplo, errores al obtener o establecer propiedades del dispositivo o devoluciones de llamada no anuladas en un controlador.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>       |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



 

 
