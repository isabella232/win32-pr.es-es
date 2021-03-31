---
title: Función RtmDeleteRoute (RTM. h)
description: La función RtmDeleteRoute elimina una entrada de ruta.
ms.assetid: a98026e9-40f5-42e9-943c-dfc561feef6d
keywords:
- RtmDeleteRoute función RAS
topic_type:
- apiref
api_name:
- RtmDeleteRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 310364bdb6e6ba7daf285316fcaaf16884e53929
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996618"
---
# <a name="rtmdeleteroute-function"></a>RtmDeleteRoute función)

\[Esta API se ha sustituido por la API del [Administrador de tablas de enrutamiento versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003. Las aplicaciones deben usar la API del administrador de tabla de enrutamiento versión 2.\]

La función **RtmDeleteRoute** elimina una entrada de ruta.

## <a name="syntax"></a>Sintaxis


```C++
DWORD RtmDeleteRoute(
  _In_  HANDLE ClientHandle,
  _In_  PVOID  Route,
  _Out_ DWORD  Flags,
  _Out_ PVOID  CurBestRoute
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ClientHandle* \[ de\]
</dt> <dd>

Identificador que identifica el cliente y, por tanto, el protocolo de enrutamiento de la ruta agregada o actualizada. Obtenga este identificador llamando a [**RtmRegisterClient**](rtmregisterclient.md).

</dd> <dt>

*Ruta* \[ de de\]
</dt> <dd>

Puntero a una estructura específica de la familia de protocolos que especifica la ruta nueva o actualizada. El administrador de tablas de enrutamiento usa los campos siguientes para actualizar la tabla de enrutamiento:



| Value                                                                                                                                                                                                         | Significado                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="RR_Network"></span><span id="rr_network"></span><span id="RR_NETWORK"></span><dl> <dt>**\_Red RR**</dt> </dl>                             | Especifica el número de red de destino. <br/>                                 |
| <span id="RR_InterfaceID"></span><span id="rr_interfaceid"></span><span id="RR_INTERFACEID"></span><dl> <dt>**RR \_ InterfaceID**</dt> </dl>             | Especifica el índice de la interfaz a través de la cual se recibió la ruta.<br/> |
| <span id="RR_NextHopAddress"></span><span id="rr_nexthopaddress"></span><span id="RR_NEXTHOPADDRESS"></span><dl> <dt>**RR \_ NextHopAddress**</dt> </dl> | Especifica la dirección de red del enrutador de próximo salto.<br/>                      |



 

</dd> <dt>

*Marcas* \[ de enuncia\]
</dt> <dd>

Puntero a un conjunto de marcas que indican el tipo del mensaje de cambio y qué información se colocó en los búferes proporcionados. Este parámetro es uno de los valores siguientes.



| Marcas                                                                                                                                                                      | Significado                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_NO_CHANGE"></span><span id="rtm_no_change"></span><dl> <dt>**RTM \_ sin \_ cambios**</dt> </dl>             | La eliminación de la ruta no afectó a la mejor ruta a ninguna red de destino. En otras palabras, otra entrada representa una ruta a la misma red de destino y tiene una métrica inferior.<br/> |
| <span id="RTM_ROUTE_DELETED"></span><span id="rtm_route_deleted"></span><dl> <dt>**\_ruta RTM \_ eliminada**</dt> </dl> | La ruta eliminada era la única ruta disponible para una red de destino determinada.<br/>                                                                                                  |
| <span id="RTM_ROUTE_CHANGED"></span><span id="rtm_route_changed"></span><dl> <dt>**\_ruta RTM \_ modificada**</dt> </dl> | Una vez eliminada esta ruta, otra ruta se convirtió en la mejor ruta a una red de destino determinada. *CurBestRoute* apunta a la información de la nueva ruta más adecuada.<br/>               |



 

</dd> <dt>

*CurBestRoute* \[ enuncia\]
</dt> <dd>

Puntero a una estructura que recibe la información de la mejor ruta actual, si existe. El tipo de la estructura es específico de la familia de protocolos, por ejemplo, IP o IPX.

Este parámetro es opcional. Si el autor de la llamada especifica **null** para este parámetro, no se devuelve la información de la mejor ruta actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto **no es un \_ error**.

Si se produce un error en la función, el valor devuelto es uno de los siguientes códigos de error.



| Value                                                                                                       | Descripción                                                                                            |
|-------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERROR \_ de \_ identificador no válido**</dt> </dl>       | El parámetro de identificador de cliente no es un identificador válido.<br/>                                          |
| <dl> <dt>**ERROR \_ de \_ parámetro no válido**</dt> </dl>    | La estructura de ruta señalada por el parámetro *Route* contiene un valor de miembro.<br/>            |
| <dl> <dt>**ERROR no se trata de una \_ \_ \_ ruta**</dt> </dl>       | No hay ninguna entrada en la tabla de enrutamiento que coincida con los parámetros de la ruta especificada.<br/> |
| <dl> <dt>**ERROR: \_ no hay \_ recursos del sistema \_**</dt> </dl> | No hay suficientes recursos para realizar la operación. <br/>                                 |



 

## <a name="remarks"></a>Observaciones

La función genera un mensaje de cambio de ruta si la mejor ruta a una red de destino ha cambiado como resultado de la eliminación. Sin embargo, el mensaje de cambio de ruta no se envía al cliente que realiza esta llamada. En su lugar, esta función devuelve directamente la información relevante a ese cliente.

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

[**RtmAddRoute**](rtmaddroute.md)
</dt> <dt>

[**RtmDequeueRouteChangeMessage**](rtmdequeueroutechangemessage.md)
</dt> </dl>

 

 





