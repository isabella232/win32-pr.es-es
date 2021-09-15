---
title: Función RtmDequeueRouteChangeMessage (Rtm.h)
description: La función RtmDequeueRouteChangeMessage devuelve el siguiente mensaje de cambio de ruta en la cola asociada al cliente especificado.
ms.assetid: 44f2116a-3c8d-4ac6-896e-b12930b218a5
keywords:
- Función RAS de RtmDequeueRouteChangeMessage
topic_type:
- apiref
api_name:
- RtmDequeueRouteChangeMessage
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 448df230742b03f82294de102bf14b50fefa035c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271924"
---
# <a name="rtmdequeueroutechangemessage-function"></a>Función RtmDequeueRouteChangeMessage

\[Esta API se ha reemplazado por la API [de Routing Table Manager versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003. Las aplicaciones deben usar la API de Routing Table Manager versión 2.\]

La **función RtmDequeueRouteChangeMessage** devuelve el siguiente mensaje de cambio de ruta en la cola asociada al cliente especificado.

## <a name="syntax"></a>Sintaxis


```C++
DWORD RtmDequeueRouteChangeMessage(
  _In_  HANDLE ClientHandle,
  _Out_ DWORD  Flags,
  _Out_ PVOID  CurBestRoute,
  _Out_ PVOID  PrevBestRoute
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ClientHandle* \[ En\]
</dt> <dd>

Identificador que identifica el cliente para el que se realiza la operación. Para obtener este identificador, llame [**a RtmRegisterClient.**](rtmregisterclient.md)

</dd> <dt>

*Marcas* \[ out\]
</dt> <dd>

Puntero a una variable **DWORD.** El valor de esta variable lo establece el administrador de tablas de enrutamiento. El valor especifica el tipo del mensaje de cambio y qué información se devolvió en los búferes proporcionados. Este parámetro es uno de los siguientes.



| Marcas                                                                                                                                                                      | Significado                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_ROUTE_ADDED"></span><span id="rtm_route_added"></span><dl> <dt>**RUTA \_ RTM \_ AGREGADA**</dt> </dl>       | Se agregó la primera ruta para una red de destino determinada. El *parámetro CurBestRoute* apunta a la información de la ruta agregada.<br/>                                                                                                                                                            |
| <span id="RTM_ROUTE_DELETED"></span><span id="rtm_route_deleted"></span><dl> <dt>**RUTA RTM \_ \_ ELIMINADA**</dt> </dl> | Se eliminó la única ruta disponible para una red de destino determinada. El *parámetro PrevBestRoute* apunta a la información de la ruta eliminada.<br/>                                                                                                                                              |
| <span id="RTM_ROUTE_CHANGED"></span><span id="rtm_route_changed"></span><dl> <dt>**RUTA RTM \_ \_ MODIFICADA**</dt> </dl> | Se cambió al menos uno de los parámetros significativos para una mejor ruta a una red de destino determinada. Los parámetros significativos son: <br/> Identificador de protocolo<br/> Índice de interfaz<br/> Dirección del próximo salto<br/> Datos específicos de la familia de protocolos (incluidas las métricas de ruta)<br/> |



 

El *parámetro PrevBestRoute* apunta a la información de ruta tal como estaba antes del cambio. El *parámetro CurBestRoute* apunta a la información de ruta actual (es decir, después del cambio).

</dd> <dt>

*CurBestRoute* \[ out\]
</dt> <dd>

Puntero a una estructura que recibe la información de mejor ruta actual (si existe). El tipo de la estructura es específico de la familia de protocolos, por ejemplo, IP o IPX.

Este parámetro es opcional. Si el autor de la llamada **especifica NULL** para este parámetro, no se devuelve la información de mejor ruta actual.

</dd> <dt>

*PrevBestRoute* \[ out\]
</dt> <dd>

Puntero a una estructura que recibe la información de mejor ruta anterior, si existe. El tipo de la estructura es específico de la familia de protocolos, por ejemplo, IP o IPX.

Este parámetro es opcional. Si el autor de la llamada **especifica NULL** para este parámetro, no se devuelve la información de mejor ruta anterior.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es uno de los códigos siguientes.



| Value                                                                                                       | Descripción                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NO \_ ERROR**</dt> </dl>                    | Este mensaje era el último mensaje de la cola del cliente. Se restablece el objeto de evento.<br/>                                                                                                                                               |
| <dl> <dt>**IDENTIFICADOR \_ DE ERROR NO \_ VÁLIDO**</dt> </dl>       | El *parámetro ClientHandle* no es un identificador válido o, en el registro, el cliente no ha especificado un objeto de evento para la notificación de mensajes de cambio (vea [**RtmRegisterClient).**](rtmregisterclient.md)<br/>                           |
| <dl> <dt>**ERROR \_ MÁS \_ MENSAJES**</dt> </dl>        | La cola del cliente contiene mensajes adicionales. El cliente debe volver a llamar a **RtmDequeueRouteChangeMessage** lo antes posible para permitir que el administrador de tablas de enrutamiento libre los recursos asociados a los mensajes pendientes.<br/> |
| <dl> <dt>**ERROR \_ SIN \_ MENSAJES**</dt> </dl>          | La cola del cliente no contiene mensajes; la llamada no se ha solicitado. El evento se restablece.<br/>                                                                                                                                            |
| <dl> <dt>**ERROR \_ NO HAY RECURSOS DEL \_ \_ SISTEMA**</dt> </dl> | No hay recursos suficientes para llevar a cabo la operación.<br/>                                                                                                                                                                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Rtm.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Rtm.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Rtm.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Referencia de la versión 1 del Administrador de tablas de enrutamiento](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Funciones de Routing Table Manager versión 1](routing-table-manager-version-1-functions.md)
</dt> <dt>

[**RtmRegisterClient**](rtmregisterclient.md)
</dt> </dl>

 

 





