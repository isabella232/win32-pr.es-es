---
description: La interfaz IWiaAppErrorHandler permite a las aplicaciones mostrar ventanas de errores (durante las transferencias de datos) desde las que el usuario puede elegir si desea continuar, cancelar o anular la transferencia.
ms.assetid: ac2597e6-2857-4694-bea7-1ea65d63b365
title: Interfaz IWiaAppErrorHandler (WIA. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720540"
---
# <a name="iwiaapperrorhandler-interface"></a>Interfaz IWiaAppErrorHandler

La interfaz **IWiaAppErrorHandler** permite a las aplicaciones mostrar ventanas de errores (durante las transferencias de datos) desde las que el usuario puede elegir si desea continuar, cancelar o anular la transferencia.

## <a name="members"></a>Miembros

La interfaz **IWiaAppErrorHandler** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IWiaAppErrorHandler** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IWiaAppErrorHandler** tiene estos métodos.



| Método                                                        | Descripción                                                                                                                                             |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetWindow**](-wia-iwiaapperrorhandler-getwindow.md)       | Obtiene un identificador para el cuadro de diálogo que muestra los mensajes de error y proporciona uno o varios botones para continuar, cancelar o anular la aplicación.<br/> |
| [**ReportStatus**](-wia-iwiaapperrorhandler-reportstatus.md) | Controla el estado del dispositivo y los mensajes de error durante las transferencias de datos de imagen y muestra los mensajes al usuario.<br/>                                  |



 

## <a name="remarks"></a>Observaciones

El objeto de control de errores, o de devolución de llamada, que implementa esta interfaz se pasa a [**IWiaTransfer::D scargar**](-wia-iwiatransfer-download.md) y [**IWiaTransfer:: upload**](-wia-iwiatransfer-upload.md).

Esta interfaz no está diseñada para controlar los errores detectados fuera de las transferencias de datos de la imagen, por ejemplo, errores al obtener o establecer las propiedades del dispositivo o las devoluciones de llamada no devueltas en un controlador.

Un controlador de errores de controlador debe implementar [**IWiaErrorHandler**](-wia-iwiaerrorhandler.md), en lugar de **IWiaAppErrorHandler**.

El objeto que implementa esta interfaz también debe implementar [**IWiaTransferCallback**](-wia-iwiatransfercallback.md).

Si desea que un controlador de errores de controlador y un controlador de errores predeterminado muestren ventanas de mensajes de error, pero no desea crear un controlador de errores completo para la aplicación, implemente esta interfaz e implemente también el método [**IWiaAppErrorHandler:: ReportStatus**](-wia-iwiaapperrorhandler-reportstatus.md) para devolver el estado de WIA \_ \_ no \_ controlado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
