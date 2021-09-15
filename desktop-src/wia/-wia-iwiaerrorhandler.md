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
ms.openlocfilehash: 7b3ea9f5556f1f919336e4abb4085f9e0c32d81d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572293"
---
# <a name="iwiaerrorhandler-interface"></a>Interfaz IWiaErrorHandler

La **interfaz IWiaErrorHandler** proporciona métodos para controlar los errores que pueden producirse cuando una aplicación solicita datos de imagen, ya sea para la versión preliminar o los bits finales.

## <a name="members"></a>Members

La **interfaz IWiaErrorHandler** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IWiaErrorHandler** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IWiaErrorHandler** tiene estos métodos.



| Método                                                                     | Descripción                                                                                             |
|:---------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**GetStatusDescription**](-wia-iwiaerrorhandler-getstatusdescription.md) | Devuelve una cadena que describe el código de estado.<br/>                                             |
| [**ReportStatus**](-wia-iwiaerrorhandler-reportstatus.md)                 | Controla los mensajes de estado y de error durante las transferencias de datos de imagen y los muestra al usuario.<br/> |



 

## <a name="remarks"></a>Observaciones

El objeto de devolución de llamada de aplicación puede implementar **IWiaErrorHandler**.

Esta interfaz no está diseñada para controlar los errores detectados fuera de las transferencias de datos de imagen, por ejemplo, errores al obtener o establecer propiedades del dispositivo o devoluciones de llamada no returnadas en un controlador.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Wia.h</dt> </dl>       |
| IDL<br/>                      | <dl> <dt>Wia.idl</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



 

 
