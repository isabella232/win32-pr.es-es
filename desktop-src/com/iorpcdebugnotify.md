---
title: IOrpcDebugNotify (interfaz)
description: Proporciona la funcionalidad de depuración remota.
ms.assetid: f91987c0-2e4b-4872-8ed6-e208a23baa49
keywords:
- IOrpcDebugNotify (interfaz COM)
- Interfaz IOrpcDebugNotify COM , descrita
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889065"
---
# <a name="iorpcdebugnotify-interface"></a>IOrpcDebugNotify (interfaz)

Proporciona la funcionalidad de depuración remota.

## <a name="when-to-implement"></a>Cuándo implementar

Implemente esta interfaz para habilitar la depuración remota a través de RPC.

## <a name="when-to-use"></a>Cuándo se usa

Esta interfaz debe usarse para la depuración remota en proceso cuando no se deben usar excepciones de software para las notificaciones del depurador COM. Permite que los depuradores en proceso se notifiquen mediante llamadas directas mediante estos métodos.

## <a name="members"></a>Members

La **interfaz IOrpcDebugNotify** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) **IOrpcDebugNotify** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IOrpcDebugNotify** tiene estos métodos.



| Método                                                              | Descripción                                                                    |
|:--------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md)       | Envía datos del depurador de cliente al depurador del servidor.<br/>         |
| [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md) | Recupera el tamaño del búfer RPC del depurador del lado cliente.<br/>        |
| [**ClientNotify**](iorpcdebugnotify-clientnotify.md)               | Informa al cliente de una solicitud del depurador saliente al servidor.<br/>   |
| [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)       | Envía datos del depurador del servidor al depurador del cliente.<br/>         |
| [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md) | Recupera el tamaño del búfer RPC del depurador del lado servidor.<br/>        |
| [**ServerNotify**](iorpcdebugnotify-servernotify.md)               | Informa al servidor de una solicitud entrante del depurador del cliente.<br/> |



 

## <a name="remarks"></a>Observaciones

Una biblioteca de importación que contiene **la interfaz IOrpcDebugNotify** no se incluye en el Kit de desarrollo de software (SDK) de Microsoft Windows. Una aplicación puede usar las funciones [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) y [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) para recuperar un puntero de función a [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) de oleaut.dll y proporcionar estos métodos a través de la interfaz **IOrpcDebugNotify.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                     |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                           |
| Encabezado<br/>                   | <dl> <dt>N/D</dt> </dl> |
| IDL<br/>                      | <dl> <dt>N/D</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)
</dt> <dt>

[**ORPC \_ DBG \_ ALL**](orpc-dbg-all.md)
</dt> <dt>

[**BÚFER \_ DE DBG DE ORPC \_**](orpc-dbg-buffer.md)
</dt> <dt>

[**ARGUMENTOS \_ DE ORPC INIT \_**](orpc-init-args.md)
</dt> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> </dl>

 

