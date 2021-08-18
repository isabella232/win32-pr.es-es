---
description: El mensaje TAPI LINE \_ PROXYREQUEST entrega una solicitud a un controlador de funciones de proxy registrado.
ms.assetid: 7f33de55-2482-4558-bd86-ee2ac1e31269
title: LINE_PROXYREQUEST mensaje (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31986420cd21178cca8e6f0a1006e743c3250e726b4a1bf79513f6d57e380a01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003163"
---
# <a name="line_proxyrequest-message"></a>Mensaje \_ LINE PROXYREQUEST

El mensaje TAPI **LINE \_ PROXYREQUEST** entrega una solicitud a un controlador de funciones de proxy registrado.


```C++
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDevice* 
</dt> <dd>

El identificador de la aplicación al dispositivo de línea en el que ha cambiado el estado del agente.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Instancia de devolución de llamada proporcionada al abrir la línea de la llamada.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Puntero a una [**estructura LINEPROXYREQUEST**](/windows/desktop/api/Tapi/ns-tapi-lineproxyrequest) que contiene la solicitud que la aplicación de controlador de proxy va a procesar.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Reservado.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Reservado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

El **mensaje \_ LINE PROXYREQUEST** solo se envía a la primera aplicación que se registró para controlar las solicitudes de proxy del tipo que se va a entregar.

La aplicación debe procesar la solicitud contenida en el búfer de proxy y llamar a [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) para devolver datos o entregar resultados. El procesamiento de la solicitud debe realizarse en el contexto de la función de devolución de llamada TAPI de la aplicación solo si se puede realizar inmediatamente, sin esperar la respuesta de ninguna otra entidad. Si la aplicación necesita comunicarse con otras entidades (por ejemplo, un proveedor de servicios para controlar el ACD basado en SAML o cualquier otro servicio del sistema que pueda dar lugar a bloqueos), la solicitud se debe poner en cola dentro de la aplicación y la función de devolución de llamada se cierra para evitar retrasar la recepción de más mensajes TAPI por parte de la aplicación.

En el momento en que **line \_ PROXYREQUEST** se entrega al controlador de proxy, TAPI ya ha devuelto un resultado positivo de la función *dwRequestID* a la aplicación original y ha desbloqueado el subproceso de llamada para continuar con la ejecución. La aplicación está esperando un mensaje [**LINE \_ REPLY,**](line-reply.md) que se genera automáticamente cuando la aplicación de controlador de proxy llama a [**lineProxyResponse.**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse)

La aplicación no liberará la memoria a la que *apunta lpProxyRequest.* TAPI libera la memoria durante la ejecución de [**lineProxyResponse.**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) La aplicación puede llamar a [**lineProxyResponse exactamente**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) una vez para cada **mensaje LINE \_ PROXYREQUEST.**

Si la aplicación recibe un mensaje [**LINE \_ CLOSE**](line-close.md) mientras tiene solicitudes de proxy pendientes, debe llamar a [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) para cada solicitud pendiente, pasando un valor *dwResult* adecuado (como LINEERR \_ OPERATIONFAILED).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LINE \_ CLOSE**](line-close.md)
</dt> <dt>

[**RESPUESTA \_ DE LÍNEA**](line-reply.md)
</dt> <dt>

[**LINEPROXYREQUEST**](/windows/desktop/api/Tapi/ns-tapi-lineproxyrequest)
</dt> <dt>

[**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse)
</dt> </dl>

 

 




