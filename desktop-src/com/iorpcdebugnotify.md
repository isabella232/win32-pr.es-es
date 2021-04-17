---
title: Interfaz IOrpcDebugNotify
description: Proporciona la funcionalidad de depuración remota.
ms.assetid: f91987c0-2e4b-4872-8ed6-e208a23baa49
keywords:
- Interfaz IOrpcDebugNotify COM
- Interfaz IOrpcDebugNotify COM, descripción
topic_type:
- apiref
api_name:
- IOrpcDebugNotify
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f4db08daf93997b2a7fa0ed383591cb5d111ac7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535440"
---
# <a name="iorpcdebugnotify-interface"></a>Interfaz IOrpcDebugNotify

Proporciona la funcionalidad de depuración remota.

## <a name="when-to-implement"></a>Cuándo implementar

Implemente esta interfaz para habilitar la depuración remota a través de RPC.

## <a name="when-to-use"></a>Cuándo se usa

Esta interfaz se debe usar para la depuración remota en proceso cuando las excepciones de software no deben usarse para las notificaciones del depurador COM. Permite a los depuradores en proceso recibir notificaciones directas mediante el uso de estos métodos.

## <a name="members"></a>Miembros

La interfaz **IOrpcDebugNotify** hereda de la interfaz [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) . **IOrpcDebugNotify** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IOrpcDebugNotify** tiene estos métodos.



| Método                                                              | Descripción                                                                    |
|:--------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md)       | Envía datos del depurador del cliente al depurador del servidor.<br/>         |
| [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md) | Recupera el tamaño del búfer de RPC desde el depurador del lado cliente.<br/>        |
| [**ClientNotify**](iorpcdebugnotify-clientnotify.md)               | Informa al cliente de una solicitud de depurador saliente al servidor.<br/>   |
| [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)       | Envía datos del depurador del servidor al depurador del cliente.<br/>         |
| [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md) | Recupera el tamaño del búfer de RPC desde el depurador del servidor.<br/>        |
| [**ServerNotify**](iorpcdebugnotify-servernotify.md)               | Informa al servidor de una solicitud de depurador entrante del cliente.<br/> |



 

## <a name="remarks"></a>Observaciones

En el kit de desarrollo de software (SDK) de Microsoft Windows no se incluye una biblioteca de importación que contiene la interfaz **IOrpcDebugNotify** . Una aplicación puede usar las funciones [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) y [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) para recuperar un puntero de función a [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) desde oleaut.dll y proporcionar estos métodos a través de la interfaz **IOrpcDebugNotify** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                     |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                           |
| Encabezado<br/>                   | <dl> <dt>N/D</dt> </dl> |
| IDL<br/>                      | <dl> <dt>N/D</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)
</dt> <dt>

[**ORPC \_ dbg \_ All**](orpc-dbg-all.md)
</dt> <dt>

[**\_búfer ORPC dbg \_**](orpc-dbg-buffer.md)
</dt> <dt>

[**ORPC \_ init \_ args**](orpc-init-args.md)
</dt> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> </dl>

 

