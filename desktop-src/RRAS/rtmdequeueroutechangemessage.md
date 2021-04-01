---
title: Función RtmDequeueRouteChangeMessage (RTM. h)
description: La función RtmDequeueRouteChangeMessage devuelve el siguiente mensaje Route-Change en la cola asociada al cliente especificado.
ms.assetid: 44f2116a-3c8d-4ac6-896e-b12930b218a5
keywords:
- RtmDequeueRouteChangeMessage función RAS
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150522"
---
# <a name="rtmdequeueroutechangemessage-function"></a>RtmDequeueRouteChangeMessage función)

\[Esta API se ha sustituido por la API del [Administrador de tablas de enrutamiento versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003. Las aplicaciones deben usar la API del administrador de tabla de enrutamiento versión 2.\]

La función **RtmDequeueRouteChangeMessage** devuelve el siguiente mensaje Route-Change en la cola asociada al cliente especificado.

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

*ClientHandle* \[ de\]
</dt> <dd>

Identificador que identifica el cliente para el que se realiza la operación. Obtenga este identificador llamando a [**RtmRegisterClient**](rtmregisterclient.md).

</dd> <dt>

*Marcas* \[ de enuncia\]
</dt> <dd>

Puntero a una variable **DWORD** . El valor de esta variable se establece en el administrador de tablas de enrutamiento. El valor especifica el tipo del mensaje de cambio y la información que se devolvió en los búferes proporcionados. Este parámetro es uno de los siguientes.



| Marcas                                                                                                                                                                      | Significado                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_ROUTE_ADDED"></span><span id="rtm_route_added"></span><dl> <dt>**\_ruta RTM \_ agregada**</dt> </dl>       | La primera ruta se agregó para una red de destino determinada. El parámetro *CurBestRoute* apunta a la información de la ruta agregada.<br/>                                                                                                                                                            |
| <span id="RTM_ROUTE_DELETED"></span><span id="rtm_route_deleted"></span><dl> <dt>**\_ruta RTM \_ eliminada**</dt> </dl> | La única ruta disponible para una red de destino determinada se ha eliminado. El parámetro *PrevBestRoute* apunta a la información de la ruta eliminada.<br/>                                                                                                                                              |
| <span id="RTM_ROUTE_CHANGED"></span><span id="rtm_route_changed"></span><dl> <dt>**\_ruta RTM \_ modificada**</dt> </dl> | Se cambió al menos uno de los parámetros significativos para una mejor ruta a una red de destino determinada. Los parámetros significativos son: <br/> Identificador de protocolo<br/> Índice de interfaz<br/> Dirección de próximo salto<br/> Datos específicos de la familia de protocolos (incluidas las métricas de ruta)<br/> |



 

El parámetro *PrevBestRoute* apunta a la información de ruta tal como estaba antes del cambio. El parámetro *CurBestRoute* apunta a la información de ruta actual (es decir, después de cambiar).

</dd> <dt>

*CurBestRoute* \[ enuncia\]
</dt> <dd>

Puntero a una estructura que recibe la información de la mejor ruta actual (si existe). El tipo de la estructura es específico de la familia de protocolos, por ejemplo, IP o IPX.

Este parámetro es opcional. Si el autor de la llamada especifica **null** para este parámetro, no se devuelve la información de la mejor ruta actual.

</dd> <dt>

*PrevBestRoute* \[ enuncia\]
</dt> <dd>

Puntero a una estructura que recibe la información de la mejor ruta anterior, si existe. El tipo de la estructura es específico de la familia de protocolos, por ejemplo, IP o IPX.

Este parámetro es opcional. Si el autor de la llamada especifica **null** para este parámetro, no se devuelve la información de la mejor ruta anterior.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es uno de los siguientes códigos.



| Value                                                                                                       | Descripción                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SIN \_ errores**</dt> </dl>                    | Este mensaje era el último mensaje de la cola del cliente. Se restablece el objeto de evento.<br/>                                                                                                                                               |
| <dl> <dt>**ERROR \_ de \_ identificador no válido**</dt> </dl>       | El parámetro *ClientHandle* no es un identificador válido o, en el registro, el cliente no proporcionó un objeto de evento para la notificación de cambio de mensaje (vea [**RtmRegisterClient**](rtmregisterclient.md)).<br/>                           |
| <dl> <dt>**\_más \_ mensajes de error**</dt> </dl>        | La cola del cliente contiene mensajes adicionales. El cliente debe volver a llamar a **RtmDequeueRouteChangeMessage** tan pronto como sea posible para permitir que el administrador de tablas de enrutamiento libere los recursos asociados a los mensajes pendientes.<br/> |
| <dl> <dt>**\_no hay \_ mensajes de error**</dt> </dl>          | La cola del cliente no contiene ningún mensaje; no se solicitó la llamada. Se restablece el evento.<br/>                                                                                                                                            |
| <dl> <dt>**ERROR: \_ no hay \_ recursos del sistema \_**</dt> </dl> | No hay suficientes recursos para realizar la operación.<br/>                                                                                                                                                                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>RTM. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>RTM. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Rtm.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Referencia de la versión 1 del administrador de tablas de enrutamiento](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Funciones de la versión 1 del administrador de tablas de enrutamiento](routing-table-manager-version-1-functions.md)
</dt> <dt>

[**RtmRegisterClient**](rtmregisterclient.md)
</dt> </dl>

 

 





