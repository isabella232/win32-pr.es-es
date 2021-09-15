---
description: La interfaz IWiaAppErrorHandler permite a las aplicaciones mostrar ventanas de error (durante las transferencias de datos) desde las que el usuario puede elegir si desea continuar, cancelar o anular la transferencia.
ms.assetid: ac2597e6-2857-4694-bea7-1ea65d63b365
title: Interfaz IWiaAppErrorHandler (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaAppErrorHandler
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 6ccac7b689055bfaab926a8db46b4632606811d7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571380"
---
# <a name="iwiaapperrorhandler-interface"></a>Interfaz IWiaAppErrorHandler

La **interfaz IWiaAppErrorHandler** permite a las aplicaciones mostrar ventanas de error (durante las transferencias de datos) desde las que el usuario puede elegir si desea continuar, cancelar o anular la transferencia.

## <a name="members"></a>Members

La **interfaz IWiaAppErrorHandler** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IWiaAppErrorHandler** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IWiaAppErrorHandler** tiene estos métodos.



| Método                                                        | Descripción                                                                                                                                             |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetWindow**](-wia-iwiaapperrorhandler-getwindow.md)       | Obtiene un identificador para el cuadro de diálogo que muestra mensajes de error y proporciona uno o varios botones para continuar, cancelar o anular la aplicación.<br/> |
| [**ReportStatus**](-wia-iwiaapperrorhandler-reportstatus.md) | Controla el estado del dispositivo y los mensajes de error durante las transferencias de datos de imagen y muestra los mensajes al usuario.<br/>                                  |



 

## <a name="remarks"></a>Observaciones

El objeto de control de errores, o devolución de llamada, que implementa esta interfaz se pasa a [**IWiaTransfer::D ownload**](-wia-iwiatransfer-download.md) e [**IWiaTransfer::Upload**](-wia-iwiatransfer-upload.md).

Esta interfaz no está diseñada para controlar los errores detectados fuera de las transferencias de datos de imagen, por ejemplo, errores al obtener o establecer propiedades del dispositivo o devoluciones de llamada no anuladas en un controlador.

Un controlador de errores de controlador debe implementar [**IWiaErrorHandler**](-wia-iwiaerrorhandler.md), en lugar **de IWiaAppErrorHandler**.

El objeto que implementa esta interfaz también debe implementar [**IWiaTransferCallback**](-wia-iwiatransfercallback.md).

Si desea que un controlador de errores de controlador y el controlador de errores predeterminado muestren ventanas de mensajes de error, pero no desea crear un controlador de errores completo para la aplicación, implemente esta interfaz e implemente también el método [**IWiaAppErrorHandler::ReportStatus**](-wia-iwiaapperrorhandler-reportstatus.md) para devolver WIA \_ STATUS NOT \_ \_ HANDLED.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
