---
title: Función RtmAddRoute (RTM. h)
description: La función RtmAddRoute agrega una entrada de ruta o actualiza una entrada de ruta existente.
ms.assetid: 09a9b57d-f10b-40b7-a3c1-2e0613f29431
keywords:
- RtmAddRoute función RAS
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
ms.openlocfilehash: a0c3ee68c9b026fc37457819777e69d2be7984e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676834"
---
# <a name="rtmaddroute-function"></a>RtmAddRoute función)

\[Esta API se ha sustituido por la API del [Administrador de tablas de enrutamiento versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003. Las aplicaciones deben usar la API del administrador de tabla de enrutamiento versión 2.\]

La función **RtmAddRoute** agrega una entrada de ruta o actualiza una entrada de ruta existente.

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

*ClientHandle* \[ de\]
</dt> <dd>

Identificador que identifica al cliente y, por tanto, el protocolo de enrutamiento, que agregó o actualizó la ruta. Obtenga este identificador llamando a [**RtmRegisterClient**](rtmregisterclient.md).

</dd> <dt>

*Ruta* \[ de de\]
</dt> <dd>

Puntero a una estructura específica de la familia de protocolos que especifica la ruta nueva o actualizada. El administrador de tablas de enrutamiento usa los campos siguientes para actualizar la tabla de enrutamiento:



| Value                                                                                                                                                                                                                                 | Significado                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RR_Network"></span><span id="rr_network"></span><span id="RR_NETWORK"></span><dl> <dt>**\_Red RR**</dt> </dl>                                                     | Especifica el número de red de destino.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="RR_InterfaceID"></span><span id="rr_interfaceid"></span><span id="RR_INTERFACEID"></span><dl> <dt>**RR \_ InterfaceID**</dt> </dl>                                     | Especifica el índice de la interfaz a través de la cual se recibió la ruta.<br/>                                                                                                                                                                                                                                                                                                                     |
| <span id="RR_NextHopAddress"></span><span id="rr_nexthopaddress"></span><span id="RR_NEXTHOPADDRESS"></span><dl> <dt>**RR \_ NextHopAddress**</dt> </dl>                         | Especifica la dirección del enrutador de próximo salto.<br/>                                                                                                                                                                                                                                                                                                                                                  |
| <span id="RR_FamilySpecificData"></span><span id="rr_familyspecificdata"></span><span id="RR_FAMILYSPECIFICDATA"></span><dl> <dt>**RR \_ FamilySpecificData**</dt> </dl>         | Especifica datos que son específicos de la familia de protocolos. Aunque los datos son transparentes para el administrador de tablas de enrutamiento, se tienen en cuenta cuando se comparan las rutas para determinar si ha cambiado la información de ruta. Los datos también se usan para establecer valores de métricas que son independientes del Protocolo de enrutamiento. Por consiguiente, estos datos se usan para determinar la mejor ruta para la red de destino.<br/> |
| <span id="RR_ProtocolSpecificData"></span><span id="rr_protocolspecificdata"></span><span id="RR_PROTOCOLSPECIFICDATA"></span><dl> <dt>**RR \_ ProtocolSpecificData**</dt> </dl> | Especifica los datos específicos del Protocolo de enrutamiento que proporcionó la ruta.<br/>                                                                                                                                                                                                                                                                                                              |
| <span id="RR_TimeStamp"></span><span id="rr_timestamp"></span><span id="RR_TIMESTAMP"></span><dl> <dt>**Marca de tiempo de RR \_**</dt> </dl>                                             | Especifica la hora actual del sistema. Este campo lo establece el administrador de tablas de enrutamiento.<br/>                                                                                                                                                                                                                                                                                                             |



 

</dd> <dt>

*TimeToLive* \[ de\]
</dt> <dd>

Especifica el número de segundos que la ruta especificada debe mantenerse en la tabla de enrutamiento. Si este parámetro se establece en Infinite, la ruta se mantiene hasta que se elimina explícitamente. El límite actual de *timeToLive* es de 2147483 segundos (24 + días).

</dd> <dt>

*Marcas* \[ de enuncia\]
</dt> <dd>

Puntero a una variable **DWORD** . El valor de esta variable se establece en el administrador de tablas de enrutamiento. El valor indica el tipo de cambio y la información que se devolvió en los búferes proporcionados. Este parámetro es uno de los siguientes.



| Marcas                                                                                                                                                                      | Significado                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_NO_CHANGE"></span><span id="rtm_no_change"></span><dl> <dt>**RTM \_ sin \_ cambios**</dt> </dl>             | La adición o actualización no cambió ninguno de los parámetros de ruta significativos, o bien la entrada de ruta afectada no es la mejor ruta entre las entradas de la red de destino.<br/>                                                                                                          |
| <span id="RTM_ROUTE_ADDED"></span><span id="rtm_route_added"></span><dl> <dt>**\_ruta RTM \_ agregada**</dt> </dl>       | La ruta se agregó para la red de destino. El parámetro *CurBestRoute* apunta a la información de la ruta agregada.<br/>                                                                                                                                                                    |
| <span id="RTM_ROUTE_CHANGED"></span><span id="rtm_route_changed"></span><dl> <dt>**\_ruta RTM \_ modificada**</dt> </dl> | Se cambió al menos uno de los parámetros significativos para la mejor ruta a la red de destino. Los parámetros significativos son: <br/> Identificador de protocolo<br/> Índice de interfaz<br/> Dirección de próximo salto<br/> Datos específicos de la familia de protocolos (incluidas las métricas de ruta)<br/> |



 

El parámetro *PrevBestRoute* apunta a la información de ruta tal como estaba antes del cambio. El parámetro *CurBestRoute* apunta a la información de ruta actual (es decir, después de cambiar).

</dd> <dt>

*CurBestRoute* \[ enuncia\]
</dt> <dd>

Puntero a una estructura que recibe la información de la mejor ruta actual, si existe. El tipo de la estructura es específico de la familia de protocolos, por ejemplo, IP o IPX.

Este parámetro es opcional. Si el autor de la llamada especifica **null** para este parámetro, no se devuelve la información de la mejor ruta actual.

</dd> <dt>

*PrevBestRoute* \[ enuncia\]
</dt> <dd>

Puntero a una estructura que recibe la información de la mejor ruta anterior, si existe. El tipo de la estructura es específico de la familia de protocolos, por ejemplo, IP o IPX.

Este parámetro es opcional. Si el autor de la llamada especifica **null** para este parámetro, no se devuelve la información de la mejor ruta anterior.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es uno de los siguientes códigos.



| Value                                                                                                       | Descripción                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**SIN \_ errores**</dt> </dl>                    | La ruta se agregó o actualizó correctamente.<br/>                 |
| <dl> <dt>**ERROR \_ de \_ identificador no válido**</dt> </dl>       | El parámetro de identificador de cliente no es un identificador válido.<br/>           |
| <dl> <dt>**ERROR \_ de \_ parámetro no válido**</dt> </dl>    | La estructura de ruta contiene un parámetro no válido.<br/>           |
| <dl> <dt>**ERROR: \_ no hay \_ recursos del sistema \_**</dt> </dl> | No hay suficientes recursos para realizar la operación.<br/> |
| <dl> <dt>**ERROR \_ de \_ memoria insuficiente \_**</dt> </dl>   | No hay memoria suficiente para asignar la entrada de ruta.<br/>    |



 

## <a name="remarks"></a>Observaciones

La función genera un mensaje de cambio de ruta si la mejor ruta a una red de destino ha cambiado como resultado de esta operación. Sin embargo, el mensaje de cambio de ruta no se envía al cliente que realiza esta llamada. En su lugar, esta función devuelve directamente información relevante a ese cliente a través de los parámetros *Flags*, *CurBestRoute* y *PrevBestRoute* .

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

[**RtmDeleteRoute**](rtmdeleteroute.md)
</dt> <dt>

[**RtmDequeueRouteChangeMessage**](rtmdequeueroutechangemessage.md)
</dt> </dl>

 

 





