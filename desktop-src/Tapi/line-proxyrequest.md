---
description: El mensaje PROXYREQUEST de línea de TAPI \_ entrega una solicitud a un controlador de función de proxy registrado.
ms.assetid: 7f33de55-2482-4558-bd86-ee2ac1e31269
title: Mensaje de LINE_PROXYREQUEST (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d536e85a9c773626bb5aacc4745d9d82817fe3c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690385"
---
# <a name="line_proxyrequest-message"></a>Mensaje de línea \_ PROXYREQUEST

El mensaje **\_ PROXYREQUEST de línea** de TAPI entrega una solicitud a un controlador de función de proxy registrado.


```C++
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Identificador de la aplicación para el dispositivo de línea en el que ha cambiado el estado del agente.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Instancia de devolución de llamada proporcionada al abrir la línea de la llamada.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Puntero a una estructura [**LINEPROXYREQUEST**](/windows/desktop/api/Tapi/ns-tapi-lineproxyrequest) que contiene la solicitud que va a ser procesada por la aplicación de controlador proxy.

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

## <a name="remarks"></a>Observaciones

El mensaje **line \_ PROXYREQUEST** se envía solo a la primera aplicación que se registró para controlar las solicitudes de proxy del tipo que se está entregando.

La aplicación debe procesar la solicitud incluida en el búfer del proxy y llamar a [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) para devolver datos o proporcionar resultados. El procesamiento de la solicitud debe realizarse en el contexto de la función de devolución de llamada TAPI de la aplicación solo si se puede realizar inmediatamente, sin esperar la respuesta de ninguna otra entidad. Si la aplicación necesita comunicarse con otras entidades (por ejemplo, un proveedor de servicios para controlar ACD basado en PBX o cualquier otro servicio del sistema que pueda provocar un bloqueo), la solicitud se debe poner en cola dentro de la aplicación y salir de la función de devolución de llamada para evitar el retraso de la recepción de mensajes TAPI adicionales por parte de la aplicación.

En el momento en que se entrega la **línea \_ PROXYREQUEST** al controlador de proxy, TAPI ya ha devuelto un resultado de función *dwRequestID* positivo a la aplicación original y desbloqueó el subproceso que realiza la llamada para continuar la ejecución. La aplicación espera un mensaje de [**\_ respuesta de línea**](line-reply.md) , que se genera automáticamente cuando la aplicación de controlador de proxy llama a [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse).

La aplicación no debe liberar la memoria a la que apunta *lpProxyRequest*. TAPI libera la memoria durante la ejecución de [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse). La aplicación puede llamar a [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) exactamente una vez por cada mensaje **\_ PROXYREQUEST de línea** .

Si la aplicación recibe un mensaje de [**\_ cierre de línea**](line-close.md) mientras tiene solicitudes de proxy pendientes, debe llamar a [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) para cada solicitud pendiente, pasando un valor de *dwResult* adecuado (como LINEERR \_ OPERATIONFAILED).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**cierre de línea \_**](line-close.md)
</dt> <dt>

[**respuesta de línea \_**](line-reply.md)
</dt> <dt>

[**LINEPROXYREQUEST**](/windows/desktop/api/Tapi/ns-tapi-lineproxyrequest)
</dt> <dt>

[**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse)
</dt> </dl>

 

 




