---
title: Función RtmAddRoute (Rtm.h)
description: La función RtmAddRoute agrega una entrada de ruta o actualiza una entrada de ruta existente.
ms.assetid: 09a9b57d-f10b-40b7-a3c1-2e0613f29431
keywords:
- Función RTMAddRoute RAS
topic_type:
- apiref
api_name:
- RtmAddRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d36b96e94ba2803664e3ff4c4fce6f4f95317c33ce5ab9ccd755c95c8d23fa21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035935"
---
# <a name="rtmaddroute-function"></a>Función RtmAddRoute

\[Esta API ha sido reemplazada por la API [de Routing Table Manager versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003. Las aplicaciones deben usar la API de Routing Table Manager versión 2.\]

La **función RtmAddRoute** agrega una entrada de ruta o actualiza una entrada de ruta existente.

## <a name="syntax"></a>Sintaxis


```C++
DWORD RtmAddRoute(
  _In_  HANDLE ClientHandle,
  _In_  PVOID  Route,
  _In_  DWORD  TimeToLive,
  _Out_ DWORD  Flags,
  _Out_ PVOID  CurBestRoute,
  _Out_ PVOID  PrevBestRoute
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ClientHandle* \[ En\]
</dt> <dd>

Identificador que identifica el cliente y, por tanto, el protocolo de enrutamiento, que agregó o actualizó la ruta. Para obtener este identificador, llame [**a RtmRegisterClient.**](rtmregisterclient.md)

</dd> <dt>

*Ruta* \[ En\]
</dt> <dd>

Puntero a una estructura específica de la familia de protocolos que especifica la ruta nueva o actualizada. El administrador de tablas de enrutamiento usa los siguientes campos para actualizar la tabla de enrutamiento:



| Value                                                                                                                                                                                                                                 | Significado                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RR_Network"></span><span id="rr_network"></span><span id="RR_NETWORK"></span><dl> <dt>**RR \_ Network**</dt> </dl>                                                     | Especifica el número de red de destino.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="RR_InterfaceID"></span><span id="rr_interfaceid"></span><span id="RR_INTERFACEID"></span><dl> <dt>**RR \_ InterfaceID**</dt> </dl>                                     | Especifica el índice de la interfaz a través de la que se recibió la ruta.<br/>                                                                                                                                                                                                                                                                                                                     |
| <span id="RR_NextHopAddress"></span><span id="rr_nexthopaddress"></span><span id="RR_NEXTHOPADDRESS"></span><dl> <dt>**RR \_ NextHopAddress**</dt> </dl>                         | Especifica la dirección del enrutador de próximo salto.<br/>                                                                                                                                                                                                                                                                                                                                                  |
| <span id="RR_FamilySpecificData"></span><span id="rr_familyspecificdata"></span><span id="RR_FAMILYSPECIFICDATA"></span><dl> <dt>**RR \_ FamilySpecificData**</dt> </dl>         | Especifica datos específicos de la familia de protocolos. Aunque los datos son transparentes para el administrador de tablas de enrutamiento, se tienen en cuenta al comparar rutas para determinar si ha cambiado la información de ruta. Los datos también se usan para establecer valores de métricas que son independientes del protocolo de enrutamiento. Por lo tanto, estos datos se usan para determinar la mejor ruta para la red de destino.<br/> |
| <span id="RR_ProtocolSpecificData"></span><span id="rr_protocolspecificdata"></span><span id="RR_PROTOCOLSPECIFICDATA"></span><dl> <dt>**Protocolo \_ RRSpecificData**</dt> </dl> | Especifica los datos que son específicos del protocolo de enrutamiento que proporcionó la ruta.<br/>                                                                                                                                                                                                                                                                                                              |
| <span id="RR_TimeStamp"></span><span id="rr_timestamp"></span><span id="RR_TIMESTAMP"></span><dl> <dt>**RR \_ TimeStamp**</dt> </dl>                                             | Especifica la hora actual del sistema. El administrador de tablas de enrutamiento establece este campo.<br/>                                                                                                                                                                                                                                                                                                             |



 

</dd> <dt>

*TimeToLive* \[ En\]
</dt> <dd>

Especifica el número de segundos que la ruta especificada debe conservarse en la tabla de enrutamiento. Si este parámetro se establece en INFINITE, la ruta se mantiene hasta que se elimina explícitamente. El límite actual de *TimeToLive* es 2147483 segundos (más de 24 días).

</dd> <dt>

*Marcas* \[ out\]
</dt> <dd>

Puntero a una variable **DWORD.** El valor de esta variable lo establece el administrador de tablas de enrutamiento. El valor indica el tipo del cambio y qué información se devolvió en los búferes proporcionados. Este parámetro es uno de los siguientes.



| Marcas                                                                                                                                                                      | Significado                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_NO_CHANGE"></span><span id="rtm_no_change"></span><dl> <dt>**RTM \_ NO \_ CHANGE**</dt> </dl>             | La adición o actualización no ha cambiado ninguno de los parámetros de ruta significativos o la entrada de ruta afectada no es la mejor ruta entre las entradas de la red de destino.<br/>                                                                                                          |
| <span id="RTM_ROUTE_ADDED"></span><span id="rtm_route_added"></span><dl> <dt>**RUTA \_ RTM \_ AGREGADA**</dt> </dl>       | La ruta se agregó para la red de destino. El *parámetro CurBestRoute* apunta a la información de la ruta agregada.<br/>                                                                                                                                                                    |
| <span id="RTM_ROUTE_CHANGED"></span><span id="rtm_route_changed"></span><dl> <dt>**RUTA RTM \_ \_ MODIFICADA**</dt> </dl> | Se cambió al menos uno de los parámetros significativos para la mejor ruta a la red de destino. Los parámetros significativos son: <br/> Identificador de protocolo<br/> Índice de interfaz<br/> Dirección del próximo salto<br/> Datos específicos de la familia de protocolos (incluidas las métricas de ruta)<br/> |



 

El *parámetro PrevBestRoute* apunta a la información de ruta tal como estaba antes del cambio. El *parámetro CurBestRoute* apunta a la información de ruta actual (es decir, después del cambio).

</dd> <dt>

*CurBestRoute* \[ out\]
</dt> <dd>

Puntero a una estructura que recibe la información de mejor ruta actual, si existe. El tipo de la estructura es específico de la familia de protocolos, por ejemplo, IP o IPX.

Este parámetro es opcional. Si el autor de la llamada **especifica NULL** para este parámetro, no se devuelve la información de mejor ruta actual.

</dd> <dt>

*PrevBestRoute* \[ out\]
</dt> <dd>

Puntero a una estructura que recibe la información de mejor ruta anterior, si existe. El tipo de la estructura es específico de la familia de protocolos, por ejemplo, IP o IPX.

Este parámetro es opcional. Si el autor de la llamada **especifica NULL para** este parámetro, no se devuelve la información de ruta recomendada anterior.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es uno de los códigos siguientes.



| Value                                                                                                       | Descripción                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**NO \_ ERROR**</dt> </dl>                    | La ruta se agregó o actualizó correctamente.<br/>                 |
| <dl> <dt>**IDENTIFICADOR \_ DE ERROR NO \_ VÁLIDO**</dt> </dl>       | El parámetro de identificador de cliente no es un identificador válido.<br/>           |
| <dl> <dt>**ERROR \_ PARÁMETRO NO \_ VÁLIDO**</dt> </dl>    | La estructura de ruta contiene un parámetro no válido.<br/>           |
| <dl> <dt>**ERROR \_ NO HAY RECURSOS DEL \_ \_ SISTEMA**</dt> </dl> | No hay recursos suficientes para llevar a cabo la operación.<br/> |
| <dl> <dt>**ERROR \_ NO HAY SUFICIENTE \_ \_ MEMORIA**</dt> </dl>   | No hay memoria suficiente para asignar la entrada de ruta.<br/>    |



 

## <a name="remarks"></a>Comentarios

La función genera un mensaje de cambio de ruta si la mejor ruta a una red de destino ha cambiado como resultado de esta operación. Sin embargo, el mensaje de cambio de ruta no se envía al cliente que realiza esta llamada. En su lugar, esta función devuelve información relevante directamente a ese cliente a través de los parámetros *Flags*, *CurBestRoute* y *PrevBestRoute.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                     |
| Header<br/>                   | <dl> <dt>Rtm.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Rtm.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Rtm.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Referencia de la versión 1 del Administrador de tablas de enrutamiento](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Funciones de Routing Table Manager versión 1](routing-table-manager-version-1-functions.md)
</dt> <dt>

[**RtmDeleteRoute**](rtmdeleteroute.md)
</dt> <dt>

[**RtmDequeueRouteChangeMessage**](rtmdequeueroutechangemessage.md)
</dt> </dl>

 

 





