---
description: El mensaje TAPI LINE \_ PROXYREQUEST entrega una solicitud a un controlador de funciones de proxy registrado.
ms.assetid: 7f33de55-2482-4558-bd86-ee2ac1e31269
title: LINE_PROXYREQUEST mensaje (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d536e85a9c773626bb5aacc4745d9d82817fe3c0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250083"
---
# <a name="line_proxyrequest-message"></a>MENSAJE \_ PROXYREQUEST DE LÍNEA

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

## <a name="remarks"></a>Observaciones

El **mensaje \_ PROXYREQUEST de LINE** solo se envía a la primera aplicación registrada para controlar las solicitudes de proxy del tipo que se entrega.

La aplicación debe procesar la solicitud contenida en el búfer de proxy y llamar a [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) para devolver datos o entregar resultados. El procesamiento de la solicitud debe realizarse en el contexto de la función de devolución de llamada TAPI de la aplicación solo si se puede realizar inmediatamente, sin esperar la respuesta de ninguna otra entidad. Si la aplicación necesita comunicarse con otras entidades (por ejemplo, un proveedor de servicios para controlar el ACD basado en SOAP o cualquier otro servicio del sistema que pueda dar lugar a bloqueos), la solicitud se debe poner en cola dentro de la aplicación y la función de devolución de llamada salió para evitar retrasar la recepción de más mensajes TAPI por parte de la aplicación.

En el momento en que **line \_ PROXYREQUEST** se entrega al controlador de proxy, TAPI ya ha devuelto un resultado positivo de la función *dwRequestID* a la aplicación original y ha desbloqueado el subproceso de llamada para continuar con la ejecución. La aplicación está esperando un mensaje [**LINE \_ REPLY,**](line-reply.md) que se genera automáticamente cuando la aplicación de controlador de proxy llama a [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse).

La aplicación no liberará la memoria a la que apunta *lpProxyRequest.* TAPI libera la memoria durante la ejecución de [**lineProxyResponse.**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) La aplicación puede llamar a [**lineProxyResponse exactamente**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) una vez para cada **mensaje \_ PROXYREQUEST de** LÍNEA.

Si la aplicación recibe un mensaje [**LINE \_ CLOSE**](line-close.md) mientras tiene solicitudes de proxy pendientes, debe llamar a [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) para cada solicitud pendiente, pasando un valor *dwResult* adecuado (como LINEERR \_ OPERATIONFAILED).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**LINE \_ CLOSE**](line-close.md)
</dt> <dt>

[**RESPUESTA \_ DE LÍNEA**](line-reply.md)
</dt> <dt>

[**LINEPROXYREQUEST**](/windows/desktop/api/Tapi/ns-tapi-lineproxyrequest)
</dt> <dt>

[**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse)
</dt> </dl>

 

 




